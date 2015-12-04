.. _sec_regionals:
================================
 Regional ShakeMap Specifications
================================

In this section we summarize specific customization employed for ShakeMap systems running or
throughout the Advanced National Seismic System (ANSS) regions
nationwide. Specifications of input parameters, data, and other configurations
used for any ShakeMap can be found in the event-specific summary files
(info.xml).



Although we developed ShakeMap
with portability in mind, region-specific issues need to be addressed as a part of the installation.
To add a new region, the following criteria must be met:
1) Parametric Data. Peak ground-motions for both horizontal components of motion must
be rapidly available following significant earthquakes. PGA and PGV are required
(instrumental intensity is derived from these) and response spectral accelerations at
0.3,1.0, and 3.0 s are highly recommended. These parametric data can be unassociated as
long as individual station files contain timing information, but preferably they are
consolidated into a flat file (later converted to XML format) or, most preferable, loaded
directly into a relational database for query from ShakeMap software upon being alarmed
for an event.
2) Mapping Files for Coverage Area. The region over which ShakeMap can be properly
constrained must be ascertained, and GMT formatted map files (roads, topography, cities,
etc.) need to be collected for this region.
3) Geology and Site Corrections. ShakeMap requires a uniformly spaced grid of site
conditions over the coverage area from which to make site corrections when performing
interpolations between stations. We rely on NEHRP Classification (A-E, given as an
associated average 30m shear velocity) and their corresponding amplification factors.
Typically, site conditions are derived from a GIS-based geology map (or at least digital)
that can be correlated appropriately with NEHRP site classifications.
4) Distance-Attenuation Relations. Ground-motion attenuation relationships (used for
infilling data gaps) must be suitable for the regional attenuation and potential earthquake
source locations and types. For example, for the Pacific Northwest, appropriate crustal
and subduction event equations are required. New relations can be easily added as PERL

**Northern California**
**Southern California**
**Pacific Northwest**
**Intermountain West**
**Mid-America**
**Northeast**
**Alaska**

**Hawaii**
*Coverage Area*. [TBS]
*Operations*
Triggering and Data Flow. [TBS]
Site Condition Map. [TBS]
Ground Motion Prediction and Conversion Equations

For deeper events, Youngs et al, (1997) is employed with coefficients for intraslab and interplate
events assigned by choosing default event depth ranges. The defaults can also be manually
overridden once independent information about the source is known. See Appendix A for more
details.

Other Local Characteristics: [TBS]

**Puerto Rico**
