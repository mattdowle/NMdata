# NMdata
Nonmem provides a flexible toolbox for PK and PK/PD modeling. However,
creating the datasets and reading the data resulting from running
Nonmem can be tedious. This package provides useful tools for these
tasks. 

## How to Install
library(remotes)

install_github("philipdelff/NMdata")

library(NMdata)

## Automated and general reader of Nonmem output data
Reading the resulting data from Nonmem can require quite a bit of
manual steps. Especially because all modelers seem to do
things a little differently. The frustrating fact is that we always
want the same - all data output from Nonmem with additional columns in
input data added, and then possibly broken down to the possible levels
of variability. This package automates this process and can save you a
lot of time. 

Take a look at this vignette for more info on the Nonmem data reader
(once NMdata is loaded):
vignette("NMscanData")

On the data-generation side, functionality is provided for
documentation of the datasets while generating them. For reading the
data resulting from the Nonmem runs, the package includes a function
to efficiently read all of this data and combine it with the input
data into a standardized representation. No more having to look at the
.lst to see which tables to read. No more having to read multiple
tables to get all the variables. No more having to merge with input
data to get variables that were not exported with nonmem. This and
much more is done automatically.

## A new package - stable functionality
NMdata is a release of functionality that used to be part of the
pmxtricks package. The code has been extensively developed and
tested. In fact, the NMdata has been separated from pmxtricks because
it is more mature than some of the other functionality in that
package. There is still improvement to be done, indeed. But the
functionality already implemented is quite stable and aimed at CRAN
release in near future.

## Create data, export to Nonmem
These are the steps that this package especially helps with. Here are some hightlights:

flagsAssign - Assign exclusion flags to a dataset based on specified table

flagsCount - Create an overview of number of retained and discarded datapoints.

NMorderColumns - Order columns in dataset for use in Nonmem.

NMwriteData - Write dataset (with creation info documentation) for use in Nonmem (and R)

## Read Nonmem results
NMscanData - automatically find Nonmem input and output tables and organize data

metadata functions for documentation of column contents are under development.

## Edit nonmem runs
NMgetSection - extract sections of Nonmem control streams

NMreplacePart - replace ($)sections of a nonmem control stream

## Handy data wrangling tools
findCovs - Extract columns that do not vary within variables in a data.frame

findVars - Extract columns that vary within values of other columns in a data.frame

mergeCheck - Merge, order, and check resulting rows and columns.
