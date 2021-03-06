# Fast-Mirror-Manhattan-Plot

I am working on a fast version of mirror manhattan plot that essentially repalces geom_point with geom_scattermore. I only modifed few places in the gmirror.R from [hudson](https://github.com/anastasia-lucas/hudson) package. 

 ```{r}
 gmirror_fast(top=gwas.t, bottom = gwas.b, tline=5e-8, bline=5e-8)
 ```
 
![Rplot02-1](https://user-images.githubusercontent.com/58570421/128565407-905caaa0-9298-4bc9-bee1-b147592671b4.png)



I also added an option of using pseduo-log-transformed y-axis. This is helpful for visualizing some traits (e.g. height) with many small p-values (and therefore much larger on -log10(p) than rest of the SNPs). 

 ```{r}
 gmirror_fast(top=gwas.t, bottom = gwas.b, tline=5e-8, bline=5e-8, log_axis=TRUE)
 ```
![gmirror-1](https://user-images.githubusercontent.com/58570421/128565456-448e658d-b56a-45d2-a829-fbad36a45c58.png)

Annotations and highlight are same as in the [hudson](https://github.com/anastasia-lucas/hudson) package.

 ```{r}
 rsid <- gwas[gwas$pval<5e-30,]$rsid
 gmirror_fast(top=gwas.t, bottom = gwas.b, tline=5e-8, bline=5e-8, log_axis=TRUE)
 ```
 ![gmirror](https://user-images.githubusercontent.com/58570421/128566570-8c8d7449-76aa-4e92-a712-9beab4b2b53c.png)
