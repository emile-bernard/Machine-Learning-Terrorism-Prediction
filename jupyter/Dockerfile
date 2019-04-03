FROM jupyter/datascience-notebook

RUN python --version

RUN conda install --quiet --yes -c \
    conda-forge osmnx dask

RUN pip install -U geopandas \
                   geopy \
                   rtree \
                   folium \
                   shapely \
                   fiona \
                   six \
                   pyproj \
                   numexpr==2.6.4 \
                   elasticsearch \
                   geojson \
                   plotly \
                   tqdm \
                   mapboxgl \
                   cufflinks \
                   geohash2 \
                   tables \
                   mixpanel \
                   GeoAlchemy2 \
		   opencv-python \
		   cv2 \
		   numpy \
		   scipy \
		   matplotlib \
		   ipython \
		   jupyter \
		   sys \
		   pandas

VOLUME /notebooks
WORKDIR /notebooks
