<div align="center">

# Awesome ICESat-2

A curated list of awesome ICESat-2 software, libraries, services, portals, and learning resources.

Inspired by [awesome-python](https://github.com/vinta/awesome-python) and structure adapted from [awesome-sar](https://github.com/RadarCODE/awesome-sar).

</div>

---

## Contents

- [General / Multi-Purpose](#general--multi-purpose)
- [Data Discovery & Access APIs](#data-discovery--access-apis)
- [Cloud & Scalable Processing](#cloud--scalable-processing)
- [Python Libraries](#python-libraries)
- [Point Cloud / Geospatial Tooling](#point-cloud--geospatial-tooling)
- [Visualization & Exploration](#visualization--exploration)
- [Thematic Science Tools](#thematic-science-tools)
- [Quality, Calibration & Ancillary Data](#quality-calibration--ancillary-data)
- [Tutorials, Courses & Notebooks](#tutorials-courses--notebooks)
- [Portals & Data Archives](#portals--data-archives)
- [Related Missions & Complementary Datasets](#related-missions--complementary-datasets)
- [Community & Communication](#community--communication)
- [Contributing](#contributing)

---

## General / Multi-Purpose

* [icepyx](https://github.com/icepyx/icepyx) - Unified Python interface for discovery, access, subsetting, and basic analysis of ICESat-2 (ATL*) products via NASA APIs.
* [SlideRule Earthdata](https://github.com/SlideRuleEarth/sliderule) - Server-side on-demand ICESat-2 photon subsetting, filtering, and derived metrics with Python & C++ API clients.
* [OpenAltimetry](https://openaltimetry.org/) - Web platform for interactive browsing, filtering, and quicklooks of ICESat-2 and ICESat elevation tracks.
* [NSIDC ICESat-2 Data Guide](https://nsidc.org/data/icesat-2) - Official product documentation, user guides, and ancillary references for all ATL datasets.
* [Earthdata Search](https://search.earthdata.nasa.gov/search?q=ICESat-2) - NASA web interface to discover, subset, and order ICESat-2 granules with custom spatial/temporal filters.

## Data Discovery & Access APIs

* [NASA CMR API](https://cmr.earthdata.nasa.gov/search/site/docs/search/api.html) - REST search endpoint for programmatic discovery of ICESat-2 granules and collections.
* [NSIDC Subsetting API](https://nsidc.org/support/subsetting) - API enabling spatial, temporal, and parameter-level subsetting of ICESat-2 ATL products.
* [Harmony API](https://harmony.earthdata.nasa.gov/) - NASA cloud orchestration API for standardized reformatting, reprojection, and subsetting (emerging ICESat-2 support).
* [SlideRule API](https://slideruleearth.io/rtd/) - High-performance RPC endpoints providing photon-level filtering, ATL03 to ATL08 style products, and derived height metrics.
* [AWS Open Data (ICESat-2)](https://registry.opendata.aws/icesat-2/) - Public S3 buckets hosting near-real-time ICESat-2 ATL products for direct cloud-native access.
* [Earthdata Login / EDL](https://urs.earthdata.nasa.gov/) - Authentication service required for most programmatic ICESat-2 data requests.
* [uip (Unified Ingest Portal) Status](https://status.earthdata.nasa.gov/) - Operational status of NASA endpoints (useful when diagnosing failed data pulls).

## Cloud & Scalable Processing

* [SlideRule on AWS](https://slideruleearth.io/) - Managed clusters and deploy recipes for large-scale photon querying and derived raster generation.
* [ICESat-2 Hackweek Cloud Templates](https://github.com/ICESAT-2HackWeek) - Reusable Jupyter/Cloud workflow examples from community hackweeks for rapid startup.
* [HyP3 (ASF)](https://hyp3-docs.asf.alaska.edu/) - On-demand processing platform (SAR-focused) that increasingly interoperates with ICESat-2 derived analyses.
* [Open Science Lab (NSIDC)](https://nsidc.org/opensciencelab) - Cloud-hosted workflows and reproducible examples including ICESat-2 Jupyter notebooks.
* [Pangeo](https://pangeo.io/) - Community cloud ecosystem enabling scalable analysis (ICESat-2 photon & gridded data with dask/xarray patterns).

## Python Libraries

* [icepyx](https://github.com/icepyx/icepyx) - Streamlines search, download, subsetting, and reading of multiple ATL product HDF5 structures.
* [sliderule-python](https://github.com/SlideRuleEarth/sliderule-python) - Python client to query SlideRule services and retrieve photon and elevation products as dataframes/arrays.
* [ATL03 Reader Examples](https://github.com/nsidc/NSIDC-Data-Tutorials/tree/main/ICESat-2) - Official sample code for opening and interpreting ATL03 & higher-level products.
* [h5py](https://github.com/h5py/h5py) - Fundamental HDF5 interface used to navigate ICESat-2 file hierarchies and metadata.
* [xarray](https://github.com/pydata/xarray) - Labeled N-D data structures facilitating gridding and combining ATL products (esp. ATL10, ATL14, ATL15).
* [geopandas](https://github.com/geopandas/geopandas) - Vector geospatial operations for ground tracks, region-of-interest clipping, and spatial joins.
* [Shapely](https://github.com/shapely/shapely) - Geometric operations used for photon filtering by polygons or buffered tracks.
* [pdal-python](https://github.com/PDAL/PDAL) - Point cloud filters and pipelines adaptable to photon-level (ATL03) processing workflows.
* [laspy](https://github.com/laspy/laspy) - Read/write LAS/LAZ allowing export/interchange of ICESat-2 derived point clouds to lidar ecosystems.
* [pyproj](https://github.com/pyproj4/pyproj) - Coordinate transformations (e.g., WGS84 <-> polar stereographic) essential for polar ATL products.
* [rasterio](https://github.com/rasterio/rasterio) - Creation and manipulation of gridded elevation/freeboard/rasterized photon density outputs.
* [scipy](https://scipy.org/) - Interpolation, signal filtering, and statistical operations on photon elevations and waveforms.
* [numpy](https://github.com/numpy/numpy) - Core numerical array computations underlying all higher-level processing.

## Point Cloud / Geospatial Tooling

* [PDAL](https://pdal.io/) - Extensible point cloud processing engine for classification, thinning, and reprojection of photon data.
* [Entwine](https://entwine.io/) - Builds efficient point cloud octrees enabling web visualization of derived ICESat-2 point sets.
* [Potree Converter](https://github.com/potree/PotreeConverter) - Converts point clouds (e.g., exported ATL03 photons) into multiresolution formats for web viewing.
* [GDAL](https://gdal.org/) - Foundational raster & vector translation library supporting HDF5 subdatasets and reprojection.
* [Proj](https://proj.org/) - Standalone cartographic transformations brand powering pyproj & GDAL coordinate operations.
* [WhiteboxTools](https://www.whiteboxgeo.com/) - Terrain analysis utilities useful after gridding surface heights from ICESat-2.

## Visualization & Exploration

* [OpenAltimetry](https://openaltimetry.org/) - Interactive web map to explore tracks, segments, elevations, and canopy metrics.
* [sliderule-jupyter](https://github.com/SlideRuleEarth/sliderule-python/tree/master/notebooks) - Notebook examples for dynamic photon queries and quick visual diagnostic plots.
* [Kepler.gl](https://kepler.gl/) - Browser-based large-scale geospatial visualization for photon point CSV exports.
* [Geoviews / Holoviews](https://geoviews.org/) - High-level Python visualization building dynamic datashaded photon density plots.
* [Plotly Express](https://plotly.com/python/plotly-express/) - Interactive scatter and profile plots of track segments and elevations.
* [Potree](https://potree.org/) - Web point cloud viewer for 3D exploration of converted photon clouds.

## Thematic Science Tools

* [ATL11 Time Series Toolkit](https://github.com/ICESAT-2HackWeek/ATL11_ice_focused) - Example workflows for multi-pass elevation change using repeat-track ATL11.
* [ATL14/ATL15 Gridded Products](https://nsidc.org/data/ATL14) - Basin-scale ice sheet elevation change and reference surface products for mass balance studies.
* [ICESat-2 Sea Ice Dashboard](https://earth.gsfc.nasa.gov/cryo/data/icesat-2) - NASA visualizations & summaries of sea ice freeboard and thickness metrics.
* [Freeboard & Thickness Notebooks](https://github.com/ICESAT-2HackWeek/sea-ice) - Community notebooks deriving sea ice freeboard/thickness from ATL07/ATL10.
* [Canopy Height (ATL08) Workflows](https://github.com/ICESAT-2HackWeek/vegetation) - Examples extracting vegetation structure metrics for ecology applications.
* [Inland Water Elevation (ATL13)](https://nsidc.org/data/ATL13) - Derived inland water surface heights facilitating hydrologic storage change analyses.
* [Ocean Surface Height (ATL12)](https://nsidc.org/data/ATL12) - Sea surface height and geophysical corrections for oceanography and circulation studies.
* [Photon Classification Models](https://github.com/ICESAT-2HackWeek/photon-classification) - Machine learning examples for separating signal and noise photons.

## Quality, Calibration & Ancillary Data

* [ATL02](https://nsidc.org/data/ATL02) - Raw telemetry with photon time-of-flight and instrument engineering for advanced calibration research.
* [ATL09](https://nsidc.org/data/ATL09) - Atmospheric layer & cloud flag data supporting photon filtering and canopy penetration assessment.
* [DEM Auxiliary Data (REMA/ArcticDEM)](https://www.pgc.umn.edu/data/arcticdem/) - Polar DEM mosaics used for reference elevation and geolocation QA.
* [ICESat GLAS (Legacy)](https://nsidc.org/data/icesat) - Historical laser altimetry providing multi-decadal context for elevation change.
* [GRACE/GRACE-FO Mascon](https://podaac.jpl.nasa.gov/GRACE) - Complementary mass balance signals to compare with ICESat-2 elevation change in ice sheets.
* [ERA5 Reanalysis](https://cds.climate.copernicus.eu/) - Atmospheric state variables for correcting backscatter or interpreting surface processes.

## Tutorials, Courses & Notebooks

* [ICESat-2 Hackweek Archives](https://icesat-2-2023.hackweek.io/) - Curated schedule, lecture recordings, and code from annual community hackweeks.
* [NSIDC Data Tutorials](https://github.com/nsidc/NSIDC-Data-Tutorials/tree/main/ICESat-2) - Official step-by-step Python notebooks for opening, filtering, and plotting ATL datasets.
* [NASA Earthdata Webinars](https://www.earthdata.nasa.gov/learn/webinars-and-tutorials) - Recorded sessions often featuring ICESat-2 access and application topics.
* [SlideRule Documentation & Notebooks](https://slideruleearth.io/rtd/) - API usage guides, performance notes, and reproducible photon workflow examples.
* [Pangeo Gallery ICESat-2](https://gallery.pangeo.io/) - Shared scientific notebooks demonstrating cloud-native analysis patterns.
* [OpenAltimetry Tutorials](https://openaltimetry.org/data/about) - Usage guides for track selection, filtering, and downloading subsets.

## Portals & Data Archives

* [NSIDC DAAC](https://nsidc.org/daac) - Primary archive and distribution for all operational ICESat-2 ATL collections and documentation.
* [NASA Earthdata Search](https://search.earthdata.nasa.gov/) - Unified granule discovery interface across DAACs including NSIDC.
* [AWS S3 ICESat-2 Buckets](https://registry.opendata.aws/icesat-2/) - Direct public object store access enabling parallelized cloud compute without downloads.
* [OpenAltimetry Download](https://openaltimetry.org/data/download) - Lightweight selection and retrieval interface for specific track segments and variables.
* [OPeNDAP (via Harmony/Hyrax)](https://wiki.esipfed.org/HDF-EOS:OPeNDAP) - Subsetting and partial variable retrieval for select ATL products to minimize transfers.
* [GCMD Keywords](https://gcmd.earthdata.nasa.gov/) - Controlled vocabulary aiding precise product discovery and dataset tagging.

## Related Missions & Complementary Datasets

* [ICESat (GLAS)](https://nsidc.org/data/icesat) - Predecessor laser altimetry mission enabling multi-epoch elevation change assessment.
* [GEDI](https://gedi.umd.edu/) - Spaceborne waveform lidar complementing ICESat-2 canopy height sampling for biomass analyses.
* [CryoSat-2](https://earth.esa.int/eogateway/missions/cryosat) - Radar altimetry mission offering complementary sea ice thickness and ice sheet elevation trends.
* [Sentinel-1 SAR](https://sentinel.esa.int/) - Active microwave backscatter supporting surface type classification and change detection alongside elevation trends.
* [Landsat Collection](https://landsat.gsfc.nasa.gov/) - Multispectral imagery for land cover context and seasonal melt pond / vegetation mapping.
* [MODIS / VIIRS Snow & Sea Ice](https://nsidc.org/data/modis) - Daily snow/ice products enabling temporal context for elevation/freeboard retrievals.

## Community & Communication

* [ICESat-2 Hackweek Slack](https://icesat-2.hackweek.io/) - Real-time discussion channels for workflows, troubleshooting, and collaboration (event-specific access).
* [NSIDC User Support](https://nsidc.org/support) - Helpdesk for data access, documentation, and product interpretation questions.
* [Earthdata Forum](https://forum.earthdata.nasa.gov/) - Official Q&A forum covering API access, subsetting, and dataset usage topics.
* [AGU Cryosphere Sessions](https://www.agu.org/) - Conference sessions highlighting latest ICESat-2 science and methods developments.
* [Twitter/X #ICESat2](https://twitter.com/search?q=%23ICESat2) - Social feed for mission news, data releases, and application highlights.

---

## Contributing

Contributions welcome! Please open an issue or pull request adding a resource with: (1) Name, (2) URL, (3) one-sentence description, (4) category suggestion. Keep descriptions concise, neutral, and avoid promotional language. Duplicates or out-of-scope links (non-ICESat-2 focused) may be declined to maintain curation quality.

---

## License

Distributed under the MIT License. See `LICENSE` for details.
