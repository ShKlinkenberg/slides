# slides
Reusable IOslides for my presentations

The child attribute does not seem to work for adding md files from websites. So to add the pages in this repository we need to use the Rcurl package and print the results asis.

The Rmd chunk attributes should be set to:

```
echo=FALSE, results="asis", warning=FALSE, message=FALSE, eval=TRUE, cache=FALSE
```

The RCurl library should be loaded and the retrieved url must be cat:

```{r, echo=FALSE, results="asis", warning=FALSE, message=FALSE, eval=TRUE, cache=FALSE}
if(!"RCurl" %in% installed.packages()) install.packages("RCurl")
library("RCurl")
cat(getURL("https://shklinkenberg.github.io/slides/file.md"))
```
