# Dimension reduction add noise

## Description
When you have a noisy dimension or two in your flow/mass cytometry data, does that ruin your dimension reduction output? Here, we iteratively add dimensions of random noise to our data in order to determine whether this is the case. 

## How to use
### add_noise.Rmd: 
This file takes in default CyTOF data, turns it into a tibble, and feeds it into loops that add noise and run a dimension reduction tool. At the time of writing, it is t-SNE and UMAP. But you can insert your own tool as you wish. Take the data import block of code and replace it with your data. Get it into a data frame or tibble with only the markers you want to bse used as input to the dimension reduction tools (eg. only the surface markers).

Data are outputted as lists of dimension reduction coordinates for each run.

### make_plots.Rmd
This file imports the aforementioned lists, and makes plots of each dimesnion reduciton run. These are then lumped together into a gif. Both the plots and the gif are outputted.

## Example
Here is t-SNE being run on a 1000 cell whole blood CyTOF dataset, with each frame being t-SNE run with one more dimension of noise added to the data.

![](tsne_slow.gif)

