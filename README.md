
# Fork of the Automated Water Supply Model (AWSM)

This is a fork of the [USDA-ARS-NWRC AWSM](https://github.com/USDA-ARS-NWRC/awsm) repo
to continue the development of the framework.

# Usage
The installation of this package provides a command line interface to run the model.
The command is called `awsm`.

## Examples
### Run the first day
```bash
awsm -c awsm.ini -sd 2024-10-01 --no_previous
```

### Run a single day
```bash
awsm -c awsm.ini -sd 2024-10-01
```

### Run days set in the configuration file
```bash
awsm -c awsm.ini
```

### Re-run after a model crash
```bash
awsm -c awsm.ini -sd 2024-10-01 --threshold
```


## Help
```bash
usage: awsm [-h] -c CONFIG_FILE [-sd START_DATE] [-np] [-t] [-mt MEDIUM_THRESHOLD]

Run AWSM with given config file.

optional arguments:
  -h, --help            show this help message and exit
  -c CONFIG_FILE, --config_file CONFIG_FILE
                        Path to .ini config file.
  -sd START_DATE, --start_date START_DATE
                        Overwrite the start date in the .ini and force a single day run. Format: YYYYMMDD or YYYY-MM-DD
  -np, --no_previous    Skip finding a previous snow state and storm day file. Usually used when running the first day.
  -t, --threshold       Run iSnobal with different mass threshold
  -mt MEDIUM_THRESHOLD, --medium_threshold MEDIUM_THRESHOLD
                        Set the medium mass threshold. Default: 25
```
## History
First used in a publication in the 
[Geoscientific Model Development](https://gmd.copernicus.org/) journal.  
[![DOI](https://zenodo.org/badge/338433127.svg)](https://zenodo.org/badge/latestdoi/338433127)
