:sunny: Awesome Meteo :umbrella:
=================

[![Mentioned in Awesome Meteo](https://awesome.re/mentioned-badge.svg)](https://github.com/blizhan/awesome-meteo)

Meteo is even more awesome, so we made this list to curate meteo related resources including open-source data, package softwares, documents and so on. Pull requests are always welcomed. 

:construction: :construction: :construction:  :rocket::rocket::rocket: In Construction :rocket::rocket::rocket: :construction: :construction: :construction:

## :books: Table of Content


* [:closed_book: Data](#closed_book-data)
    * [:paperclip: Forecast Data](#paperclip-forecast-data-partly_sunny)
    * [:paperclip: Observation Data](#paperclip-observation-data-satellite)
* [:green_book: Packages & Softwares](#green_book-packages--softwares)
    * [:paperclip: Data IO](#paperclip-data-io)
* [:orange_book: Algorithm](#orange_book-algorithm)
* [:blue_book: Documents and Tutorials](#blue_book-documents)


## :closed_book: Data
### :paperclip: Forecast Data :partly_sunny:
### :pushpin: Global Numerical Prediction Model
- ![ecmwf](static/icon/ecmwf.png)[ECMWF](https://www.ecmwf.int/en/forecasts/datasets/open-data) - A subset of ECMWF real-time forecast data with 0.4 degree resolution are made available to the public free of charge. The data includes deterministic forecasts(oper), ensemble forecasts(enfo), wave deterministic forecasts(wave) and wave ensemble forecasts(waef) .

    - ![http](static/icon/http.png)[ECMWF Data Store](https://data.ecmwf.int/forecasts/) - `https://data.ecmwf.int/forecasts/{{batch_date:%Y%m%d}}/{{batch_date:%H}}z/0p4-beta/{{product}}/{{batch_date:%Y%m%d%H}}0000-{{step}}h-{{product}}-{{datatype}}.grib2`
    - ![aws](static/icon/aws.png)[aws s3](https://registry.opendata.aws/ecmwf-forecasts/) - `s3://ecmwf-forecasts/{{batch_date:%Y%m%d}}/{{batch_date:%H}}z/0p4-beta/{{product}}/{{batch_date:%Y%m%d%H}}0000-{{step}}h-{{product}}-{{datatype}}.grib2` (from 2023-01-18 to now)
- ![noaa](static/icon/noaa.png)[NOAA]() - The data includes deterministic forecasts(gfs), ensemble forecasts(gefs) and wave forecasts(gfswave).
    - ![http](static/icon/http.png)[nomads](https://nomads.ncep.noaa.gov/pub/data/nccf/com/gfs/prod/) - `https://nomads.ncep.noaa.gov/pub/data/nccf/com/gfs/prod/gfs.{{batch_date:%Y%m%d}}/{{batch_date:%H}}/atmos/gfs.t{{batch_date:%H}}z.pgrb2.0p25.f{{step:03}}`
    - ![aws](static/icon/aws.png)[aws s3](https://registry.opendata.aws/noaa-gfs-bdp-pds/) - `s3://noaa-gfs-bdp-pds/gfs.{{batch_date:%Y%m%d}}/{{batch_date:%H}}/gfs.t{{batch_date:%H}}z.pgrb2.0p25.f{{step:03}}` (from 2021-02-26 to now)
    - ![ftp](static/icon/ftp.png)[ftp]() - `ftp://ftp.ncep.noaa.gov/pub/data/nccf/com/gfs/prod/`
- ![http](static/icon/http.png)[DWD ICON](https://opendata.dwd.de/weather/nwp/) - ICON global, ICON-EU and high-resolution regional products from Deutscher Wetterdienst covering the globe and Europe.
    - ![http](static/icon/http.png)[Open Data hub](https://opendata.dwd.de/weather/nwp/icon/global/grib/) - `https://opendata.dwd.de/weather/nwp/icon/{{domain}}/grib/{{cycle}}/{{run_date:%Y%m%d}}/{{run_hour:%H}}/icon{{domain_suffix}}_{{forecast:03}}_{{level}}_{{parameter}}.grib2`
    - HTTPS-only access; no official FTP mirror is provided by DWD for ICON open data.

### :paperclip: Observation Data :satellite:

#### :pushpin: Station Oberservation
- ![http](static/icon/http.png)[NOAA ISD](https://www.ncei.noaa.gov/products/land-based-station/integrated-surface-database) - Global hourly and synoptic station data curated by NCEI.
    - ![http](static/icon/http.png)[HTTPS](https://www.ncei.noaa.gov/data/global-hourly/) - `https://www.ncei.noaa.gov/data/global-hourly/access/{{year}}/{{usaf}}-{{wban}}.csv`
    - ![ftp](static/icon/ftp.png)[FTP](https://www.ncei.noaa.gov/data/global-hourly/archive/) - `ftp://ftp.ncei.noaa.gov/pub/data/noaa/{{year}}/{{usaf}}-{{wban}}-{{year}}.gz`
#### :pushpin: Reanalysis

- ECMWF
    - [ERA5](https://www.ecmwf.int/en/forecasts/dataset/ecmwf-reanalysis-v5) - Hourly global reanalysis from 1940 to near-real-time at 0.25°.
        - ![http](static/icon/http.png)[CDS API](https://cds.climate.copernicus.eu/api-how-to) - `https://cds.climate.copernicus.eu/api/v2/resources/reanalysis-era5-single-levels`
        - ![http](static/icon/http.png)[CDS Portal](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview)
    - [ERA5-Land](https://www.ecmwf.int/en/forecasts/dataset/era5-land) - Land-surface focused reanalysis downscaled to 9 km resolution.
        - ![http](static/icon/http.png)[CDS API](https://cds.climate.copernicus.eu/api-how-to) - `https://cds.climate.copernicus.eu/api/v2/resources/reanalysis-era5-land`
- NASA
    - [MERRA-2](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/) - Modern-Era retrospective analysis with aerosol and chemistry support.
        - ![http](static/icon/http.png)[GES DISC](https://disc.gsfc.nasa.gov/datasets/M2I1NXASM_V5.12.4/summary) - `https://gpm1.gesdisc.eosdis.nasa.gov/data/MERRA2/{{collection}}/{{year}}/{{month}}/MERRA2_{{stream}}.{{product}}.{{date}}.nc4`


## :green_book: Packages & Softwares
### :paperclip: Data IO

#### :pushpin: GRIB
- ![c](static/icon/c.png)[eccodes](https://github.com/ecmwf/eccodes) - A package developed by ECMWF which provides an application programming interface for decoding and encoding messages in GRIB 1/2 and BUFR 3/4 format.
- ![python](static/icon/python.png)[pygrib](https://github.com/jswhit/pygrib) -  A high-level wrapped interface to the eccodes library for reading GRIB files.
- ![python](static/icon/python.png)[cfgrib](https://github.com/ecmwf/cfgrib) - Python interface to read GRIB files as xarray datasets using ecCodes.
- ![c](static/icon/c.png)[wgrib2](https://www.cpc.ncep.noaa.gov/products/wesley/wgrib2/) - Command line utility for manipulating and querying GRIB2 files.

#### :pushpin: netCDF

- ![c](static/icon/c.png)[netcdf-c](https://github.com/Unidata/netcdf-c) - The C interfaces for the Unidata network Common Data Form (netCDF), which is a self-describing, network-transparent, directly accessible, and extendible data format.
- ![pythib](static/icon/python.png)[netcdf4-python](https://github.com/Unidata/netcdf4-python) - Python/numpy interface to the netCDF C library.
- ![python](static/icon/python.png)[xarray](https://github.com/pydata/xarray) - Labeled multi-dimensional arrays built on netCDF data structures.
- ![java](static/icon/java.png)[netCDF-Java](https://github.com/Unidata/netcdf-java) - Java library and tools for reading, writing, and remote access of netCDF, HDF, and related data formats.



## :orange_book: Algorithm

## :blue_book: Documents
