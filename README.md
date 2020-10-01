# pald-communities
Partitioned Local Depths Data


Data used in the paper "A social perspective on perceived distances reveals deep community structure" by Kenneth S. Berenhaut, Katherine E. Moore, and Ryan L. Melvin.



Figure 1: Eight points with structure forming a diamond, line, and an isolated point.     
Included in "fig1_data.csv"    

Figure 2: Sixteen points to illustrate varying densities.    
Included in "fig2_data.csv"     

Figure 3:   
n = 250 points generated by sampling uniformly at random from three Euclidean balls of dimension d = 2, 10, and 5000.   
Ball1: n = 50, center = (0, 0, ..., 0), radius = 0.5   
Ball2: n = 100, center = (3/sqrt(d), -3/sqrt(d), ..., 3/sqrt(d), -3/sqrt(d)), radius = 1      
Ball3: n = 100, center = (4/sqrt(d), 4/sqrt(d), ..., 4/sqrt(d)), radius = 2.5     

Figure 4:    
A: Benchmark data set Aggregation consisting of n = 788 points.     
Link to data: http://cs.joensuu.fi/sipu/datasets/Aggregation.txt  
A. Gionis, H. Mannila, and P. Tsaparas, Clustering aggregation. ACM Transactions on Knowledge Discovery from Data (TKDD), 2007. 1(1): p. 1-30.       
B: n = 250 points were sampled at random from Aggregation (see 4A).    
C: n = 500 points were generated using SciKitLearn ("noisy moons") with noise= .05.  
(https://scikit-learn.org/stable/auto_examples/cluster/plot_linkage_comparison.html)   
Included in "fig4c_data.csv"   
Scikit-learn: Machine Learning in Python, Pedregosa et al., JMLR 12, pp. 2825-2830, 2011.   
(https://jmlr.csail.mit.edu/papers/v12/pedregosa11a.html)       
D: Points which are equally-spaced on two circles.   
Included in "fig4d_data.csv"       
Inner ring: n = 36, center = (0, 0), radius = 1  
OuterRing: n = 13, center = (0, 0), radius = 1.86    
E: Points were randomly generated by sampling uniformly at random from three balls.     
Ball1: n = 30, center = (0, 0), radius = 2.5    
Ball2: n = 100, center = (6, 1.2), radius = 1    
Ball3: n = 100, center = (6, 01.2), radius = 1    
F: Points were randomly generated from a mixture of eight bivariate normal distributions with varying means and standard deviation.  
Included in "fig4f_data.csv"  
  library(mvtnorm) 
  fig4f_data<-rbind(mvrnorm(40,mu=c(-10,-10),Sigma=diag(c(8,8))),
          mvrnorm(40,mu=c(-10,5),Sigma=diag(c(1,1))),
          mvrnorm(60,mu=c(10,10),Sigma=diag(c(2,2))),
          mvrnorm(20,mu=c(0,10),Sigma=diag(c(.5,.5))),
          mvrnorm(20,mu=c(10,0),Sigma=diag(c(1,1))),
          mvrnorm(20,mu=c(15,21),Sigma=diag(c(.1,.1))),
          mvrnorm(20,mu=c(15,17),Sigma=diag(c(.1,.1))),
          mvrnorm(20,mu=c(17.5,19),Sigma=diag(c(.1,.1))))  
          
Figure 5:    


Figure 6:   

    https://github.com/genomicsclass/tissuesGeneExpression/tree/master/data  
    load("/tissuesGeneExpression.Rdata") tissue.M<-t(e)tissue.gt<-tissue


Figure 7:    



Supplementary information also includes:

Southern Oscillation Index data found in the astsa package in R.  
https://cran.r-project.org/web/packages/astsa/astsa.pdf  
library(astsa)data(soi)  

Cholera data found in the cholera package in R.  
https://CRAN.R-project.org/package=cholera
The matrix containing pairwise walking distances was produced using functions therein.  
Included in "cholera_dist.csv"
