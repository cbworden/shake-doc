.. _future-directions:

####################
Future Directions
####################


ShakeMap 4.0 (Python)
----------------------

The release of ShakeMap version 4.0 represents a major departure from previous versions. All of the important computational modules have been refactored into the Python programming language, and make use of the tools in the widely available Python “scientific distribution.” The core ShakeMap code, approaching fifteen years old, was due for a major overhaul to more organically incorporate the many extensions that had been added over its lifetime, and to facilitate several new demands from ShakeMap software and ShakeMap’s expanded role as a global provider of post-earthquake information, earthquake scenarios, and as the input to loss modeling software.  

One of the advantages of the rewrite of ShakeMap into the Python language was the availability of the GEM OpenQuake (OQ) library of Ground Motion Prediction Equations (GMPEs). The OQ hazard library provided us with a broad range of well-tested, high performance, open source GMPEs. Due to constraints imposed by the software architecture of earlier implementations of ShakeMap, the development of GMPE modules was time consuming and difficult, which restricted the number and timeliness of the available modules. The OQ library provides a broad array of current GMPE modules, as well as a framework for easily adding new modules (whether by GEM or ShakeMap staff), jumpstarting our efforts to re-implement ShakeMap.

The OQ hazard library also provides supporting functions for using the GMPE modules, including a set of software classes for computing the various distance measures required by the GMPEs. The ShakeMap fault model, however, was somewhat more general than allowed for by the OQ planar surface modules, so we sub-classed the OQ “surface” class and implemented our own high performance module. The open-source, cooperative nature of the OQ project allowed us to contribute our new module back to the OQ repository, and thus make it available to other users.

In addition to the GEM OQ library, there are a number of other advantages to using Python in an application like ShakeMap.  The dynamic nature of the language means that development time is much reduced, allowing a small team to generate useful code in a short amount of time.  Also, there is an active scientific computing Python community that has created many tools that solve common problems, including an array object for vectorized operations, input/output routines for common data formats, and plotting/mapping libraries.  These tools again help to reduce development time and effort.


Scientific
----------------------

Algorthmic 
----------------------

Limitations and shortcomings. Known, unknown. Potential areas of improvement include:

Planned Improvements
^^^^^^^^^^^^^^^^^^^^^^^^^^^
L&L grid

PGV-> intensity at high M/PGV (including simulated ground motions)
Naturally though, we are most concerned about accurately portraying the highest intensities. For example, approximately 86 percent of the residential losses in the Northridge earthquake occurred in the intensity VII-IX region (Kircher et al., 1997, p. 714). Intensity IX was the largest mapped value for that event. Despite this data, and data from a few other damaging earthquakes, the PGM-Intensity relationship is not well constrained at the highest levels of shaking. While intensities up to VIII are reasonably well represented, above this level there are still very few intensity observations that are closely paired with ground-motion recordings. While the existing GMICE assume a linear continuation of the PGM-Intensity relationships (from V/VI to VIII) to higher levels of shaking, it remains to be seen if these relationships hold, or even if PGM alone is sufficient to characterize the highest macroseismic intensities.

Scenario Library and Search Capabilities
Limitations and shortcomings. Known, unknown. Potential areas of improvement include:
Listing of topics: 

* Planned Improvements
* L&L grid
* PGV-> intensity at high M/PGV (including simulated ground motions)

Naturally though, we are most concerned about accurately portraying the highest intensities. 
For example, approximately 86 percent of the residential losses in the Northridge earthquake 
occurred in the intensity VII-IX region (Kircher et al., 1997, p. 714). Intensity IX was the 
largest mapped value for that event. Despite this data, and data from a few other damaging 
earthquakes, the PGM-Intensity relationship is not well constrained at the highest levels 
of shaking. While intensities up to VIII are reasonably well represented, above this 
level there are still very few intensity observations that are closely paired with ground-motion 
recordings. While the existing GMICE assume a linear continuation of the PGM-Intensity 
relationships (from V/VI to VIII) to higher levels of shaking, it remains to be seen if 
these relationships hold, or even if PGM alone is sufficient to characterize the highest 
macroseismic intensities.

* Virtualize Machine/CLOUD-based operations 
* GMT5/Python
* Spatial variability
* Kriging
* Canned GMPE libraries: GEM
* Interactive maps
* Rendering Info.xml
* Dynamic plots (Regression, bias, outliers, stations amplitudes, 
* Directivity (SPudich et al 2014)
* Improved and additional site amplification approaches and tables (e.g., Choi and Stewart, 2005) 
* Basin terms for NGA-West 2 GMPEs
* Consideration of vector PGM’s, duration.

We are constantly re-evaluating or considering the use of additional ground-motion parameters, 
or intensity measures, for ShakeMap.  However, any such additions cannot be made lightly.  
In part, this is due to the fact that the seismic network processing streams that produce 
parametric data for ShakeMap in different ANSS regions vary significantly. Indeed, even 
within the southern California region, ShakeMap data is produced both in real time with 
recursive filtering as well as with rapid post-processing, and this is done by three 
different agencies. Mandating changes in such systems is not straightforward. Likewise, 
the addition of parameters in the processing stream not only takes more processing time, 
but we also like to limit the number of maps due to computational, bookkeeping, and 
storage efficiency considerations. 

Candidates for additional parameters include energy or comparable measures (like 
cumulative average velocity, CAV) that include effects of duration and vector-based 
measures (e.g., Safak, 2000), and static displacement. However, ongoing engineering 
and loss-estimation research has not led to a obvious candidate that would justify 
overcoming the aforementioned obstacles so they have not warranted serious consideration 
at this time.

