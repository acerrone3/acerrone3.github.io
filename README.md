## GESTOFS-ML
This is a sister project of [GESTOFS](https://gm-ling.github.io/GESTOFS-develop/).  GESTOFS is an ADCIRC-based storm surge forecasting system for the whole globe.  GESTOFS-ML expands on this theme, but in addition to ADCIRC, it leverages a time-series forecasting ML model complete with meteorological forcing to enrich the prediction of surface water elevation.

### Site URL
[https://acerrone3.github.io/](https://acerrone3.github.io/)

### Interactive Map
The interactive map below reflects the latest forecasts rendered both by ADCIRC and the ML model.  Note that the ML forecasts were generated with the same meteorological forcing as ADCIRC.  The ML model was trained on approximately 9 months of ADCIRC nowcasts spanning 2021 and 2022.  ADCIRC and the ML model have yet to be coupled.  As the program matures, ADCIRC and the ML model will be run together to render bounded forecasts.
 
<iframe src="https://www.google.com/maps/d/embed?mid=1LqhHHF30oVMNegtRUMX-gtatV9EmigM&ehbc=2E312F" width="1000" height="800"></iframe>

### Performance
Updated July 14, 2022



### Past Forecasts
Past forecasts are posted [here](https://github.com/acerrone3/acerrone3.github.io/tree/main/Past%20Records).  Two file types are provided per forecast: comma separated value (csv) and Python-Pandas pickle (p).  To use the pickle file, simply invoke:

```
import pandas as pd

# read file into a Pandas dataframe
df = pd.read_pickle("filename.p")
```
