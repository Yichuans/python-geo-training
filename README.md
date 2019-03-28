## Python, GIS and Jupyter notebook training

An introduction of Python, GIS (ArcGIS) and Jupyter notebook. This is a follow up training.

AA, CR and YS

## Prerequisite

Have attended Spencer's [Introduction to Python for Data Science](https://github.com/spencerldixon/intro-to-data-science) or experience in using Python and Jupyter notebook. 

Have used GIS, in particular ArcGIS, but not essential.

## Who is it for

- Power GIS users who want to explore inner workings of geoprocessing, and explore the power of the web
- GIS users who want to have repeative work done by computers
- Analysts who want to analyse data, including spatial data, in a modern environment that is shareable, publishable, and reproducible.

## Setup

You need to have ArcGIS Pro (>2.2) installed on a windows machine. 

First, envoke `Python Command Prompt` from your ArcGIS Pro conda. It should be in your `ArcGIS` Folder in the Windows shortcut. You can confirm it is the ArcGIS Pro conda by the command `conda list` and check whether `arcgis` and `arcgispro` packages are in the output.

**Optional but highly recommended**

<hr>

Since the default conda environment `arcgispro-py3` is read-only, in order to keep things separate and ensure we can install additional packages and update them (or not to accidentally mess up the default environment!), we need to create a clone of the same environment by 

```bash
conda create --name {your-env-name} --clone arcgispro-py3
```

`{your-env-name}` is a name you give to the newly created environment. To test if this completed successfuly, you can run `conda env list` and check if `{your-env-name}` is in the output.

Because this environment is a clone to the original environment shipped with ArcGIS Pro and thus it also has access to `arcpy`, and no additional setting required.

<hr>

Change your working directory to this repository and start the jupyter notebook. 

```bash
jupyter notebook
```

You need to copy the token from the command window to the browser the first time you run the notebook.

## Index
- [Refresher: pandas](./Refresher-pandas.ipynb)
- [WDPA change statistics](./WDPA-update-change.ipynb)
- [extra: ArcGIS Online ??]()
- [extra: ??]()

## Tips

- Within ArcGIS Pro's python environment, you can interact with `arcpy` directly
- run scripts directly using the builtin magic function `%run`
- run shell command with `!{command}` in the notebook

## Add-ons

**Dashboard**

To enable [Jupyter Dashboards](https://jupyter-dashboards-layout.readthedocs.io/en/latest/getting-started.html)

```bash
conda install jupyter_dashboards -c conda-forge
```

**Leaflet**

For interactive maps using [`ipyleaflet`](https://ipyleaflet.readthedocs.io/en/latest/)

```bash
conda install -c conda-forge ipyleaflet
```