## GESTOFS-ML
This is a sister project of [GESTOFS](https://gm-ling.github.io/GESTOFS-develop/).  GESTOFS is an ADCIRC-based storm surge forecasting system for the whole globe.  GESTOFS-ML expands on this theme, but in addition to ADCIRC, it leverages a time-series forecasting ML model complete with meteorological forcing to enrich the prediction of surface water elevation.

### Site URL
[https://acerrone3.github.io/](https://acerrone3.github.io/)

### Latest Forecasts
Updated July 17, 2022

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
Updated July 17, 2022

Here, the ADCIRC forecasts are compared to the ML forecasts.  Comparisons are arranged in descending order based on each station's r-squared value.  Observational data has yet to be integrated for performance assessment.

|  Station                                            |         R2 |      RMSD |   Max Discrepancy (m) |
| :---------------------------------------------------|-----------:|----------:|----------------------:|
|  MIC22 SOUS43 0000022 Yap East Yap FSM Major Islan  |  0.995217  | 0.021896  |             0.0540996 |
|  MIC07 SOUS43 0000007 Yap FSM UHSLC Gauge           |  0.994609  | 0.0235353 |             0.0591068 |
|  MIC12 SOUS43 0000012 Guam North (Ritidian) Guam M  |  0.99426   | 0.0132788 |             0.032199  |
|  MIC53 SOUS43 0000053 Ngulu West Yap FSM Warning P  |  0.993716  | 0.0269296 |             0.0672093 |
|  UH123 SOUS00 GL347 Sabang Indonesia                |  0.993561  | 0.025046  |             0.0493032 |
|  MIC25 SOUS43 0000025 Yap North Yap FSM Major Isla  |  0.993517  | 0.0256299 |             0.0637273 |
|  UH118 SOUS00 Ko Miang Thailand                     |  0.993148  | 0.0395193 |             0.0656906 |
|  MIC54 SOUS43 0000054 Ngulu East Yap FSM Warning P  |  0.993046  | 0.0277833 |             0.0732766 |
|  MIC24 SOUS43 0000024 Yap West (Airport) Yap FSM M  |  0.99303   | 0.0275549 |             0.0666322 |
|  MIC43 SOUS43 0000043 Kayangel North Palau Warning  |  0.993023  | 0.0309578 |             0.0717397 |
|  MIC06 SOUS43 0000006 Malakal Palau UHSLC Gauge     |  0.992851  | 0.0334671 |             0.0942055 |
|  MIC21 SOUS43 0000021 Ngeremlengui West Palau Major |  0.992605  | 0.0338476 |             0.0834366 |
|  UH081 SOUS00 GL175 Valparaiso Chile                |  0.992584  | 0.0289078 |             0.0768374 |
|  UH030 SOUS00 Santa Cruz Ecuador                    |  0.992159  | 0.0438288 |             0.0930188 |
|  MIC46 SOUS43 0000046 Angaur East Palau Warning Poi |  0.992154  | 0.0338912 |             0.0855311 |
|  MIC48 SOUS43 0000048 Angaur South Palau Warning Po |  0.992112  | 0.0341401 |             0.0908558 |
|  MIC44 SOUS43 0000044 Peleliu East Palau Warning Po |  0.9921    | 0.0346982 |             0.0921072 |
|  MIC23 SOUS43 0000023 Yap South (Colonia) Yap FSM   |  0.992035  | 0.0284086 |             0.0706289 |
|  APRP7 SOUS43 1630000 Apra HarborGuam               |  0.991773  | 0.0171798 |             0.0454608 |
|  MIC47 SOUS43 0000047 Angaur West Palau Warning Poi |  0.991707  | 0.0353633 |             0.0862564 |
|  MIC20 SOUS43 0000020 East Melekeok Palau Major Isl |  0.991533  | 0.0335945 |             0.0825247 |
|  MIC55 SOUS43 0000055 Ulithi East (Airport) Yap FS  |  0.991378  | 0.026783  |             0.0693877 |
|  9455760 AK Nikiski                                 |  0.99121   | 0.171559  |             0.498281  |
|  UH908 SOUS00 GL038 Port Blair India                |  0.990911  | 0.0414306 |             0.0857962 |
|  MIC45 SOUS43 0000045 Peleliu West Palau Warning Po |  0.990875  | 0.0372103 |             0.0968001 |
|  MIC13 SOUS43 0000013 Rota East (Sinapalu) Rota Ma  |  0.990578  | 0.01471   |             0.0432108 |
|  UH092 SOUS00 Talara Peru                           |  0.990469  | 0.0449511 |             0.0982732 |
|  MIC14 SOUS43 0000014 Rota West (Songsong) Rota Ma  |  0.990426  | 0.0165471 |             0.0380087 |
|  MIC56 SOUS43 0000056 Fais East(Airport) Yap FSM W  |  0.990303  | 0.0264425 |             0.0681513 |
|  UH025 SOUS00 GL121 Funafuti Tuvalu                 |  0.990296  | 0.0340035 |             0.0939718 |
|  MIC19 SOUS43 0000019 Saipan North Saipan Marianas  |  0.990246  | 0.0143005 |             0.0400297 |
|  9452634 AK Elfin Cove                              |  0.990135  | 0.0926143 |             0.218134  |
|  MIC52 SOUS43 0000052 Sonsorol Southwest Palau Warn |  0.989961  | 0.0400711 |             0.0967634 |
|  UH403 SOUS00 Jackson New Zealand                   |  0.989596  | 0.0606478 |             0.151705  |
|  MIC11 SOUS43 0000011 Guam South (Cocos) Guam Mari  |  0.98959   | 0.0173008 |             0.0502984 |
|  UH816 SOUS00 GL350 Port Sonara Cameroon            |  0.989547  | 0.0327317 |             0.0691554 |
|  1497 Korea - Busan                                 |  0.989424  | 0.0342775 |             0.086611  |
|  MIC49 SOUS43 0000049 Sonsorol Northeast Palau Warn |  0.98933   | 0.0416141 |             0.104427  |
|  MIC51 SOUS43 0000051 Sonsorol Northwest Palau Warn |  0.989289  | 0.0417902 |             0.114086  |
|  MIC90 SOUS43 0000090 62 Km ENE from Helen Reef (-2 |  0.989235  | 0.0413436 |             0.102445  |
|  UH354 SOUS00 GL082 Aburatsu Japan                  |  0.989135  | 0.0378046 |             0.108313  |
|  UH011 SOUS00 GL146 Christmas Kiribati              |  0.989124  | 0.0187794 |             0.0474384 |
|  600 NM West-Northwest of Phuket Thailand           |  0.989063  | 0.0175026 |             0.0377107 |
|  UH218 SOUS00 GL250 Funchal Portugal                |  0.988829  | 0.0511124 |             0.110062  |
|  MIC57 SOUS43 0000057 Faraulep East Yap FSM Warnin  |  0.988803  | 0.0210611 |             0.0530009 |
|  MIC18 SOUS43 0000018 Saipan West (Garapan) Saipan  |  0.988755  | 0.0168266 |             0.0425506 |
|  9454050 AK Cordova                                 |  0.98866   | 0.110756  |             0.270178  |
|  MIC79 SOUS43 0000079 Eurapik East Yap FSM Populat  |  0.98857   | 0.0249284 |             0.0749028 |
|  UH223 SOUS00 GL253 Dakar Senegal                   |  0.988539  | 0.0331372 |             0.0678366 |
|  9451600 AK Sitka                                   |  0.988501  | 0.0909372 |             0.22166   |
|  UH157 SOUS00 GL035 Vishakhapatnam India            |  0.988393  | 0.0315725 |             0.0740277 |
|  UH013 SOUS00 GL145 Kanton Kiribati                 |  0.988322  | 0.0270379 |             0.0609431 |
|  9452400 Skagway AK                                 |  0.988308  | 0.173509  |             0.331283  |
|  9452400 AK Skagway Taiya Inlet                     |  0.988284  | 0.173683  |             0.380787  |
|  UH291 SOUS00 GL263 Ascension United Kingdom of Gre |  0.988261  | 0.0247631 |             0.053994  |
|  UH302 SOUS00 GL168 Balboa Panama                   |  0.988261  | 0.152726  |             0.30314   |
|  MIC50 SOUS43 0000050 Sonsorol Southeast Palau Warn |  0.988255  | 0.043182  |             0.105429  |
|  9451600 Sitka AK                                   |  0.988206  | 0.092102  |             0.209747  |
|  1656 USA - Kodiak Island, AK                       |  0.98791   | 0.0829778 |             0.216387  |
|  UH088 SOUS00 Caldera Chile                         |  0.987856  | 0.0348272 |             0.0683495 |
|  9451054 AK Port Alexander                          |  0.987671  | 0.107885  |             0.247786  |
|  UH356 SOUS00 Maisaka Japan                         |  0.987653  | 0.0342187 |             0.0950975 |
|  UH017 SOUS00 Hiva Oa France                        |  0.987651  | 0.0412066 |             0.0832519 |
|  9454240 AK Valdez                                  |  0.987361  | 0.117855  |             0.305129  |
|  UH002 SOUS00 GL113 Tarawa Bairiki Kiribati         |  0.987179  | 0.0410323 |             0.0846447 |
|  UH209 SOUS00 GL246 Cascais Portugal                |  0.987164  | 0.0765886 |             0.16223   |
|  9452210 AK Juneau                                  |  0.986929  | 0.176186  |             0.347974  |
|  MIC40 SOUS43 0000040 Majuro North Marshall Islands |  0.986799  | 0.0385559 |             0.0819245 |
|  MIC15 SOUS43 0000015 Tinian East Tinian Marianas   |  0.986781  | 0.0154318 |             0.0382677 |
|  MIC58 SOUS43 0000058 Woleai East Yap FSM Warning   |  0.98668   | 0.0247719 |             0.0723908 |
|  MIC39 SOUS43 0000039 Majuro West Marshall Islands  |  0.986676  | 0.0388308 |             0.087786  |
|  9459450 AK Sand Point                              |  0.986656  | 0.0688738 |             0.192297  |
|  MIC76 SOUS43 0000076 Mili East Marshall Islands Wa |  0.986509  | 0.0403278 |             0.0843818 |
|  UH133 SOUS00 GL068 Ambon Indonesia                 |  0.986354  | 0.0534483 |             0.143521  |
|  UH541 SOUS00 Bamfield Canada                       |  0.986244  | 0.0848578 |             0.196592  |
|  PAC24 SOUS43 0000024 WA Long Beach                 |  0.98608   | 0.0831803 |             0.190376  |
|  UH031 SOUS00 GL142 Nuku Hiva France                |  0.985994  | 0.0424897 |             0.0900447 |
|  9453220 Yakutat Bay AK                             |  0.985711  | 0.102634  |             0.230463  |
|  PAC22 SOUS43 0000022 OR Seaside                    |  0.985651  | 0.0845907 |             0.207337  |
|  UH420 SOUS00 Saumlaki Indonesia                    |  0.985609  | 0.0646362 |             0.166985  |
|  MIC89 SOUS43 0000089 Arno East Marshall Islands Po |  0.985607  | 0.0405423 |             0.0897235 |
|  8661070 SC Springmaid Pier                         |  0.985597  | 0.0501341 |             0.152463  |
|  PAC17 SOUS43 0000017 OR Neskowin Beach             |  0.985573  | 0.0819228 |             0.177777  |
|  UH392 SOUS00 Cocos Island Costa Rica               |  0.985426  | 0.0899442 |             0.179761  |
|  UH362 SOUS00 GL083 Nagasaki Japan                  |  0.985384  | 0.0740686 |             0.210901  |
|  9443090 WA Neah Bay                                |  0.985365  | 0.0831719 |             0.183325  |
|  PAC18 SOUS43 0000018 OR Pacific City               |  0.985355  | 0.0826496 |             0.166749  |
|  MIC38 SOUS43 0000038 Majuro South (Airport) Marsha |  0.985026  | 0.0416078 |             0.0913703 |
|  UH345 SOUS00 Nakano Shima Japan                    |  0.985019  | 0.0518245 |             0.137778  |
|  MIC37 SOUS43 0000037 Majuro East Marshall Islands  |  0.984852  | 0.0417282 |             0.0907343 |
|  UH684 SOUS00 GL178 Puerto Montt Chile              |  0.984834  | 0.230823  |             0.524634  |
|  UH283 SOUS00 GL336 Fortaleza Brazil                |  0.984729  | 0.0738897 |             0.170951  |
|  9411399 CA Gaviota State Park Pacifi               |  0.98468   | 0.0492654 |             0.111576  |
|  UH091 SOUS00 GL172 La Libertad Ecuador             |  0.984523  | 0.0768821 |             0.160014  |
|  UH233 SOUS00 GL259 Lagos Nigeria                   |  0.984447  | 0.0415397 |             0.0830977 |
|  UH046 SOUS00 GL348 Port Vila Vanuatu               |  0.984443  | 0.0329891 |             0.0699212 |
|  8413320 ME Bar Harbor                              |  0.984422  | 0.127569  |             0.315213  |
|  NSTP6 SOUS43 1770000 Pago Pago American Samoa      |  0.984241  | 0.0320238 |             0.0713154 |
|  UH084 SOUS00 Lobos de Afuera Peru                  |  0.983894  | 0.043864  |             0.102014  |
|  UH231 SOUS00 GL335 Takoradi Ghana                  |  0.983853  | 0.0403053 |             0.0960181 |
|  MIC73 SOUS43 0000073 Kwajalein East (Airport) Mars |  0.983765  | 0.0400285 |             0.0915418 |
|  UH830 SOUS00 GL243 La Coruna Spain                 |  0.983694  | 0.104924  |             0.230759  |
|  UH043 SOUS00 Palmyra Island United States of Ameri |  0.983499  | 0.0222687 |             0.0540389 |
|  UH227 SOUS00 GL202 Cayenne France                  |  0.983469  | 0.0753889 |             0.185056  |
|  UH107 SOUS00 GL045 Padang Indonesia                |  0.983217  | 0.035214  |             0.0878458 |
|  UH021 SOUS00 GL176 Juan Fernandez Chile            |  0.983175  | 0.0347047 |             0.0976127 |
|  MIC74 SOUS43 0000074 Ailinglaplap East (Airport) M |  0.983039  | 0.0433627 |             0.0926229 |
|  PAC16 SOUS43 0000016 OR Lincoln City               |  0.983026  | 0.0886904 |             0.203082  |
|  MIC70 SOUS43 0000070 Utirik East (Airport) Marshal |  0.982911  | 0.039969  |             0.0868984 |
|  MIC88 SOUS43 0000088 Ebon East Marshall Islands Po |  0.982889  | 0.045068  |             0.105005  |
|  PAC21 SOUS43 0000021 OR Cannon Beach               |  0.982653  | 0.0923552 |             0.187388  |
|  8531680 NJ Sandy Hook                              |  0.982642  | 0.0542228 |             0.198314  |
|  MIC81 SOUS43 0000081 Lamotrek East Yap FSM Popula  |  0.982571  | 0.0222927 |             0.0566305 |
|  1715 USA - Cutler Farris Wharf, ME                 |  0.982533  | 0.171707  |             0.391325  |
|  9459881 AK King Cove                               |  0.982508  | 0.0731291 |             0.173025  |
|  9455500 AK Seldovia                                |  0.982464  | 0.222914  |             0.531174  |
|  MIC80 SOUS43 0000080 Ifalik East Yap FSM Populate  |  0.982431  | 0.0271225 |             0.0800325 |
|  PAC14 SOUS43 0000014 OR Beaver Creek               |  0.982239  | 0.0899535 |             0.219972  |
|  UH540 SOUS00 GL155 Prince Rupert Canada            |  0.982218  | 0.182868  |             0.471642  |
|  KWJP8 SOUS43 1820000 Kwajalein Marshall Island     |  0.982193  | 0.0419307 |             0.090164  |
|  851 USA - Crescent_City_CA                         |  0.981915  | 0.0765551 |             0.188444  |
|  UH004 SOUS00 GL114 Nauru Nauru                     |  0.981881  | 0.0472923 |             0.109728  |
|  MIC71 SOUS43 0000071 Wotje East (Airport) Marshall |  0.981837  | 0.0433288 |             0.0888712 |
|  9410660 CA Los Angeles                             |  0.98181   | 0.0537449 |             0.126058  |
|  9410665 CA Los Angeles Pier J                      |  0.981766  | 0.0537539 |             0.127974  |
|  UH834 SOUS00 GL239 Malin Head Ireland              |  0.981764  | 0.102105  |             0.256157  |
|  9419945 CA Pyramid Point Smith River               |  0.981723  | 0.078361  |             0.177873  |
|  MIC59 SOUS43 0000059 Satawal East Yap FSM Warning  |  0.981565  | 0.0220637 |             0.0467744 |
|  9439040 OR Astoria                                 |  0.981551  | 0.105835  |             0.295375  |
|  1272 Norway - Andenes                              |  0.981432  | 0.0656867 |             0.136014  |
|  MIC87 SOUS43 0000087 Ebeye Wes Marshall Islands Po |  0.981413  | 0.0424364 |             0.0917228 |
|  UH289 SOUS00 GL248 Gibraltar United Kingdom of Gre |  0.981344  | 0.0278409 |             0.0601465 |
|  WAKP8 SOUS43 1890000 Wake Island Pacific Ocean     |  0.981293  | 0.0296329 |             0.0649015 |
|  9446484 WA Tacoma                                  |  0.981231  | 0.125054  |             0.270423  |
|  9415056 CA Point Pinole                            |  0.981115  | 0.0819602 |             0.19233   |
|  9455090 AK Seward                                  |  0.981008  | 0.126481  |             0.279318  |
|  UH352 SOUS00 GL086 Mera Japan                      |  0.981001  | 0.0390742 |             0.0916323 |
|  9450460 AK Ketchikan                               |  0.980993  | 0.177247  |             0.503543  |
|  UH094 SOUS00 Matarani Peru                         |  0.980987  | 0.0380124 |             0.0759954 |
|  9439011 OR Hammond                                 |  0.980975  | 0.104605  |             0.229252  |
|  UH038 SOUS00 GL125 Nuku'alofa Tonga                |  0.980826  | 0.0518583 |             0.102553  |
|  UH820 SOUS00 GL225 Nuuk Denmark                    |  0.980604  | 0.135772  |             0.272466  |
|  8410140 ME Eastport                                |  0.980594  | 0.236877  |             0.483221  |
|  MIC78 SOUS43 0000078 Wake West Wake Island Populat |  0.980547  | 0.0297722 |             0.0661681 |
|  9414290 CA San Francisco                           |  0.980471  | 0.0713342 |             0.146153  |
|  MIC34 SOUS43 0000034 Kosrae West (Walung) Kosrae   |  0.980284  | 0.0417886 |             0.103709  |
|  9415338 CA Sonoma Creek Entrance                   |  0.980265  | 0.0850027 |             0.194496  |
|  UH035 SOUS00 GL177 San Felix Chile                 |  0.980184  | 0.0334263 |             0.0796032 |
|  UH295 SOUS00 GL238 Stornoway United Kingdom of Gre |  0.980155  | 0.13506   |             0.322602  |
|  UH353 SOUS00 GL085 Kushimoto Japan                 |  0.980101  | 0.0460513 |             0.125664  |
|  9455920 AK Anchorage                               |  0.980035  | 0.284029  |             0.909608  |
|  9447130 WA Seattle Puget Sound                     |  0.979946  | 0.122621  |             0.23955   |
|  MIC72 SOUS43 0000072 Ujae East (Airport) Marshall  |  0.979937  | 0.0424461 |             0.101694  |
|  9410666 CA Los Angeles Pier 400                    |  0.979853  | 0.0566454 |             0.140862  |
|  MIC33 SOUS43 0000033 Kosrae North (Airport) Kosrae |  0.97981   | 0.0423763 |             0.103643  |
|  MIC77 SOUS43 0000077 Wake East Wake Island Populat |  0.979806  | 0.0311141 |             0.0683176 |
|  UH419 SOUS00 Lembar Indonesia                      |  0.979782  | 0.0460967 |             0.128944  |
|  UH402 SOUS00 Lautoka Fiji                          |  0.979711  | 0.0618295 |             0.113177  |
|  MIC86 SOUS43 0000086 Ebeye East Marshall Islands P |  0.97962   | 0.044976  |             0.101408  |
|  UH257 SOUS00 GL211 Settlement Point Bahamas (the)  |  0.979572  | 0.033376  |             0.0866382 |
|  MIC36 SOUS43 0000036 Kosrae East (Malem) Kosrae F  |  0.979553  | 0.0436698 |             0.111351  |
|  9432780 OR Charleston                              |  0.979441  | 0.0919594 |             0.215953  |
|  UH417 SOUS00 Sadeng Indonesia                      |  0.979336  | 0.0675484 |             0.162152  |
|  UH104 SOUS00 GL026 Diego Garcia United Kingdom of  |  0.979242  | 0.0467479 |             0.0934778 |
|  9431647 OR Port Orford                             |  0.979105  | 0.0863393 |             0.20753   |
|  UH913 SOUS00 Telukdalam Indonesia                  |  0.979036  | 0.0282158 |             0.0634404 |
|  MIC35 SOUS43 0000035 Kosrae South (Utwa Ma) Kosrae |  0.978985  | 0.0438264 |             0.108943  |
|  UH019 SOUS00 GL123 Noumea France                   |  0.978873  | 0.0435554 |             0.0763964 |
|  8443970 MA Boston                                  |  0.978823  | 0.132088  |             0.309487  |
|  8423898 NH Fort Point                              |  0.97881   | 0.12648   |             0.314215  |
|  MIC69 SOUS43 0000069 Enewetak East Marshall Island |  0.978766  | 0.0367263 |             0.0822395 |
|  UH207 SOUS00 GL249 Ceuta Spain                     |  0.97856   | 0.0308043 |             0.0722733 |
|  9447214 WA Shilshole Bay GPS Buoy                  |  0.978402  | 0.12469   |             0.253725  |
|  UH082 SOUS00 GL182 Acajutla El Salvador            |  0.978309  | 0.0870268 |             0.182953  |
|  9414863 CA Richmond                                |  0.978294  | 0.0805547 |             0.163386  |
|  9410170 CA San Diego San Diego Bay                 |  0.97824   | 0.0611711 |             0.142682  |
|  UH155 SOUS00 GL096 Dzaoudzi France                 |  0.978222  | 0.107851  |             0.23114   |
|  UH101 SOUS00 GL008 Mombasa Kenya                   |  0.97815   | 0.101686  |             0.21746   |
|  8518750 NY The Battery                             |  0.978091  | 0.0613681 |             0.253941  |
|  9418767 CA North Spit                              |  0.977949  | 0.0827529 |             0.198859  |
|  UH016 SOUS00 GL138 Rikitea France                  |  0.97755   | 0.0281377 |             0.0613524 |
|  9411406 CA Oil Platform Harvest                    |  0.977547  | 0.0589054 |             0.132147  |
|  UH149 SOUS00 Lamu Kenya                            |  0.977489  | 0.097893  |             0.238392  |
|  9410230 CA La Jolla                                |  0.977367  | 0.0586647 |             0.132574  |
|  UH163 SOUS00 GL049 Benoa Indonesia                 |  0.976781  | 0.0874577 |             0.225208  |
|  UH113 SOUS00 Masirah Oman                          |  0.976505  | 0.0671851 |             0.153521  |
|  8418150 ME Portland                                |  0.976487  | 0.137956  |             0.355245  |
|  9435380 OR South Beach                             |  0.976448  | 0.105444  |             0.336069  |
|  9414776 CA Oakland Berth 34                        |  0.976424  | 0.0871769 |             0.19662   |
|  MIC67 SOUS43 0000067 Mokil East Pohnpei FSM Warni  |  0.97636   | 0.0389395 |             0.0898265 |
|  UH221 SOUS00 GL268 Simon's Town South Africa       |  0.976294  | 0.0525759 |             0.1338    |
|  UH034 SOUS00 GL161 Cabo San Lucas Mexico           |  0.976154  | 0.0441134 |             0.109355  |
|  UH351 SOUS00 GL087 Ofunato Japan                   |  0.976025  | 0.0427738 |             0.126879  |
|  UH789 SOUS00 Prickley Bay Grenada                  |  0.975832  | 0.0210769 |             0.0485161 |
|  9455920 Anchorage AK                               |  0.975576  | 0.315623  |             0.908812  |
|  UH181 SOUS00 GL013 Durban South Africa             |  0.975564  | 0.0626591 |             0.145896  |
|  9414958 CA Bolinas Bolinas Lagoon                  |  0.975563  | 0.0705458 |             0.16265   |
|  8519483 NY Bergen Point West Reach                 |  0.975206  | 0.0683285 |             0.251661  |
|  UH275 SOUS00 GL222 Halifax Canada                  |  0.97513   | 0.0634275 |             0.165539  |
|  MIC68 SOUS43 0000068 Pingelap East Pohnpei FSM Wa  |  0.974928  | 0.042666  |             0.106191  |
|  9414311 CA San Francisco Pier 1                    |  0.974753  | 0.0888328 |             0.197347  |
|  UH171 SOUS00 GL046 Cocos Australia                 |  0.974387  | 0.0361091 |             0.0763025 |
|  UH340 SOUS00 Kaohsiung China                       |  0.974027  | 0.033653  |             0.0694969 |
|  1664 Norway - Ny Alesund                           |  0.973995  | 0.0552047 |             0.122798  |
|  UH142 SOUS00 Langkawi Malaysia                     |  0.973925  | 0.0986212 |             0.228843  |
|  UH109 SOUS00 GL027 Gan Maldives                    |  0.97354   | 0.0358831 |             0.0706467 |
|  UH365 SOUS00 Ishigaki Japan                        |  0.97353   | 0.0574934 |             0.134484  |
|  UH317 SOUS00 Ensenada Mexico                       |  0.973448  | 0.061936  |             0.147946  |
|  9414750 CA Alameda                                 |  0.973394  | 0.0982536 |             0.21192   |
|  UH259 SOUS00 GL221 Bermuda United Kingdom of Great |  0.972748  | 0.035949  |             0.105994  |
|  UH805 SOUS00 GL323 Vardo Norway                    |  0.972601  | 0.126149  |             0.287965  |
|  UH299 SOUS00 GL344 Qaqortoq Denmark                |  0.97256   | 0.112322  |             0.2568    |
|  1612480 HI Mokuoloe                                |  0.972556  | 0.0262507 |             0.0567727 |
|  UH125 SOUS00 Prigi Indonesia                       |  0.972356  | 0.0854847 |             0.19168   |
|  UH333 SOUS00 GL057 Fort Denison Australia          |  0.97221   | 0.056475  |             0.148364  |
|  902 Japan - Ishigakijima                           |  0.97216   | 0.0582294 |             0.144771  |
|  UH382 SOUS00 Subic Bay Philippines (the)           |  0.971991  | 0.0399614 |             0.0952283 |
|  UH105 SOUS00 GL019 Rodrigues Mauritius             |  0.971821  | 0.0453109 |             0.106127  |
|  MIC30 SOUS43 0000030 Pohnpei East Pohnpei FSM Maj  |  0.971582  | 0.0398667 |             0.0930129 |
|  UH288 SOUS00 GL229 Reykjavik Iceland               |  0.971511  | 0.156069  |             0.319024  |
|  UH071 SOUS00 GL101 Wellington New Zealand          |  0.971482  | 0.0684465 |             0.202392  |
|  UH806 SOUS00 Nouakchott Mauritania                 |  0.971425  | 0.0507917 |             0.131942  |
|  UH542 SOUS00 GL156 Tofino Canada                   |  0.971389  | 0.113146  |             0.311692  |
|  UH803 SOUS00 GL234 Rorvik Norway                   |  0.971372  | 0.0947767 |             0.225673  |
|  MIC29 SOUS43 0000029 Pohnpei North Pohnpei FSM Ma  |  0.971287  | 0.0385044 |             0.0849517 |
|  UH153 SOUS00 GL029 Minicoy India                   |  0.971284  | 0.0379243 |             0.0953884 |
|  9415102 CA Martinez-Amorco Pier                    |  0.970888  | 0.119982  |             0.304666  |
|  9416409 CA GREEN COVE PACIFIC OCEAN                |  0.970231  | 0.0790854 |             0.168524  |
|  UH370 SOUS00 GL073 Manila Philippines (the)        |  0.970116  | 0.0460875 |             0.124255  |
|  9457804 AK Alitak                                  |  0.970037  | 0.173093  |             0.456719  |
|  9414575 CA Coyote Creek                            |  0.96963   | 0.13584   |             0.336003  |
|  MIC66 SOUS43 0000066 Pakin East Pohnpei FSM Warni  |  0.969494  | 0.0378776 |             0.0864004 |
|  9415020 CA Point Reyes                             |  0.969017  | 0.0793547 |             0.176345  |
|  UH093 SOUS00 GL173 Callao Peru                     |  0.968908  | 0.0415326 |             0.0907244 |
|  UH147 SOUS00 GL030 Karachi Pakistan                |  0.968609  | 0.0947308 |             0.205494  |
|  UH179 SOUS00 GL024 Saint Paul France               |  0.968502  | 0.0545776 |             0.156936  |
|  MIC31 SOUS43 0000031 Pohnpei South Pohnpei FSM Ma  |  0.968404  | 0.0410416 |             0.0992962 |
|  MIC32 SOUS43 0000032 Pohnpei West Pohnpei FSM Maj  |  0.968332  | 0.0390086 |             0.0901108 |
|  UH023 SOUS00 GL139 Rarotonga Cook Islands (the)    |  0.968016  | 0.0376991 |             0.0905305 |
|  UH777 SOUS00 Puerto Plata Dominican Republic (the) |  0.967839  | 0.024745  |             0.0638645 |
|  UH108 SOUS00 GL028 Male Maldives                   |  0.967021  | 0.0346184 |             0.0722513 |
|  9444900 WA Port Townsend                           |  0.966912  | 0.118403  |             0.228512  |
|  UH114 SOUS00 GL004 Salalah Oman                    |  0.966455  | 0.0562715 |             0.127113  |
|  MIC08 SOUS43 0000008 Pohnpei FSM UHSLC Gauge       |  0.96637   | 0.0415375 |             0.0879314 |
|  UH799 SOUS00 GL209 Portu-Prince Haiti              |  0.966142  | 0.0188325 |             0.0455197 |
|  878 USA - Fort_Pulaski_GA                          |  0.965952  | 0.104178  |             0.2709    |
|  8658163 NC Wrightsville Beach                      |  0.965883  | 0.0639449 |             0.16094   |
|  8467150 CT Bridgeport                              |  0.965646  | 0.121109  |             0.276257  |
|  MIC65 SOUS43 0000065 Sapwuafik (Ngatik) East Pohnp |  0.965512  | 0.0411094 |             0.0903196 |
|  1586 New Zealand - Christchurch                    |  0.965314  | 0.124294  |             0.340973  |
|  UH162 SOUS00 GL291 Cilicap Indonesia               |  0.965007  | 0.0774626 |             0.187646  |
|  UH822 SOUS00 GL242 Brest France                    |  0.964388  | 0.274158  |             0.571827  |
|  UH173 SOUS00 GL277 Davis Australia                 |  0.963923  | 0.0609422 |             0.119076  |
|  8722670 FL Lake Worth Pier Atlantic                |  0.963621  | 0.0450041 |             0.136306  |
|  9415144 CA Port Chicago                            |  0.963611  | 0.143185  |             0.379597  |
|  UH009 SOUS00 GL066 Honiara Solomon Islands         |  0.963354  | 0.0335449 |             0.0874565 |
|  UH117 SOUS00 Hanimaadhoo Maldives                  |  0.963262  | 0.0383565 |             0.0856055 |
|  1611400 HI Nawiliwili                              |  0.962341  | 0.0277977 |             0.0717601 |
|  UH878 SOUS00 Bullen Bay Curacao                    |  0.962237  | 0.0145733 |             0.0343738 |
|  8461490 CT New London                              |  0.96223   | 0.0508052 |             0.143799  |
|  UH261 SOUS00 Charleston SC United States of Ameri  |  0.961124  | 0.0862972 |             0.218308  |
|  9464212 St Paul Island AK                          |  0.961013  | 0.0693617 |             0.140708  |
|  MIC82 SOUS43 0000082 Oroluk East Pohnpei FSM Popu  |  0.95969   | 0.0376658 |             0.0753452 |
|  9449880 WA Friday Harbor                           |  0.959613  | 0.117944  |             0.258602  |
|  8665530 SC Charleston Cooper River E               |  0.959455  | 0.0882131 |             0.265742  |
|  8724580 FL Key West                                |  0.958375  | 0.028865  |             0.0651886 |
|  9462450 AK Nikolski                                |  0.958356  | 0.0839691 |             0.181529  |
|  9461380 AK Adak Island                             |  0.957877  | 0.0734235 |             0.17473   |
|  UH052 SOUS00 GL109 Johnston United States of Ameri |  0.957574  | 0.0338051 |             0.0764363 |
|  UH041 SOUS00 GL102 Dutch Harbor AK United States   |  0.957559  | 0.0863645 |             0.183478  |
|  UH654 SOUS00 Currimao Philippines (the)            |  0.957149  | 0.0345735 |             0.0628969 |
|  UH166 SOUS00 GL040 Broome Australia                |  0.956922  | 0.47676   |             0.892256  |
|  9752619 PR Isabel Segunda Vieques Is               |  0.955934  | 0.016535  |             0.0417419 |
|  UH738 SOUS00 Santa Marta Colombia                  |  0.955603  | 0.0155029 |             0.0478337 |
|  9461380 Adak Island AK                             |  0.955416  | 0.0755418 |             0.159148  |
|  UH286 SOUS00 GL190 Puerto Deseado Argentina        |  0.954924  | 0.292376  |             0.665834  |
|  8452944 RI Conimicut Light                         |  0.954778  | 0.0668611 |             0.150106  |
|  UH276 SOUS00 GL223 St. John's Canada               |  0.954757  | 0.0726011 |             0.141958  |
|  9440569 WA Skamokawa                               |  0.954643  | 0.131099  |             0.276545  |
|  8725110 FL Naples Gulf of Mexico                   |  0.954642  | 0.0463364 |             0.101122  |
|  8723214 FL Virginia Key                            |  0.953971  | 0.041337  |             0.0984367 |
|  9461710 AK Atka                                    |  0.953834  | 0.0738078 |             0.188362  |
|  UH273 SOUS00 Port-aux-basques Canada               |  0.953514  | 0.0646822 |             0.173604  |
|  8537121 NJ Ship John Shoal                         |  0.953478  | 0.114865  |             0.323615  |
|  1617433 HI Kawaihae                                |  0.952792  | 0.0349469 |             0.0875554 |
|  UH808 SOUS00 GL343 Thule (Pituffik) Denmark        |  0.952559  | 0.117947  |             0.269407  |
|  9465261 Nushagak Bay                               |  0.951623  | 0.366666  |             0.867161  |
|  8727520 FL Cedar Key                               |  0.951392  | 0.0801813 |             0.194084  |
|  UH294 SOUS00 GL241 Newlyn Cornwall United Kingdom  |  0.951162  | 0.25879   |             0.560365  |
|  UH130 SOUS00 GL278 Casey Australia                 |  0.951116  | 0.0722257 |             0.162893  |
|  UH121 SOUS00 GL339 Pt. La Rue Seychelles           |  0.951053  | 0.058754  |             0.13827   |
|  UH271 SOUS00 Fort de France France                 |  0.950952  | 0.018828  |             0.0399189 |
|  UH335 SOUS00 GL056 Spring Bay Australia            |  0.950146  | 0.0663063 |             0.128834  |
|  MIC62 SOUS43 0000062 Fananu East Chuuk FSM Warnin  |  0.949552  | 0.0334784 |             0.0665519 |
|  MIC26 SOUS43 0000026 Chuuk Lagoon East Chuuk FSM   |  0.949275  | 0.034411  |             0.0715261 |
|  UH103 SOUS00 GL018 Port Louis Mauritius            |  0.949173  | 0.0236082 |             0.0557107 |
|  9759938 PR Mona Island                             |  0.948909  | 0.0140858 |             0.0341598 |
|  UH164 SOUS00 GL017 Reunion France                  |  0.948734  | 0.0194378 |             0.04926   |
|  8454000 RI Providence                              |  0.948646  | 0.0741062 |             0.159141  |
|  UH184 SOUS00 GL076 Port Elizabeth South Africa     |  0.948377  | 0.0830965 |             0.178226  |
|  UH029 SOUS00 GL117 Kapingamarangi Micronesia (Fede |  0.948005  | 0.04348   |             0.0825208 |
|  UH824 SOUS00 GL205 Marseille France                |  0.947963  | 0.0137251 |             0.0344552 |
|  UH316 SOUS00 GL267 Acapulco Gro. Mexico            |  0.947674  | 0.0441204 |             0.112326  |
|  8551910 DE Reedy Point                             |  0.947421  | 0.12081   |             0.323522  |
|  UH047 SOUS00 GL103 Chichijima Japan                |  0.946464  | 0.0430306 |             0.106076  |
|  8454049 RI Quonset Point                           |  0.946383  | 0.0676723 |             0.187733  |
|  UH600 SOUS00 GL181 Ushuaia Argentina               |  0.945828  | 0.11826   |             0.257276  |
|  MIC63 SOUS43 0000063 Losap East Chuuk FSM Warning  |  0.94564   | 0.0364649 |             0.0728526 |
|  UH049 SOUS00 GL104 Minamitorishima Japan           |  0.94548   | 0.0281373 |             0.0853954 |
|  8721604 FL Trident Pier Port Canaver               |  0.94534   | 0.068659  |             0.194999  |
|  1612340 HI Honolulu                                |  0.944754  | 0.0344361 |             0.0757181 |
|  MIC64 SOUS43 0000064 Lukunor East Chuuk FSM Warni  |  0.94472   | 0.0406043 |             0.0800353 |
|  UH350 SOUS00 GL089 Kushiro Japan                   |  0.944184  | 0.0654407 |             0.155052  |
|  UH119 SOUS00 GL002 Djibouti Djibouti               |  0.944111  | 0.0941601 |             0.172507  |
|  UH122 SOUS00 Sibolga Indonesia                     |  0.943858  | 0.053287  |             0.147461  |
|  8726607 FL Old Port Tampa                          |  0.943821  | 0.0430042 |             0.101285  |
|  UH334 SOUS00 GL060 Townsville Australia            |  0.94376   | 0.118425  |             0.299741  |
|  9759394 PR Mayaguez                                |  0.943758  | 0.0194872 |             0.0438972 |
|  MIC10 SOUS43 0000010 Moen I Chuuk FSM Historic CO  |  0.943528  | 0.035271  |             0.0702067 |
|  UH906 SOUS00 GL141 Moulmein Myanmar                |  0.94328   | 0.32046   |             0.788405  |
|  9752695 PR Esperanza Vieques Island                |  0.943039  | 0.0140207 |             0.0393288 |
|  UH180 SOUS00 GL023 Kerguelen France                |  0.943012  | 0.0882378 |             0.241834  |
|  8551762 DE Delaware City                           |  0.941559  | 0.128978  |             0.383566  |
|  9751381 VI Lameshur Bay St John                    |  0.941396  | 0.0144515 |             0.0277355 |
|  UH364 SOUS00 GL088 Hakodate Japan                  |  0.940674  | 0.041291  |             0.115675  |
|  MIC27 SOUS43 0000027 Chuuk Lagoon North Chuuk FSM  |  0.940585  | 0.035805  |             0.0783798 |
|  UH024 SOUS00 GL143 Penrhyn Cook Islands (the)      |  0.940581  | 0.0152189 |             0.0329754 |
|  UH699 SOUS00 GL044 Tanjong Pagar Singapore         |  0.939957  | 0.118456  |             0.255068  |
|  UH115 SOUS00 GL033 Colombo Sri Lanka               |  0.938721  | 0.0379254 |             0.0745064 |
|  UH680 SOUS00 GL130 Macquarie Is. Australia         |  0.936731  | 0.0785326 |             0.153648  |
|  8760922 LA Pilots Station East S.W.                |  0.936547  | 0.028078  |             0.0572541 |
|  8775870 TX Bob Hall Pier Corpus Chri               |  0.93638   | 0.0329447 |             0.0823014 |
|  UH189 SOUS00 GL131 Dumont d'Urville Antarctica     |  0.935869  | 0.0829257 |             0.230938  |
|  UH547 SOUS00 Barbers Point HI United States of Am  |  0.934704  | 0.0362435 |             0.0859673 |
|  UH836 SOUS00 GL333 Alert Canada                    |  0.934488  | 0.0456817 |             0.125644  |
|  UH601 SOUS00 GL185 Esperanza Argentina             |  0.934401  | 0.142281  |             0.336952  |
|  UH129 SOUS00 GL055 Portland S.Aus. Australia       |  0.932783  | 0.0633502 |             0.136875  |
|  UH833 SOUS00 GL224 Nain Canada                     |  0.9323    | 0.140522  |             0.30468   |
|  MIC28 SOUS43 0000028 Chuuk Lagoon West Chuuk FSM   |  0.931396  | 0.0372877 |             0.0790881 |
|  MIC60 SOUS43 0000060 Puluwat East Chuuk FSM Warni  |  0.930634  | 0.0365015 |             0.0824356 |
|  8539094 NJ Burlington Delaware River               |  0.930415  | 0.156738  |             0.404619  |
|  MIC61 SOUS43 0000061 Ulul East Chuuk FSM Warning   |  0.930064  | 0.035474  |             0.072825  |
|  UH290 SOUS00 GL305 Port Stanley United Kingdom of  |  0.929949  | 0.0831711 |             0.179065  |
|  8656483 NC Beaufort Duke Marine Lab                |  0.929821  | 0.0860285 |             0.213488  |
|  1619910 HI Sand Island Midway Island               |  0.928633  | 0.0278624 |             0.0702097 |
|  UH079 SOUS00 GL128 Chatham New Zealand             |  0.927773  | 0.0741448 |             0.172874  |
|  8449130 MA Nantucket Island                        |  0.927644  | 0.0897393 |             0.246332  |
|  9754228 PR Yabucoa Harbor                          |  0.927493  | 0.0157577 |             0.0399798 |
|  UH331 SOUS00 GL058 Brisbane Australia              |  0.925955  | 0.142207  |             0.390934  |
|  UH177 SOUS00 GL022 Mawson Australia                |  0.925568  | 0.0595005 |             0.114425  |
|  UH347 SOUS00 GL327 Abashiri Japan                  |  0.924098  | 0.0643341 |             0.157694  |
|  9465601 Carter Bay Kuskokwim Bay AK                |  0.92323   | 0.265441  |             0.630922  |
|  8536110 NJ Cape May                                |  0.921968  | 0.122471  |             0.287691  |
|  8658120 NC Wilmington                              |  0.921059  | 0.110806  |             0.331016  |
|  UH383 SOUS00 Vung Tau Viet Nam                     |  0.920617  | 0.181255  |             0.429261  |
|  9758053 PR Penuelas                                |  0.919803  | 0.0164544 |             0.0351325 |
|  UH220 SOUS00 GL314 Walvis Bay Namibia              |  0.916659  | 0.0881399 |             0.22251   |
|  1336 Norway - Maloy                                |  0.915552  | 0.117141  |             0.251581  |
|  8726667 FL Mckay Bay Entrance                      |  0.914092  | 0.0551834 |             0.115185  |
|  8720218 FL Mayport (Bar Pilots Dock)               |  0.911321  | 0.129226  |             0.312856  |
|  UH015 SOUS00 GL140 Papeete France                  |  0.907206  | 0.0151766 |             0.0451938 |
|  8548989 PA Newbold                                 |  0.906874  | 0.193488  |             0.506786  |
|  9465374 Snag Point Dillingham AK                   |  0.906766  | 0.518235  |             1.31481   |
|  8779748 TX South Padre Island CG Stat              |  0.906597  | 0.0346356 |             0.0752872 |
|  8538886 NJ Tacony-Palmyra Bridge                   |  0.90615   | 0.169393  |             0.464855  |
|  9759110 PR Magueyes Island                         |  0.904713  | 0.0179581 |             0.0439448 |
|  8726384 FL Port Manatee                            |  0.904283  | 0.050898  |             0.118281  |
|  8540433 PA Marcus Hook                             |  0.90387   | 0.16383   |             0.421144  |
|  UH920 SOUS00 GL020 Marion Island South Africa      |  0.896864  | 0.0553103 |             0.126336  |
|  UH266 SOUS00 GL208 Cristobal Panama                |  0.896457  | 0.0253859 |             0.0509747 |
|  8573927 MD Chesapeake City                         |  0.893831  | 0.08592   |             0.289132  |
|  8545240 PA Philadelphia                            |  0.890995  | 0.175827  |             0.532095  |
|  9761115 Barbuda                                    |  0.890201  | 0.0192593 |             0.045573  |
|  8570283 MD Ocean City Inlet                        |  0.888455  | 0.0862223 |             0.158973  |
|  UH737 SOUS00 San Andres Colombia                   |  0.883193  | 0.0246568 |             0.0586008 |
|  8723970 FL Vaca Key Florida Bay                    |  0.8777    | 0.0379982 |             0.103525  |
|  UH829 SOUS00 GL340 Trieste Italy                   |  0.877312  | 0.0883501 |             0.18599   |
|  UH700 SOUS00 GL188 Faraday Antarctica              |  0.874397  | 0.118254  |             0.237987  |
|  UH268 SOUS00 Limon Costa Rica                      |  0.870342  | 0.0293418 |             0.0656553 |
|  8729210 FL Panama City Beach                       |  0.865844  | 0.043771  |             0.108738  |
|  8510560 NY Montauk                                 |  0.862519  | 0.0683838 |             0.185919  |
|  8729108 FL Panama City                             |  0.856948  | 0.046615  |             0.124735  |
|  8720030 FL Fernandina Beach                        |  0.853582  | 0.187029  |             0.436002  |
|  8447930 MA Woods Hole                              |  0.847785  | 0.0526351 |             0.140368  |
|  UH128 SOUS00 GL308 Thevenard Australia             |  0.840074  | 0.139983  |             0.337452  |
|  8735391 AL Dog River Bridge                        |  0.83993   | 0.052979  |             0.108709  |
|  UH175 SOUS00 GL053 Fremantle Australia             |  0.839416  | 0.05225   |             0.122507  |
|  8770777 TX Manchester                              |  0.838002  | 0.0524054 |             0.117665  |
|  8571892 MD Cambridge                               |  0.834083  | 0.07136   |             0.206127  |
|  1019 Australia - Thevenard_AU                      |  0.833252  | 0.142998  |             0.367398  |
|  UH349 SOUS00 GL325 Toyama Japan                    |  0.827515  | 0.0274261 |             0.0558222 |
|  UH280 SOUS00 GL195 Ilha Fiscal RJ Brazil           |  0.815925  | 0.0863272 |             0.212069  |
|  8637689 VA Yorktown USCG Training Cen              |  0.812268  | 0.0973529 |             0.206159  |
|  8770520 TX Rainbow Bridge                          |  0.80807   | 0.0318573 |             0.0873401 |
|  8651370 NC Duck                                    |  0.801496  | 0.125871  |             0.250283  |
|  UH178 SOUS00 GL021 Crozet France                   |  0.800114  | 0.0562544 |             0.141757  |
|  8737048 AL Mobile State Docks                      |  0.790721  | 0.0625336 |             0.144696  |
|  8594900 DC Washington                              |  0.781143  | 0.112834  |             0.25636   |
|  8760721 LA Pilottown                               |  0.779564  | 0.0233188 |             0.0402106 |
|  8632200 VA Kiptopeke                               |  0.777033  | 0.112328  |             0.222254  |
|  UH360 SOUS00 GL324 Wakkanai Japan                  |  0.775609  | 0.0380189 |             0.0739303 |
|  8639348 VA Money Point                             |  0.770872  | 0.118854  |             0.246878  |
|  8764044 LA Berwick Atchafalaya River               |  0.765151  | 0.0439019 |             0.0800796 |
|  8574680 MD Baltimore Fort McHenry P                |  0.763847  | 0.0641749 |             0.164844  |
|  8771013 TX Eagle Point Galveston Bay               |  0.75643   | 0.051561  |             0.134662  |
|  UH731 SOUS00 GL191 Puerto Madryn Argentina         |  0.74735   | 1.66868   |             6.12639   |
|  8774770 TX Rockport                                |  0.743982  | 0.0158114 |             0.0374214 |
|  8638863 VA Chesapeake Bay Bridge Tunn              |  0.740103  | 0.122383  |             0.237639  |
|  8638610 VA Sewells Point                           |  0.72564   | 0.120086  |             0.267487  |
|  8764227 LA LAWMA Amerada Pass                      |  0.720779  | 0.0615912 |             0.117171  |
|  8770822 TX Texas Point Sabine Pass                 |  0.68294   | 0.0974538 |             0.258455  |
|  8747437 MS Bay Waveland Yacht Club                 |  0.660143  | 0.0687109 |             0.17694   |
|  UH176 SOUS00 GL054 Esperance Australia             |  0.658726  | 0.0904388 |             0.205861  |
|  9468132 St. Michael                                |  0.644142  | 0.248471  |             0.706204  |
|  8770475 TX Port Arthur                             |  0.642993  | 0.0520659 |             0.140123  |
|  8774513 TX Copano Bay                              |  0.633856  | 0.0212895 |             0.0489975 |
|  8573364 MD Tolchester Beach                        |  0.62082   | 0.0866567 |             0.194178  |
|  8571421 MD Bishops Head                            |  0.614511  | 0.115468  |             0.283428  |
|  8762075 LA Port Fourchon Belle Pass                |  0.592576  | 0.0555759 |             0.189264  |
|  8662245 SC Oyster Landing (N Inlet Es              |  0.576629  | 0.157112  |             0.357621  |
|  UH825 SOUS00 GL284 Cuxhaven Germany                |  0.569698  | 0.562648  |             1.24863   |
|  8577330 MD Solomons Island                         |  0.558034  | 0.0810861 |             0.201699  |
|  8635750 VA Lewisetta                               |  0.505694  | 0.0828027 |             0.194161  |
|  UH348 SOUS00 GL326 Hamada Japan                    |  0.497903  | 0.0623868 |             0.151599  |
|  8771341 TX Galveston Bay Entrance No               |  0.465002  | 0.111652  |             0.196611  |
|  9468333 Unalakleet AK                              |  0.463347  | 0.332288  |             0.895716  |
|  UH729 SOUS00 GL192 Mar del Plata Argentina         |  0.409461  | 0.347458  |             0.711112  |
|  9497645 Prudhoe Bay AK                             |  0.388157  | 0.102342  |             0.236873  |
|  8775283 TX Port Inglesid                           |  0.380009  | 0.0368786 |             0.0776943 |
|  9468756 Nome AK                                    |  0.378731  | 0.178913  |             0.406764  |
|  UH579 SOUS00 GL151 Prudhoe Bay AK United States o  |  0.355552  | 0.104958  |             0.240305  |
|  8636580 VA Windmill Point                          |  0.340172  | 0.0841194 |             0.161206  |
|  952 USA - Nome_AK                                  |  0.301555  | 0.19017   |             0.454081  |
|  8761305 LA Shell Beach                             |  0.238293  | 0.112071  |             0.239304  |
|  8654467 NC USCG Station Hatteras                   |  0.122081  | 0.0468441 |             0.105868  |
|  UH818 SOUS00 Smogen Sweden                         | -0.0778119 | 0.0909147 |             0.168152  |
|  9491094 Red Dog Dock AK                            | -0.112822  | 0.24201   |             0.499538  |
|  UH804 SOUS00 GL321 Tregde Norway                   | -0.447084  | 0.0940719 |             0.144767  |
|  8652587 NC Oregon Inlet Marina                     | -0.484778  | 0.152087  |             0.44708   |
|  UH819 SOUS00 GL233 Goteborgorsh. Sweden            | -0.789158  | 0.0953753 |             0.195621  |
|  8761927 LA New Canal Station                       | -0.861716  | 0.101232  |             0.250843  |
|  UH826 SOUS00 GL341 Stockholm Sweden                | -2.33938   | 0.0654806 |             0.189491  |

### Disclaimer
This program is under experimental development. The results should not be used for navigational purposes or emergency planning under any circumstances. Please do not duplicate and use the result figures from this website without permission.
