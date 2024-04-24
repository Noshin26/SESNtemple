[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.826368.svg)](https://doi.org/10.5281/zenodo.826368)

# SESNtemple

This repository contains data products for Stripped Envelope SNe (SESNe), ie SNe of types IIb, Ib, Ic and Ic-bl, from [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2016ApJ...827...90L), [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2016ApJ...832..108M), [Williamson et al. (2019)](http://ui.adsabs.harvard.edu/abs/2019ApJ...880L..22W), [Williamson et al. (2023)](http://ui.adsabs.harvard.edu/abs/2023ApJ...944L..49W) and for SLSNe Ic from [Liu, Modjaz & Bianco (2017)](http://adsabs.harvard.edu/abs/2016arXiv161207321L). There are two different types of SN templates we produced and used in our research, which are stored in two different folders:
- <b>/MeanSpec</b> contains all mean spectra and standard deviation spectra of different SESN types in [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2016ApJ...827...90L), [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2016ApJ...832..108M), and of SLSNe Ic in [Liu, Modjaz & Bianco (2017)](http://adsabs.harvard.edu/abs/2016arXiv161207321L), including those not shown in plots. Mean-spectra and standard deviation spectra can be used to quantify SN diversity, determine if a new transient is a novel type of explosion (note that spectra of the transient need to be flattened, which can be produced with **snidflat.pro** using the default values in **snid_pro.tgz**, downloadable at [Stephane Blondin's webpage](https://people.lam.fr/blondin.stephane/software/snid/index.html#Download)), and so on. See the README file in the folder for details of the mean-spectra. Mean spectra of SNe Ic are used as SN Ic templates for our template fitting code called "Ic_conv_Icbl_MCMC.py" (https://github.com/nyusngroup/SESNspectraLib), which measures line velocities in SNe Ic-bl based on blended lines. They live under the SESNspectraLib repository, since we want the template fitting code to be self-contained, and since those mean spectra templates were constructed from SN Ic spectra using slightly different phase ranges than the ones released here.
 
- <b>/SNIDtemplates</b> contains all SuperNova IDentification (SNID; [Blondin & Tonry 2007](http://adsabs.harvard.edu/abs/2007ApJ...666.1024B)) templates that were initially released in [Liu & Modjaz (2014)](http://adsabs.harvard.edu/abs/2014arXiv1405.1437L) based on CfA spectra, as well as additional templates that were newly created and used in [Liu et al. (2016, for IIb and Ib)](http://adsabs.harvard.edu/abs/2016ApJ...827...90L) and in [Modjaz et al. (2016, for Ic and Ic-bl)](http://adsabs.harvard.edu/abs/2016ApJ...832..108M), based on literature spectra. In addition, templates for SESNe published in the literature up to 2019 are included from [Williamson et al. (2019)](http://ui.adsabs.harvard.edu/abs/2019ApJ...880L..22W) as well as templates for young SNe Ic presented in [Williamson et al. (2023)](http://ui.adsabs.harvard.edu/abs/2023ApJ...944L..49W). Adding these templates to the spectra library database of SNID will increase the number of SESN templates in the database, which will help SN classification via SNID. See the README file in the folder for details of SN spectra that are used to construct SNID templates.

- <b>/WeightedMeanAbsorptionVel</b> contains the weighted mean absorption velocities, based on Fe II 5169, of SNe Ic, Ic-bl and SLSNe Ic as shown in [Liu, Modjaz & Bianco (2017)](http://adsabs.harvard.edu/abs/2016arXiv161207321L). Those velocities are somewhat different from those computed in [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2016ApJ...827...90L) and [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2016ApJ...832..108M), but supersede them.

### Acknowledgement:

If you use data products in this repository, please <b>acknowledge</b> this work by including in your paper:

	This work made use of the data products generated by the Modjaz group (formerly NYU SN group), and 
	released under DOI:10.5281/zenodo.58766, 
	available at \url{https://github.com/nyusngroup/SESNtemple/}.
	  
*and* <b>cite</b> the appropriate reference(s):

Liu & Modjaz (2014):

  	@ARTICLE{2014arXiv1405.1437L,
    	author = {{Liu}, Y. and {Modjaz}, M.},
     	title = "{SuperNova IDentification spectral templates of 70 stripped-envelope core-collapse supernovae}",
   	journal = {ArXiv e-prints},
  	archivePrefix = "arXiv",
     	eprint = {1405.1437},
   	primaryClass = "astro-ph.SR",
   	keywords = {Astrophysics - Solar and Stellar Astrophysics, Astrophysics - High Energy Astrophysical Phenomena},
       	year = 2014,
     	month = may,
    	adsurl = {http://adsabs.harvard.edu/abs/2014arXiv1405.1437L},
	  adsnote = {Provided by the SAO/NASA Astrophysics Data System}
  	}

Liu et al. (2016):

    @ARTICLE{2016ApJ...827...90L,
   	author = {{Liu}, Y.-Q. and {Modjaz}, M. and {Bianco}, F.~B. and {Graur}, O.
	},
    	title = "{Analyzing the Largest Spectroscopic Data Set of Stripped Supernovae to Improve Their Identifications and Constrain Their Progenitors}",
  	journal = {\apj},
	archivePrefix = "arXiv",
   	eprint = {1510.08049},
 	primaryClass = "astro-ph.HE",
 	keywords = {methods: data analysis, supernovae: general, supernovae: individual: SNe 1993J, 2005bf, 2005E, 2011dh},
     	year = 2016,
    	month = aug,
   	volume = 827,
      	eid = {90},
    	pages = {90},
      	doi = {10.3847/0004-637X/827/2/90},
   	adsurl = {http://adsabs.harvard.edu/abs/2016ApJ...827...90L},
  	adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}

Modjaz et al. (2016):
  
    @ARTICLE{2016ApJ...832..108M,
   	author = {{Modjaz}, M. and {Liu}, Y.~Q. and {Bianco}, F.~B. and {Graur}, O.
	},
    	title = "{The Spectral SN-GRB Connection: Systematic Spectral Comparisons between Type Ic Supernovae and Broad-lined Type Ic Supernovae with and without Gamma-Ray Bursts}",
 	journal = {\apj},
	archivePrefix = "arXiv",
	eprint = {1509.07124},
	primaryClass = "astro-ph.HE",
	keywords = {gamma-ray burst: general, gamma-ray burst: individual: GRB-980425, GRB-030329, GRB-060218, GRB-100316D, GRB-120422A, GRB-	130427A, GRB-130702A, GRB-130215A, supernovae: general, supernovae: individual: SN-1994I, SN-2004aw, SN-2007gr, SN-1998bw, SN-2003dh, SN-2006aj, SN-2009bb, SN-2010bh, SN-2012ap, SN-2012bz, SN-2013cq, SN-2013dx, SN-2013ez },
     	year = 2016,
    	month = dec,
   	volume = 832,
      	eid = {108},
    	pages = {108},
      	doi = {10.3847/0004-637X/832/2/108},
  	adsurl = {http://adsabs.harvard.edu/abs/2016ApJ...832..108M},
 	adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}


Liu, Modjaz & Bianco (2017):

    @ARTICLE{2017ApJ...845...85L,
    author = {{Liu}, Y.-Q. and {Modjaz}, M. and {Bianco}, F.~B.},
    title = "{Analyzing the Largest Spectroscopic Data Set of Hydrogen-poor Super-luminous Supernovae}",
	journal = {\apj},
	archivePrefix = "arXiv",
	eprint = {1612.07321},
	primaryClass = "astro-ph.HE",
	keywords = {methods: data analysis, supernovae: general, supernovae: individual: ASASSN-15lh, SN 2011kl, SN 2007bi},
	year = 2017,
	month = aug,
	volume = 845,
	eid = {85},
	pages = {85},
	doi = {10.3847/1538-4357/aa7f74},
	adsurl = {http://adsabs.harvard.edu/abs/2017ApJ...845...85L},
	adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}


 Williamson, Modjaz & Bianco (2019):

     @ARTICLE{2019ApJ...880L..22W,
         author = {{Williamson}, Marc and {Modjaz}, Maryam and {Bianco}, Federica B.},
         title = "{Optimal Classification and Outlier Detection for Stripped-envelope Core-collapse Supernovae}",
         journal = {\apjl},
         keywords = {methods: data analysis, supernovae: general, Astrophysics - Solar and Stellar Astrophysics, Astrophysics - High Energy Astrophysical Phenomena},
         year = 2019,
         month = aug,
         volume = {880},
         number = {2},
         eid = {L22},
         pages = {L22},
         doi = {10.3847/2041-8213/ab2edb},
         archivePrefix = {arXiv},
         eprint = {1903.06815},
         primaryClass = {astro-ph.SR},
         adsurl = {https://ui.adsabs.harvard.edu/abs/2019ApJ...880L..22W},
         adsnote = {Provided by the SAO/NASA Astrophysics Data System}
         }


Williamson et al. (2023):

    @ARTICLE{2023ApJ...944L..49W,
        author = {{Williamson}, Marc and {Vogl}, Christian and {Modjaz}, Maryam and {Kerzendorf}, Wolfgang and {Singhal}, Jaladh and {Boland}, Teresa and {Burke}, Jamison and {Chen}, Zhihao and {Hiramatsu}, Daichi and {Galbany}, Llu{\'\i}s and {Gonzalez}, Estefania Padilla and {Howell}, D. Andrew and {Jha}, Saurabh W. and {Kwok}, Lindsey A. and {McCully}, Curtis and {Newsome}, Megan and {Pellegrino}, Craig and {Rho}, Jeonghee and {Terreran}, Giacomo and {Wang}, Xiaofeng},
        title = "{SN 2019ewu: A Peculiar Supernova with Early Strong Carbon and Weak Oxygen Features from a New Sample of Young SN Ic Spectra}",
        journal = {\apjl},
        keywords = {Type Ic supernovae, Core-collapse supernovae, Radiative transfer simulations, Spectroscopy, Optical astronomy, 1730, 304, 1967, 1558, 1776, Astrophysics - High Energy Astrophysical Phenomena, Astrophysics - Solar and Stellar Astrophysics},
        year = 2023,
        month = feb,
        volume = {944},
        number = {2},
        eid = {L49},
        pages = {L49},
        doi = {10.3847/2041-8213/acb549},
        archivePrefix = {arXiv},
        eprint = {2211.04482},
        primaryClass = {astro-ph.HE},
        adsurl = {https://ui.adsabs.harvard.edu/abs/2023ApJ...944L..49W},
        adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}

