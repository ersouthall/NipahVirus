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

# Outbreak Data in Bangladesh

| Dates | Districts | Number of Cases | Fatality Rate (%) | Reference|
| ------------ | -------- |-------| ------------ | -------- |
| Apr - May 2001 | Meherpur | 13 | 69 | [Kulkarni](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3832692/pdf/13337_2013_Article_171.pdf) |
|Jan - Mar 2003 | Naogaon | 12 | 67 | [Kulkarni](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3832692/pdf/13337_2013_Article_171.pdf) |
|04/01/04 - 08/02/04 | Manikganj, Rajbari | 7, 35 | 57, 29 | [WHO Report 12/02/04](https://www.who.int/csr/don/2004_02_12/en/)|
|19/02/04 - 16/04/04 | Faridpur | 36 | 75 | [WHO Report 20/04/04](https://www.who.int/csr/don/2004_04_20/en/),[Gurley](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2878219/)|
|02/01/05 - 16/01/05 | Tangail | 12 | 92 | [Luby](https://www.college-de-france.fr/media/philippe-sansonetti/UPL5966270986440617893_10____luby.pdf) |
|21/01/07 - 08/02/07 | Thakurgaon | 7 | 43| [Homaira](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/7C468D7713F68FD41E7706B9AB0AA034/S0950268810000695a.pdf/nipah_virus_outbreak_with_persontoperson_transmission_in_a_district_of_bangladesh_2007.pdf)|
|Mar - May 2007 | Kushtia | 8 | 63 | [Kulkarni](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3832692/pdf/13337_2013_Article_171.pdf)|
|20/02/08 - 26/03/08 | Manikganj | 6 | Unknown | [Rahman](https://www.liebertpub.com/doi/full/10.1089/vbz.2011.0656) |
|Jan - Feb 2009 | Gaibandha, Rangpur, Nilphamari | 1,1,1 | 0,0,0 | [Kulkarni](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3832692/pdf/13337_2013_Article_171.pdf) |
|01/12/09 - 31/03/10 | Faridpur | 17 | Unknown | [Sazzad](https://wwwnc.cdc.gov/eid/article/19/2/12-0971_article) | 
|Jan 2010 | Gopalgonj, Kurigram | 8 | 86 | [Kulkarni](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3832692/pdf/13337_2013_Article_171.pdf)|
|24/01/11 - 21/02/11 | Lalmohirhat | 22 | 95 | [Chakraborty](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4675679/) |
|Jan - Feb 2011 | Dinajpur, Rangpur, Comilla, Nilphamari | 5, 8, 1, 1 | 80, 63, 100, 100 | [Chakraborty](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4675679/),[Islam](https://wwwnc.cdc.gov/eid/article/22/4/15-1747_article), [IEDCR Report 27/02/11](https://www.iedcr.gov.bd/pdf/files/nipah/Nipah-Update.pdf) |
|01/01/11 - 07/01/11 | Faridpur | 5 | 80 |  [IEDCR Report 27/02/11](https://www.iedcr.gov.bd/pdf/files/nipah/Nipah-Update.pdf)  |
|20/01/12 - Feb 2012 | Joypurhat | 12 | 83 | [IEDCR Report 01/12](https://www.iedcr.gov.bd/index.php/outbreak-at-joypurhat) |
|23/02/13 - 15/05/13 | Jhenaidah, Kurigram, Kushtia, Magura, Mymensingh, Nilphamari, Rajshahi, Pabna,Natore, Naogaon, Gaibandha, Manikganji |  1,1,1,1, 2,3,1,2,2,3,1,5 | 100, 100, 100, 100, 100, 100, 100, 50, 50, 100, 100, 80  | [IEDCR Report 23/02/13](https://iedcr.gov.bd/index.php/component/content/article/11/112-23-rd-february-2013-nipah-outbreak) |
|Jan - Feb 2014 | Manikganj, Magura, Faridpur, Shaariatpur, Kushtia, Rajshahi, Nawabganj, Natore, Dinajpur, Madaripur, Naogaon | 2,5,5,1, 1,1,1,1, 1,3,1 |100, 40,80, 100, 0,0,0,0, 0, 67, 100 | [IEDCR Report 11/02/14](https://iedcr.gov.bd/index.php?option=com_content&view=article&id=106) |
|14/01/14 - 01/02/14 | Rangpur | 4 | 50 | [Islam](https://wwwnc.cdc.gov/eid/article/22/4/15-1747_article) |
|Jan - Feb 2015 | Nilphamari, Panchagarh, Faridpur, Magura, Naogaon |1, 1, 2, 1, 3 | 100, 0, 50, 100, 100| [IEDCR Report 04/02/15](https://www.iedcr.gov.bd/pdf/files/nipah/Nipah%20Infection%20in%202015_Website%20update%20Feb%204%202015_for%20website.pdf) |
