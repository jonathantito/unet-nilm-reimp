# Reimplementing UNet-NILM

## For forked code
1) Download the dataset BLOND executing the python script `download_blond.py` in the folder `data/` without any arguments. (22 GB of data are downloaded aprox.).

**Note**: it is possible that you must execute the python script more than one time to download all the data.

2) Download UKDALE dataset in csv format using `wget http://data.ukedc.rl.ac.uk/simplebrowse/edc/efficiency/residential/EnergyConsumption/Domestic/UK-DALE-2017/UK-DALE-FULL-disaggregated/ukdale.zip` (3.5 GB of data are downloaded aprox.)

3) Execute the python script `preprocess_BLOND.py` in the folder `src/features/` without any arguments.

4) Execute the python script `preprocess_UKDALE.py` in the folder `src/features/` without any arguments.

TODO: replace code tweaks to make it work renaming the file
`/workspaces/torch-nilm/unet-nilm/unet-nilm-reimp/data/BLOND/preprocessed/BLOND-50/quantile_MacBookPro15''Mid-2014.npz` to `/workspaces/torch-nilm/unet-nilm/unet-nilm-reimp/data/BLOND/preprocessed/BLOND-50/quantile_MacBookPro15Mid-2014.npz`
5) Execute the python script `main.py`without any arguments.

6) Execute `tensorboard --logdir /workspaces/torch-nilm/logs` to see the results.

*Note*: the code was runned in a docker container with torch-nilm enviroment modified to run the code.

## Original text
Reference implementation for the following power and state estimation algorithm:  
UNet-NILM: A Deep Neural Network for Multi-tasks Appliances State Detection and Power Estimation in NILM
By author: Faustine et al.

Link to paper: https://dl.acm.org/doi/abs/10.1145/3427771.3427859  
Link to GitHub: https://github.com/sambaiga/UNETNiLM