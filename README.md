# Fast-Mirror-Manhattan-Plot

I am working on a fast version of mirror manhattan plot that essentially repalces geom_point with geom_scattermore. I only modifed few places in the gmirror.R from [hudson](https://github.com/anastasia-lucas/hudson) package. 

 ```{r}
 gmirror_fast(top=gwas.t, bottom = gwas.b, tline=5e-8, bline=5e-8)
 ```

I also added an option of using pseduo-log-transformed y axis. This is helpful for visualizing some traits (e.g. height) with many small p-values (and therefore much larger on -log10(p) than rest of the SNPs). 
