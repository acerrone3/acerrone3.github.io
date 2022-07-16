## GESTOFS-ML
This is a sister project of [GESTOFS](https://gm-ling.github.io/GESTOFS-develop/).  GESTOFS is an ADCIRC-based storm surge forecasting system for the whole globe.  GESTOFS-ML expands on this theme, but in addition to ADCIRC, it leverages a time-series forecasting ML model complete with meteorological forcing to enrich the prediction of surface water elevation.

### Site URL
[https://acerrone3.github.io/](https://acerrone3.github.io/)

### Latest Forecasts
Updated July 16, 2022

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
Updated July 16, 2022

Here, the ADCIRC forecasts are compared to the ML forecasts.  Comparisons are arranged in descending order based on each station's r-squared value.  Observational data has yet to be integrated for performance assessment.

|  Station                                            |         R2 |      RMSD |   Max Discrepancy (m) |
| :---------------------------------------------------|-----------:|----------:|----------------------:|
|  MIC12 SOUS43 0000012 Guam North (Ritidian) Guam M  |  0.995321  | 0.013099  |             0.033562  |
|  MIC22 SOUS43 0000022 Yap East Yap FSM Major Islan  |  0.994265  | 0.0264086 |             0.0601313 |
|  MIC07 SOUS43 0000007 Yap FSM UHSLC Gauge           |  0.994173  | 0.0269358 |             0.0599837 |
|  8661070 SC Springmaid Pier                         |  0.993425  | 0.0361438 |             0.104284  |
|  MIC13 SOUS43 0000013 Rota East (Sinapalu) Rota Ma  |  0.993222  | 0.0136109 |             0.0340907 |
|  MIC06 SOUS43 0000006 Malakal Palau UHSLC Gauge     |  0.992927  | 0.0369908 |             0.0875057 |
|  MIC14 SOUS43 0000014 Rota West (Songsong) Rota Ma  |  0.992898  | 0.0155989 |             0.0472431 |
|  APRP7 SOUS43 1630000 Apra HarborGuam               |  0.992775  | 0.0176326 |             0.0446103 |
|  MIC19 SOUS43 0000019 Saipan North Saipan Marianas  |  0.992374  | 0.0138584 |             0.0410884 |
|  UH081 SOUS00 GL175 Valparaiso Chile                |  0.99236   | 0.0325379 |             0.0810958 |
|  MIC53 SOUS43 0000053 Ngulu West Yap FSM Warning P  |  0.992217  | 0.0330101 |             0.0697477 |
|  MIC48 SOUS43 0000048 Angaur South Palau Warning Po |  0.992205  | 0.0376169 |             0.089011  |
|  MIC18 SOUS43 0000018 Saipan West (Garapan) Saipan  |  0.992129  | 0.0154938 |             0.0421223 |
|  MIC24 SOUS43 0000024 Yap West (Airport) Yap FSM M  |  0.992018  | 0.0325716 |             0.0725239 |
|  MIC44 SOUS43 0000044 Peleliu East Palau Warning Po |  0.99194   | 0.0389074 |             0.0964292 |
|  MIC46 SOUS43 0000046 Angaur East Palau Warning Poi |  0.991718  | 0.0385796 |             0.0904972 |
|  MIC25 SOUS43 0000025 Yap North Yap FSM Major Isla  |  0.99162   | 0.0321261 |             0.073288  |
|  MIC54 SOUS43 0000054 Ngulu East Yap FSM Warning P  |  0.991414  | 0.033954  |             0.073494  |
|  UH030 SOUS00 Santa Cruz Ecuador                    |  0.991379  | 0.0502522 |             0.124101  |
|  MIC43 SOUS43 0000043 Kayangel North Palau Warning  |  0.991326  | 0.0383445 |             0.0797271 |
|  MIC21 SOUS43 0000021 Ngeremlengui West Palau Major |  0.991295  | 0.0408662 |             0.0939112 |
|  MIC47 SOUS43 0000047 Angaur West Palau Warning Poi |  0.991224  | 0.0403544 |             0.093915  |
|  9455760 AK Nikiski                                 |  0.991094  | 0.186618  |             0.642499  |
|  MIC11 SOUS43 0000011 Guam South (Cocos) Guam Mari  |  0.991022  | 0.0174422 |             0.039633  |
|  MIC56 SOUS43 0000056 Fais East(Airport) Yap FSM W  |  0.99102   | 0.0278043 |             0.0585084 |
|  MIC55 SOUS43 0000055 Ulithi East (Airport) Yap FS  |  0.990627  | 0.0306649 |             0.064982  |
|  MIC15 SOUS43 0000015 Tinian East Tinian Marianas   |  0.990466  | 0.0143395 |             0.0349983 |
|  UH354 SOUS00 GL082 Aburatsu Japan                  |  0.990464  | 0.0400083 |             0.101489  |
|  MIC23 SOUS43 0000023 Yap South (Colonia) Yap FSM   |  0.99044   | 0.0342559 |             0.0804778 |
|  9452634 AK Elfin Cove                              |  0.990179  | 0.101264  |             0.223972  |
|  MIC20 SOUS43 0000020 East Melekeok Palau Major Isl |  0.990131  | 0.040032  |             0.0906935 |
|  MIC79 SOUS43 0000079 Eurapik East Yap FSM Populat  |  0.990053  | 0.0248341 |             0.0657643 |
|  MIC45 SOUS43 0000045 Peleliu West Palau Warning Po |  0.989913  | 0.0434158 |             0.0992778 |
|  MIC57 SOUS43 0000057 Faraulep East Yap FSM Warnin  |  0.989869  | 0.0214344 |             0.0539703 |
|  MIC52 SOUS43 0000052 Sonsorol Southwest Palau Warn |  0.989395  | 0.0457499 |             0.100079  |
|  UH025 SOUS00 GL121 Funafuti Tuvalu                 |  0.989224  | 0.0410836 |             0.109997  |
|  MIC90 SOUS43 0000090 62 Km ENE from Helen Reef (-2 |  0.989138  | 0.0460974 |             0.10981   |
|  MIC51 SOUS43 0000051 Sonsorol Northwest Palau Warn |  0.989086  | 0.0469343 |             0.110069  |
|  9451054 AK Port Alexander                          |  0.989073  | 0.111182  |             0.244915  |
|  UH092 SOUS00 Talara Peru                           |  0.988752  | 0.0535291 |             0.110312  |
|  MIC49 SOUS43 0000049 Sonsorol Northeast Palau Warn |  0.988613  | 0.0478074 |             0.106088  |
|  UH345 SOUS00 Nakano Shima Japan                    |  0.988154  | 0.0524457 |             0.117831  |
|  MIC50 SOUS43 0000050 Sonsorol Southeast Palau Warn |  0.987966  | 0.0485375 |             0.105726  |
|  UH403 SOUS00 Jackson New Zealand                   |  0.987795  | 0.0719816 |             0.155573  |
|  1497 Korea - Busan                                 |  0.987768  | 0.042328  |             0.0929805 |
|  9451600 Sitka AK                                   |  0.987716  | 0.103042  |             0.234573  |
|  9454050 AK Cordova                                 |  0.987615  | 0.127253  |             0.332161  |
|  UH017 SOUS00 Hiva Oa France                        |  0.987573  | 0.043959  |             0.0840752 |
|  UH684 SOUS00 GL178 Puerto Montt Chile              |  0.98755   | 0.22979   |             0.508803  |
|  UH118 SOUS00 Ko Miang Thailand                     |  0.987393  | 0.0616257 |             0.118119  |
|  9451600 AK Sitka                                   |  0.987383  | 0.104425  |             0.23883   |
|  8413320 ME Bar Harbor                              |  0.987356  | 0.119643  |             0.242303  |
|  UH123 SOUS00 GL347 Sabang Indonesia                |  0.98721   | 0.0405149 |             0.0836727 |
|  9454240 AK Valdez                                  |  0.987017  | 0.131277  |             0.361246  |
|  9452210 AK Juneau                                  |  0.987003  | 0.192857  |             0.413663  |
|  MIC58 SOUS43 0000058 Woleai East Yap FSM Warning   |  0.987     | 0.0261075 |             0.0663413 |
|  UH540 SOUS00 GL155 Prince Rupert Canada            |  0.986865  | 0.171365  |             0.39955   |
|  UH402 SOUS00 Lautoka Fiji                          |  0.986732  | 0.0539951 |             0.110554  |
|  9453220 Yakutat Bay AK                             |  0.98652   | 0.109532  |             0.24217   |
|  PAC22 SOUS43 0000022 OR Seaside                    |  0.98651   | 0.0883629 |             0.192899  |
|  UH013 SOUS00 GL145 Kanton Kiribati                 |  0.986373  | 0.0338912 |             0.0723554 |
|  9452400 Skagway AK                                 |  0.986208  | 0.206878  |             0.381425  |
|  UH088 SOUS00 Caldera Chile                         |  0.986111  | 0.0415137 |             0.0827192 |
|  9452400 AK Skagway Taiya Inlet                     |  0.986082  | 0.20782   |             0.431472  |
|  UH031 SOUS00 GL142 Nuku Hiva France                |  0.985957  | 0.0454178 |             0.0858484 |
|  UH218 SOUS00 GL250 Funchal Portugal                |  0.98578   | 0.0651836 |             0.13564   |
|  8443970 MA Boston                                  |  0.985766  | 0.113189  |             0.249679  |
|  NSTP6 SOUS43 1770000 Pago Pago American Samoa      |  0.98574   | 0.0325771 |             0.0790002 |
|  UH356 SOUS00 Maisaka Japan                         |  0.985538  | 0.042612  |             0.103437  |
|  UH233 SOUS00 GL259 Lagos Nigeria                   |  0.98543   | 0.0446399 |             0.0961442 |
|  UH002 SOUS00 GL113 Tarawa Bairiki Kiribati         |  0.985216  | 0.0516831 |             0.10423   |
|  UH091 SOUS00 GL172 La Libertad Ecuador             |  0.984959  | 0.0825602 |             0.178729  |
|  9455500 AK Seldovia                                |  0.984945  | 0.229406  |             0.579537  |
|  MIC40 SOUS43 0000040 Majuro North Marshall Islands |  0.984869  | 0.0481715 |             0.0961957 |
|  1715 USA - Cutler Farris Wharf, ME                 |  0.98472   | 0.167216  |             0.36445   |
|  UH223 SOUS00 GL253 Dakar Senegal                   |  0.984693  | 0.0426436 |             0.0975689 |
|  MIC76 SOUS43 0000076 Mili East Marshall Islands Wa |  0.98468   | 0.0501288 |             0.0981704 |
|  9415338 CA Sonoma Creek Entrance                   |  0.984655  | 0.0775981 |             0.181902  |
|  8410140 ME Eastport                                |  0.984655  | 0.219117  |             0.474606  |
|  MIC39 SOUS43 0000039 Majuro West Marshall Islands  |  0.98447   | 0.0489498 |             0.105208  |
|  MIC59 SOUS43 0000059 Satawal East Yap FSM Warning  |  0.984335  | 0.0214075 |             0.0494516 |
|  851 USA - Crescent_City_CA                         |  0.984284  | 0.0768277 |             0.191791  |
|  UH352 SOUS00 GL086 Mera Japan                      |  0.984255  | 0.0409306 |             0.093549  |
|  PAC24 SOUS43 0000024 WA Long Beach                 |  0.984221  | 0.0957134 |             0.217471  |
|  UH011 SOUS00 GL146 Christmas Kiribati              |  0.984074  | 0.0251984 |             0.0599087 |
|  9411399 CA Gaviota State Park Pacifi               |  0.984072  | 0.0548228 |             0.137003  |
|  8423898 NH Fort Point                              |  0.983965  | 0.115261  |             0.244978  |
|  UH157 SOUS00 GL035 Vishakhapatnam India            |  0.983962  | 0.0425748 |             0.0734591 |
|  UH034 SOUS00 GL161 Cabo San Lucas Mexico           |  0.983937  | 0.0416619 |             0.112826  |
|  MIC80 SOUS43 0000080 Ifalik East Yap FSM Populate  |  0.983815  | 0.0276215 |             0.070062  |
|  9410660 CA Los Angeles                             |  0.983656  | 0.0564325 |             0.164449  |
|  UH908 SOUS00 GL038 Port Blair India                |  0.983573  | 0.0638243 |             0.124491  |
|  MIC81 SOUS43 0000081 Lamotrek East Yap FSM Popula  |  0.983537  | 0.0227959 |             0.0570612 |
|  9450460 AK Ketchikan                               |  0.983531  | 0.180023  |             0.452444  |
|  PAC17 SOUS43 0000017 OR Neskowin Beach             |  0.983442  | 0.0945735 |             0.184059  |
|  UH021 SOUS00 GL176 Juan Fernandez Chile            |  0.983429  | 0.0384468 |             0.100105  |
|  8418150 ME Portland                                |  0.983344  | 0.121349  |             0.285595  |
|  UH038 SOUS00 GL125 Nuku'alofa Tonga                |  0.983285  | 0.0512522 |             0.105976  |
|  MIC37 SOUS43 0000037 Majuro East Marshall Islands  |  0.983236  | 0.0512487 |             0.103514  |
|  MIC89 SOUS43 0000089 Arno East Marshall Islands Po |  0.983219  | 0.0509648 |             0.102243  |
|  UH257 SOUS00 GL211 Settlement Point Bahamas (the)  |  0.983157  | 0.0328193 |             0.0619057 |
|  MIC38 SOUS43 0000038 Majuro South (Airport) Marsha |  0.9831    | 0.0516657 |             0.0994231 |
|  UH362 SOUS00 GL083 Nagasaki Japan                  |  0.983069  | 0.0916602 |             0.270159  |
|  PAC18 SOUS43 0000018 OR Pacific City               |  0.983009  | 0.095922  |             0.178217  |
|  9455090 AK Seward                                  |  0.982929  | 0.131152  |             0.28395   |
|  UH046 SOUS00 GL348 Port Vila Vanuatu               |  0.982906  | 0.0375798 |             0.0968645 |
|  9415056 CA Point Pinole                            |  0.982716  | 0.0813335 |             0.191096  |
|  UH799 SOUS00 GL209 Portu-Prince Haiti              |  0.982622  | 0.0151402 |             0.0422935 |
|  UH155 SOUS00 GL096 Dzaoudzi France                 |  0.982614  | 0.109668  |             0.234604  |
|  PAC14 SOUS43 0000014 OR Beaver Creek               |  0.982597  | 0.0960351 |             0.238541  |
|  UH392 SOUS00 Cocos Island Costa Rica               |  0.982592  | 0.105441  |             0.218373  |
|  UH043 SOUS00 Palmyra Island United States of Ameri |  0.982369  | 0.0259634 |             0.0621463 |
|  PAC21 SOUS43 0000021 OR Cannon Beach               |  0.982352  | 0.100258  |             0.225463  |
|  UH816 SOUS00 GL350 Port Sonara Cameroon            |  0.982327  | 0.0471959 |             0.0941571 |
|  UH016 SOUS00 GL138 Rikitea France                  |  0.982172  | 0.0263168 |             0.0573164 |
|  UH221 SOUS00 GL268 Simon's Town South Africa       |  0.982117  | 0.0510677 |             0.130176  |
|  UH149 SOUS00 Lamu Kenya                            |  0.982028  | 0.0990945 |             0.242147  |
|  MIC70 SOUS43 0000070 Utirik East (Airport) Marshal |  0.981977  | 0.0474998 |             0.0959794 |
|  UH302 SOUS00 GL168 Balboa Panama                   |  0.98196   | 0.204258  |             0.448946  |
|  UH209 SOUS00 GL246 Cascais Portugal                |  0.981815  | 0.102166  |             0.215666  |
|  1656 USA - Kodiak Island, AK                       |  0.981754  | 0.112313  |             0.283266  |
|  UH004 SOUS00 GL114 Nauru Nauru                     |  0.981629  | 0.056003  |             0.123934  |
|  MIC73 SOUS43 0000073 Kwajalein East (Airport) Mars |  0.981515  | 0.0500014 |             0.109144  |
|  WAKP8 SOUS43 1890000 Wake Island Pacific Ocean     |  0.981469  | 0.0334261 |             0.0758393 |
|  9414290 CA San Francisco                           |  0.98145   | 0.0736599 |             0.169182  |
|  9410666 CA Los Angeles Pier 400                    |  0.981418  | 0.0602886 |             0.160325  |
|  UH541 SOUS00 Bamfield Canada                       |  0.981254  | 0.106939  |             0.240489  |
|  9419945 CA Pyramid Point Smith River               |  0.981251  | 0.0856508 |             0.22584   |
|  UH084 SOUS00 Lobos de Afuera Peru                  |  0.981029  | 0.0527614 |             0.108788  |
|  MIC74 SOUS43 0000074 Ailinglaplap East (Airport) M |  0.980963  | 0.0538044 |             0.0984113 |
|  8531680 NJ Sandy Hook                              |  0.980621  | 0.062706  |             0.20634   |
|  PAC16 SOUS43 0000016 OR Lincoln City               |  0.980523  | 0.102509  |             0.226929  |
|  9414958 CA Bolinas Bolinas Lagoon                  |  0.980504  | 0.0675339 |             0.134406  |
|  UH181 SOUS00 GL013 Durban South Africa             |  0.980455  | 0.0643992 |             0.15428   |
|  9410665 CA Los Angeles Pier J                      |  0.980104  | 0.0624015 |             0.172591  |
|  UH283 SOUS00 GL336 Fortaleza Brazil                |  0.979997  | 0.0955689 |             0.229834  |
|  MIC88 SOUS43 0000088 Ebon East Marshall Islands Po |  0.979982  | 0.0572383 |             0.112497  |
|  9443090 WA Neah Bay                                |  0.979965  | 0.104877  |             0.217659  |
|  9447130 WA Seattle Puget Sound                     |  0.979958  | 0.13003   |             0.339933  |
|  9410230 CA La Jolla                                |  0.979928  | 0.0611669 |             0.152636  |
|  UH094 SOUS00 Matarani Peru                         |  0.979913  | 0.0432556 |             0.0922776 |
|  9455920 AK Anchorage                               |  0.979899  | 0.300586  |             1.06626   |
|  KWJP8 SOUS43 1820000 Kwajalein Marshall Island     |  0.979824  | 0.0522432 |             0.101792  |
|  UH207 SOUS00 GL249 Ceuta Spain                     |  0.979707  | 0.0335704 |             0.0851936 |
|  600 NM West-Northwest of Phuket Thailand           |  0.979613  | 0.027518  |             0.0619055 |
|  UH107 SOUS00 GL045 Padang Indonesia                |  0.9795    | 0.044347  |             0.0787586 |
|  MIC78 SOUS43 0000078 Wake West Wake Island Populat |  0.979452  | 0.0346016 |             0.0780109 |
|  UH133 SOUS00 GL068 Ambon Indonesia                 |  0.979298  | 0.0728684 |             0.196109  |
|  9439040 OR Astoria                                 |  0.979275  | 0.118639  |             0.322403  |
|  MIC77 SOUS43 0000077 Wake East Wake Island Populat |  0.979213  | 0.0357436 |             0.075353  |
|  UH101 SOUS00 GL008 Mombasa Kenya                   |  0.979195  | 0.112748  |             0.252539  |
|  9432780 OR Charleston                              |  0.979058  | 0.0998    |             0.253166  |
|  UH275 SOUS00 GL222 Halifax Canada                  |  0.979036  | 0.0629932 |             0.149893  |
|  UH019 SOUS00 GL123 Noumea France                   |  0.97902   | 0.047723  |             0.110657  |
|  9431647 OR Port Orford                             |  0.978899  | 0.0936465 |             0.243833  |
|  MIC71 SOUS43 0000071 Wotje East (Airport) Marshall |  0.978773  | 0.0544166 |             0.105726  |
|  UH333 SOUS00 GL057 Fort Denison Australia          |  0.978476  | 0.0549016 |             0.127161  |
|  UH351 SOUS00 GL087 Ofunato Japan                   |  0.978467  | 0.0462021 |             0.132964  |
|  MIC87 SOUS43 0000087 Ebeye Wes Marshall Islands Po |  0.978225  | 0.0538177 |             0.108492  |
|  9446484 WA Tacoma                                  |  0.978119  | 0.143993  |             0.317663  |
|  9455920 Anchorage AK                               |  0.977999  | 0.315975  |             1.14256   |
|  UH231 SOUS00 GL335 Takoradi Ghana                  |  0.977893  | 0.052559  |             0.120554  |
|  UH289 SOUS00 GL248 Gibraltar United Kingdom of Gre |  0.977886  | 0.0340736 |             0.0829058 |
|  UH417 SOUS00 Sadeng Indonesia                      |  0.977883  | 0.0780378 |             0.172667  |
|  UH353 SOUS00 GL085 Kushimoto Japan                 |  0.97787   | 0.055695  |             0.149997  |
|  UH104 SOUS00 GL026 Diego Garcia United Kingdom of  |  0.977815  | 0.0555225 |             0.105545  |
|  9418767 CA North Spit                              |  0.977603  | 0.0896455 |             0.235716  |
|  9410170 CA San Diego San Diego Bay                 |  0.977537  | 0.0692997 |             0.177664  |
|  9411406 CA Oil Platform Harvest                    |  0.977419  | 0.0642077 |             0.144311  |
|  8518750 NY The Battery                             |  0.977248  | 0.0685728 |             0.237642  |
|  9447214 WA Shilshole Bay GPS Buoy                  |  0.977097  | 0.136138  |             0.289505  |
|  9459450 AK Sand Point                              |  0.977049  | 0.099752  |             0.229222  |
|  UH419 SOUS00 Lembar Indonesia                      |  0.97704   | 0.0568122 |             0.148492  |
|  MIC86 SOUS43 0000086 Ebeye East Marshall Islands P |  0.97698   | 0.055919  |             0.114931  |
|  UH295 SOUS00 GL238 Stornoway United Kingdom of Gre |  0.976975  | 0.164585  |             0.34308   |
|  UH317 SOUS00 Ensenada Mexico                       |  0.976958  | 0.0642923 |             0.157537  |
|  UH227 SOUS00 GL202 Cayenne France                  |  0.976917  | 0.0999089 |             0.214454  |
|  UH420 SOUS00 Saumlaki Indonesia                    |  0.976852  | 0.0913475 |             0.236819  |
|  UH291 SOUS00 GL263 Ascension United Kingdom of Gre |  0.976646  | 0.039685  |             0.0901171 |
|  UH125 SOUS00 Prigi Indonesia                       |  0.976335  | 0.088183  |             0.197039  |
|  UH109 SOUS00 GL027 Gan Maldives                    |  0.975998  | 0.0387889 |             0.0790812 |
|  MIC72 SOUS43 0000072 Ujae East (Airport) Marshall  |  0.975978  | 0.0543738 |             0.110478  |
|  UH009 SOUS00 GL066 Honiara Solomon Islands         |  0.975721  | 0.0300462 |             0.0844434 |
|  UH913 SOUS00 Telukdalam Indonesia                  |  0.975585  | 0.0350528 |             0.0760297 |
|  1272 Norway - Andenes                              |  0.975402  | 0.0836423 |             0.182271  |
|  UH113 SOUS00 Masirah Oman                          |  0.975319  | 0.0754856 |             0.143241  |
|  UH035 SOUS00 GL177 San Felix Chile                 |  0.975187  | 0.0410536 |             0.083264  |
|  UH834 SOUS00 GL239 Malin Head Ireland              |  0.975061  | 0.136638  |             0.331274  |
|  UH023 SOUS00 GL139 Rarotonga Cook Islands (the)    |  0.974921  | 0.035132  |             0.0723179 |
|  8658163 NC Wrightsville Beach                      |  0.974918  | 0.0588889 |             0.174383  |
|  UH830 SOUS00 GL243 La Coruna Spain                 |  0.974816  | 0.145333  |             0.326699  |
|  UH805 SOUS00 GL323 Vardo Norway                    |  0.974767  | 0.131299  |             0.259725  |
|  9414863 CA Richmond                                |  0.974324  | 0.0920296 |             0.227562  |
|  8519483 NY Bergen Point West Reach                 |  0.97423   | 0.0766754 |             0.26508   |
|  MIC34 SOUS43 0000034 Kosrae West (Walung) Kosrae   |  0.974149  | 0.0561087 |             0.117334  |
|  9414776 CA Oakland Berth 34                        |  0.974115  | 0.0961652 |             0.249585  |
|  MIC33 SOUS43 0000033 Kosrae North (Airport) Kosrae |  0.973981  | 0.056405  |             0.122181  |
|  MIC36 SOUS43 0000036 Kosrae East (Malem) Kosrae F  |  0.97367   | 0.0581096 |             0.118121  |
|  9459881 AK King Cove                               |  0.973626  | 0.0992352 |             0.238737  |
|  UH820 SOUS00 GL225 Nuuk Denmark                    |  0.973571  | 0.176471  |             0.337099  |
|  UH108 SOUS00 GL028 Male Maldives                   |  0.973539  | 0.0349364 |             0.0686984 |
|  9414750 CA Alameda                                 |  0.973515  | 0.102839  |             0.247009  |
|  9439011 OR Hammond                                 |  0.973356  | 0.131143  |             0.386073  |
|  UH047 SOUS00 GL103 Chichijima Japan                |  0.973053  | 0.0347876 |             0.0878073 |
|  UH273 SOUS00 Port-aux-basques Canada               |  0.972981  | 0.0550819 |             0.172394  |
|  9416409 CA GREEN COVE PACIFIC OCEAN                |  0.972897  | 0.0812605 |             0.191832  |
|  UH261 SOUS00 Charleston SC United States of Ameri  |  0.972709  | 0.0781504 |             0.217522  |
|  UH153 SOUS00 GL029 Minicoy India                   |  0.972684  | 0.0396975 |             0.0810874 |
|  MIC35 SOUS43 0000035 Kosrae South (Utwa Ma) Kosrae |  0.972615  | 0.0586817 |             0.116037  |
|  UH365 SOUS00 Ishigaki Japan                        |  0.972491  | 0.0662357 |             0.143287  |
|  8723214 FL Virginia Key                            |  0.972294  | 0.0342065 |             0.095771  |
|  MIC67 SOUS43 0000067 Mokil East Pohnpei FSM Warni  |  0.972292  | 0.0493198 |             0.094808  |
|  8537121 NJ Ship John Shoal                         |  0.972288  | 0.0923323 |             0.220779  |
|  9414311 CA San Francisco Pier 1                    |  0.972176  | 0.0983105 |             0.257593  |
|  UH179 SOUS00 GL024 Saint Paul France               |  0.971961  | 0.0574063 |             0.158802  |
|  UH093 SOUS00 GL173 Callao Peru                     |  0.971927  | 0.0440614 |             0.106021  |
|  1586 New Zealand - Christchurch                    |  0.971897  | 0.11718   |             0.268307  |
|  902 Japan - Ishigakijima                           |  0.971729  | 0.0663614 |             0.148816  |
|  878 USA - Fort_Pulaski_GA                          |  0.97171   | 0.102139  |             0.258973  |
|  1664 Norway - Ny Alesund                           |  0.971684  | 0.063999  |             0.154666  |
|  UH163 SOUS00 GL049 Benoa Indonesia                 |  0.971676  | 0.108421  |             0.263692  |
|  9415102 CA Martinez-Amorco Pier                    |  0.971648  | 0.12307   |             0.362095  |
|  MIC68 SOUS43 0000068 Pingelap East Pohnpei FSM Wa  |  0.971371  | 0.0534491 |             0.114795  |
|  UH130 SOUS00 GL278 Casey Australia                 |  0.971369  | 0.0656556 |             0.171012  |
|  8722670 FL Lake Worth Pier Atlantic                |  0.971253  | 0.0430643 |             0.108789  |
|  MIC69 SOUS43 0000069 Enewetak East Marshall Island |  0.971226  | 0.0498523 |             0.0974318 |
|  UH789 SOUS00 Prickley Bay Grenada                  |  0.971111  | 0.0256379 |             0.0744375 |
|  UH147 SOUS00 GL030 Karachi Pakistan                |  0.970851  | 0.102347  |             0.245012  |
|  8665530 SC Charleston Cooper River E               |  0.97083   | 0.0808903 |             0.204458  |
|  UH082 SOUS00 GL182 Acajutla El Salvador            |  0.970791  | 0.106774  |             0.197     |
|  UH542 SOUS00 GL156 Tofino Canada                   |  0.970458  | 0.118569  |             0.32209   |
|  9457804 AK Alitak                                  |  0.970136  | 0.190877  |             0.46817   |
|  UH806 SOUS00 Nouakchott Mauritania                 |  0.969866  | 0.0587324 |             0.126159  |
|  8724580 FL Key West                                |  0.969138  | 0.0265064 |             0.0567103 |
|  UH117 SOUS00 Hanimaadhoo Maldives                  |  0.969123  | 0.0381617 |             0.0826191 |
|  MIC30 SOUS43 0000030 Pohnpei East Pohnpei FSM Maj  |  0.968962  | 0.048814  |             0.0936938 |
|  9415020 CA Point Reyes                             |  0.968868  | 0.0855137 |             0.199113  |
|  UH803 SOUS00 GL234 Rorvik Norway                   |  0.968654  | 0.109433  |             0.249147  |
|  UH105 SOUS00 GL019 Rodrigues Mauritius             |  0.968654  | 0.0550189 |             0.124003  |
|  MIC29 SOUS43 0000029 Pohnpei North Pohnpei FSM Ma  |  0.968539  | 0.0470842 |             0.0873527 |
|  1612480 HI Mokuoloe                                |  0.968433  | 0.0309939 |             0.078619  |
|  9414575 CA Coyote Creek                            |  0.967991  | 0.144407  |             0.361005  |
|  MIC66 SOUS43 0000066 Pakin East Pohnpei FSM Warni  |  0.967762  | 0.0455327 |             0.0854284 |
|  UH184 SOUS00 GL076 Port Elizabeth South Africa     |  0.967617  | 0.074284  |             0.189164  |
|  8467150 CT Bridgeport                              |  0.967185  | 0.124473  |             0.288445  |
|  MIC65 SOUS43 0000065 Sapwuafik (Ngatik) East Pohnp |  0.967093  | 0.0470973 |             0.100027  |
|  UH171 SOUS00 GL046 Cocos Australia                 |  0.967077  | 0.0459701 |             0.102362  |
|  9444900 WA Port Townsend                           |  0.966949  | 0.12506   |             0.24219   |
|  UH777 SOUS00 Puerto Plata Dominican Republic (the) |  0.966921  | 0.0267974 |             0.0546879 |
|  8725110 FL Naples Gulf of Mexico                   |  0.966915  | 0.043952  |             0.125452  |
|  UH382 SOUS00 Subic Bay Philippines (the)           |  0.966824  | 0.0514363 |             0.122765  |
|  8461490 CT New London                              |  0.966692  | 0.0502457 |             0.12553   |
|  UH041 SOUS00 GL102 Dutch Harbor AK United States   |  0.966667  | 0.0798942 |             0.186912  |
|  9415144 CA Port Chicago                            |  0.966613  | 0.141017  |             0.390846  |
|  MIC32 SOUS43 0000032 Pohnpei West Pohnpei FSM Maj  |  0.966144  | 0.0471318 |             0.0897295 |
|  UH142 SOUS00 Langkawi Malaysia                     |  0.966082  | 0.129818  |             0.28753   |
|  MIC08 SOUS43 0000008 Pohnpei FSM UHSLC Gauge       |  0.965969  | 0.0487824 |             0.0844525 |
|  MIC31 SOUS43 0000031 Pohnpei South Pohnpei FSM Ma  |  0.965571  | 0.0502129 |             0.100523  |
|  UH024 SOUS00 GL143 Penrhyn Cook Islands (the)      |  0.965548  | 0.0129302 |             0.0310161 |
|  UH259 SOUS00 GL221 Bermuda United Kingdom of Great |  0.965419  | 0.0443958 |             0.0934676 |
|  UH071 SOUS00 GL101 Wellington New Zealand          |  0.965373  | 0.0761842 |             0.210834  |
|  UH316 SOUS00 GL267 Acapulco Gro. Mexico            |  0.965069  | 0.0346398 |             0.0897695 |
|  9461710 AK Atka                                    |  0.964836  | 0.0682581 |             0.14816   |
|  1611400 HI Nawiliwili                              |  0.964785  | 0.0292726 |             0.0651891 |
|  9462450 AK Nikolski                                |  0.964744  | 0.0811479 |             0.212237  |
|  UH299 SOUS00 GL344 Qaqortoq Denmark                |  0.964455  | 0.141405  |             0.28884   |
|  UH738 SOUS00 Santa Marta Colombia                  |  0.964423  | 0.0146102 |             0.0366805 |
|  9449880 WA Friday Harbor                           |  0.964406  | 0.114669  |             0.232967  |
|  9759938 PR Mona Island                             |  0.964149  | 0.0126685 |             0.0325711 |
|  UH164 SOUS00 GL017 Reunion France                  |  0.964051  | 0.0191235 |             0.0485667 |
|  9759394 PR Mayaguez                                |  0.963391  | 0.0170329 |             0.0413762 |
|  UH103 SOUS00 GL018 Port Louis Mauritius            |  0.963343  | 0.0233784 |             0.0551668 |
|  8452944 RI Conimicut Light                         |  0.963074  | 0.0653465 |             0.123128  |
|  UH878 SOUS00 Bullen Bay Curacao                    |  0.961526  | 0.0154182 |             0.0398804 |
|  UH162 SOUS00 GL291 Cilicap Indonesia               |  0.961488  | 0.0906267 |             0.218629  |
|  UH286 SOUS00 GL190 Puerto Deseado Argentina        |  0.961178  | 0.287421  |             0.821892  |
|  9435380 OR South Beach                             |  0.96115   | 0.144406  |             0.461495  |
|  UH288 SOUS00 GL229 Reykjavik Iceland               |  0.961067  | 0.204428  |             0.388137  |
|  UH370 SOUS00 GL073 Manila Philippines (the)        |  0.961014  | 0.0619621 |             0.150399  |
|  UH049 SOUS00 GL104 Minamitorishima Japan           |  0.960951  | 0.0267147 |             0.083895  |
|  UH114 SOUS00 GL004 Salalah Oman                    |  0.960856  | 0.0644461 |             0.140142  |
|  9440569 WA Skamokawa                               |  0.960556  | 0.127092  |             0.304203  |
|  UH334 SOUS00 GL060 Townsville Australia            |  0.960491  | 0.108565  |             0.246541  |
|  UH654 SOUS00 Currimao Philippines (the)            |  0.959615  | 0.0397788 |             0.084264  |
|  UH029 SOUS00 GL117 Kapingamarangi Micronesia (Fede |  0.95948   | 0.0445316 |             0.0829775 |
|  9461380 AK Adak Island                             |  0.959455  | 0.076101  |             0.209228  |
|  MIC10 SOUS43 0000010 Moen I Chuuk FSM Historic CO  |  0.959064  | 0.0337945 |             0.0678174 |
|  9461380 Adak Island AK                             |  0.95833   | 0.0771507 |             0.199502  |
|  UH294 SOUS00 GL241 Newlyn Cornwall United Kingdom  |  0.958297  | 0.263439  |             0.581524  |
|  9465261 Nushagak Bay                               |  0.958234  | 0.348661  |             0.776038  |
|  UH340 SOUS00 Kaohsiung China                       |  0.957942  | 0.0496012 |             0.125705  |
|  UH331 SOUS00 GL058 Brisbane Australia              |  0.957933  | 0.117978  |             0.36569   |
|  1617433 HI Kawaihae                                |  0.957439  | 0.0359951 |             0.0853747 |
|  UH052 SOUS00 GL109 Johnston United States of Ameri |  0.957353  | 0.0375713 |             0.082596  |
|  UH276 SOUS00 GL223 St. John's Canada               |  0.957225  | 0.0785088 |             0.166453  |
|  MIC82 SOUS43 0000082 Oroluk East Pohnpei FSM Popu  |  0.957137  | 0.045294  |             0.0836573 |
|  UH121 SOUS00 GL339 Pt. La Rue Seychelles           |  0.95706   | 0.0602517 |             0.138117  |
|  8721604 FL Trident Pier Port Canaver               |  0.956908  | 0.0653331 |             0.155998  |
|  UH220 SOUS00 GL314 Walvis Bay Namibia              |  0.956779  | 0.0725299 |             0.177439  |
|  1612340 HI Honolulu                                |  0.956568  | 0.0330345 |             0.06873   |
|  9751381 VI Lameshur Bay St John                    |  0.956152  | 0.0134698 |             0.0386726 |
|  9464212 St Paul Island AK                          |  0.956079  | 0.0761258 |             0.157781  |
|  UH808 SOUS00 GL343 Thule (Pituffik) Denmark        |  0.955225  | 0.126202  |             0.278345  |
|  MIC26 SOUS43 0000026 Chuuk Lagoon East Chuuk FSM   |  0.954625  | 0.037029  |             0.0768935 |
|  UH115 SOUS00 GL033 Colombo Sri Lanka               |  0.954448  | 0.0363038 |             0.0695154 |
|  MIC61 SOUS43 0000061 Ulul East Chuuk FSM Warning   |  0.954138  | 0.0314011 |             0.0734891 |
|  8727520 FL Cedar Key                               |  0.954122  | 0.08493   |             0.233361  |
|  UH822 SOUS00 GL242 Brest France                    |  0.953804  | 0.348771  |             0.731985  |
|  UH271 SOUS00 Fort de France France                 |  0.953103  | 0.0202961 |             0.0539375 |
|  MIC62 SOUS43 0000062 Fananu East Chuuk FSM Warnin  |  0.953094  | 0.036822  |             0.071997  |
|  MIC64 SOUS43 0000064 Lukunor East Chuuk FSM Warni  |  0.952831  | 0.0433755 |             0.0828759 |
|  MIC60 SOUS43 0000060 Puluwat East Chuuk FSM Warni  |  0.952611  | 0.0327502 |             0.0796043 |
|  MIC63 SOUS43 0000063 Losap East Chuuk FSM Warning  |  0.951839  | 0.0392219 |             0.0763285 |
|  UH189 SOUS00 GL131 Dumont d'Urville Antarctica     |  0.951392  | 0.0817966 |             0.175676  |
|  UH836 SOUS00 GL333 Alert Canada                    |  0.951014  | 0.0435813 |             0.112442  |
|  8454000 RI Providence                              |  0.950886  | 0.0777386 |             0.146839  |
|  8551910 DE Reedy Point                             |  0.950852  | 0.122277  |             0.307533  |
|  UH122 SOUS00 Sibolga Indonesia                     |  0.950224  | 0.0570784 |             0.15737   |
|  MIC27 SOUS43 0000027 Chuuk Lagoon North Chuuk FSM  |  0.948878  | 0.0375137 |             0.0827463 |
|  UH119 SOUS00 GL002 Djibouti Djibouti               |  0.948421  | 0.0978774 |             0.236832  |
|  9752619 PR Isabel Segunda Vieques Is               |  0.947997  | 0.019021  |             0.0416547 |
|  9752695 PR Esperanza Vieques Island                |  0.947995  | 0.0144045 |             0.0377975 |
|  8760922 LA Pilots Station East S.W.                |  0.947934  | 0.0273698 |             0.0544431 |
|  8536110 NJ Cape May                                |  0.947918  | 0.107724  |             0.24485   |
|  9754228 PR Yabucoa Harbor                          |  0.947576  | 0.0143821 |             0.0384891 |
|  UH600 SOUS00 GL181 Ushuaia Argentina               |  0.947047  | 0.122138  |             0.271483  |
|  UH180 SOUS00 GL023 Kerguelen France                |  0.945991  | 0.0949907 |             0.239671  |
|  9759110 PR Magueyes Island                         |  0.945928  | 0.0142562 |             0.0319449 |
|  UH166 SOUS00 GL040 Broome Australia                |  0.945689  | 0.584631  |             0.992827  |
|  MIC28 SOUS43 0000028 Chuuk Lagoon West Chuuk FSM   |  0.945319  | 0.0369126 |             0.0818792 |
|  UH290 SOUS00 GL305 Port Stanley United Kingdom of  |  0.944473  | 0.0861553 |             0.180168  |
|  8551762 DE Delaware City                           |  0.943833  | 0.132264  |             0.403639  |
|  UH173 SOUS00 GL277 Davis Australia                 |  0.943832  | 0.0843402 |             0.174276  |
|  UH347 SOUS00 GL327 Abashiri Japan                  |  0.943526  | 0.0645824 |             0.173014  |
|  8570283 MD Ocean City Inlet                        |  0.943299  | 0.0664234 |             0.146877  |
|  UH601 SOUS00 GL185 Esperanza Argentina             |  0.942979  | 0.152131  |             0.364969  |
|  8726607 FL Old Port Tampa                          |  0.94246   | 0.0449149 |             0.102691  |
|  UH547 SOUS00 Barbers Point HI United States of Am  |  0.942101  | 0.0368126 |             0.0818679 |
|  9758053 PR Penuelas                                |  0.940366  | 0.0150941 |             0.0326138 |
|  UH350 SOUS00 GL089 Kushiro Japan                   |  0.940279  | 0.07775   |             0.199456  |
|  1336 Norway - Maloy                                |  0.939822  | 0.108313  |             0.243416  |
|  8449130 MA Nantucket Island                        |  0.939253  | 0.0861659 |             0.180603  |
|  UH833 SOUS00 GL224 Nain Canada                     |  0.938461  | 0.145982  |             0.301933  |
|  8656483 NC Beaufort Duke Marine Lab                |  0.937389  | 0.0860032 |             0.198985  |
|  9465601 Carter Bay Kuskokwim Bay AK                |  0.936948  | 0.249866  |             0.609318  |
|  8548989 PA Newbold                                 |  0.936938  | 0.162978  |             0.523803  |
|  8454049 RI Quonset Point                           |  0.936576  | 0.0803307 |             0.16523   |
|  UH015 SOUS00 GL140 Papeete France                  |  0.936219  | 0.0146036 |             0.0308743 |
|  8726384 FL Port Manatee                            |  0.934452  | 0.0445965 |             0.104951  |
|  8573927 MD Chesapeake City                         |  0.934316  | 0.0683821 |             0.175718  |
|  8726667 FL Mckay Bay Entrance                      |  0.93388   | 0.0506343 |             0.114252  |
|  8720218 FL Mayport (Bar Pilots Dock)               |  0.933728  | 0.119565  |             0.278889  |
|  UH824 SOUS00 GL205 Marseille France                |  0.933652  | 0.0170963 |             0.0470492 |
|  UH383 SOUS00 Vung Tau Viet Nam                     |  0.932683  | 0.186553  |             0.434752  |
|  1619910 HI Sand Island Midway Island               |  0.932649  | 0.0272096 |             0.0704455 |
|  8539094 NJ Burlington Delaware River               |  0.931879  | 0.160038  |             0.392004  |
|  8729108 FL Panama City                             |  0.93099   | 0.0352325 |             0.0957636 |
|  UH335 SOUS00 GL056 Spring Bay Australia            |  0.930634  | 0.0828231 |             0.165444  |
|  UH680 SOUS00 GL130 Macquarie Is. Australia         |  0.93009   | 0.0852128 |             0.174064  |
|  UH079 SOUS00 GL128 Chatham New Zealand             |  0.929697  | 0.0741365 |             0.140325  |
|  8658120 NC Wilmington                              |  0.929365  | 0.105723  |             0.279566  |
|  UH129 SOUS00 GL055 Portland S.Aus. Australia       |  0.929327  | 0.0726569 |             0.141226  |
|  UH920 SOUS00 GL020 Marion Island South Africa      |  0.92551   | 0.0532043 |             0.126433  |
|  UH737 SOUS00 San Andres Colombia                   |  0.922756  | 0.020576  |             0.0480119 |
|  8775870 TX Bob Hall Pier Corpus Chri               |  0.922206  | 0.0390024 |             0.0903957 |
|  UH266 SOUS00 GL208 Cristobal Panama                |  0.920427  | 0.0227706 |             0.0469148 |
|  9465374 Snag Point Dillingham AK                   |  0.91888   | 0.49101   |             1.28477   |
|  UH364 SOUS00 GL088 Hakodate Japan                  |  0.918588  | 0.0560045 |             0.13124   |
|  8540433 PA Marcus Hook                             |  0.917382  | 0.157306  |             0.373836  |
|  UH268 SOUS00 Limon Costa Rica                      |  0.915692  | 0.0242158 |             0.0515488 |
|  UH699 SOUS00 GL044 Tanjong Pagar Singapore         |  0.911133  | 0.154991  |             0.36817   |
|  8729210 FL Panama City Beach                       |  0.908938  | 0.0391462 |             0.0769836 |
|  8545240 PA Philadelphia                            |  0.90794   | 0.16652   |             0.418808  |
|  9761115 Barbuda                                    |  0.906518  | 0.0189089 |             0.0501053 |
|  8538886 NJ Tacony-Palmyra Bridge                   |  0.906385  | 0.174793  |             0.450825  |
|  UH906 SOUS00 GL141 Moulmein Myanmar                |  0.90487   | 0.452122  |             1.27005   |
|  8723970 FL Vaca Key Florida Bay                    |  0.896087  | 0.0373803 |             0.0943052 |
|  8637689 VA Yorktown USCG Training Cen              |  0.895324  | 0.0753027 |             0.166005  |
|  8571892 MD Cambridge                               |  0.895122  | 0.0570763 |             0.14235   |
|  8720030 FL Fernandina Beach                        |  0.894046  | 0.167558  |             0.416523  |
|  UH829 SOUS00 GL340 Trieste Italy                   |  0.89209   | 0.0910413 |             0.241952  |
|  8639348 VA Money Point                             |  0.879657  | 0.0899657 |             0.211649  |
|  8651370 NC Duck                                    |  0.873168  | 0.108761  |             0.237105  |
|  8510560 NY Montauk                                 |  0.872404  | 0.0702144 |             0.137509  |
|  8632200 VA Kiptopeke                               |  0.869885  | 0.0905639 |             0.180691  |
|  UH177 SOUS00 GL022 Mawson Australia                |  0.867198  | 0.0916658 |             0.216068  |
|  8638610 VA Sewells Point                           |  0.864119  | 0.0882615 |             0.215267  |
|  8770777 TX Manchester                              |  0.862081  | 0.0499889 |             0.127031  |
|  8594900 DC Washington                              |  0.856048  | 0.0940445 |             0.251244  |
|  8638863 VA Chesapeake Bay Bridge Tunn              |  0.854801  | 0.0972938 |             0.199215  |
|  8770520 TX Rainbow Bridge                          |  0.84485   | 0.0285046 |             0.0619192 |
|  8779748 TX South Padre Island CG Stat              |  0.838299  | 0.0483048 |             0.0864103 |
|  UH280 SOUS00 GL195 Ilha Fiscal RJ Brazil           |  0.832937  | 0.0956146 |             0.263585  |
|  8735391 AL Dog River Bridge                        |  0.830267  | 0.0594506 |             0.129805  |
|  8447930 MA Woods Hole                              |  0.829691  | 0.0591034 |             0.121895  |
|  8771013 TX Eagle Point Galveston Bay               |  0.824962  | 0.0422138 |             0.0989105 |
|  UH178 SOUS00 GL021 Crozet France                   |  0.817637  | 0.0580214 |             0.146309  |
|  8574680 MD Baltimore Fort McHenry P                |  0.81716   | 0.052246  |             0.117778  |
|  UH700 SOUS00 GL188 Faraday Antarctica              |  0.814703  | 0.151688  |             0.343159  |
|  UH360 SOUS00 GL324 Wakkanai Japan                  |  0.811873  | 0.0409626 |             0.0848895 |
|  UH176 SOUS00 GL054 Esperance Australia             |  0.805292  | 0.0818263 |             0.178442  |
|  8770475 TX Port Arthur                             |  0.7986    | 0.0387771 |             0.108595  |
|  8770822 TX Texas Point Sabine Pass                 |  0.797077  | 0.0839243 |             0.220424  |
|  8635750 VA Lewisetta                               |  0.785018  | 0.0567719 |             0.132179  |
|  UH349 SOUS00 GL325 Toyama Japan                    |  0.775948  | 0.0350998 |             0.0999939 |
|  UH128 SOUS00 GL308 Thevenard Australia             |  0.773836  | 0.19699   |             0.528748  |
|  1019 Australia - Thevenard_AU                      |  0.772284  | 0.197752  |             0.570538  |
|  UH731 SOUS00 GL191 Puerto Madryn Argentina         |  0.763764  | 1.61278   |             6.86991   |
|  8737048 AL Mobile State Docks                      |  0.757718  | 0.0745868 |             0.146005  |
|  8577330 MD Solomons Island                         |  0.747577  | 0.0614871 |             0.136468  |
|  UH348 SOUS00 GL326 Hamada Japan                    |  0.740097  | 0.0541075 |             0.134646  |
|  UH825 SOUS00 GL284 Cuxhaven Germany                |  0.731533  | 0.466407  |             1.12746   |
|  8774770 TX Rockport                                |  0.725703  | 0.0167598 |             0.0354996 |
|  8571421 MD Bishops Head                            |  0.719759  | 0.101638  |             0.225514  |
|  8760721 LA Pilottown                               |  0.713962  | 0.0270767 |             0.0564291 |
|  8573364 MD Tolchester Beach                        |  0.703637  | 0.0713094 |             0.154795  |
|  8764044 LA Berwick Atchafalaya River               |  0.703513  | 0.048033  |             0.108258  |
|  UH175 SOUS00 GL053 Fremantle Australia             |  0.700807  | 0.075902  |             0.186507  |
|  8662245 SC Oyster Landing (N Inlet Es              |  0.692662  | 0.14167   |             0.350697  |
|  8747437 MS Bay Waveland Yacht Club                 |  0.681083  | 0.0715184 |             0.209491  |
|  8636580 VA Windmill Point                          |  0.676539  | 0.060052  |             0.131738  |
|  9468132 St. Michael                                |  0.664745  | 0.248995  |             0.683521  |
|  8764227 LA LAWMA Amerada Pass                      |  0.601379  | 0.0719298 |             0.149275  |
|  9468333 Unalakleet AK                              |  0.580755  | 0.304778  |             0.796322  |
|  UH729 SOUS00 GL192 Mar del Plata Argentina         |  0.551458  | 0.303743  |             0.623894  |
|  8774513 TX Copano Bay                              |  0.545449  | 0.0250815 |             0.0656367 |
|  UH579 SOUS00 GL151 Prudhoe Bay AK United States o  |  0.506579  | 0.0580686 |             0.199994  |
|  9497645 Prudhoe Bay AK                             |  0.496529  | 0.0585224 |             0.194911  |
|  8762075 LA Port Fourchon Belle Pass                |  0.4853    | 0.0628807 |             0.285579  |
|  8771341 TX Galveston Bay Entrance No               |  0.419327  | 0.123074  |             0.206146  |
|  8654467 NC USCG Station Hatteras                   |  0.375392  | 0.0402425 |             0.0865508 |
|  UH818 SOUS00 Smogen Sweden                         |  0.360287  | 0.0790245 |             0.165985  |
|  9468756 Nome AK                                    |  0.344837  | 0.160006  |             0.383117  |
|  952 USA - Nome_AK                                  |  0.278303  | 0.168313  |             0.44811   |
|  8761305 LA Shell Beach                             |  0.132009  | 0.116122  |             0.267661  |
|  9491094 Red Dog Dock AK                            |  0.109289  | 0.19      |             0.564604  |
|  8652587 NC Oregon Inlet Marina                     |  0.0505364 | 0.108948  |             0.28945   |
|  8775283 TX Port Inglesid                           |  0.0235834 | 0.043701  |             0.0881527 |
|  UH819 SOUS00 GL233 Goteborgorsh. Sweden            |  0.0219575 | 0.0735328 |             0.158611  |
|  UH804 SOUS00 GL321 Tregde Norway                   | -0.208531  | 0.0835996 |             0.148675  |
|  8761927 LA New Canal Station                       | -0.487934  | 0.0869337 |             0.180032  |
|  UH826 SOUS00 GL341 Stockholm Sweden                | -0.998101  | 0.0436639 |             0.120281  |

### Disclaimer
This program is under experimental development. The results should not be used for navigational purposes or emergency planning under any circumstances. Please do not duplicate and use the result figures from this website without permission.
