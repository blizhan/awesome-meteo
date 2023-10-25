:sunny: Awesome Meteo :umbrella:
==

[![Mentioned in Awesome Meteo](https://awesome.re/mentioned-badge.svg)](https://github.com/blizhan/awesome-meteo)

Meteo is even more awesome, so we made this list to curate meteo related resources including open-source data, package softwares, documents and so on. Pull requests are always welcomed. 

:construction: :construction: :construction:  :rocket::rocket::rocket: In Construction :rocket::rocket::rocket: :construction: :construction: :construction:

## :books: Content

- :closed_book: [Data](#:closed_book:-Data)
- :green_book: [Packages & Softwares](#:green_book:-Packages-&-Softwares)
- :orange_book: [Algorithm](#:orange_book:-Algorithm)
- :blue_book: [Documents and Tutorials](#:blue_book:-Documents)



## :closed_book: Data

### :paperclip: Forecast Data :partly_sunny:

### :pushpin: Global Numerical Prediction Model
- ![ecmwf](static/icon/ecmwf.png)[ECMWF](https://www.ecmwf.int/en/forecasts/datasets/open-data) - A subset of ECMWF real-time forecast data with 0.4 degree resolution are made available to the public free of charge. The data includes deterministic forecasts(oper), ensemble forecasts(enfo), wave deterministic forecasts(wave) and wave ensemble forecasts(waef) .

    - ![http](static/icon/http.png)[ECMWF Data Store](https://data.ecmwf.int/forecasts/) - `https://data.ecmwf.int/forecasts/{{batch_date:%Y%m%d}}/{{batch_date:%H}}z/0p4-beta/{{product}}/{{batch_date:%Y%m%d%H}}0000-{{step}}h-{{product}}-{{datatype}}.grib2`
    - ![aws](static/icon/aws.png)[aws s3](https://registry.opendata.aws/ecmwf-forecasts/) - `s3://ecmwf-forecasts/{{batch_date:%Y%m%d}}/{{batch_date:%H}}z/0p4-beta/{{product}}/{{batch_date:%Y%m%d%H}}0000-{{step}}h-{{product}}-{{datatype}}.grib2`
- ![noaa](static/icon/noaa.png)[NOAA]()
    - ![http](static/icon/http.png)[nomads]()
    - ![aws](static/icon/aws.png)[aws s3]()
    - ![ftp](static/icon/ftp.png)[ftp](ftp://ftp.ncep.noaa.gov/pub/data/nccf/com/gfs/prod)

### :paperclip: Observation Data :satellite:

## :green_book: Packages & Softwares

### :paperclip: Data IO

#### GRIB
- ![c](static/icon/c.png)[eccodes](https://github.com/ecmwf/eccodes) - A package developed by ECMWF which provides an application programming interface for decoding and encoding messages in GRIB 1/2 and BUFR 3/4 format.
- ![python](static/icon/python.png)[pygrib](https://github.com/jswhit/pygrib) -  A high-level wrapped interface to the eccodes library for reading GRIB files.

#### netCDF

- ![c](static/icon/c.png)[netcdf-c](https://github.com/Unidata/netcdf-c) - The C interfaces for the Unidata network Common Data Form (netCDF), which is a self-describing, network-transparent, directly accessible, and extendible data format.

- ![pythib](static/icon/python.png)[netcdf4-python](https://github.com/Unidata/netcdf4-python) - Python/numpy interface to the netCDF C library.



## :orange_book: Algorithm
## :blue_book: Documents
