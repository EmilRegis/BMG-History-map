!/bin/bash

# do NOT forget to install `python-gdal` library
# assuming you are on a debian like OS
#sudo apt install python-gdal

# get the tool
test ! -f gdal2tiles.py \
  && curl https://raw.githubusercontent.com/commenthol/gdal2tiles-leaflet/master/gdal2tiles.py \
  > gdal2tiles.py
# process ...
python ./gdal2tiles.py -l -p raster -z 0-5 -w none map.png tiles

echo 'Now open "index.html" in your browser.'
