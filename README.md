# Low-z IRRC Data Release

Publicly available catalogue released in Molnár et al 2021 (link TBD).
[![DOI](https://zenodo.org/badge/344211798.svg)](https://zenodo.org/badge/latestdoi/344211798)


Column description:

  Column (1): SDSS ObjID -- Galaxy IDs from SDSS DR12 (corresponding to the SDSS spectroscopic ID when available, otherwise it is the SDSS photometric ID; see SpecFlag in column 5).
 
  Column (2): R.A. [J2000] -- Right ascension in degrees from SDSS DR12.
  
  Column (3): Dec. [J2000] -- Declination in degrees from SDSS DR12.
 
  Column (4): z -- spectroscopic or photometric redshift from SDSS DR12, see column (5) detected.
  Column (5): Specflag -- Set to 1 if a source was spectroscopically detected, otherwise 0.
 
  Column (6): BPTflag -- Flag values of 0, 1 and 2 denote SFG, composite and AGN sources, respectively, as described in Sect. 3.2.1. A value of -1 indicates the lack of high quality spectral line detection, or have no $H_{\alpha}$ detections at the SNR $>$ 3 level in the MPA/JHU value-added catalogue, and consequently in SDSS DR 8.\\We note that our redshifts were drawn from SDSS DR 12, therefore a flag of 0 in column (5) in a handful of cases does not correspond to a flag of -1 in this column and vice versa.
 
  Column (7): MIRflag -- Set to 1 if a source was labelled as an AGN based on its MIR colours (for details see Sect. 3.2.2), otherwise 0.\\We caution users against including sources with MIR flag = 1 in their analyses, since our SED templates assumed pure SF across the entire IR wavelength regime. As a result, their log(LTIR) (and by extension, qTIR) values are likely overestimated. We note that galaxies labelled as AGN based on optical emission lines but not on their MIR colours are still considered to have robust log(LTIR) estimates.
 
  Column (8): FIRSTflag -- Set to 1 for galaxies in covered by the FIRST survey, otherwise 0. It is required to reproduce our depth-matched sample (Sect. 3.3).
 
  Column (9): SEDflag -- Set to 1 for galaxies with robust IR SED models, otherwise 0.
 
  Column (10 - 37): S_band and E_band -- flux densities and their errors as tabulated in the various archival catalogues used to assemble our data (see Sect 2) in Jy. These bands are $22\,\mu$m WISE, $60\,\mu$m IRAS, $100\,\mu$m IRAS, $100\,\mu$m H-ATLAS, $100\,\mu$m PPSC, $160\,\mu$m H-ATLAS, $160\,\mu$m PPSC, $250\,\mu$m H-ATLAS, $250\,\mu$m SPSC, $350\,\mu$m H-ATLAS, $350\,\mu$m SPSC, $500\,\mu$m H-ATLAS, $500\,\mu$m SPSC, $1.4$GHz flux density (either NVSS or FIRST, see Sect. 2.2), respectively. We note that the IR flux values published here are \textit{not} re-scaled/corrected\footnote{Before SED fitting we carried out the following modifications: (i) we multiplied our $100$ and $160\,\mu$m PPSC data by 1.19 and 1.10, respectively; (ii) we increased the uncertainty of all PPSC and HPSC measurements by adding 0.05, 0.08, 0.06, 0.05 and 0.03 Jy in quadrature to the tabulated flux density uncertainties of 100, 160, 250, 350 and 500 $\mu$m data.}
 
  Column (38): logL1.4 -- 1.4 GHz radio luminosity in units of $\log(\mathrm{W Hz^{-1}})$.
 
  Column (39): logdL1.4 -- 1.4 GHz radio luminosity uncertainty.
 
  Column (40): logLTIR -- Total IR logarithmic luminosity from IR SED fitting (see Sect. 3.1.1) in units of $\log(L_{\odot})$.
 
  Column (41): logLFIR -- Far-IR logarithmic luminosity from IR SED fitting (see Sect. 3.1.1) in units of $\log(L_{\odot})$.
 
  Column (42): logdLFIR_upp -- Upper log(LTIR) luminosity uncertainty corresponding to the difference of the 84th percentile and the median of the marginalized log(LTIR) posterior distributions from our MCMC fits. We note that the errors on $\log(L_{\rm FIR})$ and log(LTIR) are considered to be equal.
 
  Column (43): logdLFIR_low -- Lower log(LTIR) luminosity uncertainty corresponding to the difference of the median and the 16th percentile of the marginalized log(LTIR) posterior distributions from our MCMC fits. We note that the errors on $\log(L_{\rm FIR})$ and log(LTIR) are considered to be equal.
 
  Column (44): qTIR -- qTIR calculated with Columns (38) and (40).
 
  Column (45): qFIR -- qFIR calculated with Columns (38) and (41). By definition qFIR is lower than qTIR by logLTIR - logLFIR.
 
  Column (46): dqTIR_upp -- Upper error on qTIR, calculated by propagating the uncertainties in Columns (39) and (42)).
 
  Column (47): dqTIR_low -- Lower error on qTIR, calculated by propagating the uncertainties in Columns (39) and (43).
