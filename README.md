### Talha Aksoy

Associate Professor (Doçent), Department of Landscape Architecture, Kırklareli University.
I work at the intersection of remote sensing, GIS, spatial statistics and computational
landscape analysis — Google Earth Engine, UAV photogrammetry, and physics-derived measures
of spatial order applied to ecological and landscape problems.

The tools below are small, single-purpose and dependency-light. Each runs entirely in the
browser: no server, no upload, nothing leaves the device. They exist because the field work
needed them.

---

#### 🛰️ [Overpass Planner](https://tlhksy.github.io/Overpass/) · [repo](https://github.com/tlhksy/Overpass)

When will a satellite pass over my field site, and where will the sun be at that moment?
Click a point on the map; the page fetches current orbital elements, propagates them with
SGP4, and returns the overpass times for Sentinel-2, Landsat, Sentinel-1 and MODIS — each
with the sub-satellite ground track, a swath-edge warning, and the solar elevation, zenith
and **true solar time** at closest approach. Built to align UAV flights with satellite
acquisitions, so drone and image see the same illumination geometry.

#### 🗺️ [Pafta — GIS ⇄ CAD converter](https://tlhksy.github.io/Convert/) · [repo](https://github.com/tlhksy/Convert)

A vector converter between GIS and CAD formats: reads Shapefile, GeoJSON, KML, GPX, CSV;
writes DXF, Shapefile, GeoJSON, KML, CSV; transforms coordinate reference systems. The point
is not the conversion — it is the **loss report**. Every run says exactly what it gave up:
field names truncated to ten characters, layers transliterated to ASCII, polygon holes split
into separate polylines. It refuses to write a DXF in geographic coordinates, because a
unitless drawing measured in degrees is silently broken. Transforms agree with PROJ to better
than a millimetre; outputs are checked in CI against pyshp and ezdxf, not its own readers.
Turkish TUREF and ED50 zones alongside the standard UTM grid.

#### 🚶 [Field Visibility Recorder](https://tlhksy.github.io/LandscapeWalker-/) · [repo](https://github.com/tlhksy/LandscapeWalker-)

A phone-first field tool for walking a transect: at each stop, photograph and classify the
view, and the app records position, camera azimuth, route bearing, GPS elevation and segment
slope. A built-in clinometer measures ground slope and object height from the phone's
orientation sensors. Everything is stored on the device and picks up where you left off;
export as a printable site report, GeoJSON for GIS/GEE, or a CSV attribute table.

---

<sub>Turkish and English · falsification-first · methods before conclusions</sub>
