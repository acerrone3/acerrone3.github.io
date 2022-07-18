## GESTOFS-ML
This is a sister project of [GESTOFS](https://gm-ling.github.io/GESTOFS-develop/).  GESTOFS is an ADCIRC-based storm surge forecasting system for the whole globe.  GESTOFS-ML expands on this theme, but in addition to ADCIRC, it leverages a time-series forecasting ML model complete with meteorological forcing to enrich the prediction of surface water elevation.

### Site URL
[https://acerrone3.github.io/](https://acerrone3.github.io/)

### Latest Forecasts
Updated July 18, 2022

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
Updated July 18, 2022

Here, the ADCIRC forecasts are compared to the ML forecasts.  Comparisons are arranged in descending order based on each station's r-squared value.  Observational data has yet to be integrated for performance assessment.

|  Station                                            |         R2 |      RMSD |   Max Discrepancy (m) |
| :---------------------------------------------------|-----------:|----------:|----------------------:|
|  UH081 SOUS00 GL175 Valparaiso Chile                |  0.994966  | 0.0214822 |             0.0561576 |
|  UH816 SOUS00 GL350 Port Sonara Cameroon            |  0.993399  | 0.0232706 |             0.0589652 |
|  UH030 SOUS00 Santa Cruz Ecuador                    |  0.993395  | 0.0366273 |             0.0917134 |
|  UH403 SOUS00 Jackson New Zealand                   |  0.993091  | 0.0453807 |             0.101249  |
|  MIC22 SOUS43 0000022 Yap East Yap FSM Major Islan  |  0.992961  | 0.0244575 |             0.0680759 |
|  UH392 SOUS00 Cocos Island Costa Rica               |  0.992819  | 0.0579988 |             0.116318  |
|  MIC53 SOUS43 0000053 Ngulu West Yap FSM Warning P  |  0.992674  | 0.0267182 |             0.0601272 |
|  UH209 SOUS00 GL246 Cascais Portugal                |  0.992389  | 0.0524021 |             0.105194  |
|  MIC25 SOUS43 0000025 Yap North Yap FSM Major Isla  |  0.992364  | 0.0255807 |             0.0602394 |
|  MIC43 SOUS43 0000043 Kayangel North Palau Warning  |  0.992321  | 0.0295553 |             0.060248  |
|  UH092 SOUS00 Talara Peru                           |  0.992241  | 0.0367042 |             0.0856873 |
|  9455760 AK Nikiski                                 |  0.992222  | 0.151894  |             0.430771  |
|  UH088 SOUS00 Caldera Chile                         |  0.992219  | 0.025184  |             0.0562425 |
|  MIC07 SOUS43 0000007 Yap FSM UHSLC Gauge           |  0.991876  | 0.026586  |             0.0631935 |
|  MIC44 SOUS43 0000044 Peleliu East Palau Warning Po |  0.991851  | 0.0319213 |             0.0751176 |
|  MIC54 SOUS43 0000054 Ngulu East Yap FSM Warning P  |  0.991767  | 0.0278405 |             0.0672247 |
|  MIC24 SOUS43 0000024 Yap West (Airport) Yap FSM M  |  0.991744  | 0.0274932 |             0.0704904 |
|  MIC21 SOUS43 0000021 Ngeremlengui West Palau Major |  0.991723  | 0.0323617 |             0.0667121 |
|  MIC48 SOUS43 0000048 Angaur South Palau Warning Po |  0.991662  | 0.0318811 |             0.0722973 |
|  MIC20 SOUS43 0000020 East Melekeok Palau Major Isl |  0.991599  | 0.0305394 |             0.0675064 |
|  MIC06 SOUS43 0000006 Malakal Palau UHSLC Gauge     |  0.991569  | 0.0329061 |             0.0747229 |
|  UH091 SOUS00 GL172 La Libertad Ecuador             |  0.991257  | 0.0525363 |             0.112492  |
|  MIC47 SOUS43 0000047 Angaur West Palau Warning Poi |  0.991225  | 0.0329809 |             0.0767036 |
|  MIC46 SOUS43 0000046 Angaur East Palau Warning Poi |  0.99117   | 0.0326683 |             0.0753061 |
|  MIC45 SOUS43 0000045 Peleliu West Palau Warning Po |  0.990989  | 0.0335001 |             0.0808158 |
|  PAC22 SOUS43 0000022 OR Seaside                    |  0.990932  | 0.0641251 |             0.14117   |
|  UH362 SOUS00 GL083 Nagasaki Japan                  |  0.990912  | 0.0512287 |             0.121112  |
|  UH218 SOUS00 GL250 Funchal Portugal                |  0.990802  | 0.0410682 |             0.104513  |
|  9454240 AK Valdez                                  |  0.990796  | 0.0928724 |             0.228284  |
|  UH118 SOUS00 Ko Miang Thailand                     |  0.990774  | 0.0394604 |             0.0828527 |
|  MIC23 SOUS43 0000023 Yap South (Colonia) Yap FSM   |  0.990599  | 0.0284241 |             0.0650139 |
|  PAC24 SOUS43 0000024 WA Long Beach                 |  0.990444  | 0.065767  |             0.148598  |
|  UH908 SOUS00 GL038 Port Blair India                |  0.990275  | 0.0369877 |             0.077873  |
|  MIC55 SOUS43 0000055 Ulithi East (Airport) Yap FS  |  0.990214  | 0.0264867 |             0.0719991 |
|  UH302 SOUS00 GL168 Balboa Panama                   |  0.989881  | 0.129162  |             0.294382  |
|  9454050 AK Cordova                                 |  0.989851  | 0.0972735 |             0.246575  |
|  9455090 AK Seward                                  |  0.989728  | 0.0862356 |             0.199782  |
|  UH289 SOUS00 GL248 Gibraltar United Kingdom of Gre |  0.989627  | 0.0182927 |             0.0487015 |
|  UH123 SOUS00 GL347 Sabang Indonesia                |  0.989582  | 0.0276479 |             0.0675437 |
|  PAC21 SOUS43 0000021 OR Cannon Beach               |  0.989534  | 0.0683748 |             0.144556  |
|  851 USA - Crescent_City_CA                         |  0.989432  | 0.0564504 |             0.125647  |
|  9419945 CA Pyramid Point Smith River               |  0.989369  | 0.0576476 |             0.129106  |
|  UH227 SOUS00 GL202 Cayenne France                  |  0.989242  | 0.0541979 |             0.135922  |
|  UH207 SOUS00 GL249 Ceuta Spain                     |  0.98923   | 0.0192106 |             0.0522306 |
|  UH541 SOUS00 Bamfield Canada                       |  0.988949  | 0.0721285 |             0.150459  |
|  9452634 AK Elfin Cove                              |  0.988806  | 0.0917451 |             0.210052  |
|  9459450 AK Sand Point                              |  0.988719  | 0.0594119 |             0.17056   |
|  MIC12 SOUS43 0000012 Guam North (Ritidian) Guam M  |  0.988714  | 0.0180728 |             0.0518533 |
|  MIC49 SOUS43 0000049 Sonsorol Northeast Palau Warn |  0.988615  | 0.0388316 |             0.0946265 |
|  MIC52 SOUS43 0000052 Sonsorol Southwest Palau Warn |  0.988489  | 0.0388329 |             0.0867727 |
|  PAC17 SOUS43 0000017 OR Neskowin Beach             |  0.988448  | 0.070031  |             0.153883  |
|  UH291 SOUS00 GL263 Ascension United Kingdom of Gre |  0.988354  | 0.0216496 |             0.0472335 |
|  UH354 SOUS00 GL082 Aburatsu Japan                  |  0.9883    | 0.0353266 |             0.101215  |
|  PAC18 SOUS43 0000018 OR Pacific City               |  0.988292  | 0.0705719 |             0.147314  |
|  MIC51 SOUS43 0000051 Sonsorol Northwest Palau Warn |  0.988214  | 0.0395908 |             0.101315  |
|  MIC39 SOUS43 0000039 Majuro West Marshall Islands  |  0.98815   | 0.0313659 |             0.0769297 |
|  MIC50 SOUS43 0000050 Sonsorol Southeast Palau Warn |  0.988143  | 0.0392897 |             0.0919208 |
|  UH233 SOUS00 GL259 Lagos Nigeria                   |  0.988112  | 0.0324597 |             0.0715416 |
|  MIC56 SOUS43 0000056 Fais East(Airport) Yap FSM W  |  0.988028  | 0.0274503 |             0.0649458 |
|  UH365 SOUS00 Ishigaki Japan                        |  0.987916  | 0.0346837 |             0.0840614 |
|  MIC76 SOUS43 0000076 Mili East Marshall Islands Wa |  0.987898  | 0.0328029 |             0.0702007 |
|  UH333 SOUS00 GL057 Fort Denison Australia          |  0.987862  | 0.0339167 |             0.06834   |
|  UH017 SOUS00 Hiva Oa France                        |  0.98786   | 0.0389576 |             0.0796606 |
|  9451600 AK Sitka                                   |  0.987724  | 0.0883518 |             0.213177  |
|  1497 Korea - Busan                                 |  0.987675  | 0.0318862 |             0.0823449 |
|  MIC90 SOUS43 0000090 62 Km ENE from Helen Reef (-2 |  0.987551  | 0.0402861 |             0.0966204 |
|  UH223 SOUS00 GL253 Dakar Senegal                   |  0.987526  | 0.0306649 |             0.0584891 |
|  UH025 SOUS00 GL121 Funafuti Tuvalu                 |  0.987454  | 0.0348088 |             0.0948989 |
|  UH830 SOUS00 GL243 La Coruna Spain                 |  0.987271  | 0.0822963 |             0.159806  |
|  UH084 SOUS00 Lobos de Afuera Peru                  |  0.987249  | 0.0351653 |             0.0873729 |
|  UH013 SOUS00 GL145 Kanton Kiribati                 |  0.987213  | 0.0248826 |             0.0711725 |
|  MIC40 SOUS43 0000040 Majuro North Marshall Islands |  0.987158  | 0.0325791 |             0.0778296 |
|  UH046 SOUS00 GL348 Port Vila Vanuatu               |  0.987154  | 0.028448  |             0.0828504 |
|  9451600 Sitka AK                                   |  0.987152  | 0.0903922 |             0.201347  |
|  1272 Norway - Andenes                              |  0.987111  | 0.0482692 |             0.109781  |
|  UH002 SOUS00 GL113 Tarawa Bairiki Kiribati         |  0.987093  | 0.0355651 |             0.101526  |
|  MIC38 SOUS43 0000038 Majuro South (Airport) Marsha |  0.987065  | 0.0331449 |             0.075091  |
|  PAC16 SOUS43 0000016 OR Lincoln City               |  0.986975  | 0.0743455 |             0.168164  |
|  9455500 AK Seldovia                                |  0.986938  | 0.174456  |             0.366646  |
|  UH011 SOUS00 GL146 Christmas Kiribati              |  0.986909  | 0.0187709 |             0.0408347 |
|  902 Japan - Ishigakijima                           |  0.986814  | 0.0357977 |             0.0835109 |
|  UH283 SOUS00 GL336 Fortaleza Brazil                |  0.986745  | 0.061726  |             0.167467  |
|  APRP7 SOUS43 1630000 Apra HarborGuam               |  0.986627  | 0.0210694 |             0.0570626 |
|  UH789 SOUS00 Prickley Bay Grenada                  |  0.986576  | 0.0145512 |             0.0360048 |
|  UH031 SOUS00 GL142 Nuku Hiva France                |  0.986444  | 0.0397697 |             0.0791358 |
|  MIC89 SOUS43 0000089 Arno East Marshall Islands Po |  0.986248  | 0.0340569 |             0.0781158 |
|  9451054 AK Port Alexander                          |  0.985988  | 0.106805  |             0.244545  |
|  UH157 SOUS00 GL035 Vishakhapatnam India            |  0.985889  | 0.0302298 |             0.0761592 |
|  UH345 SOUS00 Nakano Shima Japan                    |  0.985869  | 0.0447049 |             0.118216  |
|  UH231 SOUS00 GL335 Takoradi Ghana                  |  0.985794  | 0.0337627 |             0.0927984 |
|  PAC14 SOUS43 0000014 OR Beaver Creek               |  0.985701  | 0.0774321 |             0.17397   |
|  9439011 OR Hammond                                 |  0.985683  | 0.0863455 |             0.278833  |
|  UH288 SOUS00 GL229 Reykjavik Iceland               |  0.985425  | 0.0983783 |             0.210219  |
|  UH356 SOUS00 Maisaka Japan                         |  0.985406  | 0.0339239 |             0.0973585 |
|  MIC37 SOUS43 0000037 Majuro East Marshall Islands  |  0.985284  | 0.0352685 |             0.083153  |
|  UH043 SOUS00 Palmyra Island United States of Ameri |  0.985243  | 0.0188601 |             0.0446115 |
|  UH021 SOUS00 GL176 Juan Fernandez Chile            |  0.98516   | 0.0290153 |             0.0759865 |
|  MIC14 SOUS43 0000014 Rota West (Songsong) Rota Ma  |  0.985154  | 0.0200946 |             0.0543098 |
|  9453220 Yakutat Bay AK                             |  0.985104  | 0.0983983 |             0.213673  |
|  9452400 Skagway AK                                 |  0.98488   | 0.18011   |             0.362816  |
|  9443090 WA Neah Bay                                |  0.98487   | 0.0802392 |             0.151396  |
|  MIC73 SOUS43 0000073 Kwajalein East (Airport) Mars |  0.984799  | 0.0331844 |             0.0859294 |
|  9452400 AK Skagway Taiya Inlet                     |  0.984796  | 0.180609  |             0.380731  |
|  UH834 SOUS00 GL239 Malin Head Ireland              |  0.98477   | 0.0810859 |             0.201822  |
|  MIC74 SOUS43 0000074 Ailinglaplap East (Airport) M |  0.984556  | 0.0354064 |             0.0865235 |
|  9411399 CA Gaviota State Park Pacifi               |  0.984338  | 0.0489688 |             0.110111  |
|  KWJP8 SOUS43 1820000 Kwajalein Marshall Island     |  0.98422   | 0.0338167 |             0.0825122 |
|  UH417 SOUS00 Sadeng Indonesia                      |  0.98389   | 0.0529772 |             0.119698  |
|  UH540 SOUS00 GL155 Prince Rupert Canada            |  0.983717  | 0.161014  |             0.397555  |
|  9414863 CA Richmond                                |  0.983709  | 0.0689441 |             0.212894  |
|  UH035 SOUS00 GL177 San Felix Chile                 |  0.983592  | 0.0277019 |             0.0758538 |
|  MIC71 SOUS43 0000071 Wotje East (Airport) Marshall |  0.983531  | 0.0355218 |             0.0893704 |
|  8661070 SC Springmaid Pier                         |  0.983514  | 0.050925  |             0.138264  |
|  MIC87 SOUS43 0000087 Ebeye Wes Marshall Islands Po |  0.983426  | 0.0343252 |             0.0866489 |
|  UH133 SOUS00 GL068 Ambon Indonesia                 |  0.983407  | 0.0545014 |             0.132951  |
|  MIC88 SOUS43 0000088 Ebon East Marshall Islands Po |  0.983403  | 0.0379896 |             0.0896324 |
|  MIC11 SOUS43 0000011 Guam South (Cocos) Guam Mari  |  0.983396  | 0.0214621 |             0.0502916 |
|  9414290 CA San Francisco                           |  0.983161  | 0.0652727 |             0.177106  |
|  MIC18 SOUS43 0000018 Saipan West (Garapan) Saipan  |  0.983015  | 0.0202604 |             0.0493759 |
|  MIC69 SOUS43 0000069 Enewetak East Marshall Island |  0.982938  | 0.0283193 |             0.0807919 |
|  UH402 SOUS00 Lautoka Fiji                          |  0.982924  | 0.0534293 |             0.11959   |
|  UH019 SOUS00 GL123 Noumea France                   |  0.982923  | 0.0355468 |             0.0769827 |
|  9435380 OR South Beach                             |  0.982915  | 0.0864911 |             0.370414  |
|  UH038 SOUS00 GL125 Nuku'alofa Tonga                |  0.982905  | 0.0463294 |             0.0964342 |
|  9452210 AK Juneau                                  |  0.982726  | 0.18489   |             0.432365  |
|  UH101 SOUS00 GL008 Mombasa Kenya                   |  0.98272   | 0.0795127 |             0.18766   |
|  1656 USA - Kodiak Island, AK                       |  0.982691  | 0.0920973 |             0.199429  |
|  MIC70 SOUS43 0000070 Utirik East (Airport) Marshal |  0.982688  | 0.0346395 |             0.0879849 |
|  MIC19 SOUS43 0000019 Saipan North Saipan Marianas  |  0.982653  | 0.018915  |             0.0529683 |
|  MIC86 SOUS43 0000086 Ebeye East Marshall Islands P |  0.982577  | 0.0356328 |             0.0865523 |
|  9410665 CA Los Angeles Pier J                      |  0.98242   | 0.0515167 |             0.117587  |
|  9431647 OR Port Orford                             |  0.98242   | 0.0763454 |             0.160131  |
|  MIC79 SOUS43 0000079 Eurapik East Yap FSM Populat  |  0.982391  | 0.0299614 |             0.0761916 |
|  9414311 CA San Francisco Pier 1                    |  0.982345  | 0.0731272 |             0.200086  |
|  9414776 CA Oakland Berth 34                        |  0.982343  | 0.0742096 |             0.192127  |
|  MIC72 SOUS43 0000072 Ujae East (Airport) Marshall  |  0.982314  | 0.0341244 |             0.0815523 |
|  NSTP6 SOUS43 1770000 Pago Pago American Samoa      |  0.982294  | 0.0321516 |             0.0716781 |
|  MIC77 SOUS43 0000077 Wake East Wake Island Populat |  0.982247  | 0.0254276 |             0.0643838 |
|  MIC78 SOUS43 0000078 Wake West Wake Island Populat |  0.982214  | 0.0248302 |             0.0622633 |
|  8531680 NJ Sandy Hook                              |  0.982212  | 0.0515283 |             0.182561  |
|  MIC13 SOUS43 0000013 Rota East (Sinapalu) Rota Ma  |  0.981987  | 0.0201952 |             0.0557428 |
|  UH163 SOUS00 GL049 Benoa Indonesia                 |  0.981827  | 0.0683986 |             0.173055  |
|  WAKP8 SOUS43 1890000 Wake Island Pacific Ocean     |  0.981695  | 0.0255254 |             0.0601647 |
|  9432780 OR Charleston                              |  0.981686  | 0.0835612 |             0.194628  |
|  9410170 CA San Diego San Diego Bay                 |  0.981676  | 0.054217  |             0.117756  |
|  UH820 SOUS00 GL225 Nuuk Denmark                    |  0.981524  | 0.116647  |             0.263695  |
|  UH353 SOUS00 GL085 Kushimoto Japan                 |  0.981474  | 0.0403073 |             0.10124   |
|  9450460 AK Ketchikan                               |  0.98136   | 0.161804  |             0.449859  |
|  UH125 SOUS00 Prigi Indonesia                       |  0.98128   | 0.0625827 |             0.152244  |
|  9411406 CA Oil Platform Harvest                    |  0.981236  | 0.0528287 |             0.113698  |
|  MIC57 SOUS43 0000057 Faraulep East Yap FSM Warnin  |  0.981182  | 0.0267101 |             0.064813  |
|  9439040 OR Astoria                                 |  0.981174  | 0.10176   |             0.277154  |
|  600 NM West-Northwest of Phuket Thailand           |  0.981109  | 0.0202587 |             0.0542224 |
|  UH155 SOUS00 GL096 Dzaoudzi France                 |  0.980912  | 0.0881792 |             0.199663  |
|  UH420 SOUS00 Saumlaki Indonesia                    |  0.980884  | 0.0683065 |             0.166499  |
|  UH171 SOUS00 GL046 Cocos Australia                 |  0.980752  | 0.0280448 |             0.0640731 |
|  9447130 WA Seattle Puget Sound                     |  0.980614  | 0.119163  |             0.290871  |
|  MIC67 SOUS43 0000067 Mokil East Pohnpei FSM Warni  |  0.980582  | 0.0304345 |             0.0806714 |
|  UH299 SOUS00 GL344 Qaqortoq Denmark                |  0.980433  | 0.0844466 |             0.166525  |
|  UH004 SOUS00 GL114 Nauru Nauru                     |  0.980309  | 0.0425251 |             0.117848  |
|  MIC34 SOUS43 0000034 Kosrae West (Walung) Kosrae   |  0.980294  | 0.0357031 |             0.098567  |
|  9457804 AK Alitak                                  |  0.980278  | 0.128535  |             0.328302  |
|  UH082 SOUS00 GL182 Acajutla El Salvador            |  0.980148  | 0.0775738 |             0.176672  |
|  MIC29 SOUS43 0000029 Pohnpei North Pohnpei FSM Ma  |  0.98009   | 0.0279251 |             0.0743966 |
|  UH107 SOUS00 GL045 Padang Indonesia                |  0.980049  | 0.0333052 |             0.0761407 |
|  9418767 CA North Spit                              |  0.979769  | 0.0771328 |             0.164729  |
|  9446484 WA Tacoma                                  |  0.979598  | 0.128618  |             0.283252  |
|  MIC33 SOUS43 0000033 Kosrae North (Airport) Kosrae |  0.979576  | 0.0364602 |             0.101001  |
|  UH149 SOUS00 Lamu Kenya                            |  0.979453  | 0.0825074 |             0.199934  |
|  UH295 SOUS00 GL238 Stornoway United Kingdom of Gre |  0.979327  | 0.120834  |             0.248267  |
|  UH684 SOUS00 GL178 Puerto Montt Chile              |  0.979247  | 0.24546   |             0.685439  |
|  MIC66 SOUS43 0000066 Pakin East Pohnpei FSM Warni  |  0.979209  | 0.0274023 |             0.0810731 |
|  MIC36 SOUS43 0000036 Kosrae East (Malem) Kosrae F  |  0.979193  | 0.0376661 |             0.103069  |
|  9415338 CA Sonoma Creek Entrance                   |  0.979184  | 0.08592   |             0.197393  |
|  1664 Norway - Ny Alesund                           |  0.979012  | 0.0440202 |             0.107345  |
|  MIC30 SOUS43 0000030 Pohnpei East Pohnpei FSM Maj  |  0.978957  | 0.0297609 |             0.0798325 |
|  UH166 SOUS00 GL040 Broome Australia                |  0.97877   | 0.295866  |             0.569684  |
|  9414750 CA Alameda                                 |  0.978725  | 0.0864499 |             0.220042  |
|  UH806 SOUS00 Nouakchott Mauritania                 |  0.978697  | 0.0383249 |             0.103736  |
|  9410666 CA Los Angeles Pier 400                    |  0.978611  | 0.0571571 |             0.138013  |
|  MIC35 SOUS43 0000035 Kosrae South (Utwa Ma) Kosrae |  0.978588  | 0.0378067 |             0.0967787 |
|  MIC58 SOUS43 0000058 Woleai East Yap FSM Warning   |  0.978457  | 0.0307734 |             0.0758636 |
|  MIC15 SOUS43 0000015 Tinian East Tinian Marianas   |  0.978449  | 0.019935  |             0.0498777 |
|  UH913 SOUS00 Telukdalam Indonesia                  |  0.978181  | 0.024982  |             0.0558081 |
|  9447214 WA Shilshole Bay GPS Buoy                  |  0.977858  | 0.125118  |             0.284172  |
|  9415020 CA Point Reyes                             |  0.977775  | 0.0651788 |             0.146442  |
|  9410660 CA Los Angeles                             |  0.977757  | 0.0581414 |             0.14821   |
|  UH805 SOUS00 GL323 Vardo Norway                    |  0.977745  | 0.103799  |             0.210267  |
|  9410230 CA La Jolla                                |  0.977728  | 0.0562716 |             0.115617  |
|  UH257 SOUS00 GL211 Settlement Point Bahamas (the)  |  0.977493  | 0.0332607 |             0.0797355 |
|  MIC32 SOUS43 0000032 Pohnpei West Pohnpei FSM Maj  |  0.977443  | 0.0287784 |             0.0790897 |
|  9459881 AK King Cove                               |  0.977281  | 0.0790436 |             0.193459  |
|  MIC81 SOUS43 0000081 Lamotrek East Yap FSM Popula  |  0.976985  | 0.0260864 |             0.0589198 |
|  MIC68 SOUS43 0000068 Pingelap East Pohnpei FSM Wa  |  0.976603  | 0.0354355 |             0.0987566 |
|  MIC59 SOUS43 0000059 Satawal East Yap FSM Warning  |  0.976536  | 0.0254796 |             0.0535056 |
|  UH352 SOUS00 GL086 Mera Japan                      |  0.976428  | 0.0402141 |             0.0901475 |
|  9414958 CA Bolinas Bolinas Lagoon                  |  0.976348  | 0.0676769 |             0.13846   |
|  9415056 CA Point Pinole                            |  0.976346  | 0.0905378 |             0.213369  |
|  MIC08 SOUS43 0000008 Pohnpei FSM UHSLC Gauge       |  0.976345  | 0.0303304 |             0.0820653 |
|  UH803 SOUS00 GL234 Rorvik Norway                   |  0.976323  | 0.0759477 |             0.168166  |
|  UH351 SOUS00 GL087 Ofunato Japan                   |  0.976174  | 0.0394527 |             0.108262  |
|  UH094 SOUS00 Matarani Peru                         |  0.976037  | 0.0391802 |             0.0818148 |
|  MIC31 SOUS43 0000031 Pohnpei South Pohnpei FSM Ma  |  0.975808  | 0.0311868 |             0.0834703 |
|  9416409 CA GREEN COVE PACIFIC OCEAN                |  0.975718  | 0.0698807 |             0.153785  |
|  UH419 SOUS00 Lembar Indonesia                      |  0.975093  | 0.0466712 |             0.111606  |
|  MIC80 SOUS43 0000080 Ifalik East Yap FSM Populate  |  0.975079  | 0.0319463 |             0.0699611 |
|  UH799 SOUS00 GL209 Portu-Prince Haiti              |  0.974874  | 0.0152557 |             0.0374902 |
|  UH542 SOUS00 GL156 Tofino Canada                   |  0.974564  | 0.103994  |             0.248395  |
|  UH109 SOUS00 GL027 Gan Maldives                    |  0.974507  | 0.0309958 |             0.0671566 |
|  8413320 ME Bar Harbor                              |  0.974417  | 0.156636  |             0.337098  |
|  MIC65 SOUS43 0000065 Sapwuafik (Ngatik) East Pohnp |  0.973884  | 0.0313119 |             0.0857192 |
|  UH034 SOUS00 GL161 Cabo San Lucas Mexico           |  0.973876  | 0.043006  |             0.111212  |
|  UH271 SOUS00 Fort de France France                 |  0.97368   | 0.0136235 |             0.0350393 |
|  UH104 SOUS00 GL026 Diego Garcia United Kingdom of  |  0.973632  | 0.0450547 |             0.0917286 |
|  8423898 NH Fort Point                              |  0.973625  | 0.13474   |             0.323742  |
|  UH023 SOUS00 GL139 Rarotonga Cook Islands (the)    |  0.973393  | 0.0317925 |             0.0787731 |
|  9752619 PR Isabel Segunda Vieques Is               |  0.973328  | 0.0134377 |             0.033478  |
|  UH016 SOUS00 GL138 Rikitea France                  |  0.973294  | 0.0303163 |             0.0730344 |
|  1715 USA - Cutler Farris Wharf, ME                 |  0.973026  | 0.204478  |             0.450059  |
|  UH113 SOUS00 Masirah Oman                          |  0.972527  | 0.06835   |             0.149314  |
|  8518750 NY The Battery                             |  0.97219   | 0.0657125 |             0.161439  |
|  UH142 SOUS00 Langkawi Malaysia                     |  0.972008  | 0.0872593 |             0.219415  |
|  UH340 SOUS00 Kaohsiung China                       |  0.971521  | 0.0322328 |             0.0746858 |
|  UH317 SOUS00 Ensenada Mexico                       |  0.971396  | 0.061867  |             0.138462  |
|  UH153 SOUS00 GL029 Minicoy India                   |  0.971296  | 0.0364412 |             0.093206  |
|  UH147 SOUS00 GL030 Karachi Pakistan                |  0.971125  | 0.0821624 |             0.212562  |
|  UH173 SOUS00 GL277 Davis Australia                 |  0.971071  | 0.0562555 |             0.133126  |
|  1612480 HI Mokuoloe                                |  0.970937  | 0.0262891 |             0.0747154 |
|  1586 New Zealand - Christchurch                    |  0.970688  | 0.108102  |             0.308242  |
|  8410140 ME Eastport                                |  0.970509  | 0.279479  |             0.534181  |
|  UH179 SOUS00 GL024 Saint Paul France               |  0.97041   | 0.0466551 |             0.126102  |
|  UH108 SOUS00 GL028 Male Maldives                   |  0.970167  | 0.0297251 |             0.0661464 |
|  8418150 ME Portland                                |  0.969905  | 0.149092  |             0.361666  |
|  UH162 SOUS00 GL291 Cilicap Indonesia               |  0.969888  | 0.0640377 |             0.192073  |
|  MIC82 SOUS43 0000082 Oroluk East Pohnpei FSM Popu  |  0.969846  | 0.0291967 |             0.0788825 |
|  UH052 SOUS00 GL109 Johnston United States of Ameri |  0.96793   | 0.0267288 |             0.0614209 |
|  UH878 SOUS00 Bullen Bay Curacao                    |  0.967747  | 0.0145861 |             0.0334905 |
|  UH221 SOUS00 GL268 Simon's Town South Africa       |  0.967715  | 0.0532494 |             0.136919  |
|  8443970 MA Boston                                  |  0.967681  | 0.155572  |             0.330604  |
|  UH117 SOUS00 Hanimaadhoo Maldives                  |  0.967652  | 0.0339143 |             0.0813931 |
|  878 USA - Fort_Pulaski_GA                          |  0.967631  | 0.0965196 |             0.218998  |
|  UH822 SOUS00 GL242 Brest France                    |  0.966895  | 0.231427  |             0.477483  |
|  8452944 RI Conimicut Light                         |  0.966794  | 0.053303  |             0.105427  |
|  9455920 AK Anchorage                               |  0.966761  | 0.344855  |             1.02469   |
|  UH114 SOUS00 GL004 Salalah Oman                    |  0.966382  | 0.0567603 |             0.146586  |
|  UH093 SOUS00 GL173 Callao Peru                     |  0.966248  | 0.0396673 |             0.0821171 |
|  UH808 SOUS00 GL343 Thule (Pituffik) Denmark        |  0.965962  | 0.0911557 |             0.238421  |
|  9759938 PR Mona Island                             |  0.965756  | 0.0124771 |             0.029937  |
|  UH181 SOUS00 GL013 Durban South Africa             |  0.965698  | 0.0637439 |             0.138396  |
|  9444900 WA Port Townsend                           |  0.964676  | 0.12275   |             0.307225  |
|  8726607 FL Old Port Tampa                          |  0.96463   | 0.0341309 |             0.07441   |
|  8519483 NY Bergen Point West Reach                 |  0.964078  | 0.0784826 |             0.265678  |
|  UH777 SOUS00 Puerto Plata Dominican Republic (the) |  0.963518  | 0.0255626 |             0.0652683 |
|  UH370 SOUS00 GL073 Manila Philippines (the)        |  0.963047  | 0.0474574 |             0.114438  |
|  UH382 SOUS00 Subic Bay Philippines (the)           |  0.962927  | 0.0427317 |             0.109065  |
|  UH105 SOUS00 GL019 Rodrigues Mauritius             |  0.962795  | 0.044735  |             0.0965975 |
|  9415144 CA Port Chicago                            |  0.962432  | 0.14378   |             0.329843  |
|  8461490 CT New London                              |  0.962363  | 0.048924  |             0.123593  |
|  8467150 CT Bridgeport                              |  0.962149  | 0.121661  |             0.270362  |
|  8658163 NC Wrightsville Beach                      |  0.962081  | 0.0640396 |             0.182565  |
|  9751381 VI Lameshur Bay St John                    |  0.962023  | 0.0127235 |             0.0253488 |
|  9462450 AK Nikolski                                |  0.961488  | 0.0831434 |             0.175417  |
|  UH275 SOUS00 GL222 Halifax Canada                  |  0.961414  | 0.0734397 |             0.205222  |
|  8724580 FL Key West                                |  0.961388  | 0.0267448 |             0.0621324 |
|  8727520 FL Cedar Key                               |  0.961175  | 0.06715   |             0.145832  |
|  UH259 SOUS00 GL221 Bermuda United Kingdom of Great |  0.961125  | 0.0398371 |             0.111155  |
|  UH273 SOUS00 Port-aux-basques Canada               |  0.960906  | 0.0542545 |             0.160409  |
|  MIC62 SOUS43 0000062 Fananu East Chuuk FSM Warnin  |  0.960207  | 0.0283341 |             0.0597162 |
|  9414575 CA Coyote Creek                            |  0.959971  | 0.153983  |             0.474011  |
|  9461380 AK Adak Island                             |  0.959966  | 0.0739086 |             0.173527  |
|  UH041 SOUS00 GL102 Dutch Harbor AK United States   |  0.959879  | 0.0852759 |             0.173392  |
|  9415102 CA Martinez-Amorco Pier                    |  0.959696  | 0.139376  |             0.28861   |
|  UH009 SOUS00 GL066 Honiara Solomon Islands         |  0.958495  | 0.034892  |             0.080749  |
|  UH276 SOUS00 GL223 St. John's Canada               |  0.958114  | 0.0609152 |             0.15074   |
|  UH654 SOUS00 Currimao Philippines (the)            |  0.957945  | 0.0319431 |             0.0717593 |
|  8537121 NJ Ship John Shoal                         |  0.957782  | 0.103828  |             0.242294  |
|  9449880 WA Friday Harbor                           |  0.95737   | 0.126383  |             0.345617  |
|  8454049 RI Quonset Point                           |  0.957369  | 0.0561716 |             0.156466  |
|  1611400 HI Nawiliwili                              |  0.956887  | 0.029284  |             0.0926885 |
|  9461380 Adak Island AK                             |  0.956715  | 0.0768525 |             0.177761  |
|  9759394 PR Mayaguez                                |  0.956106  | 0.0176714 |             0.0471117 |
|  UH119 SOUS00 GL002 Djibouti Djibouti               |  0.955549  | 0.0802115 |             0.205455  |
|  MIC26 SOUS43 0000026 Chuuk Lagoon East Chuuk FSM   |  0.95507   | 0.0309416 |             0.0671006 |
|  8454000 RI Providence                              |  0.954757  | 0.0646933 |             0.161266  |
|  UH115 SOUS00 GL033 Colombo Sri Lanka               |  0.954385  | 0.0289461 |             0.0727795 |
|  9461710 AK Atka                                    |  0.953317  | 0.0771256 |             0.181932  |
|  UH290 SOUS00 GL305 Port Stanley United Kingdom of  |  0.95305   | 0.0617597 |             0.139574  |
|  8723214 FL Virginia Key                            |  0.953042  | 0.0400724 |             0.104249  |
|  9455920 Anchorage AK                               |  0.953004  | 0.412029  |             1.12562   |
|  MIC10 SOUS43 0000010 Moen I Chuuk FSM Historic CO  |  0.95277   | 0.0312733 |             0.0721264 |
|  9440569 WA Skamokawa                               |  0.952468  | 0.129015  |             0.285914  |
|  8722670 FL Lake Worth Pier Atlantic                |  0.952465  | 0.0489147 |             0.140522  |
|  UH294 SOUS00 GL241 Newlyn Cornwall United Kingdom  |  0.952387  | 0.229944  |             0.44926   |
|  8665530 SC Charleston Cooper River E               |  0.952346  | 0.0905683 |             0.203671  |
|  MIC64 SOUS43 0000064 Lukunor East Chuuk FSM Warni  |  0.952285  | 0.0350539 |             0.0769248 |
|  9464212 St Paul Island AK                          |  0.951784  | 0.0770159 |             0.188266  |
|  9465261 Nushagak Bay                               |  0.951611  | 0.357072  |             0.781753  |
|  UH261 SOUS00 Charleston SC United States of Ameri  |  0.951588  | 0.0911912 |             0.220365  |
|  UH833 SOUS00 GL224 Nain Canada                     |  0.951372  | 0.106682  |             0.227543  |
|  MIC63 SOUS43 0000063 Losap East Chuuk FSM Warning  |  0.95111   | 0.0328502 |             0.0692256 |
|  UH029 SOUS00 GL117 Kapingamarangi Micronesia (Fede |  0.95099   | 0.0390688 |             0.0779583 |
|  9752695 PR Esperanza Vieques Island                |  0.950794  | 0.0142711 |             0.0336647 |
|  UH738 SOUS00 Santa Marta Colombia                  |  0.95005   | 0.0184685 |             0.0472844 |
|  8551910 DE Reedy Point                             |  0.949369  | 0.112805  |             0.254439  |
|  1617433 HI Kawaihae                                |  0.949074  | 0.0353009 |             0.10054   |
|  UH071 SOUS00 GL101 Wellington New Zealand          |  0.948834  | 0.0904437 |             0.223034  |
|  8725110 FL Naples Gulf of Mexico                   |  0.948709  | 0.0456893 |             0.0883911 |
|  UH286 SOUS00 GL190 Puerto Deseado Argentina        |  0.947876  | 0.2946    |             0.672625  |
|  MIC27 SOUS43 0000027 Chuuk Lagoon North Chuuk FSM  |  0.946637  | 0.0328947 |             0.0705141 |
|  UH600 SOUS00 GL181 Ushuaia Argentina               |  0.945113  | 0.116237  |             0.257723  |
|  8551762 DE Delaware City                           |  0.94485   | 0.118782  |             0.269922  |
|  9754228 PR Yabucoa Harbor                          |  0.944674  | 0.0151242 |             0.0362169 |
|  UH184 SOUS00 GL076 Port Elizabeth South Africa     |  0.943278  | 0.075869  |             0.188999  |
|  8760922 LA Pilots Station East S.W.                |  0.943173  | 0.0275357 |             0.0544122 |
|  1612340 HI Honolulu                                |  0.942886  | 0.0345622 |             0.0966192 |
|  UH316 SOUS00 GL267 Acapulco Gro. Mexico            |  0.942825  | 0.0480953 |             0.109758  |
|  1619910 HI Sand Island Midway Island               |  0.941608  | 0.0249861 |             0.0586432 |
|  9758053 PR Penuelas                                |  0.941492  | 0.0156834 |             0.0357946 |
|  9759110 PR Magueyes Island                         |  0.941016  | 0.0158648 |             0.0354872 |
|  8721604 FL Trident Pier Port Canaver               |  0.94096   | 0.0679533 |             0.200054  |
|  UH121 SOUS00 GL339 Pt. La Rue Seychelles           |  0.940936  | 0.0603874 |             0.137152  |
|  UH177 SOUS00 GL022 Mawson Australia                |  0.939346  | 0.0583562 |             0.125769  |
|  MIC28 SOUS43 0000028 Chuuk Lagoon West Chuuk FSM   |  0.93934   | 0.0348457 |             0.0704107 |
|  UH047 SOUS00 GL103 Chichijima Japan                |  0.938925  | 0.0423441 |             0.0888279 |
|  UH350 SOUS00 GL089 Kushiro Japan                   |  0.938783  | 0.062961  |             0.136428  |
|  UH180 SOUS00 GL023 Kerguelen France                |  0.938765  | 0.080518  |             0.232709  |
|  UH130 SOUS00 GL278 Casey Australia                 |  0.938023  | 0.0806574 |             0.235329  |
|  UH220 SOUS00 GL314 Walvis Bay Namibia              |  0.937305  | 0.0670828 |             0.226203  |
|  9761115 Barbuda                                    |  0.936979  | 0.0154824 |             0.0413704 |
|  8449130 MA Nantucket Island                        |  0.936826  | 0.0800275 |             0.199316  |
|  UH049 SOUS00 GL104 Minamitorishima Japan           |  0.936196  | 0.0285133 |             0.0855919 |
|  MIC61 SOUS43 0000061 Ulul East Chuuk FSM Warning   |  0.9347    | 0.0348292 |             0.0828472 |
|  UH122 SOUS00 Sibolga Indonesia                     |  0.93308   | 0.052223  |             0.114841  |
|  UH547 SOUS00 Barbers Point HI United States of Am  |  0.932857  | 0.0367242 |             0.0999243 |
|  UH335 SOUS00 GL056 Spring Bay Australia            |  0.931897  | 0.0656738 |             0.12644   |
|  MIC60 SOUS43 0000060 Puluwat East Chuuk FSM Warni  |  0.931154  | 0.0373687 |             0.080131  |
|  UH699 SOUS00 GL044 Tanjong Pagar Singapore         |  0.929756  | 0.117724  |             0.237693  |
|  1336 Norway - Maloy                                |  0.92956   | 0.0961777 |             0.187236  |
|  UH364 SOUS00 GL088 Hakodate Japan                  |  0.928254  | 0.0421728 |             0.10323   |
|  UH331 SOUS00 GL058 Brisbane Australia              |  0.927764  | 0.128982  |             0.386853  |
|  UH829 SOUS00 GL340 Trieste Italy                   |  0.927121  | 0.0630224 |             0.126493  |
|  UH906 SOUS00 GL141 Moulmein Myanmar                |  0.927055  | 0.34511   |             1.38707   |
|  8536110 NJ Cape May                                |  0.926981  | 0.114013  |             0.222175  |
|  8726667 FL Mckay Bay Entrance                      |  0.925885  | 0.050319  |             0.121597  |
|  8726384 FL Port Manatee                            |  0.925732  | 0.0430175 |             0.116282  |
|  UH383 SOUS00 Vung Tau Viet Nam                     |  0.924287  | 0.166209  |             0.409146  |
|  UH266 SOUS00 GL208 Cristobal Panama                |  0.923853  | 0.0245105 |             0.0630434 |
|  8656483 NC Beaufort Duke Marine Lab                |  0.923423  | 0.084384  |             0.22233   |
|  UH347 SOUS00 GL327 Abashiri Japan                  |  0.92284   | 0.059627  |             0.130077  |
|  UH824 SOUS00 GL205 Marseille France                |  0.922414  | 0.0142558 |             0.0303138 |
|  UH103 SOUS00 GL018 Port Louis Mauritius            |  0.921029  | 0.0259698 |             0.0888794 |
|  UH024 SOUS00 GL143 Penrhyn Cook Islands (the)      |  0.917824  | 0.0165712 |             0.0296941 |
|  9465601 Carter Bay Kuskokwim Bay AK                |  0.917441  | 0.274466  |             0.613457  |
|  UH079 SOUS00 GL128 Chatham New Zealand             |  0.911731  | 0.0815182 |             0.186238  |
|  UH268 SOUS00 Limon Costa Rica                      |  0.91044   | 0.0267429 |             0.0672295 |
|  UH601 SOUS00 GL185 Esperanza Argentina             |  0.908936  | 0.152723  |             0.366329  |
|  8539094 NJ Burlington Delaware River               |  0.908578  | 0.175795  |             0.391358  |
|  8720218 FL Mayport (Bar Pilots Dock)               |  0.908024  | 0.12497   |             0.280706  |
|  UH164 SOUS00 GL017 Reunion France                  |  0.906617  | 0.0227806 |             0.0700926 |
|  8775870 TX Bob Hall Pier Corpus Chri               |  0.906084  | 0.0414111 |             0.104236  |
|  UH836 SOUS00 GL333 Alert Canada                    |  0.901218  | 0.0493604 |             0.123814  |
|  8570283 MD Ocean City Inlet                        |  0.90002   | 0.0763027 |             0.153681  |
|  8779748 TX South Padre Island CG Stat              |  0.899094  | 0.037604  |             0.0751774 |
|  UH737 SOUS00 San Andres Colombia                   |  0.897629  | 0.0257494 |             0.0720845 |
|  UH680 SOUS00 GL130 Macquarie Is. Australia         |  0.897184  | 0.0768161 |             0.181195  |
|  UH334 SOUS00 GL060 Townsville Australia            |  0.896871  | 0.161309  |             0.421016  |
|  UH129 SOUS00 GL055 Portland S.Aus. Australia       |  0.893336  | 0.0635428 |             0.13612   |
|  8538886 NJ Tacony-Palmyra Bridge                   |  0.890707  | 0.177522  |             0.423255  |
|  UH360 SOUS00 GL324 Wakkanai Japan                  |  0.889789  | 0.0294368 |             0.0683596 |
|  UH700 SOUS00 GL188 Faraday Antarctica              |  0.88932   | 0.115732  |             0.20953   |
|  8548989 PA Newbold                                 |  0.887455  | 0.209376  |             0.535906  |
|  8545240 PA Philadelphia                            |  0.886899  | 0.172493  |             0.396188  |
|  8658120 NC Wilmington                              |  0.886673  | 0.129168  |             0.42712   |
|  8729108 FL Panama City                             |  0.879484  | 0.0433343 |             0.122042  |
|  UH189 SOUS00 GL131 Dumont d'Urville Antarctica     |  0.878687  | 0.111115  |             0.237648  |
|  8540433 PA Marcus Hook                             |  0.877062  | 0.177465  |             0.456569  |
|  8735391 AL Dog River Bridge                        |  0.876168  | 0.0476699 |             0.0906495 |
|  8573927 MD Chesapeake City                         |  0.870857  | 0.0932106 |             0.249938  |
|  8510560 NY Montauk                                 |  0.868765  | 0.0639989 |             0.145372  |
|  8737048 AL Mobile State Docks                      |  0.865892  | 0.0507582 |             0.106727  |
|  8729210 FL Panama City Beach                       |  0.862821  | 0.0446071 |             0.0978364 |
|  UH349 SOUS00 GL325 Toyama Japan                    |  0.855994  | 0.0239039 |             0.0529379 |
|  9465374 Snag Point Dillingham AK                   |  0.855392  | 0.636881  |             1.60749   |
|  UH015 SOUS00 GL140 Papeete France                  |  0.852265  | 0.0178793 |             0.0562965 |
|  8720030 FL Fernandina Beach                        |  0.849859  | 0.181745  |             0.413924  |
|  UH920 SOUS00 GL020 Marion Island South Africa      |  0.841907  | 0.0593463 |             0.145801  |
|  8571892 MD Cambridge                               |  0.823876  | 0.0714137 |             0.193776  |
|  8651370 NC Duck                                    |  0.806235  | 0.116467  |             0.246961  |
|  8637689 VA Yorktown USCG Training Cen              |  0.803048  | 0.0950179 |             0.191621  |
|  8447930 MA Woods Hole                              |  0.802109  | 0.0571593 |             0.125711  |
|  8639348 VA Money Point                             |  0.797377  | 0.105233  |             0.230854  |
|  8770777 TX Manchester                              |  0.795607  | 0.0585594 |             0.127382  |
|  8632200 VA Kiptopeke                               |  0.791711  | 0.103173  |             0.19092   |
|  8594900 DC Washington                              |  0.774268  | 0.115733  |             0.280205  |
|  UH175 SOUS00 GL053 Fremantle Australia             |  0.767925  | 0.0687957 |             0.189235  |
|  8764044 LA Berwick Atchafalaya River               |  0.765924  | 0.0448548 |             0.0943721 |
|  8770520 TX Rainbow Bridge                          |  0.759555  | 0.0371485 |             0.100722  |
|  UH128 SOUS00 GL308 Thevenard Australia             |  0.759384  | 0.161351  |             0.420591  |
|  8638863 VA Chesapeake Bay Bridge Tunn              |  0.75542   | 0.112028  |             0.212491  |
|  8574680 MD Baltimore Fort McHenry P                |  0.755177  | 0.0655147 |             0.152115  |
|  8760721 LA Pilottown                               |  0.750127  | 0.0254702 |             0.0540451 |
|  8638610 VA Sewells Point                           |  0.749854  | 0.108805  |             0.233382  |
|  8723970 FL Vaca Key Florida Bay                    |  0.749465  | 0.0542619 |             0.153058  |
|  1019 Australia - Thevenard_AU                      |  0.73784   | 0.168533  |             0.438691  |
|  UH280 SOUS00 GL195 Ilha Fiscal RJ Brazil           |  0.729483  | 0.0938353 |             0.20037   |
|  8764227 LA LAWMA Amerada Pass                      |  0.724698  | 0.0623956 |             0.117328  |
|  8771013 TX Eagle Point Galveston Bay               |  0.69993   | 0.0608058 |             0.148251  |
|  UH825 SOUS00 GL284 Cuxhaven Germany                |  0.68298   | 0.469837  |             0.923529  |
|  UH178 SOUS00 GL021 Crozet France                   |  0.68103   | 0.0667035 |             0.159361  |
|  UH176 SOUS00 GL054 Esperance Australia             |  0.680528  | 0.100226  |             0.312592  |
|  8770822 TX Texas Point Sabine Pass                 |  0.674348  | 0.101651  |             0.299986  |
|  8747437 MS Bay Waveland Yacht Club                 |  0.66669   | 0.067584  |             0.163081  |
|  9468132 St. Michael                                |  0.655416  | 0.249846  |             0.577198  |
|  UH731 SOUS00 GL191 Puerto Madryn Argentina         |  0.640898  | 1.92987   |             6.62624   |
|  UH348 SOUS00 GL326 Hamada Japan                    |  0.636791  | 0.0524628 |             0.109233  |
|  8774770 TX Rockport                                |  0.610431  | 0.020203  |             0.0520015 |
|  8577330 MD Solomons Island                         |  0.588324  | 0.0761775 |             0.174016  |
|  8571421 MD Bishops Head                            |  0.587368  | 0.114502  |             0.241021  |
|  8774513 TX Copano Bay                              |  0.585409  | 0.0220435 |             0.0501132 |
|  8635750 VA Lewisetta                               |  0.585044  | 0.0735694 |             0.148574  |
|  8770475 TX Port Arthur                             |  0.574199  | 0.0602331 |             0.162809  |
|  8771341 TX Galveston Bay Entrance No               |  0.567853  | 0.105609  |             0.184594  |
|  9468756 Nome AK                                    |  0.557032  | 0.178195  |             0.327887  |
|  8573364 MD Tolchester Beach                        |  0.533898  | 0.0966866 |             0.231869  |
|  952 USA - Nome_AK                                  |  0.517715  | 0.186381  |             0.37584   |
|  8762075 LA Port Fourchon Belle Pass                |  0.513964  | 0.0594727 |             0.185483  |
|  UH729 SOUS00 GL192 Mar del Plata Argentina         |  0.506622  | 0.309115  |             0.69897   |
|  9468333 Unalakleet AK                              |  0.500337  | 0.335757  |             0.649969  |
|  9497645 Prudhoe Bay AK                             |  0.461026  | 0.0869587 |             0.196631  |
|  8662245 SC Oyster Landing (N Inlet Es              |  0.452211  | 0.167931  |             0.299605  |
|  UH579 SOUS00 GL151 Prudhoe Bay AK United States o  |  0.444708  | 0.0883392 |             0.194154  |
|  8775283 TX Port Inglesid                           |  0.358652  | 0.0412091 |             0.0808593 |
|  8636580 VA Windmill Point                          |  0.313564  | 0.0813283 |             0.154101  |
|  UH826 SOUS00 GL341 Stockholm Sweden                |  0.182533  | 0.0326873 |             0.0763796 |
|  8761305 LA Shell Beach                             |  0.165832  | 0.1219    |             0.290029  |
|  9491094 Red Dog Dock AK                            |  0.0391605 | 0.19853   |             0.391251  |
|  UH818 SOUS00 Smogen Sweden                         |  0.0285639 | 0.0727493 |             0.160558  |
|  UH804 SOUS00 GL321 Tregde Norway                   |  0.0261058 | 0.064716  |             0.121411  |
|  8654467 NC USCG Station Hatteras                   | -0.180158  | 0.052229  |             0.141864  |
|  8652587 NC Oregon Inlet Marina                     | -0.522703  | 0.137745  |             0.435886  |
|  UH819 SOUS00 GL233 Goteborgorsh. Sweden            | -0.729295  | 0.0807426 |             0.173201  |
|  8761927 LA New Canal Station                       | -1.02347   | 0.0957233 |             0.185213  |

### Disclaimer
This program is under experimental development. The results should not be used for navigational purposes or emergency planning under any circumstances. Please do not duplicate and use the result figures from this website without permission.
