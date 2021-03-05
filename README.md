# Low-z IRRC Data Release

Publicly available catalogue released in Molnár et al 2021 (link TBD).
[![DOI](https://zenodo.org/badge/344211798.svg)](https://zenodo.org/badge/latestdoi/344211798)


Column description:

1: SDSS ObjID -- Galaxy IDs from SDSS DR12 (corresponding to the SDSS spectroscopic ID when available, otherwise it is the SDSS photometric ID; see SpecFlag in column 5).

2: R.A. [J2000] -- Right ascension in degrees from SDSS DR12.

3: Dec. [J2000] -- Declination in degrees from SDSS DR12.

4: z -- spectroscopic or photometric redshift from SDSS DR12, see column (5) detected.

5: Specflag -- Set to 1 if a source was spectroscopically detected, otherwise 0.

6: BPTflag -- Flag values of 0, 1 and 2 denote SFG, composite and AGN sources, respectively, as described in Sect. \ref{sect::bpt}. A value of -1 indicates the lack of high quality spectral line detection, or have no $H_{\alpha}$ detections at the SNR $>$ 3 level in the MPA/JHU value-added catalogue, and consequently in SDSS DR 8. We note that our redshifts were drawn from SDSS DR 12, therefore a flag of 0 in column (5) in a handful of cases does not correspond to a flag of -1 in this column and vice versa.

7: MIRflag -- Set to 1 if a source was labelled as an AGN based on its MIR colours (for details see Sect. \ref{sect::mir_agn}), otherwise 0.\\We caution users against including sources with MIR flag $=$1 in their analyses, since our SED templates assumed pure SF across the entire IR wavelength regime. As a result, their $\log(L_{\rm TIR})$ (and by extension, $q_{\rm TIR}$) values are likely overestimated. We note that galaxies labelled as AGN based on optical emission lines but not on their MIR colours are still considered to have robust $\log(L_{\rm TIR})$ estimates.

8: FIRSTflag -- Set to 1 for galaxies in covered by the FIRST survey, otherwise 0. It is required to reproduce our depth-matched sample (Sect. \ref{sect::fluxmatch_samp}).

9: SEDflag -- Set to 1 for galaxies with robust IR SED models, otherwise 0.

10 - 37: $S_{\rm band}$ and $\Delta S_{\rm band}$ -- flux densities and their errors as tabulated in the various archival catalogues used to assemble our data (see Sect \ref{sect::dat}) in Jy. These bands are $22\,\mu$m WISE, $60\,\mu$m IRAS, $100\,\mu$m IRAS, $100\,\mu$m H-ATLAS, $100\,\mu$m PPSC, $160\,\mu$m H-ATLAS, $160\,\mu$m PPSC, $250\,\mu$m H-ATLAS, $250\,\mu$m SPSC, $350\,\mu$m H-ATLAS, $350\,\mu$m SPSC, $500\,\mu$m H-ATLAS, $500\,\mu$m SPSC, $1.4$GHz FIRST and $1.4$GHz NVSS. We note that the values published here are \textit{not} re-scaled/corrected\footnote{Before SED fitting we carried out the following modifications: (i) we multiplied our $100$ and $160\,\mu$m PPSC data by 1.19 and 1.10, respectively; (ii) we increased the uncertainty of all PPSC and HPSC measurements by adding 0.05, 0.08, 0.06, 0.05 and 0.03 Jy in quadrature to the tabulated flux density uncertainties of 100, 160, 250, 350 and 500 $\mu$m data; (iii) we multiplied FIRST flux densities by 1.22.}

38: $\log(L_{1.4})$ -- 1.4\,GHz radio luminosity in units of $\log(\mathrm{W Hz^{-1}})$.

39: $\Delta\log(L_{1.4})$ -- 1.4\,GHz radio luminosity uncertainty.

40: $\log(L_{\rm TIR})$ -- Total IR luminosity from IR SED fitting (see Sect. \ref{sect::sed_fits}) in units of $\log(L_{\odot})$.

41: $\log(L_{\rm FIR})$ -- Far-IR luminosity from IR SED fitting (see Sect. \ref{sect::sed_fits}) in units of $\log(L_{\odot})$.

42: $\Delta\log(L_{\rm IR, upp})$ -- Upper $\log(L_{\rm TIR})$ luminosity uncertainty corresponding to the difference of the 84th percentile and the median of the marginalized $\log(L_{\rm TIR})$ posterior distributions from our MCMC fits. We note that the errors on $\log(L_{\rm FIR})$ and $\log(L_{\rm TIR})$ are considered to be equal.

43: $\Delta\log(L_{\rm IR, low})$ -- Lower $\log(L_{\rm TIR})$ luminosity uncertainty corresponding to the difference of the median and the 16th percentile of the marginalized $\log(L_{\rm TIR})$ posterior distributions from our MCMC fits. We note that the errors on $\log(L_{\rm FIR})$ and $\log(L_{\rm TIR})$ are considered to be equal.

44: $q_{\rm TIR}$ -- $q_{\rm TIR}$ calculated with Columns (38) and (40). By definition $q_{\rm FIR}$ is lower than $q_{\rm TIR}$ by $\log(L_{\rm TIR}) - \log(L_{\rm FIR})$.

45: $q_{\rm TIR, upp}$ -- Upper error on $q_{\rm TIR}$, calculated by propagating the uncertainties in Columns (39), (42) and (43).

46: $q_{\rm TIR, low}$ -- Lower error on $q_{\rm TIR}$, calculated by propagating the uncertainties in Columns (15) and (17).

47: $q_{\rm FIR}$ -- $q_{\rm FIR}$ calculated with Columns (38) and (41). By definition $q_{\rm FIR}$ is lower than $q_{\rm TIR}$ by $\log(L_{\rm TIR}) - \log(L_{\rm FIR})$.
