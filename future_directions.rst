.. image:: _static/usgs_banner.*

.. _future-directions:

####################
Future Directions
####################

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

