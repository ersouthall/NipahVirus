# Epidemiological Model for Nipah Virus (NiV) 

- Stochastic Model 
- Disease emergence
- Basic Reproduction Number
- Gillespie Algorithm: SIR, SEIR, SEIHR and SEIR with external force of infection
- Adaptive Gillespie Algorithm (for non constant rates)
- Approximate Bayesian Computation (ABC)
- Parameter fitting to published epidemiological case data - Faridpur 2004 and 2010 outbreak www.iedcr.gov.bd/pdf/files/nipah/Nipah-Update.pdf
- Mapping population densities with osgeo, gdal
- Data imputation from worldpop data http://www.worldpop.org.uk/ 
- Predict the variance and coefficient of variation from Fokker-Planck Equation
- Master Equations 
- Fourier Transforms 
- Quasi-stationary state

# Outbreak Data Collected

| Dates | Districts | Number of Cases | Fatality Rate (%) | Reference|
| ------------ | -------- |-------| ------------ | -------- |
| Apr-May 2001 | Meherpur | 13 | 69 | ... |
|Jan-Mar 2003 | Naogaon | 12 | 67 | ...|
|04/01/04 \- 08/02/04 | Rajbari | 29 | 76 | ...|
|19/02/04 - 16/04/04 | Faridpur | 36 | 75 | ...|
|02/01/05 - 16/01/05 | Tangail | 12 | 92 | ...|
|21/01/07 - 08/02/07 | Thakurgaon | 7 | 43| ...|
|Mar-May 2007 | Kushtia | 8 | 63 | ...|
|20/02/08-26/03/08 | Manikganj | 6 | Unknown | ...|
|Jan-Feb 2009 | Gaibandha, Rangpur, Nilphamari | 1,1,1 | 0,0,0 | ...|
|01/12/09-31/03/10 | Faridpur | 17 | Unknown |...| 
|Jan 2010 | Gopalgonj, Kurigram | 8 | 86 |... |
|24/01/11 - 21/02/11 | Lalmohirhat | 22 | 95 | ...|
|Jan-Feb 2011 | Dinajpur, Rangpur, Comilla, Nilphamari | 5, 8, 1, 1 | 80, 63, 100, 100 |... |
|01/01/11 - 07/01/11 | Faridpur | 5 | 80 | ... |
|20/01/12-Feb 2012 | Joypurhat | 12 | 83 | ...|
|23/02/13-15/05/13 | Jhenaidah, Kurigram, Kushtia, Magura, Mymensingh, Nilphamari, Rajshahi, Pabna,Natore, Naogaon, Gaibandha, Manikganji |  1,1,1,1, 2,3,1,2,2,3,1,5 | 100, 100, 100, 100, 100, 100, 100, 50, 50, 100, 100, 80  | ...|
|Jan - Feb 2014 | Manikganj, Magura, Faridpur, Shaariatpur, Kushtia, Rajshahi, Nawabganj, Natore, Dinajpur, Madaripur, Naogaon | 2,5,5,1, 1,1,1,1, 1,3,1 |100, 40,80, 100, | 0,0,0,0, | 0, 67, 100 | ...|
|14/01/14-01/02/14 | Rangpur | 4 | 50 | ... |
|Jan-Feb 2015 | Nilphamari, Panchagarh, Faridpur, Magura, Naogaon |1, 1, 2, 1, 3 | 100, 0, 50, 100, 100|... |
