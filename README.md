Reproducibility in ecology literature
=====================================

If we choose a bunch of random papers from the BES and ESA journals, which all enforce data availability to some degree, can we actually reproduce the results?!

Paper center piece will be a table with papers as rows, and columns descrribing the degree to which the paper enables reproduction (e.g. columns - is the data available?; is code provided?; could the authors preproduce results/plots? etc.)

TO DO:
* Decide on sample number (40 minimum?)  
* Decie on which journals to include
* Decide on table format  
* Decide on how many from each journal, possibly based on total number of articles/suitability, and then simply review the first n randomly selected articles that are chosen to be suitable (i.e. remove review article or opinion piece for example)  


Choosing papers
---------------
Papers from July 2014 - to ensure data policy in full swing. The sections below detail the volume/issue/page range for each of the BES/ESA journals.

R Functions to choose papers (Functions have set.seed() built in to ensure reproducibility):

```r
# function that randomly chooses a page within the range specified
# we reviewed papers that fell on sampled page number
ChooseByPage = function(PageMin, PageMax, n) {
  set.seed(100)
  paste0("Journal pages chosen: ", paste0(sample(x=PageMin:PageMax, size=n), collapse=", "))
}

# as above, but for journals without page numbers
# we reviewed paper numbers selected
ChooseByArticle = function(ArtMin, ArtMax, n) {
  set.seed(100)
  paste0("Articles chosen: ", paste0(sample(x=ArtMin:ArtMax, size=n), collapse=", "))
}
```


BES Journals
------------
### BES position on open data
Data are important products of the scientific enterprise, and they should be preserved and usable for decades in the future. The British Ecological Society thus requires that data (or, for theoretical papers, mathematical and computer models) supporting the results in papers published in its journals will be archived in an appropriate public archive, such as Dryad, TreeBASE, NERC data centre, GenBank, Movebank, figshare or another archive of the author's choice that provides comparable access and guarantee of preservation. Authors may elect to have the data made publicly available at time of publication or, if the technology of the archive allows, may opt to embargo access to the data for a period of up to a year after publication. - See more at: http://www.britishecologicalsociety.org/publications/journal-policies/#data

### Functional Ecology
Volume 28
Issues 4-6
Pages 787-1555


```r
ChooseByPage(787,1555,3)
```

```
## [1] "Journal pages chosen: 1023, 984, 1210"
```
Random artical selection:
```
Achatz, M., Morris, E. K., M�ller, F., Hilker, M., & Rillig, M. C. (2014). Soil hypha-mediated movement of allelochemicals: arbuscular mycorrhizae extend the bioactive zone of juglone. Functional Ecology.

Higgins, J. K., MacLean, H. J., Buckley, L. B., & Kingsolver, J. G. (2013). Geographic differences and microevolutionary changes in thermal sensitivity of butterfly larvae in response to climate. Functional Ecology.

Merilaita, S., & Dimitrova, M. (2014). Accuracy of background matching and prey detection: predation by blue tits indicates intense selection for highly matching prey colour pattern. Functional Ecology.
```

### Journal of Animal Ecology
Volume 83
Issues 4-6
Pages 741-1552

### Journal of Applied Ecology
Volume 51
Issue 4-6
Pages 835-1759

### Journal of Ecology
Volume 102
Issue 4-6
Pages 823-1696

### Methods in Ecology and Evolution
Volume 5
Issue 7-11 (no December issue at time of check)
Pages 599-1263

### Ecology & Evolution
Volume 4
Issue 13-22 (no December issues at time of check)
Pages 2625-4428


ESA Journals
------------
### ESA position on open data
The editors and publisher expect authors to make the data underlying published articles available. As a condition for publication in Ecological Monographs (submitted as of January 1, 2011) and Ecological Applications (submitted as of January 1, 2014), all data associated with the results reported in accepted manuscripts must be made available in a permanent, publicly-accessible data archive or repository. See the specific policies for Ecological Monographs and Ecological Applications.

Although public data availability is not strictly a requirement for manuscripts published in Ecology and Ecosphere at this time, any information on materials, methods or data necessary to verify the conclusions of the research reported must be made available to the Subject-matter Editor upon request.

Mitch note - no official policy on other journals found

### Ecosphere
Volume 5
Issues 7-11 (no December issue at time of check)
Articles 78-149

### Ecology
Volume 95
Issues 7-11 (no December issue at time of check)
Pages 1717-3236

### Ecological Monographs
Volume 84
Issues 3-4
Pages 355-659

### Ecological Applications
Volume 24
Issues 5-7 (no December issue at time of check)
Pages 913-1877

### Frontiers in Ecology and the Environment
Volume 12
Issues 6-9 (no December issue at time of check)
Pages 315-536

### Bulletin of the Ecological Society of America
Not appropriate for our work

