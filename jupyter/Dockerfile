FROM jupyter/datascience-notebook

RUN python --version

RUN conda install --quiet --yes -c \
    conda-forge osmnx dask

RUN pip install -U cufflinks \
		elasticsearch \
		fiona \
		folium \
		GeoAlchemy2 \
		geohash2 \
		geojson \
		geopandas \
		geopy \
		h5py \
		ipython \
		jupyter \
		keras \
		mapboxgl \
		matplotlib \
		mixpanel \
		numexpr==2.6.4 \
		numpy \
		pandas \
		pillow \
		plotly \
		pyproj \
		rtree \
		scikit-learn \
		scipy \
		seaborn \
		shapely \
		six \
		tables \
		tensorflow \
		tqdm

VOLUME /notebooks
WORKDIR /notebooks
