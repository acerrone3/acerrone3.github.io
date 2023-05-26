## G-STOFS for Tropical Cyclones
NOAA runs the Global Surge and Tide Operational Forecast System (G-STOFS) four times per day.  At Notre Dame, the Computational Hydraulics Group (CHL) runs a shadow of G-STOFS once per day.  This shadow product has both experimental and forthcoming features.  The public can easily access its forecasts [here](https://dylnwood.github.io/GESTOFS-develop/).  

The CHL has been investigating ways to make G-STOFS more responsive to tropical cyclones.  In particular, we are focused on assimilating the skillful forecasts of the National Hurricane Center (NHC) and the Joint Typhoon Warning Center (JTWC) with dynamical forecast products like the Global Forecast System (GFS) which we use to force the underlying hydrodynamics driver in G-STOFS, ADCIRC.

Our assimilation strategy involves sourcing recent advisory data from NHC and/or JTWC and, in space and time, bootstrapping this to the recent GFS forecast.  In general, we find that GFS winds tend to be a bit muted compared to wind speeds forecasted by NHC and JTWC.  Consequently, we apply an amplification factor that draws GFS (in the vicinity of a tropical cyclone) in closer correspondence to the advisory wind speeds.  These enriched GFS winds then force ADCIRC within our shadow G-STOFS.  

We publish these amplification factors on this website.  Additionally, we publish the advisories that we source from NHC and JTWC.

Under no circumstances should this website be used for tropical cyclone preparedness or management.  It should not be used for navigational purposes.  Data sourced from NHC and JTWC was processed on our servers, and consequently, there is no guarantee that they are a true representation of the advisories from NHC and JTWC.  For example, JTWC radii were calculated from shapes embeddded in a KMZ file, and this methodology might be prone to error.  Please consult NHC and JTWC directly.

### Site URL
[https://acerrone3.github.io/](https://acerrone3.github.io/)

### Advisories
Access our GFS, NHC, and JTWC maximum winds from advisories [here](Historical_Data).
