## GESTOFS-ML
This is a sister project of [GESTOFS](https://gm-ling.github.io/GESTOFS-develop/).  GESTOFS is an ADCIRC-based storm surge forecasting system for the whole globe.  GESTOFS-ML expands on this theme, but in addition to ADCIRC, it leverages a time-series forecasting ML model complete with meteorological forcing to enrich the prediction of surface water elevation.

### Site URL
[https://acerrone3.github.io/](https://acerrone3.github.io/)

### Latest Forecasts
Updated July 14, 2022

The interactive map below reflects the latest forecasts rendered both by ADCIRC and the ML model.  Note that the ML forecasts were generated with the same meteorological forcing as ADCIRC.  The ML model was trained on approximately 9 months of ADCIRC nowcasts spanning 2021 and 2022.  ADCIRC and the ML model have yet to be coupled.  As the program matures, ADCIRC and the ML model will be run together to render bounded forecasts.
 
<iframe src="https://www.google.com/maps/d/embed?mid=1LqhHHF30oVMNegtRUMX-gtatV9EmigM&ehbc=2E312F" width="1000" height="800"></iframe>

### Past Forecasts
Past forecasts are posted [here](https://github.com/acerrone3/acerrone3.github.io/tree/main/Past%20Records).  Two file types are provided per forecast: comma separated value (csv) and Python-Pandas pickle (p).  To use the pickle file, simply invoke:

```
import pandas as pd

# read file into a Pandas dataframe
df = pd.read_pickle("filename.p")
```

### Performance
Updated July 14, 2022

Here, the ADCIRC forecasts are compared to the ML forecasts.  Comparisons are arranged in descending order based on each station's r-squared value.  Observational data has yet to be integrated for performance assessment.

|  Station                                            |         R2 |       RMSD |   Max Discrepancy (m) |
| :---------------------------------------------------|-----------:|-----------:|----------------------:|
|  UH149 SOUS00 Lamu Kenya                            |  0.998594  | 0.0336052  |             0.114812  |
|  UH101 SOUS00 GL008 Mombasa Kenya                   |  0.998558  | 0.0359312  |             0.0789922 |
|  UH052 SOUS00 GL109 Johnston United States of Ameri |  0.998327  | 0.00888011 |             0.0242915 |
|  9452400 Skagway AK                                 |  0.997416  | 0.103436   |             0.376213  |
|  UH088 SOUS00 Caldera Chile                         |  0.997356  | 0.0212978  |             0.0538187 |
|  UH820 SOUS00 GL225 Nuuk Denmark                    |  0.997125  | 0.0664068  |             0.15724   |
|  UH046 SOUS00 GL348 Port Vila Vanuatu               |  0.997092  | 0.0185017  |             0.0414508 |
|  MIC77 SOUS43 0000077 Wake East Wake Island Populat |  0.99689   | 0.0163735  |             0.0388905 |
|  UH417 SOUS00 Sadeng Indonesia                      |  0.996801  | 0.0344086  |             0.0916862 |
|  9453220 Yakutat Bay AK                             |  0.996717  | 0.06375    |             0.169269  |
|  9452400 AK Skagway Taiya Inlet                     |  0.996691  | 0.11706    |             0.410059  |
|  9454240 AK Valdez                                  |  0.996638  | 0.0783506  |             0.15926   |
|  UH223 SOUS00 GL253 Dakar Senegal                   |  0.996627  | 0.0234628  |             0.0688651 |
|  MIC43 SOUS43 0000043 Kayangel North Palau Warning  |  0.996503  | 0.0289735  |             0.072073  |
|  9454050 AK Cordova                                 |  0.996428  | 0.080044   |             0.184594  |
|  UH023 SOUS00 GL139 Rarotonga Cook Islands (the)    |  0.996409  | 0.0143809  |             0.0341182 |
|  MIC07 SOUS43 0000007 Yap FSM UHSLC Gauge           |  0.996394  | 0.025415   |             0.0707408 |
|  UH294 SOUS00 GL241 Newlyn Cornwall United Kingdom  |  0.99638   | 0.0873929  |             0.206743  |
|  UH025 SOUS00 GL121 Funafuti Tuvalu                 |  0.996218  | 0.0307573  |             0.0713733 |
|  UH295 SOUS00 GL238 Stornoway United Kingdom of Gre |  0.996192  | 0.0787196  |             0.177578  |
|  UH163 SOUS00 GL049 Benoa Indonesia                 |  0.99617   | 0.0467764  |             0.102574  |
|  UH091 SOUS00 GL172 La Libertad Ecuador             |  0.996064  | 0.0474724  |             0.13833   |
|  MIC78 SOUS43 0000078 Wake West Wake Island Populat |  0.995919  | 0.0182159  |             0.0401147 |
|  WAKP8 SOUS43 1890000 Wake Island Pacific Ocean     |  0.995822  | 0.0187809  |             0.0475616 |
|  MIC52 SOUS43 0000052 Sonsorol Southwest Palau Warn |  0.995816  | 0.0340422  |             0.0871193 |
|  9451600 AK Sitka                                   |  0.995807  | 0.0709896  |             0.184173  |
|  9459450 AK Sand Point                              |  0.99577   | 0.0513487  |             0.116121  |
|  UH283 SOUS00 GL336 Fortaleza Brazil                |  0.995693  | 0.0534572  |             0.143621  |
|  MIC70 SOUS43 0000070 Utirik East (Airport) Marshal |  0.995496  | 0.0292275  |             0.0634257 |
|  9451600 Sitka AK                                   |  0.99538   | 0.074527   |             0.181358  |
|  MIC76 SOUS43 0000076 Mili East Marshall Islands Wa |  0.995349  | 0.0345729  |             0.0774922 |
|  UH125 SOUS00 Prigi Indonesia                       |  0.995269  | 0.045658   |             0.0998017 |
|  UH299 SOUS00 GL344 Qaqortoq Denmark                |  0.995262  | 0.0594885  |             0.171813  |
|  MIC21 SOUS43 0000021 Ngeremlengui West Palau Major |  0.995215  | 0.0360366  |             0.095249  |
|  MIC40 SOUS43 0000040 Majuro North Marshall Islands |  0.9952    | 0.0339762  |             0.0869068 |
|  UH181 SOUS00 GL013 Durban South Africa             |  0.995183  | 0.0394111  |             0.085163  |
|  MIC39 SOUS43 0000039 Majuro West Marshall Islands  |  0.995182  | 0.0341838  |             0.0784285 |
|  MIC53 SOUS43 0000053 Ngulu West Yap FSM Warning P  |  0.995131  | 0.0311965  |             0.0809731 |
|  MIC71 SOUS43 0000071 Wotje East (Airport) Marshall |  0.995059  | 0.0325399  |             0.0783109 |
|  9452210 AK Juneau                                  |  0.99503   | 0.137837   |             0.535211  |
|  MIC89 SOUS43 0000089 Arno East Marshall Islands Po |  0.995007  | 0.0346594  |             0.0753624 |
|  UH288 SOUS00 GL229 Reykjavik Iceland               |  0.994968  | 0.086134   |             0.235018  |
|  MIC51 SOUS43 0000051 Sonsorol Northwest Palau Warn |  0.994939  | 0.0378898  |             0.078918  |
|  9452634 AK Elfin Cove                              |  0.994901  | 0.0854367  |             0.202534  |
|  MIC47 SOUS43 0000047 Angaur West Palau Warning Poi |  0.99487   | 0.0366993  |             0.0992558 |
|  1656 USA - Kodiak Island, AK                       |  0.994792  | 0.0704673  |             0.238008  |
|  MIC44 SOUS43 0000044 Peleliu East Palau Warning Po |  0.994752  | 0.0373384  |             0.103958  |
|  MIC54 SOUS43 0000054 Ngulu East Yap FSM Warning P  |  0.994741  | 0.0317644  |             0.0802335 |
|  UH218 SOUS00 GL250 Funchal Portugal                |  0.994741  | 0.047991   |             0.114422  |
|  8665530 SC Charleston Cooper River E               |  0.994713  | 0.0391233  |             0.0904194 |
|  UH227 SOUS00 GL202 Cayenne France                  |  0.994685  | 0.0571957  |             0.16066   |
|  MIC86 SOUS43 0000086 Ebeye East Marshall Islands P |  0.994658  | 0.033694   |             0.0803523 |
|  9455090 AK Seward                                  |  0.99465   | 0.0864641  |             0.208232  |
|  UH816 SOUS00 GL350 Port Sonara Cameroon            |  0.994515  | 0.0308797  |             0.0850376 |
|  MIC57 SOUS43 0000057 Faraulep East Yap FSM Warnin  |  0.994447  | 0.0196029  |             0.0495853 |
|  9457804 AK Alitak                                  |  0.994388  | 0.0981014  |             0.221186  |
|  MIC06 SOUS43 0000006 Malakal Palau UHSLC Gauge     |  0.994378  | 0.0392862  |             0.0960888 |
|  UH081 SOUS00 GL175 Valparaiso Chile                |  0.99437   | 0.0332909  |             0.0902515 |
|  MIC45 SOUS43 0000045 Peleliu West Palau Warning Po |  0.994341  | 0.0386778  |             0.104495  |
|  9451054 AK Port Alexander                          |  0.994308  | 0.0937757  |             0.193211  |
|  MIC73 SOUS43 0000073 Kwajalein East (Airport) Mars |  0.994291  | 0.0348048  |             0.0778489 |
|  MIC49 SOUS43 0000049 Sonsorol Northeast Palau Warn |  0.994264  | 0.040222   |             0.1077    |
|  UH092 SOUS00 Talara Peru                           |  0.994261  | 0.04365    |             0.104891  |
|  MIC88 SOUS43 0000088 Ebon East Marshall Islands Po |  0.99426   | 0.0387551  |             0.0796837 |
|  MIC87 SOUS43 0000087 Ebeye Wes Marshall Islands Po |  0.994173  | 0.0349329  |             0.0887771 |
|  UH261 SOUS00 Charleston SC United States of Ameri  |  0.994172  | 0.0410321  |             0.0858506 |
|  MIC22 SOUS43 0000022 Yap East Yap FSM Major Islan  |  0.994131  | 0.0320539  |             0.0843335 |
|  UH362 SOUS00 GL083 Nagasaki Japan                  |  0.994117  | 0.0662616  |             0.193675  |
|  MIC48 SOUS43 0000048 Angaur South Palau Warning Po |  0.994116  | 0.038867   |             0.120274  |
|  MIC25 SOUS43 0000025 Yap North Yap FSM Major Isla  |  0.994092  | 0.0323581  |             0.087974  |
|  MIC72 SOUS43 0000072 Ujae East (Airport) Marshall  |  0.994058  | 0.0339245  |             0.073823  |
|  MIC08 SOUS43 0000008 Pohnpei FSM UHSLC Gauge       |  0.994031  | 0.0262847  |             0.055554  |
|  8443970 MA Boston                                  |  0.994023  | 0.0797375  |             0.205919  |
|  9455500 AK Seldovia                                |  0.994011  | 0.169259   |             0.542884  |
|  UH233 SOUS00 GL259 Lagos Nigeria                   |  0.993985  | 0.0335806  |             0.0945477 |
|  UH155 SOUS00 GL096 Dzaoudzi France                 |  0.993942  | 0.0782521  |             0.172672  |
|  UH002 SOUS00 GL113 Tarawa Bairiki Kiribati         |  0.993926  | 0.041943   |             0.0948063 |
|  MIC46 SOUS43 0000046 Angaur East Palau Warning Poi |  0.993851  | 0.0395139  |             0.104846  |
|  MIC74 SOUS43 0000074 Ailinglaplap East (Airport) M |  0.993822  | 0.0384687  |             0.0875126 |
|  MIC37 SOUS43 0000037 Majuro East Marshall Islands  |  0.993792  | 0.0390428  |             0.0806759 |
|  UH231 SOUS00 GL335 Takoradi Ghana                  |  0.993758  | 0.0325556  |             0.0703597 |
|  UH004 SOUS00 GL114 Nauru Nauru                     |  0.993757  | 0.0418257  |             0.11476   |
|  MIC58 SOUS43 0000058 Woleai East Yap FSM Warning   |  0.993733  | 0.0221683  |             0.0619282 |
|  UH209 SOUS00 GL246 Cascais Portugal                |  0.993698  | 0.0714757  |             0.164477  |
|  UH108 SOUS00 GL028 Male Maldives                   |  0.993688  | 0.0206138  |             0.051987  |
|  MIC38 SOUS43 0000038 Majuro South (Airport) Marsha |  0.993677  | 0.0396465  |             0.0872209 |
|  PAC17 SOUS43 0000017 OR Neskowin Beach             |  0.993615  | 0.0701563  |             0.195381  |
|  MIC56 SOUS43 0000056 Fais East(Airport) Yap FSM W  |  0.993597  | 0.0283868  |             0.0890656 |
|  UH113 SOUS00 Masirah Oman                          |  0.993568  | 0.0472557  |             0.114042  |
|  UH420 SOUS00 Saumlaki Indonesia                    |  0.993521  | 0.0575641  |             0.142861  |
|  MIC68 SOUS43 0000068 Pingelap East Pohnpei FSM Wa  |  0.993512  | 0.0324695  |             0.0741834 |
|  UH834 SOUS00 GL239 Malin Head Ireland              |  0.993472  | 0.0832495  |             0.186803  |
|  MIC20 SOUS43 0000020 East Melekeok Palau Major Isl |  0.99346   | 0.038825   |             0.105778  |
|  UH822 SOUS00 GL242 Brest France                    |  0.993431  | 0.148319   |             0.390242  |
|  UH291 SOUS00 GL263 Ascension United Kingdom of Gre |  0.993417  | 0.0251811  |             0.0671402 |
|  9432780 OR Charleston                              |  0.993393  | 0.0671626  |             0.225836  |
|  MIC50 SOUS43 0000050 Sonsorol Southeast Palau Warn |  0.993392  | 0.0425925  |             0.109852  |
|  KWJP8 SOUS43 1820000 Kwajalein Marshall Island     |  0.993376  | 0.0374902  |             0.0817194 |
|  1664 Norway - Ny Alesund                           |  0.993319  | 0.0352686  |             0.0941901 |
|  MIC32 SOUS43 0000032 Pohnpei West Pohnpei FSM Maj  |  0.993305  | 0.0270736  |             0.0580182 |
|  UH082 SOUS00 GL182 Acajutla El Salvador            |  0.993247  | 0.055263   |             0.138995  |
|  MIC80 SOUS43 0000080 Ifalik East Yap FSM Populate  |  0.99323   | 0.0219605  |             0.0614432 |
|  PAC16 SOUS43 0000016 OR Lincoln City               |  0.993203  | 0.0723133  |             0.17405   |
|  9414750 CA Alameda                                 |  0.993202  | 0.0609547  |             0.169786  |
|  UH123 SOUS00 GL347 Sabang Indonesia                |  0.993187  | 0.0358849  |             0.0829719 |
|  MIC79 SOUS43 0000079 Eurapik East Yap FSM Populat  |  0.993181  | 0.0249097  |             0.0673043 |
|  MIC55 SOUS43 0000055 Ulithi East (Airport) Yap FS  |  0.993124  | 0.0316301  |             0.0885283 |
|  MIC67 SOUS43 0000067 Mokil East Pohnpei FSM Warni  |  0.993106  | 0.0314695  |             0.069825  |
|  MIC18 SOUS43 0000018 Saipan West (Garapan) Saipan  |  0.993089  | 0.0186473  |             0.0418434 |
|  UH541 SOUS00 Bamfield Canada                       |  0.993078  | 0.0772161  |             0.216327  |
|  878 USA - Fort_Pulaski_GA                          |  0.993073  | 0.0583718  |             0.132552  |
|  MIC36 SOUS43 0000036 Kosrae East (Malem) Kosrae F  |  0.992993  | 0.0381169  |             0.0845397 |
|  8661070 SC Springmaid Pier                         |  0.992968  | 0.0430582  |             0.140001  |
|  UH084 SOUS00 Lobos de Afuera Peru                  |  0.992939  | 0.037317   |             0.0914403 |
|  MIC33 SOUS43 0000033 Kosrae North (Airport) Kosrae |  0.992935  | 0.037355   |             0.0829612 |
|  9419945 CA Pyramid Point Smith River               |  0.992886  | 0.0635628  |             0.211389  |
|  UH392 SOUS00 Cocos Island Costa Rica               |  0.992881  | 0.0742489  |             0.216752  |
|  MIC90 SOUS43 0000090 62 Km ENE from Helen Reef (-2 |  0.992818  | 0.0443743  |             0.125516  |
|  1715 USA - Cutler Farris Wharf, ME                 |  0.992696  | 0.124646   |             0.365053  |
|  MIC31 SOUS43 0000031 Pohnpei South Pohnpei FSM Ma  |  0.992687  | 0.0298985  |             0.0586376 |
|  MIC69 SOUS43 0000069 Enewetak East Marshall Island |  0.992641  | 0.0314964  |             0.0685944 |
|  UH830 SOUS00 GL243 La Coruna Spain                 |  0.992631  | 0.0915867  |             0.26364   |
|  MIC65 SOUS43 0000065 Sapwuafik (Ngatik) East Pohnp |  0.992608  | 0.0290339  |             0.0606687 |
|  MIC23 SOUS43 0000023 Yap South (Colonia) Yap FSM   |  0.992606  | 0.0361432  |             0.0847003 |
|  UH302 SOUS00 GL168 Balboa Panama                   |  0.992605  | 0.144811   |             0.348508  |
|  MIC34 SOUS43 0000034 Kosrae West (Walung) Kosrae   |  0.992579  | 0.038267   |             0.0880658 |
|  851 USA - Crescent_City_CA                         |  0.992559  | 0.0637284  |             0.191521  |
|  UH038 SOUS00 GL125 Nuku'alofa Tonga                |  0.992558  | 0.0376031  |             0.10559   |
|  1272 Norway - Andenes                              |  0.992518  | 0.0525872  |             0.125967  |
|  UH043 SOUS00 Palmyra Island United States of Ameri |  0.992493  | 0.0207083  |             0.0525635 |
|  9414575 CA Coyote Creek                            |  0.992489  | 0.0780336  |             0.228077  |
|  UH162 SOUS00 GL291 Cilicap Indonesia               |  0.99247   | 0.0464339  |             0.117409  |
|  MIC24 SOUS43 0000024 Yap West (Airport) Yap FSM M  |  0.992463  | 0.0379416  |             0.0950086 |
|  PAC18 SOUS43 0000018 OR Pacific City               |  0.992429  | 0.0764443  |             0.190323  |
|  8410140 ME Eastport                                |  0.992399  | 0.165632   |             0.403648  |
|  APRP7 SOUS43 1630000 Apra HarborGuam               |  0.99237   | 0.0226888  |             0.0497693 |
|  MIC30 SOUS43 0000030 Pohnpei East Pohnpei FSM Maj  |  0.992343  | 0.0311842  |             0.0684346 |
|  8720218 FL Mayport (Bar Pilots Dock)               |  0.992335  | 0.0465311  |             0.148685  |
|  MIC66 SOUS43 0000066 Pakin East Pohnpei FSM Warni  |  0.992321  | 0.028615   |             0.0633113 |
|  PAC14 SOUS43 0000014 OR Beaver Creek               |  0.992237  | 0.0766977  |             0.238058  |
|  9443090 WA Neah Bay                                |  0.992174  | 0.0785756  |             0.197392  |
|  PAC24 SOUS43 0000024 WA Long Beach                 |  0.992157  | 0.080494   |             0.19401   |
|  MIC63 SOUS43 0000063 Losap East Chuuk FSM Warning  |  0.992154  | 0.0214031  |             0.0538897 |
|  UH805 SOUS00 GL323 Vardo Norway                    |  0.992143  | 0.0809704  |             0.168945  |
|  UH118 SOUS00 Ko Miang Thailand                     |  0.992091  | 0.0588207  |             0.145384  |
|  UH104 SOUS00 GL026 Diego Garcia United Kingdom of  |  0.99209   | 0.0407104  |             0.104599  |
|  UH171 SOUS00 GL046 Cocos Australia                 |  0.992078  | 0.0268013  |             0.0517539 |
|  UH109 SOUS00 GL027 Gan Maldives                    |  0.992039  | 0.027537   |             0.0604087 |
|  8723214 FL Virginia Key                            |  0.992038  | 0.0207551  |             0.0590649 |
|  MIC29 SOUS43 0000029 Pohnpei North Pohnpei FSM Ma  |  0.992024  | 0.0304712  |             0.0622027 |
|  9439011 OR Hammond                                 |  0.992005  | 0.0831766  |             0.178632  |
|  9455760 AK Nikiski                                 |  0.99199   | 0.203753   |             0.56132   |
|  PAC22 SOUS43 0000022 OR Seaside                    |  0.991952  | 0.0811768  |             0.221258  |
|  PAC21 SOUS43 0000021 OR Cannon Beach               |  0.991943  | 0.0807464  |             0.225419  |
|  MIC12 SOUS43 0000012 Guam North (Ritidian) Guam M  |  0.991885  | 0.0217588  |             0.0432484 |
|  8721604 FL Trident Pier Port Canaver               |  0.991852  | 0.0328348  |             0.0759129 |
|  MIC35 SOUS43 0000035 Kosrae South (Utwa Ma) Kosrae |  0.99185   | 0.0407522  |             0.0968785 |
|  8418150 ME Portland                                |  0.991819  | 0.0921788  |             0.217638  |
|  UH803 SOUS00 GL234 Rorvik Norway                   |  0.991806  | 0.0626066  |             0.168718  |
|  UH093 SOUS00 GL173 Callao Peru                     |  0.991792  | 0.0282689  |             0.0637664 |
|  9459881 AK King Cove                               |  0.991707  | 0.0674544  |             0.16352   |
|  8423898 NH Fort Point                              |  0.991661  | 0.0897768  |             0.213195  |
|  UH908 SOUS00 GL038 Port Blair India                |  0.991644  | 0.0547453  |             0.141672  |
|  9414776 CA Oakland Berth 34                        |  0.991626  | 0.0645049  |             0.1807    |
|  MIC14 SOUS43 0000014 Rota West (Songsong) Rota Ma  |  0.991594  | 0.0215921  |             0.0445503 |
|  UH105 SOUS00 GL019 Rodrigues Mauritius             |  0.991541  | 0.0354162  |             0.0802789 |
|  MIC13 SOUS43 0000013 Rota East (Sinapalu) Rota Ma  |  0.991507  | 0.0196961  |             0.0403385 |
|  UH121 SOUS00 GL339 Pt. La Rue Seychelles           |  0.991488  | 0.0331807  |             0.0888103 |
|  UH345 SOUS00 Nakano Shima Japan                    |  0.991463  | 0.0550872  |             0.121297  |
|  UH133 SOUS00 GL068 Ambon Indonesia                 |  0.991345  | 0.0561933  |             0.140356  |
|  9414863 CA Richmond                                |  0.991341  | 0.0629564  |             0.160592  |
|  UH789 SOUS00 Prickley Bay Grenada                  |  0.991275  | 0.0174518  |             0.0421625 |
|  MIC11 SOUS43 0000011 Guam South (Cocos) Guam Mari  |  0.99124   | 0.0219536  |             0.0477039 |
|  UH029 SOUS00 GL117 Kapingamarangi Micronesia (Fede |  0.991167  | 0.0278088  |             0.0649649 |
|  9450460 AK Ketchikan                               |  0.990977  | 0.154722   |             0.35208   |
|  UH259 SOUS00 GL221 Bermuda United Kingdom of Great |  0.99095   | 0.0267285  |             0.0634323 |
|  MIC82 SOUS43 0000082 Oroluk East Pohnpei FSM Popu  |  0.990925  | 0.0272198  |             0.0476482 |
|  9415056 CA Point Pinole                            |  0.990882  | 0.0672957  |             0.17281   |
|  UH011 SOUS00 GL146 Christmas Kiribati              |  0.990751  | 0.0231347  |             0.0580021 |
|  9431647 OR Port Orford                             |  0.99061   | 0.0750739  |             0.210971  |
|  MIC64 SOUS43 0000064 Lukunor East Chuuk FSM Warni  |  0.990533  | 0.0259502  |             0.0723919 |
|  9414311 CA San Francisco Pier 1                    |  0.990494  | 0.068072   |             0.17902   |
|  9418767 CA North Spit                              |  0.990481  | 0.0700154  |             0.197755  |
|  MIC26 SOUS43 0000026 Chuuk Lagoon East Chuuk FSM   |  0.990295  | 0.0231859  |             0.0639469 |
|  UH030 SOUS00 Santa Cruz Ecuador                    |  0.990257  | 0.0606062  |             0.178636  |
|  UH806 SOUS00 Nouakchott Mauritania                 |  0.990033  | 0.0402834  |             0.10495   |
|  9411399 CA Gaviota State Park Pacifi               |  0.99001   | 0.0555352  |             0.149056  |
|  9414290 CA San Francisco                           |  0.989854  | 0.0656794  |             0.171683  |
|  UH094 SOUS00 Matarani Peru                         |  0.98977   | 0.0363073  |             0.081385  |
|  UH114 SOUS00 GL004 Salalah Oman                    |  0.989767  | 0.0405474  |             0.0881316 |
|  MIC19 SOUS43 0000019 Saipan North Saipan Marianas  |  0.989731  | 0.0209571  |             0.0391109 |
|  UH257 SOUS00 GL211 Settlement Point Bahamas (the)  |  0.9897    | 0.0296629  |             0.0744528 |
|  9415144 CA Port Chicago                            |  0.989681  | 0.0857032  |             0.192593  |
|  UH035 SOUS00 GL177 San Felix Chile                 |  0.98958   | 0.0310344  |             0.0739825 |
|  UH034 SOUS00 GL161 Cabo San Lucas Mexico           |  0.989394  | 0.0452605  |             0.108249  |
|  MIC27 SOUS43 0000027 Chuuk Lagoon North Chuuk FSM  |  0.989345  | 0.0232465  |             0.063717  |
|  UH153 SOUS00 GL029 Minicoy India                   |  0.989304  | 0.0294843  |             0.0732553 |
|  UH009 SOUS00 GL066 Honiara Solomon Islands         |  0.989049  | 0.0261693  |             0.0599359 |
|  8413320 ME Bar Harbor                              |  0.989024  | 0.120921   |             0.271929  |
|  UH207 SOUS00 GL249 Ceuta Spain                     |  0.988883  | 0.0298063  |             0.0936858 |
|  9410170 CA San Diego San Diego Bay                 |  0.988868  | 0.0622395  |             0.166447  |
|  UH540 SOUS00 GL155 Prince Rupert Canada            |  0.98885   | 0.183571   |             0.393445  |
|  UH031 SOUS00 GL142 Nuku Hiva France                |  0.988684  | 0.0461327  |             0.143372  |
|  9410666 CA Los Angeles Pier 400                    |  0.988667  | 0.0607183  |             0.153044  |
|  9416409 CA GREEN COVE PACIFIC OCEAN                |  0.988429  | 0.0654128  |             0.193569  |
|  UH271 SOUS00 Fort de France France                 |  0.988346  | 0.0131845  |             0.0310885 |
|  9414958 CA Bolinas Bolinas Lagoon                  |  0.988322  | 0.065038   |             0.168471  |
|  UH147 SOUS00 GL030 Karachi Pakistan                |  0.988123  | 0.0792331  |             0.161414  |
|  9410660 CA Los Angeles                             |  0.9881    | 0.0621826  |             0.157311  |
|  9415102 CA Martinez-Amorco Pier                    |  0.98799   | 0.0876457  |             0.194601  |
|  UH289 SOUS00 GL248 Gibraltar United Kingdom of Gre |  0.987948  | 0.0302641  |             0.0956323 |
|  UH117 SOUS00 Hanimaadhoo Maldives                  |  0.987931  | 0.0283154  |             0.0677692 |
|  8722670 FL Lake Worth Pier Atlantic                |  0.987852  | 0.032406   |             0.0809893 |
|  UH221 SOUS00 GL268 Simon's Town South Africa       |  0.987629  | 0.0523936  |             0.111315  |
|  UH013 SOUS00 GL145 Kanton Kiribati                 |  0.987597  | 0.0408847  |             0.11477   |
|  UH833 SOUS00 GL224 Nain Canada                     |  0.987517  | 0.074524   |             0.195906  |
|  UH142 SOUS00 Langkawi Malaysia                     |  0.987443  | 0.0946454  |             0.187824  |
|  NSTP6 SOUS43 1770000 Pago Pago American Samoa      |  0.987318  | 0.0353891  |             0.0927418 |
|  MIC62 SOUS43 0000062 Fananu East Chuuk FSM Warnin  |  0.98728   | 0.0257092  |             0.0699968 |
|  9410230 CA La Jolla                                |  0.987222  | 0.0629677  |             0.183409  |
|  9415020 CA Point Reyes                             |  0.987124  | 0.0678327  |             0.13776   |
|  UH402 SOUS00 Lautoka Fiji                          |  0.987031  | 0.062776   |             0.145339  |
|  MIC81 SOUS43 0000081 Lamotrek East Yap FSM Popula  |  0.986866  | 0.025945   |             0.0526634 |
|  9411406 CA Oil Platform Harvest                    |  0.986712  | 0.0627738  |             0.138991  |
|  UH017 SOUS00 Hiva Oa France                        |  0.986585  | 0.0515338  |             0.134525  |
|  UH419 SOUS00 Lembar Indonesia                      |  0.986559  | 0.057136   |             0.135894  |
|  9447130 WA Seattle Puget Sound                     |  0.986126  | 0.129366   |             0.300605  |
|  MIC10 SOUS43 0000010 Moen I Chuuk FSM Historic CO  |  0.986095  | 0.0268185  |             0.0689992 |
|  9415338 CA Sonoma Creek Entrance                   |  0.986083  | 0.0834683  |             0.188529  |
|  9447214 WA Shilshole Bay GPS Buoy                  |  0.98602   | 0.12608    |             0.215734  |
|  1497 Korea - Busan                                 |  0.985922  | 0.0547081  |             0.125646  |
|  UH115 SOUS00 GL033 Colombo Sri Lanka               |  0.985815  | 0.0244571  |             0.0467815 |
|  1336 Norway - Maloy                                |  0.985699  | 0.0600246  |             0.164448  |
|  UH403 SOUS00 Jackson New Zealand                   |  0.985615  | 0.0887047  |             0.22218   |
|  MIC28 SOUS43 0000028 Chuuk Lagoon West Chuuk FSM   |  0.985474  | 0.0260089  |             0.0637003 |
|  9410665 CA Los Angeles Pier J                      |  0.985467  | 0.0684987  |             0.156043  |
|  UH808 SOUS00 GL343 Thule (Pituffik) Denmark        |  0.985464  | 0.0830254  |             0.200097  |
|  UH275 SOUS00 GL222 Halifax Canada                  |  0.985438  | 0.060016   |             0.128192  |
|  UH913 SOUS00 Telukdalam Indonesia                  |  0.985314  | 0.032676   |             0.0713153 |
|  600 NM West-Northwest of Phuket Thailand           |  0.985099  | 0.0291794  |             0.0609662 |
|  UH333 SOUS00 GL057 Fort Denison Australia          |  0.984981  | 0.0544234  |             0.131751  |
|  UH777 SOUS00 Puerto Plata Dominican Republic (the) |  0.984766  | 0.0215536  |             0.0433447 |
|  UH601 SOUS00 GL185 Esperanza Argentina             |  0.984696  | 0.0960854  |             0.222755  |
|  8467150 CT Bridgeport                              |  0.98465   | 0.0919686  |             0.225846  |
|  UH157 SOUS00 GL035 Vishakhapatnam India            |  0.984563  | 0.0508962  |             0.125517  |
|  UH179 SOUS00 GL024 Saint Paul France               |  0.984487  | 0.0496793  |             0.108246  |
|  9759394 PR Mayaguez                                |  0.984326  | 0.0141789  |             0.0311865 |
|  8720030 FL Fernandina Beach                        |  0.984236  | 0.0733251  |             0.187691  |
|  UH049 SOUS00 GL104 Minamitorishima Japan           |  0.984077  | 0.0218886  |             0.0503503 |
|  UH354 SOUS00 GL082 Aburatsu Japan                  |  0.983951  | 0.0655257  |             0.177687  |
|  9439040 OR Astoria                                 |  0.983948  | 0.116506   |             0.262829  |
|  9455920 AK Anchorage                               |  0.983642  | 0.292621   |             0.806234  |
|  9446484 WA Tacoma                                  |  0.983585  | 0.145695   |             0.281401  |
|  UH021 SOUS00 GL176 Juan Fernandez Chile            |  0.983567  | 0.0454198  |             0.13388   |
|  1612340 HI Honolulu                                |  0.983466  | 0.0260318  |             0.0675215 |
|  9455920 Anchorage AK                               |  0.983344  | 0.29674    |             0.712831  |
|  UH684 SOUS00 GL178 Puerto Montt Chile              |  0.983156  | 0.306237   |             0.789347  |
|  UH317 SOUS00 Ensenada Mexico                       |  0.983094  | 0.0713692  |             0.199894  |
|  UH547 SOUS00 Barbers Point HI United States of Am  |  0.983052  | 0.025385   |             0.0671536 |
|  8658163 NC Wrightsville Beach                      |  0.982973  | 0.0554401  |             0.124623  |
|  9462450 AK Nikolski                                |  0.982779  | 0.0679248  |             0.129362  |
|  9444900 WA Port Townsend                           |  0.982654  | 0.111095   |             0.249718  |
|  9435380 OR South Beach                             |  0.982611  | 0.10979    |             0.216677  |
|  UH542 SOUS00 GL156 Tofino Canada                   |  0.982483  | 0.0998007  |             0.245791  |
|  8519483 NY Bergen Point West Reach                 |  0.982389  | 0.0735233  |             0.236159  |
|  1612480 HI Mokuoloe                                |  0.982349  | 0.0297977  |             0.0717443 |
|  UH041 SOUS00 GL102 Dutch Harbor AK United States   |  0.982329  | 0.0670492  |             0.183502  |
|  1611400 HI Nawiliwili                              |  0.982318  | 0.0265458  |             0.0800708 |
|  UH119 SOUS00 GL002 Djibouti Djibouti               |  0.981665  | 0.0713871  |             0.165612  |
|  902 Japan - Ishigakijima                           |  0.981308  | 0.0660253  |             0.139081  |
|  8531680 NJ Sandy Hook                              |  0.981285  | 0.0710269  |             0.182784  |
|  UH365 SOUS00 Ishigaki Japan                        |  0.981259  | 0.0668403  |             0.150539  |
|  UH107 SOUS00 GL045 Padang Indonesia                |  0.981011  | 0.0506162  |             0.128195  |
|  UH356 SOUS00 Maisaka Japan                         |  0.980833  | 0.062719   |             0.123957  |
|  MIC15 SOUS43 0000015 Tinian East Tinian Marianas   |  0.980593  | 0.0272671  |             0.0500186 |
|  UH103 SOUS00 GL018 Port Louis Mauritius            |  0.979501  | 0.0230709  |             0.0453809 |
|  8518750 NY The Battery                             |  0.979441  | 0.0750103  |             0.257274  |
|  UH382 SOUS00 Subic Bay Philippines (the)           |  0.979356  | 0.0559226  |             0.115543  |
|  1617433 HI Kawaihae                                |  0.979321  | 0.0317233  |             0.0856124 |
|  8536110 NJ Cape May                                |  0.978825  | 0.0789007  |             0.243152  |
|  UH019 SOUS00 GL123 Noumea France                   |  0.978477  | 0.0562986  |             0.14376   |
|  9465261 Nushagak Bay                               |  0.977602  | 0.26996    |             0.563902  |
|  8656483 NC Beaufort Duke Marine Lab                |  0.977526  | 0.0590632  |             0.124116  |
|  UH166 SOUS00 GL040 Broome Australia                |  0.977322  | 0.420086   |             1.15868   |
|  1586 New Zealand - Christchurch                    |  0.977159  | 0.111236   |             0.269824  |
|  9464212 St Paul Island AK                          |  0.976993  | 0.0630536  |             0.132161  |
|  MIC59 SOUS43 0000059 Satawal East Yap FSM Warning  |  0.976734  | 0.0335267  |             0.0698124 |
|  UH286 SOUS00 GL190 Puerto Deseado Argentina        |  0.976709  | 0.228458   |             0.794895  |
|  8724580 FL Key West                                |  0.976293  | 0.0281154  |             0.0779228 |
|  MIC61 SOUS43 0000061 Ulul East Chuuk FSM Warning   |  0.976217  | 0.0307965  |             0.0782807 |
|  UH164 SOUS00 GL017 Reunion France                  |  0.975965  | 0.021114   |             0.0422084 |
|  9461380 Adak Island AK                             |  0.975531  | 0.0716204  |             0.156436  |
|  9449880 WA Friday Harbor                           |  0.975453  | 0.119553   |             0.28793   |
|  8727520 FL Cedar Key                               |  0.975397  | 0.0709094  |             0.226034  |
|  UH016 SOUS00 GL138 Rikitea France                  |  0.975321  | 0.0363604  |             0.0845742 |
|  UH024 SOUS00 GL143 Penrhyn Cook Islands (the)      |  0.974291  | 0.0142596  |             0.0436932 |
|  UH799 SOUS00 GL209 Portu-Prince Haiti              |  0.974102  | 0.0224143  |             0.05695   |
|  UH351 SOUS00 GL087 Ofunato Japan                   |  0.974016  | 0.0647857  |             0.144718  |
|  UH383 SOUS00 Vung Tau Viet Nam                     |  0.973892  | 0.145442   |             0.305868  |
|  8725110 FL Naples Gulf of Mexico                   |  0.973793  | 0.0477635  |             0.105161  |
|  UH331 SOUS00 GL058 Brisbane Australia              |  0.973404  | 0.112603   |             0.273395  |
|  8726384 FL Port Manatee                            |  0.973389  | 0.0346663  |             0.091381  |
|  8461490 CT New London                              |  0.973305  | 0.0516601  |             0.150681  |
|  UH370 SOUS00 GL073 Manila Philippines (the)        |  0.973025  | 0.0700796  |             0.13511   |
|  9461380 AK Adak Island                             |  0.972841  | 0.0754584  |             0.164889  |
|  MIC60 SOUS43 0000060 Puluwat East Chuuk FSM Warni  |  0.972422  | 0.0339018  |             0.0734766 |
|  UH350 SOUS00 GL089 Kushiro Japan                   |  0.972322  | 0.0656547  |             0.150652  |
|  9440569 WA Skamokawa                               |  0.972179  | 0.113271   |             0.300335  |
|  UH184 SOUS00 GL076 Port Elizabeth South Africa     |  0.971597  | 0.0873352  |             0.204571  |
|  UH836 SOUS00 GL333 Alert Canada                    |  0.971597  | 0.0391565  |             0.0933343 |
|  UH273 SOUS00 Port-aux-basques Canada               |  0.971519  | 0.0670632  |             0.155434  |
|  UH047 SOUS00 GL103 Chichijima Japan                |  0.971011  | 0.0476069  |             0.0999152 |
|  UH353 SOUS00 GL085 Kushimoto Japan                 |  0.970845  | 0.081388   |             0.178095  |
|  9752619 PR Isabel Segunda Vieques Is               |  0.970805  | 0.0190002  |             0.0476818 |
|  9461710 AK Atka                                    |  0.970065  | 0.0771482  |             0.17887   |
|  UH015 SOUS00 GL140 Papeete France                  |  0.970051  | 0.0131177  |             0.0345433 |
|  UH654 SOUS00 Currimao Philippines (the)            |  0.969549  | 0.0481108  |             0.0923245 |
|  8537121 NJ Ship John Shoal                         |  0.969099  | 0.1085     |             0.331726  |
|  UH352 SOUS00 GL086 Mera Japan                      |  0.96888   | 0.0746277  |             0.166489  |
|  UH364 SOUS00 GL088 Hakodate Japan                  |  0.967688  | 0.0431139  |             0.110204  |
|  9751381 VI Lameshur Bay St John                    |  0.967188  | 0.0162509  |             0.0442462 |
|  UH347 SOUS00 GL327 Abashiri Japan                  |  0.966627  | 0.0660853  |             0.164899  |
|  8726607 FL Old Port Tampa                          |  0.96606   | 0.0413696  |             0.0916031 |
|  UH878 SOUS00 Bullen Bay Curacao                    |  0.965428  | 0.0196786  |             0.0461939 |
|  9759938 PR Mona Island                             |  0.965419  | 0.0172366  |             0.0392666 |
|  8760922 LA Pilots Station East S.W.                |  0.965216  | 0.0318183  |             0.0786779 |
|  9758053 PR Penuelas                                |  0.964454  | 0.0163316  |             0.0401211 |
|  UH316 SOUS00 GL267 Acapulco Gro. Mexico            |  0.964214  | 0.0348692  |             0.109715  |
|  9754228 PR Yabucoa Harbor                          |  0.962763  | 0.0169788  |             0.0445565 |
|  UH334 SOUS00 GL060 Townsville Australia            |  0.961796  | 0.143586   |             0.353657  |
|  8454049 RI Quonset Point                           |  0.961697  | 0.0747348  |             0.176612  |
|  9761115 Barbuda                                    |  0.961456  | 0.0168802  |             0.0409637 |
|  UH276 SOUS00 GL223 St. John's Canada               |  0.960253  | 0.0865131  |             0.225832  |
|  UH130 SOUS00 GL278 Casey Australia                 |  0.959679  | 0.0969788  |             0.189247  |
|  1619910 HI Sand Island Midway Island               |  0.959443  | 0.022878   |             0.0565132 |
|  UH071 SOUS00 GL101 Wellington New Zealand          |  0.958925  | 0.0849717  |             0.217234  |
|  UH699 SOUS00 GL044 Tanjong Pagar Singapore         |  0.958396  | 0.113426   |             0.28396   |
|  UH600 SOUS00 GL181 Ushuaia Argentina               |  0.958373  | 0.123086   |             0.2652    |
|  UH189 SOUS00 GL131 Dumont d'Urville Antarctica     |  0.956062  | 0.101008   |             0.237791  |
|  9752695 PR Esperanza Vieques Island                |  0.955621  | 0.0185999  |             0.0543204 |
|  UH738 SOUS00 Santa Marta Colombia                  |  0.955516  | 0.0217765  |             0.0470145 |
|  9759110 PR Magueyes Island                         |  0.955091  | 0.0180449  |             0.0497048 |
|  8449130 MA Nantucket Island                        |  0.955088  | 0.0793921  |             0.178269  |
|  UH122 SOUS00 Sibolga Indonesia                     |  0.954638  | 0.0658993  |             0.176393  |
|  UH340 SOUS00 Kaohsiung China                       |  0.953827  | 0.068269   |             0.145457  |
|  8570283 MD Ocean City Inlet                        |  0.953317  | 0.0699138  |             0.196165  |
|  UH268 SOUS00 Limon Costa Rica                      |  0.952592  | 0.0231875  |             0.0530055 |
|  8651370 NC Duck                                    |  0.951706  | 0.077006   |             0.169322  |
|  8452944 RI Conimicut Light                         |  0.950222  | 0.0910487  |             0.20574   |
|  UH920 SOUS00 GL020 Marion Island South Africa      |  0.948681  | 0.0564856  |             0.124561  |
|  8454000 RI Providence                              |  0.94866   | 0.0954073  |             0.245318  |
|  8540433 PA Marcus Hook                             |  0.947819  | 0.135107   |             0.369605  |
|  UH079 SOUS00 GL128 Chatham New Zealand             |  0.9477    | 0.0658318  |             0.142202  |
|  8538886 NJ Tacony-Palmyra Bridge                   |  0.946988  | 0.137937   |             0.410948  |
|  UH266 SOUS00 GL208 Cristobal Panama                |  0.946203  | 0.0242135  |             0.0551225 |
|  UH335 SOUS00 GL056 Spring Bay Australia            |  0.945763  | 0.0799568  |             0.188811  |
|  8510560 NY Montauk                                 |  0.945543  | 0.0540849  |             0.123856  |
|  8551762 DE Delaware City                           |  0.945317  | 0.140244   |             0.45899   |
|  UH220 SOUS00 GL314 Walvis Bay Namibia              |  0.944552  | 0.100781   |             0.240494  |
|  UH290 SOUS00 GL305 Port Stanley United Kingdom of  |  0.943304  | 0.105535   |             0.203517  |
|  UH737 SOUS00 San Andres Colombia                   |  0.942157  | 0.0235199  |             0.0499787 |
|  8539094 NJ Burlington Delaware River               |  0.941048  | 0.15817    |             0.443669  |
|  UH829 SOUS00 GL340 Trieste Italy                   |  0.940985  | 0.0829476  |             0.206183  |
|  UH173 SOUS00 GL277 Davis Australia                 |  0.940846  | 0.107548   |             0.26754   |
|  8639348 VA Money Point                             |  0.940317  | 0.0714255  |             0.182266  |
|  9465601 Carter Bay Kuskokwim Bay AK                |  0.940187  | 0.267351   |             0.729059  |
|  8545240 PA Philadelphia                            |  0.939852  | 0.142095   |             0.421091  |
|  8726667 FL Mckay Bay Entrance                      |  0.93985   | 0.0584642  |             0.162436  |
|  8551910 DE Reedy Point                             |  0.939825  | 0.145457   |             0.545058  |
|  8548989 PA Newbold                                 |  0.93777   | 0.174377   |             0.455119  |
|  UH180 SOUS00 GL023 Kerguelen France                |  0.936208  | 0.122585   |             0.257663  |
|  8723970 FL Vaca Key Florida Bay                    |  0.935801  | 0.0333369  |             0.0720245 |
|  8729108 FL Panama City                             |  0.935211  | 0.0466431  |             0.10733   |
|  8658120 NC Wilmington                              |  0.934971  | 0.111774   |             0.344702  |
|  8770822 TX Texas Point Sabine Pass                 |  0.934314  | 0.0637131  |             0.150842  |
|  8779748 TX South Padre Island CG Stat              |  0.931423  | 0.043659   |             0.107145  |
|  8632200 VA Kiptopeke                               |  0.931284  | 0.0754817  |             0.167725  |
|  9465374 Snag Point Dillingham AK                   |  0.928969  | 0.473716   |             1.40793   |
|  8638863 VA Chesapeake Bay Bridge Tunn              |  0.928422  | 0.0784209  |             0.190257  |
|  8637689 VA Yorktown USCG Training Cen              |  0.925807  | 0.0704092  |             0.198896  |
|  UH700 SOUS00 GL188 Faraday Antarctica              |  0.925245  | 0.128165   |             0.264314  |
|  UH824 SOUS00 GL205 Marseille France                |  0.920759  | 0.0224319  |             0.0614764 |
|  8737048 AL Mobile State Docks                      |  0.919089  | 0.0571893  |             0.127553  |
|  8638610 VA Sewells Point                           |  0.916878  | 0.0783495  |             0.197352  |
|  8573927 MD Chesapeake City                         |  0.91673   | 0.0782098  |             0.204165  |
|  8735391 AL Dog River Bridge                        |  0.916595  | 0.0551629  |             0.128241  |
|  8770475 TX Port Arthur                             |  0.910688  | 0.0325717  |             0.0870389 |
|  8447930 MA Woods Hole                              |  0.90929   | 0.0539396  |             0.120489  |
|  8729210 FL Panama City Beach                       |  0.908855  | 0.0540708  |             0.140292  |
|  UH360 SOUS00 GL324 Wakkanai Japan                  |  0.903487  | 0.036557   |             0.095912  |
|  8662245 SC Oyster Landing (N Inlet Es              |  0.899133  | 0.0829361  |             0.196382  |
|  UH906 SOUS00 GL141 Moulmein Myanmar                |  0.895609  | 0.547022   |             1.75961   |
|  8775870 TX Bob Hall Pier Corpus Chri               |  0.894283  | 0.0651218  |             0.148217  |
|  8770777 TX Manchester                              |  0.885521  | 0.0531791  |             0.130607  |
|  8594900 DC Washington                              |  0.884056  | 0.0884641  |             0.247026  |
|  8760721 LA Pilottown                               |  0.883271  | 0.025111   |             0.0470284 |
|  UH280 SOUS00 GL195 Ilha Fiscal RJ Brazil           |  0.87744   | 0.102628   |             0.205325  |
|  UH129 SOUS00 GL055 Portland S.Aus. Australia       |  0.860414  | 0.107339   |             0.272259  |
|  8571892 MD Cambridge                               |  0.857415  | 0.0718628  |             0.185599  |
|  8771341 TX Galveston Bay Entrance No               |  0.85588   | 0.081562   |             0.134237  |
|  UH348 SOUS00 GL326 Hamada Japan                    |  0.854899  | 0.0485795  |             0.10354   |
|  8652587 NC Oregon Inlet Marina                     |  0.845475  | 0.0476597  |             0.148771  |
|  8771013 TX Eagle Point Galveston Bay               |  0.845119  | 0.0459206  |             0.134663  |
|  UH680 SOUS00 GL130 Macquarie Is. Australia         |  0.836893  | 0.139266   |             0.311729  |
|  UH177 SOUS00 GL022 Mawson Australia                |  0.828978  | 0.138544   |             0.311201  |
|  UH178 SOUS00 GL021 Crozet France                   |  0.827385  | 0.0668213  |             0.140412  |
|  UH825 SOUS00 GL284 Cuxhaven Germany                |  0.827338  | 0.389111   |             1.25622   |
|  UH175 SOUS00 GL053 Fremantle Australia             |  0.826916  | 0.0794244  |             0.168382  |
|  8747437 MS Bay Waveland Yacht Club                 |  0.81666   | 0.0743501  |             0.210056  |
|  8577330 MD Solomons Island                         |  0.813531  | 0.0577974  |             0.147584  |
|  8762075 LA Port Fourchon Belle Pass                |  0.804636  | 0.0712471  |             0.194017  |
|  8770520 TX Rainbow Bridge                          |  0.803568  | 0.0385449  |             0.091978  |
|  8635750 VA Lewisetta                               |  0.800086  | 0.0602736  |             0.176462  |
|  8636580 VA Windmill Point                          |  0.794825  | 0.0533125  |             0.142805  |
|  8571421 MD Bishops Head                            |  0.789916  | 0.0971144  |             0.225522  |
|  UH128 SOUS00 GL308 Thevenard Australia             |  0.761614  | 0.22339    |             0.581602  |
|  8574680 MD Baltimore Fort McHenry P                |  0.761482  | 0.0660774  |             0.147972  |
|  UH176 SOUS00 GL054 Esperance Australia             |  0.758781  | 0.113097   |             0.240179  |
|  1019 Australia - Thevenard_AU                      |  0.751592  | 0.228144   |             0.584566  |
|  8764044 LA Berwick Atchafalaya River               |  0.731995  | 0.0537352  |             0.148073  |
|  8573364 MD Tolchester Beach                        |  0.730455  | 0.0738388  |             0.192388  |
|  UH349 SOUS00 GL325 Toyama Japan                    |  0.69618   | 0.0504125  |             0.113166  |
|  9468132 St. Michael                                |  0.689889  | 0.280365   |             0.711797  |
|  9468333 Unalakleet AK                              |  0.678671  | 0.298398   |             0.653159  |
|  8774513 TX Copano Bay                              |  0.670785  | 0.0215445  |             0.0424356 |
|  8764227 LA LAWMA Amerada Pass                      |  0.670774  | 0.080776   |             0.170229  |
|  9491094 Red Dog Dock AK                            |  0.663243  | 0.0985221  |             0.213776  |
|  8654467 NC USCG Station Hatteras                   |  0.642646  | 0.0337239  |             0.0799325 |
|  UH818 SOUS00 Smogen Sweden                         |  0.639293  | 0.0763381  |             0.203479  |
|  8774770 TX Rockport                                |  0.636424  | 0.0177348  |             0.0379191 |
|  UH579 SOUS00 GL151 Prudhoe Bay AK United States o  |  0.625867  | 0.0593127  |             0.12075   |
|  9468756 Nome AK                                    |  0.613851  | 0.119614   |             0.253615  |
|  8761305 LA Shell Beach                             |  0.591209  | 0.0908879  |             0.22779   |
|  9497645 Prudhoe Bay AK                             |  0.580718  | 0.0627131  |             0.16315   |
|  UH729 SOUS00 GL192 Mar del Plata Argentina         |  0.555792  | 0.302959   |             0.864772  |
|  UH804 SOUS00 GL321 Tregde Norway                   |  0.548929  | 0.0684844  |             0.171215  |
|  952 USA - Nome_AK                                  |  0.544751  | 0.130178   |             0.289021  |
|  UH731 SOUS00 GL191 Puerto Madryn Argentina         |  0.479878  | 3.00464    |            17.5486    |
|  UH819 SOUS00 GL233 Goteborgorsh. Sweden            |  0.375497  | 0.0851471  |             0.218797  |
|  8775283 TX Port Inglesid                           |  0.353092  | 0.041388   |             0.091934  |
|  8761927 LA New Canal Station                       | -0.0297535 | 0.0522582  |             0.149097  |
|  UH826 SOUS00 GL341 Stockholm Sweden                | -0.0372145 | 0.0551371  |             0.14199   |

### Disclaimer
This program is under experimental development. The results should not be used for navigational purposes or emergency planning under any circumstances. Please do not duplicate and use the result figures from this website without permission.
