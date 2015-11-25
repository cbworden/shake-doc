.. _users-guide:

####################
User's Guide
####################

ShakeMap originated primarily as an internet-based system for real-time display.  Although the online color-coded intensity maps are the most visible result of ShakeMap system and constitute the most commonly accessed and downloaded product, they are just one representation of the ShakeMap output.  ShakeMap produces grids of acceleration and velocity amplitudes, spectral response values, instrumental intensities, and uncertainty estimates as well as a variety of formats including: PDF, KML, GIS files, and a host of other products for the varied user needs and applications.  

In this User's Guide, we describe the basic ShakeMap products and their current and potential uses.  First, we provide an overview of the current ShakeMap users and applications.  We then explain the different formats and types of maps available and describe the ShakeMap web pages.  Next, we expand on different automated mechanisms to receive ShakeMap, including JSON and RSS feeds, and ShakeCast.  We also describe Scenario Earthquake ShakeMaps, which provide the basis for understanding the potential effects of large earthquakes in the future both for planning and mitigation efforts.  In each subsection, we try to provide concrete examples of potential uses of each product as well as notable users for each example.

===================
Background
===================

Until the development of ShakeMap, the most common information available immediately following a significant earthquake was typically its magnitude and epicenter.  However, the damage pattern is not a simple function of these two parameters alone, and more detailed information must be provided to properly ascertain the situation.  For example, for the magnitude-6.7 February 9, 1971, California earthquake, the northern San Fernando Valley was the region with the most damage, even though it was more than 15 km from the epicenter.  Likewise, areas strongly affected by the 1989 Loma Prieta and 1994 Northridge, California, earthquakes (magnitudes 6.9 and 6.7, respectively) that were either distant from the epicentral region or out of the immediate media limelight were not fully appreciated until long after the initial reports of damage. The full extent of damage from the magnitude-6.9 1995 Kobe, Japan, earthquake was not recognized by the central government in Tokyo until many hours later (e.g., Yamakawa, 1997), seriously delaying rescue and recovery efforts.

A ShakeMap is a representation of ground shaking produced by an earthquake. The information it presents is different from the earthquake magnitude and epicenter that are released after an earthquake because ShakeMap focuses on the ground-shaking produced by the earthquake, rather than the parameters describing the earthquake starting point (its hypocenter) and size (magnitude). So, although an earthquake has one magnitude and one epicenter, it produces a range of ground shaking levels at sites throughout the region, depending on distance from the earthquake fault that ruptured, the rock and soil conditions at sites, and variations in the propagation of seismic waves from the earthquake due to complexities in the structure of the Earth's crust. 

Part of the strategy for generating rapid-response ground-motion maps was to determine the best format for reliable presentation of the maps given the diverse audience, which includes scientists, businesses, emergency response agencies, media, and the general public.  In an effort to simplify and maximize the flow of information to the public, we have developed a means of generating not only peak ground acceleration and velocity maps, but also an instrumentally-derived, estimated Modified Mercalli Intensity (MMI) map.  This “instrumental intensity” map makes it easier to relate the recorded ground-motions to the expected felt and damage distribution. At the same time, we preserve a full range of utilities of recorded ground-motion data by producing maps of response spectral acceleration, which are not particularly useful to the general public, but which provide fundamental data for loss estimation and earthquake engineering assessments.


ShakeMap provides maps of peak ground-acceleration, velocity and spectral acceleration maps as well as Modified Mercalli Intensity. Intensity ShakeMaps depict estimated intensities derived from peak ground motions as well as (optionally) from reported intensities. Intensity maps make it easier to relate the recorded and estimated ground motions to the expected felt and damage distributions. Estimating intensities from ground shaking is based on analyses of intensities reported near recorded seismic stations for past earthquakes. The legend on the ShakeMap indicates which relationship was used to estimate intensities from ground motions, and vice versa. 

.. note:: **ShakeMap Symbology**. ShakeMap depicts seismic stations as **triangles** and intensity observations as **circles** (for cities) or **squares** (for geocoded boxes). On intensity maps, symbols are see-thru so that the underlying intensity values are visible. On peak ground motion maps observations are (optionally) color-coded to their amplitude according to the legend shown below each map. The epicenter is indicated with a **star**, and for larger earthquakes the surface projection of the causative fault is shown with **black lines**. 

Station locations are the best indicator of where the map is most accurate: Near seismic stations the shaking is well constrained by data; far from such stations, the shaking is estimated using standard seismological inferences and geospatial interpolation. Details about the interpolation, uncertainty maps, and codes for the seismic station components, network contributors, and potential outlier or clipped flag codes are provided in the ShakeMap Manual. **Peak** horizontal acceleration and spectral acceleration values are in units of percent-g (where g = acceleration due to the force of gravity = 981 cm/s/s). The peak values of the vertical components are not used in the construction of the maps. Peak velocity values are given (in cm/sec) at each station. Acceleration spectra are the response of a 5% critically damped, single-degree-of-freedom oscillator to the recorded ground motion at three reference periods: 0.3, 1.0, and 3.0 seconds. 

**ShakeMap Archives**. The ShakeMap Archives consist of **Recent ShakeMaps**, the **ShakeMap Atlas** for historic earthquakes (primarily 1970-2012), and hypothetical earthquake **ShakeMap Scenarios**. For example, scenario earthquakes compiled for northern and southern California represent over 200 different earthquake ruptures studied for California, as detailed in the section on ShakeMap Scenarios.

=================================
Applications of ShakeMap
=================================

Prior to fully describing the array of ShakeMap products and formats, we briefly expand on the most common applications of ShakeMap.

Emergency Management and Response
-------------------------------------------------

The distribution of shaking in a large earthquake, whether expressed as peak acceleration or intensity, provides responding organizations a significant increment of information beyond magnitude and epicenter.  Real-time ground-shaking maps provide an immediate opportunity to assess the scope of an event, that is, to determine what areas were subject to the highest intensities and probable impacts as well as those that received only weak motions and are likely to be undamaged.  These maps have found additional utility in supporting decision-making regarding mobilization of resources, mutual aid, damage assessment, and aid to victims

For example, the M7.1 Hector Mine earthquake of October 16, 1999, provides an important lesson in the use of ShakeMap to assess the scope of the event and to determine the level of mobilization necessary.  This earthquake produced ground-motion that was widely felt in the Los Angeles basin and, at least in the immediate aftermath, required an assessment of potential impacts.  It was rapidly apparent, based on ShakeMap, that the Hector Mine earthquake was not a disaster and despite an extensive area of strong ground shaking, only a few small desert settlements were affected. Thus, mobilization of a response effort was limited to a small number of companies with infrastructure in the region and brief activations of emergency operations centers in San Bernardino and Riverside Counties and the California Office of Emergency Services (now the California Emergency Management Agency, or EMA), Southern Region.

Unnecessary response in an effort to fully assess the potential effects of an earthquake, although not as costly as inadequate or misguided response in a real disaster, can be costly as well. Had a magnitude-7 earthquake occurred in urban Los Angeles or another urban area in California, ShakeMap could have been employed to quickly identify the communities and jurisdictions requiring immediate response.  To help facilitate the use of ShakeMap in emergency response, ShakeMap is now provided to organizations with critical emergency response functions automatically through ShakeCast (see section Error! Reference source not found.) and other web-based tools. These organizations and utilities include, for example, the U. S. Nuclear Regulatory Commission, the International Atomic Energy Agency (IAEA), the State of California EMA, the Los Angeles County Office of Emergency Management, the California Department of Transportation, East Bay Metropolitan Utility District, and the Los Angeles Metropolitan Water District.  

ShakeMap ground-motion maps are also customized and formatted into Geographic Information Systems (GIS) shape files for direct input into the FEMA’s Hazards U.S. (HAZUS; FEMA REF) loss estimation software. These maps are rapidly and automatically distributed to FEMA for computing HAZUS loss estimates and for coordinating State and Federal response efforts.  This is a major improvement in loss-estimation accuracy because actual ground-motion observations are used directly to assess damage rather than relying on simpler estimates based on epicenter and magnitude alone, as was customary.

A ShakeMap-driven calculation of estimated regional losses can provide focus to the mobilization of resources and expedite the local, State, and Federal disaster declaration process, thus initiating the response and recovery machinery of Government.  ShakeMap, when overlaid with inventories of critical lifelines and facilities (e.g., hospitals, utilities, and substations, etc.), highways and bridges, and vulnerable structures, provides an important means of prioritizing response. Such response activities include: shelter and mass care, emergency management, damage and safety assessment, utility and lifeline restoration, and emergency public information.

In addition to GIS-formatted maps specifically design for HAZUS, we also make shape files for more general GIS use.  A number of new product formats are now provided to keep up with developments in web, GIS, imagery, and automated downloading and data parsing. These formats include: i) grid.xml, an XML file of the latitude/longitude pairs that make up the ShakeMap grid, including all estimated parameters (intensity measures), along with the Vs30 values used at each grid point for site corrections, ii) an enhanced KML file for Google Earth allowing for overlays, zoom capabilities, station locations, fault files, and parameter contour lines, iii) uncertainty grids for all ground-motion parameters, iv) ESRI raster grid files, and v) ground-motion contours and stations in text and GeoJSON format. These formats are described in detail below. 


Loss Estimation and Financial Decision-Making
----------------------------------------------------------

 [TBS]
 
Earthquake Engineering and Seismological Research
-----------------------------------------------------
For potentially damaging earthquakes, ShakeMap also produces response spectral acceleration values at three periods (0.3, 1.0, and 3.0 s) for use not only in loss estimation as mentioned earlier, but also for earthquake engineering analyses.  Response spectra for a given location are useful for portraying the potential effects of shaking on particular types of buildings and structures.  Following a damaging earthquake, ShakeMaps of spectral response will be key for prioritizing and focusing post-earthquake occupancy and damage inspection by civil engineers.

In addition to providing information on recent events, ShakeMap Web pages provide maps of shaking and ground-motion parameters for past significant earthquakes.  Engineers have found these maps helpful in evaluating the maximum and cumulative effects of seismic loading for the life of any particular structure.  This is particularly relevant given the discovery of the potential damage to column/beam welds in steel buildings following the 1994 Northridge earthquake.
 
In seismological research, ShakeMap has been proven particularly effective in gaining a quick overview of the effects of geological structure and earthquake rupture processes on the nature of recorded ground-motions.  ShakeMaps showing the distribution of recorded peak ground acceleration (PGA) and peak ground velocity (PGV) overlain on regional topography maps allow scientists to gauge the effects of local site amplification because topography is a simple proxy for rock versus deep-basin soil-site conditions.  This can lead to more detailed investigations into the nature of the controlling factors in generating localized regions of damaging ground-motions.

ShakeMap is also a source frequently used by scientists developing Ground Motion Prediction Equations (GMPEs), Ground Motion/Intensity Conversation Equations (GMICEs), and other studies where accumulated peak ground motion data are useful.

 [TBS] IPEs, loss modeling, L&L, Atlas uses, etc. (REFERENCES)

Public Information and Education
-----------------------------------------
The rapid availability of ShakeMap on the Internet combined with the urgent desire for information following a significant earthquake makes this mapping tool a source of emergency public information and education. In instances in which an earthquake receives significant news coverage, the ShakeMap site as well as the “Did You Feel It?” (DYFI) system receives an enormous increase in web site visitors.  

Acknowledging the importance of ShakeMap as a tool for public information and education, we developed

 [TBS]

[Web page update 

 [TBS]


=========================
Products and Formats
=========================
ShakeMap is fundamentally a geographic product: the spatial representation of the potentially very complex shaking associated with an earthquake. Because of its complicated nature, we are required to generate numerous maps that portray various aspects of the shaking that are customized for specific uses or audiences.  For some uses, it is not the maps but the components that make up the ShakeMaps that are of interest in order to recreate or further customize the maps.  In this section we further describe these ShakeMap component products and the variety of maps and formats.

Input Files
---------------------
The downloadable products include sufficient information to reproduce the ShakeMap. In particular, stationlist.xml and the fault .txt file(s) provide the input files, grid.xml provides the Vs30 grid (see above), and info.xml provides the important configuration and processing parameters [including the name(s) of the fault file(s)].

*Station Lists*. The file stationlist.xml contains the combined input data from all of the original processing center’s input files in a ShakeMap-readable format. The file may contain seismic station data, intensity data, or a combination of both. The file also contains an event tag with the earthquake source specifications. [Note: At this time it is necessary to copy the event tag and place it in a file event.xml in the event’s input directory for ShakeMap to process the event normally. We hope to remove this requirement in a future release.] See the ShakeMap Software Guide for a complete specification of the ShakeMap input XML formats.

For reasons of backward compatibility we also provide stationlist.txt. As with grid.xyz the use of this file is deprecated and it may disappear in a future release.

*Fault Files*. Fault files are named <something>_fault.txt and are listed in info.xml. Zero or more fault files may be present in the ShakeMap input directory. See the ShakeMap Software Guide for a complete specification of the fault file format. For the purposes of reproducing the ShakeMap for an earthquake, it is sufficient to copy the specified file(s) into the event’s input directory.

Output Files
---------------------

For each earthquake that warrants generating a ShakeMap, all maps and associated products for that event are available via the “Downloads” link on the earthquake-specific Web pages.

ShakeMap products include:

* **Metadata and Primary ShakeMap Constraint and Runtime Information**
   * XML file of processing parameters
   * FGDC-compliant metadata

* **Input files**
   * XML earthquake and station data file
   * Fault file(s)
 
* **Grids of interpolated ground shaking**
   * XML grid of ground motions
   * XML grid of ground motions on “rock”
   * XML grid of ground-motion uncertainty
   * Text grid of ground motions (deprecated)

* **GIS files of ground shaking**
   * Shapefiles of ground motions
   * Shapefiles specifically formatted for use in HAZUS
   * ESRI raster grid files
   * KML files for Google Earth

* **Images (JPEG and compressed PostScript)**
   * Macroseismic Intensity
   * Peak Ground Acceleration, Peak Ground Velocity, and Pseudo-Spectral Acceleration (when appropriate)
   * Uncertainty

Each of these products is described in more detail in the sections that follow.

**Metadata and ShakeMap Constraints and Runtime Information**

* FGDC-compliant metadata. [TBS]
* XML file of processing parameters [TBS]

.. _sec_interpolated_grid_file:
     
Interpolated Grid Files
^^^^^^^^^^^^^^^^^^^^^^^^^

As described in the Technical Manual, the fundamental output product of the ShakeMap processing system is a finely sampled grid of latitude and longitude pairs with associated amplitude values of shaking parameters at each point.  These amplitude values are derived by interpolation of a combination of the recorded ground shaking observation and estimated amplitudes, with consideration of site amplification at all interpolated points.  The resulting grid of amplitude values provides the basis for generating color-coded intensity contour maps, for further interpolation to infer shaking at selected locations, and for generating GIS-formatted files for further analyses.

**XML Grid**. The ShakeMap XML grid file is the basis for nearly all ShakeMap products, as well as for computerized post-processing in systems such as ShakeCast and PAGER [section refs??]. The XML grid is available as both plain text (grid.xml) and compressed as a zip file (grid.xml.zip).

As XML, the grid is meant to be self-describing, however we describe the format here for the sake of completeness.

After the XML header, the first line is the shakemap_grid tag:

 ::

   <shakemap_grid xsi:schemaLocation="http://earthquake.usgs.gov
   http://earthquake.usgs.gov/eqcenter/shakemap/xml/schemas/shakemap.xsd" event_id="19940117123055" 
   shakemap_id="19940117123055" shakemap_version="2" code_version="3.5.1446" process_timestamp=
   "2015-10-30T20:38:19Z" shakemap_originator="us" map_status="RELEASED" shakemap_event_type=
   "ACTUAL"><event event_id="19940117123055" magnitude="6.6" depth="19" lat="34.211000" lon="-118.546000"  
   event_timestamp="1994-01-17T12:30:55UTC" event_network="us" event_description="Northridge,
   California"/><grid_specification lon_min="-120.296000" lat_min="32.763750" lon_max="-116.796000" 
   lat_max="35.658250" nominal_lon_spacing="0.008333" nominal_lat_spacing="0.008341" nlon="421"
   nlat="348"/><event_specific_uncertainty name="pga" value="0.442632" numsta="871"/><event_specific_
   uncertainty name="pgv" value="0.488617" numsta="868"/><event_specific_uncertainty name="mi" value="0.677466" 
   numsta="875"/><event_specific_uncertainty name="psa03" value="0.514850" numsta="864"/><event_specific_
   uncertainty name="psa10" value="0.541189" numsta="869"/><event_specific_uncertainty name="psa30" 
   value="0.568793" numsta="867"/><grid_field index="1" name="LON" units="dd"/><grid_field index="2" 
   name="LAT" units="dd"/><grid_field index="3" name="PGA" units="pctg"/><grid_field index="4" name="PGV"
   units="cms"/><grid_field index="5" name="MMI" units="intensity"/><grid_field index="6" name="PSA03"
   units="pctg"/><grid_field index="7" name="PSA10" units="pctg"/><grid_field index="8" name="PSA30"
   units="pctg"/><grid_field index="9" name="STDPGA" units="ln(pctg)"/><grid_field index="10" name="URAT"
   units=""/><grid_field index="11" name="SVEL" units="ms"/><grid_data>

Aside from schema information, the shake_map grid tag provides the following attributes:

 :: 

  *event_id*:  Typically this will a string of numbers and/or letters with with or without a network
  ID prefix (e.g., “us100003ywp”), though in the case of major historic earthquakes, scenarios, or
  other special cases it may be a descriptive string, as above (“Northridge”).
  *shakemap_id*: Currently the same as event_id, above.
  *shakemap_version*: The version of this map, incremented each time a map is revised or reprocessed 
  and transferred.
  *code_version*: The version of the ShakeMap software used to make the map.
  *process_timestamp*: The date and time the event was processed.
  *shakemap_originator*: The network code of the center that produced the map.
  *map_status*: Currently always the string “RELEASED” but other strings may be used in the future.
  *shakemap_event_type*: Either “ACTUAL” (for real earthquakes) or “SCENARIO” for scenarios.

The next tag describes the earthquake source:

 ::

  <event event_id="Northridge" magnitude="6.7" depth="18" lat="34.213000" lon="-118.535700"
   event_timestamp="1994-01-17T12:30:55GMT" event_network="ci" event_description="Northridge" />

Most of the attributes are self-explanatory:

 :: 

  *event_id*: See above.
  *magnitude*: The earthquake magnitude.
  *depth*: The depth (in km) of the earthquake hypocenter.
  *lat/lon*: The latitude and longitude of the earthquake epicenter.
  *event_timestamp*: The date and time of the earthquake.
  *event_network*: The authoritative seismic network in which the earthquake occurred.
  *event_description*: A string containing the earthquake name or a location string (e.g., “13 km SW of Newhall, CA”).

Following the event tag is the grid_specification tag:

 ::

   <grid_specification lon_min="-119.785700" lat_min="33.379666" lon_max="-117.285700" 
   lat_max="35.046334" nominal_lon_spacing="0.008333" nominal_lat_spacing="0.008333" nlon="301"
   nlat="201" />
  *lon_min/lon_max*: The boundaries of the grid in longitude.
  *lat_min/lat_max*: The boundaries of the grid in latitude.
  *nominal_lon_spacing*: The expected grid interval in longitude within the resolution of the 
  numeric format of the output.
  *nominal_lat_spacing*: The expected grid interval in latitude within the resolution of the 
  numeric format of the output.
  *nlon/nlat*:	The number of grid points in longitude and latitude. The grid data table will contain nlon times nlat rows.

This is followed by a number of grid_field tags:

 ::

 <grid_field index="1" name="LON" units="dd" />
 <grid_field index="2" name="LAT" units="dd" />
 <grid_field index="3" name="PGA" units="pctg" />
 <grid_field index="4" name="PGV" units="cms" />
 <grid_field index="5" name="MMI" units="intensity" />
 <grid_field index="6" name="PSA03" units="pctg" />
 <grid_field index="7" name="PSA10" units="pctg" />
 <grid_field index="8" name="PSA30" units="pctg" />
 <grid_field index="9" name="STDPGA" units="ln(pctg)" />
 <grid_field index="10" name="URAT" units="" />
 <grid_field index="11" name="SVEL" units="ms" />

Each tag specifies a column in the grid table that follows.

 ::

  index:  The column number where the specified parameter may be found. The first column is column “1.”
  name:   Description of the parameter in the given column.
  LON:    Longitude of the grid location (the “site”).
  LAT:    Latitude of the site.
  PGA:    Peak ground acceleration at the site.
  PGV:    Peak ground velocity.
  MMI:    Seismic intensity.
  PSA03:  0.3 s pseudo-spectral acceleration.
  PSA10:  1.0 s pseudo-spectral acceleration.
  PSA30:  3.0 s pseudo-spectral acceleration.
  STDPGA: The standard error of PGA at the site (in natural log units).
  URAT:   The uncertainty ratio. The ratio STDPGA to the nominal standard error of the GMPE at the site (no units).
  SVEL:   The 30-meter shear wave velocity (Vs30) at the site.

The measurement units:

 ::

   dd:   	Decimal degrees.
   pctg: 	Percent “g” (i.e., nominal Earth gravity).
   cms: 	Centimeters per second.
   intensity: 	Generally Modified Mercalli Intensity, but potentially other intensity measures.
   ms: 		Meters per second.
   ln(pctg):	Natural log of percent g.
   ln(cms):	Natural log of centimeters per second.

The number of grid_field tags will vary: smaller-magnitude earthquakes may not have the pseudo-spectral acceleration values; scenarios will not have STDPGA or URAT; maps that have not been site corrected will not have SVEL.

The grid_field tags are followed by the grid_data tag, the gridded data, and the closing tags:

 ::

  <grid_data>
  -119.7857 35.0463 4.3 4.21 5.26 5.76 5.76 1.09 0.5 1 800
  -119.7774 35.0463 4.34 4.23 5.27 5.8 5.78 1.1 0.5 1 800
  -119.7690 35.0463 4.37 4.25 5.27 5.84 5.81 1.1 0.5 1 800
  …
  </grid_data>
  </shakemap_grid>

The fast index for the coordinates is longitude, the slow index is latitude. Dimensions are from upper left to lower right (i.e., from longitude minimum/latitude maximum to longitude maximum/latitude minimum). The GMT program “xyz2grd” (coupled with “gmtconvert”) is particularly useful for converting the grid.xml data into a usable grid file.

**Rock Grid XML**. The file rock_grid.xml.zip is a zipped XML file containing the interpolated grid without site amplifications applied. The grid has the same structure as grid.xml (see section Error! Reference source not found. above), but Vs30 values and PGA uncertainty values are not supplied. 

**Uncertainty Grid XML**. The file uncertainty.xml.zip is a zipped XML file containing the standard errors for each of the ground-motion parameters at each point in the output grid. It has the same structure as grid.xml (see section Error! Reference source not found. above), with the additional grid_field names:

 ::

  STDPGA:	Standard error of peak ground acceleration.
  STDPGV:	Standard error of peak ground velocity.
  STDMMI:	Standard error of seismic intensity.
  STDPSA03:	Standard error of 0.3 s pseudo-spectral acceleration.
  STDPSA10:	Standard error of 1.0 s pseudo-spectral acceleration.
  STDPSA30:	Standard error of 3.0 s pseudo-spectral acceleration.

The standard errors are given in natural log units, except for intensity (linear units). The PSA entries will be available only if the PSA ground motion parameters were mapped (typically only for earthquakes of M ≥ 5.0.

No ground motion data or Vs30 values are available in uncertainty.xml.zip; for those, use grid.xml.zip.

**Grid XYZ**

grid.xyz is a plain-text, comma-separated, file of gridded ground motions.

.. note:: the use of this file is deprecated. It is difficult to maintain and have it remain backward compatible. All users are urged to use the XML grids instead, and to switch to the XML grids if they are using grid.xyz. grid.xyz will disappear in a future ShakeMap release.

GIS Products
^^^^^^^^^^^^^^^^^^^^
ShakeMap processing does not occur in a Geographic Information System (GIS), but we post-process the grid file (above) into raster and shape files for direct import into GIS. The file base names in each archive are abbreviations of the type of ground-motion parameter:

 ::

	mi    =  macroseismic intensity (usually, but not necessarily, mmi)
	pga   =  peak ground acceleration
	pgv   =  peak ground velocity
	psa03 =  0.3 s pseudo-spectral acceleration
	psa10 =  1.0 s pseudo-spectral acceleration
	psa30 =  3.0 s pseudo-spectral acceleration

The sub-sections that follow describe available file and product types.

*Shape Files*. GIS shape files are comprised of four or five standard associated GIS files:

 :: 

  .dbf = A DBase file with layer attributes
  .shp = The file with geographic coordinates
  .shx = An index file 
  .prj = A file containing projection information 
  .lyr = A file containing presentation properties (only available for PGA, PGV, and MMI)

In this application, the shape files are contour polygons of the peak ground-motion amplitudes in ArcView shape files. These contour polygons are actually equal-valued donut-like polygons that sample the contour map at fine enough intervals to accurately represent the surface function. We generate the shape files independent of a GIS using a shareware package (shapelib.c). Contouring, as well as polygon formation and nesting, is performed by a program written in C by Bruce Worden, and included in the ShakeMap software distribution.

There is an archive of files (four or five files for each of the mapped parameters) compressed in Zip format. The following two subsections describe the two shape file archives routinely produced by ShakeMap.

*HAZUS’99 Shape Files and HAZUS-MH Geodatabases*. We generate shape files that are designed with intervals that are appropriate for use with the Federal Emergency Management Agency’s (FEMA) HAZUS software, though they may be imported into any GIS package that can read ArcView shape files.  Because HAZUS software requires peak ground velocity (PGV) in inches/s, this file may not be suitable for all applications.  The contour intervals are 0.04g for PGA and the two spectral acceleration parameters (HAZUS only uses the 0.3 and 1. s periods), and 4 inches/s for PGV. 

HAZUS’99 users can use the hazus.zip shape files (see below) directly.  However, the 2004 release of HAZUS-MH uses geodatabases, not shape files.  As of this writing, FEMA has a temporary fix in the form of Visual Basic script that imports ShakeMap shape files and exports geodatabases.  FEMA has plans to incorporate such a tool directly into HAZUS-MH in the next official release  (D. Baush, FEMA, Region VIII, oral commun., 2004).

HAZUS traditionally used the epicenter and magnitude of an earthquake as reported, and used empirical relationships to estimate ground-motions over the affected area.  These simplified ground estimates would drive the computation of losses to structures and infrastructure, estimates of casualties and displaced households (for more details, see Kircher et al., 1997; FEMA, 1997).  With the improvements to seismic systems nationally, particularly in digital strong-motion data acquisition, and the advent of ShakeMap, HAZUS now can directly import a much more accurate description of ground shaking.  The improved accuracy of the input to loss- estimation routines can dramatically reduce the uncertainty in loss estimation due to poorly constrained shaking approximations.  

The HAZUS GIS files are only generated for events that are larger than (typically) magnitude 4.5.  The set of shape files for these parameters is an archive of files (three files for each of the mapped parameters) compressed in Zip format (hazus.zip) to facilitate file transfer.

.. note:: An important note on the values of the parameters in the HAZUS shape files is that they are empirically corrected from the standard ShakeMap peak ground-motion values to approximate the (geometric) mean values as used for HAZUS loss estimation.  HAZUS was calibrated to work with mean ground-motion values (FEMA, 1997).  Peak amplitudes are corrected by scaling values down by 15 percent (Campbell, 1997; Joyner, oral commun., 2000). 

If you are unfamiliar with using shape files to run HAZUS, we have created a brief tutorial in cooperation with the California Office of Emergency Services (OES, now CA EMA) that can be downloaded from the ShakeMap Web pages (under Products).

*GIS Shape File*. Contour polygons for the peak ground-motion parameters are also available as shape files intended for use with any GIS software that can read ArcView shape files.  Note, however, that the peak ground velocity (PGV) contours are in cm/s, and are therefore NOT suitable for HAZUS input. 

The contour intervals are 0.04g for peak ground acceleration (PGA) and the three spectral-acceleration parameters, and 2 cm/s for PGV. The file also includes MMI contour polygons in intervals of 0.2 intensity units.  These shape files have the same units as the online ShakeMaps.

The archive of files (three files for each of the mapped parameters) is compressed in Zip format, and called shape.zip.  The shape.zip file is available for all events, but the spectral values are generally only included for earthquakes of magnitude 5.0 and larger.

*ESRI Raster Files (.fit files)*. ESRI raster grids of the ground-motion parameters and their uncertainties are also available. The files are found in a Zipped archive called raster.zip. Each archive contains four files per parameter: <param>.fit and <param>.hdr, which contain the ground-motion data, and <param>_std.fit and <param>_std.hdr, which contain the uncertainties for the ground motions. See grid.xml for information on units. As with the other GIS files, PGA, PGV and MMI are available for all events, while the spectral-acceleration parameters are usually included for earthquakes M5.0 and larger.

This page lists all of the individual files from each of the products we use to convey information about an earthquake.  A "product", in this context, is something like ShakeMap, PAGER, or Did You Feel It (DYFI), each of which contains various maps, graphs, and data files in various formats. ShakeMap products have the most geospatial data.  For GIS users, the two files you might be the most interested in are the "GIS Files" and the "ESRI Raster Files". For FEMA’s HAZUS users, the appropriate files are zipped together in the “hazus.zip” file. 

The GIS Files (zipped) are a collection of shapefiles of contours of the ShakeMap model outputs for each shaking metric: MMI, PGA, PGV, and PSA at three periods.  These vectors should be easily importable into a GIS. The ESRI Raster Files (also zipped) are a collection of ESRI formatted binary files.  It should be relatively easy to convert these to (for example) ArcGIS GRIDS using the standard tools provided with the software. The contours are useful primarily for overlaying with other data for visualization purposes.  If you plan to do analysis, where you need to know the MMI value at a particular point(s), then we would suggest using the raster data.

**Loading ShakeMaps into ArcGIS**.

1) Open the ArcToolbox in ArcMap
2) Select Multidimension Tools->Make NetCDF Raster Layer
3) In the dialog that appears, select the input .grd file you downloaded and unzipped, and name the layer appropriately ("vs30", etc.)
4) The vs30 layer should appear in your list of layers.
5) Note: This layer is ephemeral - if you want to keep the raster version of the data, you'll have to save the layer to a file.

For examples, find the GIS files on the "Downloads" tab for the `Oct 15, 2013 Philippines earthquake
<http://earthquake.usgs.gov/earthquakes/eventpage/usb000kdb4#>`_. 

Google Earth Overlay
^^^^^^^^^^^^^^^^^^^^^^^^^
The file <event_id>.kml enables the user to view the ShakeMap within Google Earth (or other KML-compliant application). A color-scaled intensity overlay is provided along with a complete station list, contours of intensity and peak ground motion, a fault representation (if provided), epicenter indicator, intensity scale, and a USGS logo. The transparency of the intensity overlay is adjustable by the user, as is the appearance of seismic stations. The KML file automatically links to several other files in the event’s download directory:

 :: 

   epicenter.kmz
   fault.kmz
   overlay.kmz (links to ii_overlay.png)
   stations.kmz
   contours.kmz

These files are loaded as network links with reasonable timeouts so the user can expect them to update as new versions of the event’s ShakeMap are produced and updated.

In addition to the ShakeMap produced KML file, the USGS produces a KML file (linked near the top of the page in the event-centric pages with the title “Google Earth KML”) which contains not only ShakeMap data, but also data from PAGER, Did You Feel It?, and other sources. This file should be the preferred source, as it will have the most up to date links.

Map Images
^^^^^^^^^^^^^^^^^^
ShakeMap generates a number of ground-motion maps for various parameters. Most of these maps are available in JPEG format, as well as zipped PostScript. The next three subsections describe these maps.

*Intensity Maps*. These maps, typically of MMI, but potentially other intensity measures, are the most familiar ShakeMap products. The main intensity map consists of a colored overlay of intensity with the epicenter (and the causative fault, if supplied) prominently marked, (usually) overlain upon the region’s topography, with other geologic and cultural features (cities, roads, faults, etc.) plotted, depending on the configuration of the ShakeMap system. A detailed scale of intensity is also provided.

[ Insert Intensity map here ]

If seismic stations are available they are usually plotted as colored triangles. Intensity observations, when available, are usually plotted as colored circles. On the web site, clicking on the stations will bring up a list of the stations and their amplitudes. 

ShakeMap also produces two versions of the intensity map designed for use by the media. These media maps are somewhat larger, use larger, bold fonts, have less text overall, and use a simplified intensity scale. One version of the media map has a few cultural features (large cities, roads), and a distance scale. The “bare” version of the map has only the intensity overlain upon topography, the epicenter, and the fault (if one is used) – this allows art departments to dress the map according to the media outlets’ standards.

[ Insert media map here ] [ Insert bare media map here ]

An info sheet (called tvguide.txt) is also available to accompany the media maps. The info sheet, intended to bring reporters quickly up to speed, provides references, contact information, and a simplified description of ShakeMap and seismic intensity.

*Ground-Motion Maps*. In addition to the high-visibility intensity maps, ShakeMap also produces maps of the various PGM parameters. These maps typically have colored topography (as opposed to the intensity map’s shaded topography), a set of cultural and geographic features similar to the intensity map’s, but the ground motions are indicated by a set of isoseismal contours. The locations of the seismic stations and intensity observations are usually indicated by filled triangles and circles, respectively. The fill color may indicate the identity of the source network or, optionally, may indicate the ground motion of the station converted to intensity. When the color indicates intensity, a color scale bar will be provided at the bottom of the map.

[ Insert PGM map here ]

*Uncertainty Maps*. As discussed in section XXXX, gridded uncertainty is available for all ground motion parameters, as well as the ratio of the ShakeMap PGA uncertainty to the GMPE’s uncertainty (see section XXXX). 

We utilize the uncertainty ratio to produce a graded map of uncertainty. Where the ratio is 1.0 (meaning the ShakeMap is purely predictive), the map is colored white. Where the ratio is greater than 1.0 (meaning that the ShakeMap uncertainty is high because of unknown fault geometry) the map shades toward dark red, and where the uncertainty is less than 1.0 (because the presence of data decreases the uncertainty) the map shades toward dark blue. These maps provide a quick visual summary of quality of the ground motion estimates over the area of interest.

ShakeMaps are also given a letter grade, based on the mean uncertainty ratio within the area of the MMI 6 contour (on the theory that this is the area most important to accurately represent). A ratio of 1.0 is given a grade of “C.” Maps with mean ratios greater than 1.0 get grades of “D” or “F.” Ratios less than 1.0 earn grades of “B” or “A.” If the map does not contain areas of MMI ≥ 6, no grade is assigned. See the example map below.

[ Insert Uncertainty map here ]

*Supplemental Grid Information: info.xml*. The file info.xml provides a machine-readable rundown of many important ShakeMap processing parameters. It includes information about the data and fault input files, the source mechanism, the GMPE, IPE, and GMICE used, the type and source of the site amplifications, the map boundaries, the bias and maximum amplitude for each parameter, and other information useful in understanding or reproducing the way the event was processed.

Grid File Metadata
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Because the grid is the fundamental derived product from the ShakeMap processing, it is fully described in an accompanying metadata file following Federal Geographic Data Committee (FGDC) standards for geospatial information.  We do not generate metadata for the parametric data, because that is archived by the regional seismic networks.  In fact, because all other ShakeMap products are derived from the gird file, it is sufficient to fully characterize only the grid file using the metadata standards. 

This metadata file is distributed via the event-specific Web pages for each earthquake on the download page. The metadata are provided in text, HTML, and XML formats in the files metadata.txt, metadata.html, and metadata.xml, respectively.

Real-Time Product Distribution, Automatic Access and Feeds
---------------------------------------------------------------
ShakeMap products are distributed by a number of means immediately after they are produced. The intent of these products is to help emergency responders and other responsible parties to effectively manage their post-earthquake activities, and so we make it as easy as possible for users with a variety of technological sophistication and infrastructure to access them. The general are: interactive Web downloads, RSS feeds, GeoJSON feeds, ShakeCast, the Product Delivery Layer (PDL) client, and with ArcGIS (Web Mapping) services. 

Interactive Web Downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The easiest way to obtain ShakeMap products immediately following an earthquake is from the `ShakeMap <http://earthquake.usgs.gov/shakemap/>`_ or `USGS Earthquake Program web pages <http://earthquake.usgs.gov/>`_. The variety of formats for ShakeMap are described in the previous section.

RSS Feeds
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
USGS Earthquake Program earthquake information `Feeds <http://earthquake.usgs.gov/earthquakes/feed/v1.0/>`_ currently include Really Simply Syndication (RSS) feeds. The RSS feeds are being demoted; they will be decommission in 2016. 

GeoJSON Feeds
^^^^^^^^^^^^^^^^^^^^^^^^
Automatically Retrieving Earthquake Data and ShakeMap Files 
In order to automatically ingest the above data, then use our automated feeds:
http://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php

GeoJSON is an extension of the standard JavaScript Object Notation (JSON) format.  There are JSON parsers in most modern languages, including Python, Perl, Matlab, and R.

Mike Hearne (USGS), provides `example python scripts <https://github.com/mhearne-usgs/>`_
(e.g., *getevent.py*) for querying the USGS M2.5+ 30 day GeoJSON feed, and downloading the most recent version of the event products desired by the user.

ShakeCast System
^^^^^^^^^^^^^^^^^^^^^^^^
:ref:`ShakeCast <sec_shakecast>` delivers user-specified
ShakeMap products to the user’s machine(s), and runs fragility-based damage (or
inspection priority) calculations for specific portfolios. 

More advanced features of ShakeCast include a complete suite of damage
estimation and mapping tools, coupled with sophisticated tools to notify
responsible parties within an organization on a per-facility basis.

Product Delivery Layer (PDL) Client
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Finally, for academic and government users, ShakeMap products (and other earthquake products) are communicated through the USGS’s Product Distribution Layer (PDL)

 
Web Mapping (GIS) Services 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In addition to downloadable GIS formatted ShakeMaps (including shapefiles) are readily available for each ShakeMap event, USGS also hosts a real-time `30-day *Signficant* Earthquake GIS ShakeMap Feed  <http://geohazards.usgs.gov/arcgis/rest/services/ShakeMap/ShakeMap/MapServer>`_. `ESRI <http://www.esri.com/>`_ provides a separate `Disaster Response ArcGIS service <http://www.esri.com/>`_, providing live feeds to `live feeds <https://tmservices1.esri.com/arcgis/rest/services/LiveFeeds/USGS_Seismic_Data/MapServer>`_ to several USGS post-earthquake products. 

.. note:: `USGS 30-day *Signficant* Earthquake GIS ShakeMap Feed <http://geohazards.usgs.gov/arcgis/rest/services/ShakeMap/ShakeMap/MapServer>`_

.. seealso:: `ESRI USGS post-earthquake products Web Mapping Service  <https://tmservices1.esri.com/arcgis/rest/services/LiveFeeds/USGS_Seismic_Data/MapServer>`_

.. sidebar:: Related GIS Service Interactions

   Users can access the ShakeMap data behind the GIS service in a variety of ways via the ArcGIS Server REST API. Some examples of commonly used data access options are detailed below.

   `Export Map Image <http://resources.arcgis.com/en/help/rest/apiref/export.html>`_: Download a static image of the map to include in their work.

   `Identify <http://resources.arcgis.com/en/help/rest/apiref/identify.html>`_: Retrieve service data for given geographic location. (Point, Line, Polygon or Envelop)

   `Find <http://resources.arcgis.com/en/help/rest/apiref/find.html>`_: Query service data that contains certain attributes. (ex. ShakeMap data for distinct event id)  

   `Query <http://resources.arcgis.com/en/help/rest/apiref/query.html>`_: Query a specific layer in a service and return a detailed featureset. 

   Along with the common GIS service interactions listed above, there are many other calls that GIS developers can make through the `REST API <http://resources.arcgis.com/en/help/rest/apiref/>`_.

A note on *earthquake significance*: The NEIC associates a `*significance* <https://github.com/usgs/earthquake-event-ws/blob/master/src/lib/sql/fdsnws/getEventSummary.sql#L157>`_
number with each earthquake event. Larger numbers indicate more significance. This value is determined by a number of factors, including: magnitude, maximum MMI, felt reports, and estimated impact.  The significance number ranges from 0 to 1000.  The "30 day significant earthquake feed" that determines which events are included in the ShakeMap GIS feed, uses events with a significance of 600 and greater.  

Accessing ShakeMap GIS Files. While this GIS service only provides access to significant earthquakes that have occurred within the last 30 days, users can download GIS files for `significant events <https://tmservices1.esri.com/arcgis/rest/services/LiveFeeds/USGS_Seismic_Data/MapServer>`_ on our website after the 30 day period.  The significant earthquake archive has a list of large events with links to each event’s web page.  From the event page, users can click on the ShakeMap tab and navigate to the “Downloads” section to get a zipped bundle of shapefiles.

Acknowledgement: USGS appreciates guidance from the Esri Aggregated Live Feed team, more specifically Derrick Burke and Paul Dodd.  Their willingness to share best practices for robust real time sharing of GIS data enabled this project to be completed.

=================================
Online ShakeMap Repositories
=================================

All ShakeMaps are available for viewing and download online. There are three primary repositories. 

Real-time ShakeMaps
---------------------------------------------------

 [TBS]

ShakeMap Atlas
---------------------------------------------------

 [TBS] (Garcia et al, 2012)

ShakeMap Scenarios
--------------------------
ShakeMap earthquake scenarios are ordinary ShakeMaps, but made for specific potential earthquakes. By specifying a fault geometry and location, and earthquake magnitude, the ShakeMap system can generate predictive maps of potential median ground motions for that scenario. ShakeMap automatically includes local effects due to site conditions, and can include effects from basin depth and directivity, if desired.

In planning and coordinating emergency response, utilities, local government, and other organizations are best served by conducting training exercises based on realistic earthquake situations—ones that they are most likely to face. Scenario earthquakes can fill this role. Scenario maps can be used to examine exposure of structures, lifelines, utilities, and transportation conduits to specific potential earthquakes. The ShakeMap Web pages now have a special section under the Archives pages that display selected earthquake scenarios.  Additional scenario events will be supplied as they are requested. To request a scenario, please contact the ShakeMap Development Team through the comment form available on the Web site.

Given a selected event, we have developed tools to make it relatively easy to generate a ShakeMap earthquake scenario. First we need to assume a particular fault or fault segment will (or did) rupture over a certain length or segment. We then determine the magnitude of the earthquake based on assumed rupture dimensions. Next, we estimate the ground shaking at all locations in the chosen area around the fault, and then represent these motions visually by producing ShakeMaps. The scenario earthquake ground-motion maps are identical to those made for real earthquakes—with one exception: ShakeMap scenarios are labeled with the word “SCENARIO” prominently displayed to avoid potential confusion with real earthquake occurrences.  

At present, ground-motions are estimated using empirical attenuation relationships (though we can use gridded ground motion estimates from other sources for those who wish to provide them). We then correct the amplitudes based on the local site soil conditions (NEHRP, see Borcherdt, 1994) as we do in the general ShakeMap interpolation scheme.  Fault finiteness is included explicitly, basin depth can be incorporated where appropriate, and source directivity is included via the relationships developed by Rowshandel (2010).  Depending on the level of complexity needed for the scenario, event-specific factors, such as variable slip distribution, could also be incorporated in the amplitude estimates fed to ShakeMap.  

ShakeMap earthquake scenarios can be an integral part of earthquake emergency response planning. ShakeMap scenarios are particularly useful in planning and exercises when combined with loss estimation systems, such as PAGER, HAZUS and ShakeCast, which provide ShakeMap-based estimates of overall social and economic impact, detailed loss estimates, and inspection priorities, respectively. Since its inception, ShakeMap operators have generated hundreds of earthquake scenarios that have been used in formal earthquake response exercises around the Nation and around the world. 

The U.S. Geological Survey has evaluated the probabilistic hazard from active faults in the United States for the National Seismic Hazard Mapping Project.  From these maps it is possible to prioritize the best scenario earthquakes to be used in planning exercises by considering the most likely candidate earthquake fault first, followed by the next likely, and so on.  Such an analysis is easily accomplished by hazard disaggregation, in which the contributions of individual earthquakes to the total seismic hazard, their probability of occurrence, and the severity of the ground-motions are ranked.  Using the individual component earthquakes of these hazard maps, a user can properly select the appropriate scenarios given their location, regional extent, and specific planning requirements. As of this writing, we are in the process of generating scenario maps for all of the events in the current NSHMP hazard maps, and they should be available on the web site soon.
Scenarios are of fundamental interest to scientific audiences interested in the nature of the ground shaking likely experienced in past earthquakes as well as the possible effects due to rupture on known faults in the future.  In addition, more detailed and careful analysis of the ground-motion time histories (seismograms) produced by such scenario earthquakes is highly beneficial for earthquake-engineering considerations.  Engineers require site-specific ground-motions for detailed structural response analysis of existing structures and future structures designed around specified performance levels. 

They can also be used as a planning tool to identify shortcomings in the existing seismic networks to clarify where instrumentation should be focused.  

Our ShakeMap earthquake scenarios have become an integral part of emergency-response planning.  Primary users include city, county, State and Federal Government agencies (e.g., the California EMA, FEMA), and emergency-response planners and managers for utilities, businesses, and other large organizations. Scenarios are particularly useful in planning and exercises when combined with loss-estimation systems such as HAZUS, which provides scenario-based estimates of social and economic impacts.


===================
Related Systems
===================

While ShakeMap has met with success as a standalone product for communicating earthquake effects to the public and the emergency response and recovery community, it is increasingly being incorporated into value-added products that help in the assessment of earthquake impacts for response management and government officials.

As discussed in detail the :ref:`technical-guide`, ShakeMap is augmented by DYFI? input for constraining intensities, and from those, estimates of peak ground motions (in some cases, and for some regions), as shown in Figure #related-systems. DYFI? and ShakeMap in conjuction then represent the shaking hazard input for two other primary systems that estimated losses: ShakeCast and PAGER. ShakeCast is intended for specific users to priority response for specific user-centric portfolios of facilities; PAGER is for more general society impact assessments, providing estimated loss-of-life and economic impacts for the region affected. 

.. figure::  _static/SMap.SCast.DYFI.PAGER.png
   :scale: 45%
   :alt: Related Systems
   :align: center
   :target: Related Systems

   Interplay between ShakeMap, DYFI?, ShakeCast and PAGER.	    

.. figure::  _static/IAEA.ShakeCast.*
   :scale: 35%
   :alt: IAEA ShakeCast
   :align: right
   :target: IAEA ShakeCast

   Interational Atomic Enegery Agency (IAEA) ShakeCast Report
 
.. _sec_shakecast:

ShakeCast
---------------------------------------------------

`ShakeCast <http://earthquake.usgs.gov/shakecast/>`_ is a freely available,
post-earthquake situational awareness application that automatically retrieves
earthquake shaking data from ShakeMap, compares intensity measures against
users’ facilities, and generates potential damage assessment notifications,
facility damage maps, and other Web-based products for emergency managers and
responders.

ShakeCast, short for ShakeMap Broadcast, is a fully automated system for
delivering specific ShakeMap products to critical users and for triggering
established post-earthquake response protocols. While ShakeMap was developed
and is used primarily for emergency response, loss estimation, and public
information, for an informed response to a serious earthquake, critical users
must go beyond just looking at ShakeMap, and understand the likely extent and
severity of impact on the facilities for which they are responsible. To this
end the USGS has developed ShakeCast.

ShakeCast allows utilities, transportation agencies, businesses, and other
large organizations to control and optimize the earthquake information they
receive. With ShakeCast, they can automatically determine the shaking value at
their facilities, set thresholds for notification of damage states for each
facility, and then automatically notify (by pager, cell phone, or email)
specified operators and inspectors within their organizations who are
responsible for those particular facilities so they can set priorities for
response.

.. figure::  _static/Nepal.M7.8.onepager.V5.*
   :scale: 25%
   :alt: Nepal onePAGER 
   :align: right
   :target: Nepal OnePAGER Alert Example 

   Nepal OnePAGER Alert Example  
 
PAGER
---------------------------------------------------
Another important USGS product that uses ShakeMap output as its primary data source is `PAGER (Prompt Assessment of Global Earthquakes for Response) <http://earthquake.usgs.gov/pager/>`_, an automated system that produces content concerning the impact of significant earthquakes around the world, informing emergency responders, government and aid agencies, and the media of the scope of the potential disaster. PAGER rapidly assesses earthquake impacts by comparing the population exposed to each level of shaking intensity with models of economic and fatality losses based on past earthquakes in each country or region of the world. Earthquake alerts – which were formerly sent based only on event magnitude and location, or population exposure to shaking – now will also be generated based on the estimated range of fatalities and economic losses.

================
Disclaimers
================

General Disclaimer
---------------------------


.. warning:: Some USGS information accessed through this page may be preliminary in nature and presented prior to final review and approval by the Director of the USGS. This information is provided with the understanding that it is not guaranteed to be correct or complete, and conclusions drawn from such information are the sole responsibility of the user. In addition, ShakeMaps are automatic, computer-generated maps and have not necessarily been checked by human oversight, so they may contain errors. Further, the input data is raw and unchecked, and may contain errors.

* Contours can be misleading since data gaps may exist. Caution should be used in deciding which features in the contour patterns are required by the data. Ground motions and intensities can vary greatly over small distances, so these maps are only approximate.

* Locations within the same intensity area will not necessarily experience the same level of damage since damage depends heavily on the type of structure, the nature of the construction, and the details of the ground motion at that site. For these reasons, more or less damage than described in the intensity scale may occur. The ground motion levels and descriptions associated with each intensity value are based on recent damaging earthquakes. There may be revisions in these parameters as more data become available or due to further improvements in methodologies.

* Large earthquakes can generate very long-period ground motions that can cause damage at great distances from the epicenter; although the intensity estimated from the ground motions may be small, significant effects to large structures (bridges, tall buildings, storage tanks) may be notable.

ShakeMap Update Policy
---------------------------------------------------

.. warning:: ShakeMaps are preliminary in nature and will be updated as data arrives from a variety of distributed sources. Our practice is to improve the maps as soon as possible, but there are factors beyond our control that can result in delayed updates (see examples below).

* For regions around the world, were there are insufficient near-real time strong motion seismic stations to generate an adequate, strong-ground-motion data-controlled ShakeMap, we can still provide a very useful estimate of the shaking distribution using the ShakeMap software. Site amplification is approximated from a relationship developed between topographic gradient and shear-wave velocity. Additional constraints for these predictive maps come primarily from  additional earthquake source information, particularly fault rupture dimensions, observed macroseismic intensities (including via the USGS "Did You Feel It?" system, and observed strong ground motions, when and where available.
    
* There is no formal “final” version of any ShakeMap. Version Control is up to users. ShakeMap version numbers and time  stamps are provided on the maps, web pages, and grid files, and metadata.

* Our strategy is to update ShakeMaps as warranted from a scientific perspective. We reserve the option to update ShakeMaps as needed to add data or to improve scientific merit and/or presentation of the maps in any way beneficial. This most typical update is after new data arrive, finite-fault models get established or revised, magnitude gets revised, or as improved site amplification maps, ground motion prediction equations, or even interpolation or other procedures become available. 

.. sidebar:: Recent ShakeMap update examples:

  * For the very deadly 2008 Wenchuan, China, earthquake, the Chinese strong motion data were not made available for several months. 
  * For the 2011, Tohoku, Japan earthquake, the magnitude was updated from 7.9 to 8.9 over the course of the first hour after origin time. The Japanese strong motion data processing center was impacted by the earthquake yet they provided data for nearly a thousand seismic stations within several days after the earthquake. These vital data were added to the ShakeMap as soon as they became available. .
  * Due to telemetry limitations, some important seismic station data for the 2014 American Canyon, California, earthquake came in minutes, hours, and as late as four days after that event. The data were added to the ShakeMap soon after they were received and processed. The magnitude also changed from an initial M5.7 to M6.0 and this, too, affected the ShakeMap. Lastly, the causative fault location was added by the Northern California ShakeMap operators several days after the earthquake, modifying the ShakeMap.

**Updates to Online Maps**

   * **Real-time ShakeMap Updates**. Changes can be tracked with the ShakeMap version numbers and time stamps found in the metadata, the *info.xml* and *grid.xml* files, and on the maps themselves (time generated). The info.xml file contains time stamps, number of stations used, GMPE  information, and many other attributes that could have changed from version to version. Often a text statement is provided that notes significant changes for a particular version. 

   * **ShakeMap Atlas Updates**. The ShakeMap Atlas also uses version numbers for each Atlas event, yet the overall Atlas collections is also Versioned. Currently ShakeMap Atlas Version 2.0 is online in the ComCat database, yet the older Atlas (Version 1.0) can be found online on the `legacy ShakeMap Archives pages <http://earthquake.usgs.gov/earthquakes/shakemap/>`_.

   * **Scenario Revisions**. ShakeMap Scenario collections also uses version numbers for each event, yet the overall scenario collections is also named according to their source. The latest collection is [TBS]. Currently ShakeMap Atlas Version 2.0 is online in the USGS `Comprehensive Catalogue (ComCat) Earthquake database <http://earthquake.usgs.gov/earthquakes/search/>`_, Some archival (older) scenarios are online on the `legacy ShakeMap Archives pages <http://earthquake.usgs.gov/earthquakes/shakemap/>`_. Scenario ShakeMaps will be revised when the underlying problabilistic seismic map fault segmentation or other particulars (like GMPE selection) change. Older versions will be archived in `ComCat <http://earthquake.usgs.gov/earthquakes/search/>`_.


	
