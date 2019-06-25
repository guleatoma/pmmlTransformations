This is a **modified** version of thepmmlTransformations package that brings some fixes to the [PMML cran package](https://cran.r-project.org/web/packages/pmmlTransformations/index.html) under GPL licence. 

This version is still under development. Use at your own risk

To install the package use devtools: 

```{r}
devtools::install_github("turo/pmmlTransformations")
```

The package currently brings fixes targeted to some specific use cases listed below.

# Modifications brought to the package:

## FunctionXform can be applied several times

In the regular package, having applying several time FunctionXform would result in a failure:

Example: 
```{r}
dataBox = WrapData(data)

dataBox <- FunctionXform(dataBox,
                           origFieldName="x1",
                           newFieldName="x2",
                           formulaText="x1 + 1")

dataBox <- FunctionXform(dataBox,
                       origFieldName="x3",
                       newFieldName="x4",
                       formulaText="x3 * 2")                         
```
would throw an error. This version fixes the issue


## pmml package
You can also find fixes for the pmml package [here](https://github.com/turo/pmml).

