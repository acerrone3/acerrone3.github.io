## GESTOFS-ML
This is a sister project of [GESTOFS](https://gm-ling.github.io/GESTOFS-develop/).  GESTOFS is an ADCIRC-based storm surge forecasting system for the whole globe.  GESTOFS-ML expands on this theme, but in addition to ADCIRC, it leverages a time-series forecasting ML model complete with meteorological forcing to enrich the prediction of surface water elevation.

### Site URL
[https://acerrone3.github.io/](https://acerrone3.github.io/)

### Latest Forecasts
Updated July 19, 2022

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
Updated July 19, 2022

Here, the ADCIRC forecasts are compared to the ML forecasts.  Comparisons are arranged in descending order based on each station's r-squared value.  Observational data has yet to be integrated for performance assessment.

|  Station                                            |        R2 |      RMSD |   Max Discrepancy (m) |
| :---------------------------------------------------|----------:|----------:|----------------------:|
|  UH030 SOUS00 Santa Cruz Ecuador                    |  0.995795 | 0.0264282 |             0.0790757 |
|  UH209 SOUS00 GL246 Cascais Portugal                |  0.994578 | 0.0395774 |             0.119433  |
|  UH081 SOUS00 GL175 Valparaiso Chile                |  0.994263 | 0.0212667 |             0.0729225 |
|  9455500 AK Seldovia                                |  0.994195 | 0.107397  |             0.242211  |
|  UH392 SOUS00 Cocos Island Costa Rica               |  0.994107 | 0.0476065 |             0.101429  |
|  UH088 SOUS00 Caldera Chile                         |  0.993482 | 0.0215422 |             0.0557184 |
|  UH218 SOUS00 GL250 Funchal Portugal                |  0.993413 | 0.0312875 |             0.0725583 |
|  PAC24 SOUS43 0000024 WA Long Beach                 |  0.993296 | 0.0540142 |             0.143714  |
|  9451600 AK Sitka                                   |  0.992356 | 0.067173  |             0.20447   |
|  UH830 SOUS00 GL243 La Coruna Spain                 |  0.992088 | 0.0573828 |             0.125473  |
|  MIC43 SOUS43 0000043 Kayangel North Palau Warning  |  0.991853 | 0.0285223 |             0.0959957 |
|  9454240 AK Valdez                                  |  0.991686 | 0.0834858 |             0.231332  |
|  9454050 AK Cordova                                 |  0.991518 | 0.084447  |             0.225657  |
|  UH123 SOUS00 GL347 Sabang Indonesia                |  0.991426 | 0.0219493 |             0.0494842 |
|  UH302 SOUS00 GL168 Balboa Panama                   |  0.991413 | 0.10684   |             0.26392   |
|  MIC48 SOUS43 0000048 Angaur South Palau Warning Po |  0.991237 | 0.0305861 |             0.10369   |
|  1272 Norway - Andenes                              |  0.991137 | 0.0355864 |             0.0964861 |
|  9419945 CA Pyramid Point Smith River               |  0.991031 | 0.0533712 |             0.134768  |
|  UH541 SOUS00 Bamfield Canada                       |  0.991017 | 0.062963  |             0.149355  |
|  MIC21 SOUS43 0000021 Ngeremlengui West Palau Major |  0.990998 | 0.0313994 |             0.0921648 |
|  MIC44 SOUS43 0000044 Peleliu East Palau Warning Po |  0.990994 | 0.0313021 |             0.103488  |
|  9455760 AK Nikiski                                 |  0.990976 | 0.154631  |             0.415293  |
|  UH288 SOUS00 GL229 Reykjavik Iceland               |  0.990947 | 0.0689681 |             0.245572  |
|  MIC54 SOUS43 0000054 Ngulu East Yap FSM Warning P  |  0.990724 | 0.0281556 |             0.0801887 |
|  UH227 SOUS00 GL202 Cayenne France                  |  0.990572 | 0.0466649 |             0.102107  |
|  UH816 SOUS00 GL350 Port Sonara Cameroon            |  0.990566 | 0.0251973 |             0.0700989 |
|  MIC53 SOUS43 0000053 Ngulu West Yap FSM Warning P  |  0.990483 | 0.0289393 |             0.0950649 |
|  9451600 Sitka AK                                   |  0.990443 | 0.075113  |             0.218605  |
|  9452634 AK Elfin Cove                              |  0.990393 | 0.0815281 |             0.237985  |
|  UH091 SOUS00 GL172 La Libertad Ecuador             |  0.99031  | 0.0499023 |             0.108003  |
|  MIC20 SOUS43 0000020 East Melekeok Palau Major Isl |  0.990222 | 0.0310124 |             0.101759  |
|  UH283 SOUS00 GL336 Fortaleza Brazil                |  0.990213 | 0.0489596 |             0.155181  |
|  UH118 SOUS00 Ko Miang Thailand                     |  0.990188 | 0.0352833 |             0.0706605 |
|  MIC78 SOUS43 0000078 Wake West Wake Island Populat |  0.989781 | 0.0165997 |             0.0367115 |
|  MIC47 SOUS43 0000047 Angaur West Palau Warning Poi |  0.989774 | 0.0332599 |             0.106918  |
|  9451054 AK Port Alexander                          |  0.989722 | 0.087341  |             0.248397  |
|  UH403 SOUS00 Jackson New Zealand                   |  0.989599 | 0.0502224 |             0.155559  |
|  MIC45 SOUS43 0000045 Peleliu West Palau Warning Po |  0.989546 | 0.0336756 |             0.111084  |
|  9455090 AK Seward                                  |  0.989542 | 0.0826277 |             0.217744  |
|  MIC46 SOUS43 0000046 Angaur East Palau Warning Poi |  0.989522 | 0.0333168 |             0.111209  |
|  MIC49 SOUS43 0000049 Sonsorol Northeast Palau Warn |  0.989351 | 0.0348925 |             0.107929  |
|  9443090 WA Neah Bay                                |  0.989331 | 0.0669243 |             0.193296  |
|  MIC50 SOUS43 0000050 Sonsorol Southeast Palau Warn |  0.98921  | 0.0349658 |             0.110201  |
|  MIC07 SOUS43 0000007 Yap FSM UHSLC Gauge           |  0.989205 | 0.0292487 |             0.0960542 |
|  PAC22 SOUS43 0000022 OR Seaside                    |  0.989196 | 0.068924  |             0.17653   |
|  UH295 SOUS00 GL238 Stornoway United Kingdom of Gre |  0.989046 | 0.0792011 |             0.194273  |
|  PAC21 SOUS43 0000021 OR Cannon Beach               |  0.988857 | 0.0694625 |             0.157948  |
|  UH354 SOUS00 GL082 Aburatsu Japan                  |  0.988809 | 0.0328248 |             0.085888  |
|  9450460 AK Ketchikan                               |  0.988793 | 0.118229  |             0.31255   |
|  851 USA - Crescent_City_CA                         |  0.988679 | 0.0589403 |             0.135557  |
|  MIC77 SOUS43 0000077 Wake East Wake Island Populat |  0.988649 | 0.0179405 |             0.0415835 |
|  MIC51 SOUS43 0000051 Sonsorol Northwest Palau Warn |  0.988561 | 0.0362242 |             0.111606  |
|  UH834 SOUS00 GL239 Malin Head Ireland              |  0.988449 | 0.0632298 |             0.135126  |
|  9452400 AK Skagway Taiya Inlet                     |  0.98842  | 0.146385  |             0.370664  |
|  UH908 SOUS00 GL038 Port Blair India                |  0.988385 | 0.0348306 |             0.0740215 |
|  MIC52 SOUS43 0000052 Sonsorol Southwest Palau Warn |  0.988361 | 0.0364111 |             0.118927  |
|  UH011 SOUS00 GL146 Christmas Kiribati              |  0.988323 | 0.0166803 |             0.0391348 |
|  UH017 SOUS00 Hiva Oa France                        |  0.988202 | 0.0369481 |             0.0924245 |
|  MIC06 SOUS43 0000006 Malakal Palau UHSLC Gauge     |  0.988193 | 0.0362714 |             0.114938  |
|  MIC24 SOUS43 0000024 Yap West (Airport) Yap FSM M  |  0.988059 | 0.0313954 |             0.100021  |
|  UH031 SOUS00 GL142 Nuku Hiva France                |  0.987946 | 0.0360708 |             0.0963569 |
|  MIC25 SOUS43 0000025 Yap North Yap FSM Major Isla  |  0.987918 | 0.0306679 |             0.0922899 |
|  UH101 SOUS00 GL008 Mombasa Kenya                   |  0.987772 | 0.0602294 |             0.135135  |
|  9452400 Skagway AK                                 |  0.987656 | 0.151135  |             0.371859  |
|  UH038 SOUS00 GL125 Nuku'alofa Tonga                |  0.98763  | 0.0373053 |             0.0885982 |
|  UH540 SOUS00 GL155 Prince Rupert Canada            |  0.987568 | 0.132592  |             0.279959  |
|  UH155 SOUS00 GL096 Dzaoudzi France                 |  0.987558 | 0.0631091 |             0.167832  |
|  MIC90 SOUS43 0000090 62 Km ENE from Helen Reef (-2 |  0.987514 | 0.037666  |             0.122515  |
|  UH046 SOUS00 GL348 Port Vila Vanuatu               |  0.987475 | 0.0276881 |             0.0673641 |
|  UH133 SOUS00 GL068 Ambon Indonesia                 |  0.987392 | 0.04554   |             0.118211  |
|  UH207 SOUS00 GL249 Ceuta Spain                     |  0.987382 | 0.0186774 |             0.0437788 |
|  UH362 SOUS00 GL083 Nagasaki Japan                  |  0.987263 | 0.0555075 |             0.192841  |
|  9452210 AK Juneau                                  |  0.987183 | 0.14842   |             0.364216  |
|  9459450 AK Sand Point                              |  0.987153 | 0.0638407 |             0.222161  |
|  MIC70 SOUS43 0000070 Utirik East (Airport) Marshal |  0.987102 | 0.0265488 |             0.0722498 |
|  UH402 SOUS00 Lautoka Fiji                          |  0.987089 | 0.0447351 |             0.114875  |
|  UH092 SOUS00 Talara Peru                           |  0.986913 | 0.0430936 |             0.123149  |
|  UH157 SOUS00 GL035 Vishakhapatnam India            |  0.986883 | 0.0259127 |             0.0572395 |
|  UH289 SOUS00 GL248 Gibraltar United Kingdom of Gre |  0.986536 | 0.0187569 |             0.057445  |
|  UH299 SOUS00 GL344 Qaqortoq Denmark                |  0.986462 | 0.062539  |             0.121974  |
|  MIC23 SOUS43 0000023 Yap South (Colonia) Yap FSM   |  0.986443 | 0.0325986 |             0.0894091 |
|  UH043 SOUS00 Palmyra Island United States of Ameri |  0.986422 | 0.0167724 |             0.0402269 |
|  MIC39 SOUS43 0000039 Majuro West Marshall Islands  |  0.98631  | 0.0302516 |             0.0773141 |
|  UH417 SOUS00 Sadeng Indonesia                      |  0.986302 | 0.0436702 |             0.110346  |
|  UH125 SOUS00 Prigi Indonesia                       |  0.986298 | 0.0476434 |             0.127176  |
|  MIC22 SOUS43 0000022 Yap East Yap FSM Major Islan  |  0.986264 | 0.0326178 |             0.0978987 |
|  MIC55 SOUS43 0000055 Ulithi East (Airport) Yap FS  |  0.986209 | 0.0303873 |             0.099891  |
|  PAC18 SOUS43 0000018 OR Pacific City               |  0.985949 | 0.0763638 |             0.187658  |
|  MIC76 SOUS43 0000076 Mili East Marshall Islands Wa |  0.985937 | 0.031815  |             0.0866335 |
|  UH149 SOUS00 Lamu Kenya                            |  0.985799 | 0.062123  |             0.130537  |
|  PAC16 SOUS43 0000016 OR Lincoln City               |  0.985665 | 0.0771505 |             0.186238  |
|  MIC71 SOUS43 0000071 Wotje East (Airport) Marshall |  0.985625 | 0.0295524 |             0.065909  |
|  PAC17 SOUS43 0000017 OR Neskowin Beach             |  0.985595 | 0.0773327 |             0.192898  |
|  MIC89 SOUS43 0000089 Arno East Marshall Islands Po |  0.985531 | 0.0312587 |             0.080762  |
|  MIC73 SOUS43 0000073 Kwajalein East (Airport) Mars |  0.985445 | 0.0290415 |             0.071854  |
|  9457804 AK Alitak                                  |  0.985439 | 0.104814  |             0.240492  |
|  PAC14 SOUS43 0000014 OR Beaver Creek               |  0.985437 | 0.0772227 |             0.170069  |
|  WAKP8 SOUS43 1890000 Wake Island Pacific Ocean     |  0.985412 | 0.02011   |             0.047165  |
|  MIC40 SOUS43 0000040 Majuro North Marshall Islands |  0.985351 | 0.0311997 |             0.0848472 |
|  9411399 CA Gaviota State Park Pacifi               |  0.985349 | 0.0495374 |             0.116395  |
|  UH233 SOUS00 GL259 Lagos Nigeria                   |  0.985335 | 0.0328847 |             0.079072  |
|  MIC69 SOUS43 0000069 Enewetak East Marshall Island |  0.985291 | 0.0238319 |             0.0552162 |
|  UH356 SOUS00 Maisaka Japan                         |  0.98511  | 0.0332842 |             0.120158  |
|  9453220 Yakutat Bay AK                             |  0.985    | 0.0951949 |             0.253357  |
|  UH820 SOUS00 GL225 Nuuk Denmark                    |  0.984836 | 0.0932074 |             0.21636   |
|  1656 USA - Kodiak Island, AK                       |  0.984532 | 0.0834182 |             0.228431  |
|  9416409 CA GREEN COVE PACIFIC OCEAN                |  0.984472 | 0.0575684 |             0.143718  |
|  MIC38 SOUS43 0000038 Majuro South (Airport) Marsha |  0.984364 | 0.0327532 |             0.0805367 |
|  9415020 CA Point Reyes                             |  0.984353 | 0.0566378 |             0.136862  |
|  KWJP8 SOUS43 1820000 Kwajalein Marshall Island     |  0.984303 | 0.0301646 |             0.0829044 |
|  UH806 SOUS00 Nouakchott Mauritania                 |  0.984287 | 0.02889   |             0.0811794 |
|  9411406 CA Oil Platform Harvest                    |  0.984099 | 0.0508167 |             0.107277  |
|  UH420 SOUS00 Saumlaki Indonesia                    |  0.984072 | 0.059144  |             0.124968  |
|  UH094 SOUS00 Matarani Peru                         |  0.983972 | 0.0302882 |             0.0702921 |
|  9410170 CA San Diego San Diego Bay                 |  0.98392  | 0.0525348 |             0.101892  |
|  600 NM West-Northwest of Phuket Thailand           |  0.983449 | 0.0171362 |             0.0473148 |
|  UH345 SOUS00 Nakano Shima Japan                    |  0.983315 | 0.0452681 |             0.0898927 |
|  MIC66 SOUS43 0000066 Pakin East Pohnpei FSM Warni  |  0.98319  | 0.0235129 |             0.0473923 |
|  UH353 SOUS00 GL085 Kushimoto Japan                 |  0.983182 | 0.0371144 |             0.133978  |
|  UH223 SOUS00 GL253 Dakar Senegal                   |  0.983125 | 0.0317752 |             0.0934519 |
|  MIC56 SOUS43 0000056 Fais East(Airport) Yap FSM W  |  0.983093 | 0.0318725 |             0.0931519 |
|  MIC87 SOUS43 0000087 Ebeye Wes Marshall Islands Po |  0.982954 | 0.0311423 |             0.0749312 |
|  MIC86 SOUS43 0000086 Ebeye East Marshall Islands P |  0.982712 | 0.0317272 |             0.0800819 |
|  9418767 CA North Spit                              |  0.982655 | 0.071903  |             0.163207  |
|  MIC29 SOUS43 0000029 Pohnpei North Pohnpei FSM Ma  |  0.98263  | 0.0246963 |             0.0619635 |
|  UH684 SOUS00 GL178 Puerto Montt Chile              |  0.982597 | 0.210455  |             0.475819  |
|  UH035 SOUS00 GL177 San Felix Chile                 |  0.982557 | 0.0269903 |             0.0680322 |
|  9432780 OR Charleston                              |  0.982546 | 0.0812058 |             0.155754  |
|  UH163 SOUS00 GL049 Benoa Indonesia                 |  0.982513 | 0.0597154 |             0.151379  |
|  9414290 CA San Francisco                           |  0.982424 | 0.0683841 |             0.183948  |
|  9414958 CA Bolinas Bolinas Lagoon                  |  0.982351 | 0.0604357 |             0.143844  |
|  MIC37 SOUS43 0000037 Majuro East Marshall Islands  |  0.982254 | 0.0347647 |             0.099942  |
|  9431647 OR Port Orford                             |  0.982063 | 0.0773894 |             0.17036   |
|  UH291 SOUS00 GL263 Ascension United Kingdom of Gre |  0.982033 | 0.0241238 |             0.0757215 |
|  MIC72 SOUS43 0000072 Ujae East (Airport) Marshall  |  0.981866 | 0.0310726 |             0.0734152 |
|  UH084 SOUS00 Lobos de Afuera Peru                  |  0.981834 | 0.0382889 |             0.101184  |
|  9414311 CA San Francisco Pier 1                    |  0.981527 | 0.076334  |             0.213295  |
|  UH082 SOUS00 GL182 Acajutla El Salvador            |  0.981496 | 0.0687006 |             0.167674  |
|  9410665 CA Los Angeles Pier J                      |  0.981478 | 0.0552717 |             0.160732  |
|  APRP7 SOUS43 1630000 Apra HarborGuam               |  0.981454 | 0.0251824 |             0.0751623 |
|  UH166 SOUS00 GL040 Broome Australia                |  0.981268 | 0.236057  |             0.560537  |
|  UH231 SOUS00 GL335 Takoradi Ghana                  |  0.981189 | 0.0353236 |             0.0876975 |
|  UH365 SOUS00 Ishigaki Japan                        |  0.981097 | 0.0403515 |             0.0994687 |
|  9414776 CA Oakland Berth 34                        |  0.981088 | 0.0782811 |             0.199859  |
|  9414863 CA Richmond                                |  0.980807 | 0.0764729 |             0.209034  |
|  UH013 SOUS00 GL145 Kanton Kiribati                 |  0.980667 | 0.0284182 |             0.0832488 |
|  MIC30 SOUS43 0000030 Pohnpei East Pohnpei FSM Maj  |  0.980662 | 0.0269207 |             0.0639969 |
|  902 Japan - Ishigakijima                           |  0.980583 | 0.0404483 |             0.100664  |
|  NSTP6 SOUS43 1770000 Pago Pago American Samoa      |  0.980521 | 0.0324624 |             0.0754824 |
|  9414750 CA Alameda                                 |  0.980244 | 0.08439   |             0.220848  |
|  MIC12 SOUS43 0000012 Guam North (Ritidian) Guam M  |  0.980036 | 0.0246617 |             0.072975  |
|  MIC67 SOUS43 0000067 Mokil East Pohnpei FSM Warni  |  0.97989  | 0.028828  |             0.0757431 |
|  UH002 SOUS00 GL113 Tarawa Bairiki Kiribati         |  0.97985  | 0.040726  |             0.120125  |
|  UH025 SOUS00 GL121 Funafuti Tuvalu                 |  0.979798 | 0.0421963 |             0.120493  |
|  MIC74 SOUS43 0000074 Ailinglaplap East (Airport) M |  0.979718 | 0.0364576 |             0.0960509 |
|  UH142 SOUS00 Langkawi Malaysia                     |  0.979671 | 0.0631553 |             0.188003  |
|  UH171 SOUS00 GL046 Cocos Australia                 |  0.979588 | 0.0267873 |             0.0626461 |
|  9410666 CA Los Angeles Pier 400                    |  0.979428 | 0.058302  |             0.151     |
|  MIC81 SOUS43 0000081 Lamotrek East Yap FSM Popula  |  0.979426 | 0.0263072 |             0.0767573 |
|  UH805 SOUS00 GL323 Vardo Norway                    |  0.979349 | 0.0899998 |             0.202192  |
|  UH333 SOUS00 GL057 Fort Denison Australia          |  0.97931  | 0.0427966 |             0.110138  |
|  9410230 CA La Jolla                                |  0.979274 | 0.0564015 |             0.134945  |
|  8661070 SC Springmaid Pier                         |  0.979151 | 0.0560115 |             0.12521   |
|  MIC08 SOUS43 0000008 Pohnpei FSM UHSLC Gauge       |  0.978891 | 0.0272136 |             0.0622618 |
|  UH789 SOUS00 Prickley Bay Grenada                  |  0.978642 | 0.018227  |             0.050212  |
|  9415338 CA Sonoma Creek Entrance                   |  0.978552 | 0.0884713 |             0.224221  |
|  MIC18 SOUS43 0000018 Saipan West (Garapan) Saipan  |  0.978517 | 0.0237775 |             0.072435  |
|  UH052 SOUS00 GL109 Johnston United States of Ameri |  0.978483 | 0.020467  |             0.0463227 |
|  8519483 NY Bergen Point West Reach                 |  0.97847  | 0.0599066 |             0.160482  |
|  1664 Norway - Ny Alesund                           |  0.978417 | 0.0394555 |             0.0977731 |
|  MIC59 SOUS43 0000059 Satawal East Yap FSM Warning  |  0.978387 | 0.026338  |             0.064834  |
|  9459881 AK King Cove                               |  0.978353 | 0.0789847 |             0.184737  |
|  MIC14 SOUS43 0000014 Rota West (Songsong) Rota Ma  |  0.978225 | 0.0251298 |             0.0744345 |
|  MIC32 SOUS43 0000032 Pohnpei West Pohnpei FSM Maj  |  0.978118 | 0.0270674 |             0.0587077 |
|  MIC34 SOUS43 0000034 Kosrae West (Walung) Kosrae   |  0.977939 | 0.0346048 |             0.0861552 |
|  MIC88 SOUS43 0000088 Ebon East Marshall Islands Po |  0.977698 | 0.0399564 |             0.102901  |
|  9410660 CA Los Angeles                             |  0.977657 | 0.0606262 |             0.168202  |
|  MIC11 SOUS43 0000011 Guam South (Cocos) Guam Mari  |  0.977575 | 0.0259563 |             0.0762036 |
|  MIC36 SOUS43 0000036 Kosrae East (Malem) Kosrae F  |  0.977312 | 0.0359521 |             0.0863562 |
|  9439011 OR Hammond                                 |  0.977069 | 0.10675   |             0.292492  |
|  UH340 SOUS00 Kaohsiung China                       |  0.97698  | 0.0297057 |             0.074605  |
|  MIC57 SOUS43 0000057 Faraulep East Yap FSM Warnin  |  0.976875 | 0.0304291 |             0.0849858 |
|  8531680 NJ Sandy Hook                              |  0.976812 | 0.0577313 |             0.20197   |
|  UH351 SOUS00 GL087 Ofunato Japan                   |  0.976788 | 0.039591  |             0.137886  |
|  UH317 SOUS00 Ensenada Mexico                       |  0.976625 | 0.0579813 |             0.116926  |
|  MIC31 SOUS43 0000031 Pohnpei South Pohnpei FSM Ma  |  0.976571 | 0.0291305 |             0.0635555 |
|  MIC19 SOUS43 0000019 Saipan North Saipan Marianas  |  0.976526 | 0.0233345 |             0.0678176 |
|  MIC79 SOUS43 0000079 Eurapik East Yap FSM Populat  |  0.976499 | 0.0349937 |             0.105854  |
|  1497 Korea - Busan                                 |  0.976356 | 0.0395789 |             0.141779  |
|  9439040 OR Astoria                                 |  0.976324 | 0.111262  |             0.34918   |
|  9446484 WA Tacoma                                  |  0.976165 | 0.142847  |             0.46258   |
|  MIC68 SOUS43 0000068 Pingelap East Pohnpei FSM Wa  |  0.976106 | 0.033146  |             0.0800004 |
|  UH023 SOUS00 GL139 Rarotonga Cook Islands (the)    |  0.976067 | 0.0270948 |             0.0625027 |
|  UH108 SOUS00 GL028 Male Maldives                   |  0.976017 | 0.0248904 |             0.0561817 |
|  UH913 SOUS00 Telukdalam Indonesia                  |  0.975971 | 0.0236409 |             0.051325  |
|  8518750 NY The Battery                             |  0.975753 | 0.0605921 |             0.159113  |
|  MIC13 SOUS43 0000013 Rota East (Sinapalu) Rota Ma  |  0.97549  | 0.0248105 |             0.0735267 |
|  MIC65 SOUS43 0000065 Sapwuafik (Ngatik) East Pohnp |  0.975452 | 0.0293059 |             0.0647208 |
|  MIC33 SOUS43 0000033 Kosrae North (Airport) Kosrae |  0.975362 | 0.0366198 |             0.0947907 |
|  UH352 SOUS00 GL086 Mera Japan                      |  0.975193 | 0.0413879 |             0.102812  |
|  9415056 CA Point Pinole                            |  0.974642 | 0.0950525 |             0.225747  |
|  UH109 SOUS00 GL027 Gan Maldives                    |  0.974451 | 0.0279986 |             0.0652569 |
|  MIC35 SOUS43 0000035 Kosrae South (Utwa Ma) Kosrae |  0.974426 | 0.0378248 |             0.0958491 |
|  MIC15 SOUS43 0000015 Tinian East Tinian Marianas   |  0.974354 | 0.0235278 |             0.0746437 |
|  9461380 Adak Island AK                             |  0.973757 | 0.0621239 |             0.143953  |
|  9461380 AK Adak Island                             |  0.973349 | 0.0626036 |             0.131806  |
|  UH382 SOUS00 Subic Bay Philippines (the)           |  0.973203 | 0.039253  |             0.0849414 |
|  9462450 AK Nikolski                                |  0.973031 | 0.0738353 |             0.155757  |
|  9447214 WA Shilshole Bay GPS Buoy                  |  0.972756 | 0.143094  |             0.39      |
|  878 USA - Fort_Pulaski_GA                          |  0.972492 | 0.0859897 |             0.218455  |
|  9447130 WA Seattle Puget Sound                     |  0.972455 | 0.146143  |             0.408704  |
|  9455920 AK Anchorage                               |  0.972439 | 0.295185  |             0.745391  |
|  MIC82 SOUS43 0000082 Oroluk East Pohnpei FSM Popu  |  0.972244 | 0.027655  |             0.0602034 |
|  9435380 OR South Beach                             |  0.97168  | 0.110686  |             0.421701  |
|  UH107 SOUS00 GL045 Padang Indonesia                |  0.971145 | 0.035776  |             0.0781722 |
|  MIC58 SOUS43 0000058 Woleai East Yap FSM Warning   |  0.970933 | 0.036463  |             0.103009  |
|  UH173 SOUS00 GL277 Davis Australia                 |  0.970922 | 0.0588502 |             0.16957   |
|  9414575 CA Coyote Creek                            |  0.970795 | 0.129481  |             0.370254  |
|  UH419 SOUS00 Lembar Indonesia                      |  0.970615 | 0.0503133 |             0.129325  |
|  UH822 SOUS00 GL242 Brest France                    |  0.970577 | 0.192198  |             0.387553  |
|  8724580 FL Key West                                |  0.970487 | 0.0236851 |             0.0581885 |
|  UH370 SOUS00 GL073 Manila Philippines (the)        |  0.970441 | 0.0450563 |             0.103632  |
|  UH004 SOUS00 GL114 Nauru Nauru                     |  0.970397 | 0.0483139 |             0.129887  |
|  UH113 SOUS00 Masirah Oman                          |  0.97023  | 0.070627  |             0.173867  |
|  MIC80 SOUS43 0000080 Ifalik East Yap FSM Populate  |  0.970191 | 0.0359534 |             0.0947567 |
|  UH019 SOUS00 GL123 Noumea France                   |  0.969685 | 0.0439366 |             0.0915047 |
|  8418150 ME Portland                                |  0.969336 | 0.143281  |             0.391062  |
|  UH016 SOUS00 GL138 Rikitea France                  |  0.969153 | 0.0328777 |             0.0695575 |
|  UH162 SOUS00 GL291 Cilicap Indonesia               |  0.968971 | 0.0585131 |             0.171869  |
|  UH542 SOUS00 GL156 Tofino Canada                   |  0.968783 | 0.112472  |             0.296602  |
|  8658163 NC Wrightsville Beach                      |  0.968132 | 0.0567568 |             0.134434  |
|  UH034 SOUS00 GL161 Cabo San Lucas Mexico           |  0.967483 | 0.0491821 |             0.118197  |
|  8423898 NH Fort Point                              |  0.967474 | 0.14251   |             0.400059  |
|  8443970 MA Boston                                  |  0.966809 | 0.149413  |             0.333506  |
|  UH041 SOUS00 GL102 Dutch Harbor AK United States   |  0.965969 | 0.0824484 |             0.185304  |
|  UH878 SOUS00 Bullen Bay Curacao                    |  0.965769 | 0.017067  |             0.0513423 |
|  UH257 SOUS00 GL211 Settlement Point Bahamas (the)  |  0.965553 | 0.0398581 |             0.0857348 |
|  UH803 SOUS00 GL234 Rorvik Norway                   |  0.965252 | 0.0814454 |             0.171074  |
|  UH117 SOUS00 Hanimaadhoo Maldives                  |  0.965124 | 0.03433   |             0.0882178 |
|  1612480 HI Mokuoloe                                |  0.964618 | 0.0310062 |             0.108004  |
|  UH021 SOUS00 GL176 Juan Fernandez Chile            |  0.964468 | 0.0436247 |             0.094569  |
|  MIC62 SOUS43 0000062 Fananu East Chuuk FSM Warnin  |  0.964263 | 0.0279742 |             0.0523595 |
|  UH654 SOUS00 Currimao Philippines (the)            |  0.963919 | 0.0322967 |             0.0988286 |
|  8413320 ME Bar Harbor                              |  0.963887 | 0.177698  |             0.404716  |
|  8665530 SC Charleston Cooper River E               |  0.963366 | 0.0768112 |             0.186322  |
|  1715 USA - Cutler Farris Wharf, ME                 |  0.96317  | 0.228115  |             0.564829  |
|  9455920 Anchorage AK                               |  0.963026 | 0.343766  |             0.871177  |
|  8726607 FL Old Port Tampa                          |  0.962968 | 0.0364107 |             0.103289  |
|  9444900 WA Port Townsend                           |  0.962883 | 0.134155  |             0.302147  |
|  UH115 SOUS00 GL033 Colombo Sri Lanka               |  0.962658 | 0.0237604 |             0.0625545 |
|  9415144 CA Port Chicago                            |  0.962599 | 0.144911  |             0.352341  |
|  UH153 SOUS00 GL029 Minicoy India                   |  0.962457 | 0.0416043 |             0.125023  |
|  9461710 AK Atka                                    |  0.962281 | 0.0724945 |             0.189113  |
|  UH104 SOUS00 GL026 Diego Garcia United Kingdom of  |  0.961658 | 0.0469184 |             0.106394  |
|  UH271 SOUS00 Fort de France France                 |  0.961491 | 0.0176773 |             0.0562999 |
|  UH294 SOUS00 GL241 Newlyn Cornwall United Kingdom  |  0.961464 | 0.186669  |             0.406895  |
|  8727520 FL Cedar Key                               |  0.961308 | 0.0653465 |             0.181855  |
|  UH777 SOUS00 Puerto Plata Dominican Republic (the) |  0.961194 | 0.0268182 |             0.072285  |
|  1586 New Zealand - Christchurch                    |  0.960055 | 0.120942  |             0.304741  |
|  UH833 SOUS00 GL224 Nain Canada                     |  0.959908 | 0.0880385 |             0.177759  |
|  9415102 CA Martinez-Amorco Pier                    |  0.958621 | 0.142652  |             0.329028  |
|  9440569 WA Skamokawa                               |  0.958496 | 0.117452  |             0.272567  |
|  UH114 SOUS00 GL004 Salalah Oman                    |  0.958445 | 0.0667833 |             0.178036  |
|  UH261 SOUS00 Charleston SC United States of Ameri  |  0.957879 | 0.0822735 |             0.193143  |
|  8723214 FL Virginia Key                            |  0.957697 | 0.0369079 |             0.0940398 |
|  UH009 SOUS00 GL066 Honiara Solomon Islands         |  0.957416 | 0.0375689 |             0.0843021 |
|  UH147 SOUS00 GL030 Karachi Pakistan                |  0.957182 | 0.0960994 |             0.22158   |
|  9752619 PR Isabel Segunda Vieques Is               |  0.957017 | 0.0190911 |             0.0634456 |
|  8410140 ME Eastport                                |  0.956669 | 0.323196  |             0.722981  |
|  8467150 CT Bridgeport                              |  0.956622 | 0.125371  |             0.370707  |
|  UH259 SOUS00 GL221 Bermuda United Kingdom of Great |  0.95604  | 0.0407382 |             0.101514  |
|  UH290 SOUS00 GL305 Port Stanley United Kingdom of  |  0.955856 | 0.0615473 |             0.128364  |
|  UH177 SOUS00 GL022 Mawson Australia                |  0.955729 | 0.0541846 |             0.174233  |
|  9759938 PR Mona Island                             |  0.955027 | 0.0163485 |             0.0363891 |
|  1619910 HI Sand Island Midway Island               |  0.954565 | 0.0222557 |             0.0521751 |
|  UH600 SOUS00 GL181 Ushuaia Argentina               |  0.953799 | 0.106999  |             0.257941  |
|  UH049 SOUS00 GL104 Minamitorishima Japan           |  0.953573 | 0.0242734 |             0.054018  |
|  MIC26 SOUS43 0000026 Chuuk Lagoon East Chuuk FSM   |  0.953498 | 0.0331601 |             0.0681482 |
|  1611400 HI Nawiliwili                              |  0.953291 | 0.0325376 |             0.119223  |
|  MIC64 SOUS43 0000064 Lukunor East Chuuk FSM Warni  |  0.953232 | 0.0357086 |             0.0728028 |
|  UH071 SOUS00 GL101 Wellington New Zealand          |  0.952199 | 0.0834488 |             0.233262  |
|  MIC10 SOUS43 0000010 Moen I Chuuk FSM Historic CO  |  0.951951 | 0.0334394 |             0.0675217 |
|  UH799 SOUS00 GL209 Portu-Prince Haiti              |  0.951861 | 0.0211121 |             0.0575392 |
|  UH364 SOUS00 GL088 Hakodate Japan                  |  0.951423 | 0.033913  |             0.0815448 |
|  UH029 SOUS00 GL117 Kapingamarangi Micronesia (Fede |  0.9507   | 0.0407434 |             0.0821637 |
|  8537121 NJ Ship John Shoal                         |  0.950451 | 0.110347  |             0.342462  |
|  UH130 SOUS00 GL278 Casey Australia                 |  0.950381 | 0.0759645 |             0.209599  |
|  1617433 HI Kawaihae                                |  0.950293 | 0.0363478 |             0.118943  |
|  9449880 WA Friday Harbor                           |  0.950015 | 0.148609  |             0.409393  |
|  UH105 SOUS00 GL019 Rodrigues Mauritius             |  0.949673 | 0.0454421 |             0.0990593 |
|  MIC63 SOUS43 0000063 Losap East Chuuk FSM Warning  |  0.949634 | 0.0350726 |             0.070547  |
|  MIC27 SOUS43 0000027 Chuuk Lagoon North Chuuk FSM  |  0.949381 | 0.0339351 |             0.0677573 |
|  9751381 VI Lameshur Bay St John                    |  0.949084 | 0.0170164 |             0.038225  |
|  UH273 SOUS00 Port-aux-basques Canada               |  0.949083 | 0.0591986 |             0.153939  |
|  8461490 CT New London                              |  0.948764 | 0.0561384 |             0.13107   |
|  UH286 SOUS00 GL190 Puerto Deseado Argentina        |  0.948537 | 0.27701   |             0.565435  |
|  8760922 LA Pilots Station East S.W.                |  0.948512 | 0.0305726 |             0.0664071 |
|  9752695 PR Esperanza Vieques Island                |  0.948456 | 0.0169306 |             0.0400787 |
|  9464212 St Paul Island AK                          |  0.947976 | 0.0822145 |             0.253367  |
|  UH275 SOUS00 GL222 Halifax Canada                  |  0.946108 | 0.0822587 |             0.175743  |
|  UH221 SOUS00 GL268 Simon's Town South Africa       |  0.945952 | 0.0624616 |             0.199195  |
|  UH093 SOUS00 GL173 Callao Peru                     |  0.945928 | 0.0472262 |             0.104255  |
|  8722670 FL Lake Worth Pier Atlantic                |  0.94583  | 0.0506965 |             0.130645  |
|  UH738 SOUS00 Santa Marta Colombia                  |  0.945617 | 0.0218671 |             0.0635265 |
|  9759394 PR Mayaguez                                |  0.94539  | 0.021048  |             0.055405  |
|  8658120 NC Wilmington                              |  0.944595 | 0.0853223 |             0.239057  |
|  UH179 SOUS00 GL024 Saint Paul France               |  0.943474 | 0.0565788 |             0.128068  |
|  UH119 SOUS00 GL002 Djibouti Djibouti               |  0.942574 | 0.0927783 |             0.255181  |
|  1336 Norway - Maloy                                |  0.942068 | 0.077974  |             0.159411  |
|  UH122 SOUS00 Sibolga Indonesia                     |  0.941356 | 0.0427524 |             0.100548  |
|  UH350 SOUS00 GL089 Kushiro Japan                   |  0.941284 | 0.0625608 |             0.128898  |
|  1612340 HI Honolulu                                |  0.939537 | 0.0375992 |             0.123012  |
|  UH266 SOUS00 GL208 Cristobal Panama                |  0.938644 | 0.0247216 |             0.0528772 |
|  9758053 PR Penuelas                                |  0.93812  | 0.0186273 |             0.0465247 |
|  9754228 PR Yabucoa Harbor                          |  0.937718 | 0.0185656 |             0.0424909 |
|  9465261 Nushagak Bay                               |  0.93765  | 0.403124  |             0.919132  |
|  MIC28 SOUS43 0000028 Chuuk Lagoon West Chuuk FSM   |  0.937425 | 0.0382518 |             0.0781763 |
|  8726384 FL Port Manatee                            |  0.937358 | 0.0414567 |             0.134577  |
|  MIC61 SOUS43 0000061 Ulul East Chuuk FSM Warning   |  0.936977 | 0.0374154 |             0.084202  |
|  UH316 SOUS00 GL267 Acapulco Gro. Mexico            |  0.936724 | 0.051468  |             0.11791   |
|  UH347 SOUS00 GL327 Abashiri Japan                  |  0.93668  | 0.0576025 |             0.118865  |
|  UH824 SOUS00 GL205 Marseille France                |  0.936477 | 0.0118287 |             0.0220963 |
|  8725110 FL Naples Gulf of Mexico                   |  0.93626  | 0.0506805 |             0.13449   |
|  8452944 RI Conimicut Light                         |  0.935517 | 0.0706732 |             0.200924  |
|  8721604 FL Trident Pier Port Canaver               |  0.935496 | 0.0694779 |             0.171659  |
|  UH808 SOUS00 GL343 Thule (Pituffik) Denmark        |  0.934919 | 0.117218  |             0.316296  |
|  UH383 SOUS00 Vung Tau Viet Nam                     |  0.934483 | 0.156029  |             0.368097  |
|  UH181 SOUS00 GL013 Durban South Africa             |  0.934442 | 0.0762554 |             0.177169  |
|  MIC60 SOUS43 0000060 Puluwat East Chuuk FSM Warni  |  0.933897 | 0.0403313 |             0.0850587 |
|  UH121 SOUS00 GL339 Pt. La Rue Seychelles           |  0.933498 | 0.0634192 |             0.140712  |
|  UH335 SOUS00 GL056 Spring Bay Australia            |  0.932227 | 0.0626311 |             0.125963  |
|  9759110 PR Magueyes Island                         |  0.930383 | 0.0197902 |             0.0427704 |
|  9465601 Carter Bay Kuskokwim Bay AK                |  0.929722 | 0.262279  |             0.618652  |
|  UH547 SOUS00 Barbers Point HI United States of Am  |  0.928889 | 0.0403581 |             0.123973  |
|  8454000 RI Providence                              |  0.928079 | 0.077137  |             0.217648  |
|  UH047 SOUS00 GL103 Chichijima Japan                |  0.92733  | 0.0460842 |             0.0956659 |
|  8454049 RI Quonset Point                           |  0.923787 | 0.0726132 |             0.220809  |
|  8720218 FL Mayport (Bar Pilots Dock)               |  0.922631 | 0.111229  |             0.230308  |
|  8775870 TX Bob Hall Pier Corpus Chri               |  0.921457 | 0.0429425 |             0.110464  |
|  9761115 Barbuda                                    |  0.921272 | 0.0199928 |             0.067485  |
|  UH220 SOUS00 GL314 Walvis Bay Namibia              |  0.920349 | 0.0706876 |             0.185809  |
|  8449130 MA Nantucket Island                        |  0.919734 | 0.0877802 |             0.252982  |
|  UH276 SOUS00 GL223 St. John's Canada               |  0.919554 | 0.0749416 |             0.148285  |
|  8551910 DE Reedy Point                             |  0.918987 | 0.139136  |             0.464594  |
|  8779748 TX South Padre Island CG Stat              |  0.918685 | 0.0380765 |             0.0833569 |
|  8726667 FL Mckay Bay Entrance                      |  0.91817  | 0.0549774 |             0.174532  |
|  UH184 SOUS00 GL076 Port Elizabeth South Africa     |  0.917718 | 0.0790001 |             0.216729  |
|  UH129 SOUS00 GL055 Portland S.Aus. Australia       |  0.917361 | 0.0601514 |             0.13934   |
|  UH268 SOUS00 Limon Costa Rica                      |  0.916144 | 0.029192  |             0.0699651 |
|  UH331 SOUS00 GL058 Brisbane Australia              |  0.915265 | 0.133404  |             0.29355   |
|  UH699 SOUS00 GL044 Tanjong Pagar Singapore         |  0.914109 | 0.12136   |             0.250729  |
|  8551762 DE Delaware City                           |  0.91178  | 0.147557  |             0.457887  |
|  8656483 NC Beaufort Duke Marine Lab                |  0.908152 | 0.0912729 |             0.24057   |
|  UH836 SOUS00 GL333 Alert Canada                    |  0.907769 | 0.0431127 |             0.110079  |
|  UH829 SOUS00 GL340 Trieste Italy                   |  0.902588 | 0.0715318 |             0.178173  |
|  UH024 SOUS00 GL143 Penrhyn Cook Islands (the)      |  0.902063 | 0.0172479 |             0.0308124 |
|  UH180 SOUS00 GL023 Kerguelen France                |  0.899829 | 0.0932169 |             0.235741  |
|  UH737 SOUS00 San Andres Colombia                   |  0.898535 | 0.0286867 |             0.0636801 |
|  8729108 FL Panama City                             |  0.895661 | 0.0467452 |             0.132657  |
|  UH103 SOUS00 GL018 Port Louis Mauritius            |  0.894254 | 0.0291289 |             0.0832069 |
|  UH601 SOUS00 GL185 Esperanza Argentina             |  0.891089 | 0.163668  |             0.346685  |
|  UH906 SOUS00 GL141 Moulmein Myanmar                |  0.890873 | 0.399794  |             1.27775   |
|  UH680 SOUS00 GL130 Macquarie Is. Australia         |  0.890852 | 0.0661095 |             0.177936  |
|  8735391 AL Dog River Bridge                        |  0.889144 | 0.0514216 |             0.132019  |
|  UH700 SOUS00 GL188 Faraday Antarctica              |  0.88876  | 0.11852   |             0.240379  |
|  UH164 SOUS00 GL017 Reunion France                  |  0.88247  | 0.0254543 |             0.0614947 |
|  UH334 SOUS00 GL060 Townsville Australia            |  0.881257 | 0.189234  |             0.512896  |
|  8729210 FL Panama City Beach                       |  0.880488 | 0.0484019 |             0.135582  |
|  8720030 FL Fernandina Beach                        |  0.878827 | 0.157034  |             0.356106  |
|  UH079 SOUS00 GL128 Chatham New Zealand             |  0.878324 | 0.0962947 |             0.196909  |
|  8737048 AL Mobile State Docks                      |  0.877718 | 0.0551903 |             0.132063  |
|  9465374 Snag Point Dillingham AK                   |  0.874852 | 0.576274  |             1.51169   |
|  8548989 PA Newbold                                 |  0.874556 | 0.224111  |             0.590231  |
|  8539094 NJ Burlington Delaware River               |  0.874343 | 0.208586  |             0.569401  |
|  8536110 NJ Cape May                                |  0.869678 | 0.148617  |             0.362073  |
|  8540433 PA Marcus Hook                             |  0.866886 | 0.180617  |             0.444385  |
|  UH189 SOUS00 GL131 Dumont d'Urville Antarctica     |  0.865617 | 0.119251  |             0.278347  |
|  8545240 PA Philadelphia                            |  0.863121 | 0.18598   |             0.453582  |
|  8538886 NJ Tacony-Palmyra Bridge                   |  0.861729 | 0.198195  |             0.485473  |
|  8510560 NY Montauk                                 |  0.846961 | 0.0693028 |             0.151275  |
|  UH920 SOUS00 GL020 Marion Island South Africa      |  0.842999 | 0.0517556 |             0.137609  |
|  8764044 LA Berwick Atchafalaya River               |  0.829744 | 0.04028   |             0.0862479 |
|  UH349 SOUS00 GL325 Toyama Japan                    |  0.829562 | 0.0274055 |             0.0672347 |
|  UH360 SOUS00 GL324 Wakkanai Japan                  |  0.825119 | 0.0377136 |             0.0886547 |
|  8723970 FL Vaca Key Florida Bay                    |  0.825034 | 0.0486105 |             0.130517  |
|  8573927 MD Chesapeake City                         |  0.824707 | 0.103522  |             0.332704  |
|  UH280 SOUS00 GL195 Ilha Fiscal RJ Brazil           |  0.814786 | 0.0751653 |             0.156834  |
|  UH015 SOUS00 GL140 Papeete France                  |  0.814736 | 0.0202472 |             0.0524582 |
|  UH175 SOUS00 GL053 Fremantle Australia             |  0.808553 | 0.0705099 |             0.199573  |
|  8570283 MD Ocean City Inlet                        |  0.803109 | 0.107383  |             0.275988  |
|  8760721 LA Pilottown                               |  0.798984 | 0.0265996 |             0.0549983 |
|  8571892 MD Cambridge                               |  0.795176 | 0.0797275 |             0.202495  |
|  8764227 LA LAWMA Amerada Pass                      |  0.788282 | 0.0592564 |             0.113689  |
|  8447930 MA Woods Hole                              |  0.787078 | 0.0610164 |             0.164261  |
|  8770777 TX Manchester                              |  0.785593 | 0.0653156 |             0.145802  |
|  8594900 DC Washington                              |  0.783657 | 0.10987   |             0.306586  |
|  UH178 SOUS00 GL021 Crozet France                   |  0.769848 | 0.0454331 |             0.131625  |
|  UH731 SOUS00 GL191 Puerto Madryn Argentina         |  0.769132 | 1.4642    |             6.5365    |
|  8770520 TX Rainbow Bridge                          |  0.761759 | 0.0402858 |             0.0928936 |
|  8651370 NC Duck                                    |  0.726017 | 0.138314  |             0.364032  |
|  8747437 MS Bay Waveland Yacht Club                 |  0.711035 | 0.0704647 |             0.171352  |
|  8574680 MD Baltimore Fort McHenry P                |  0.696343 | 0.0765981 |             0.195937  |
|  8632200 VA Kiptopeke                               |  0.692878 | 0.124102  |             0.301073  |
|  UH128 SOUS00 GL308 Thevenard Australia             |  0.689189 | 0.18808   |             0.480337  |
|  8637689 VA Yorktown USCG Training Cen              |  0.689035 | 0.121455  |             0.335074  |
|  8771341 TX Galveston Bay Entrance No               |  0.686482 | 0.0981925 |             0.165257  |
|  UH176 SOUS00 GL054 Esperance Australia             |  0.680181 | 0.098587  |             0.262453  |
|  1019 Australia - Thevenard_AU                      |  0.679857 | 0.191011  |             0.490789  |
|  8639348 VA Money Point                             |  0.673392 | 0.137069  |             0.35992   |
|  UH825 SOUS00 GL284 Cuxhaven Germany                |  0.668327 | 0.473352  |             1.2807    |
|  8771013 TX Eagle Point Galveston Bay               |  0.666435 | 0.0711022 |             0.158245  |
|  8770822 TX Texas Point Sabine Pass                 |  0.665377 | 0.110875  |             0.330447  |
|  8638863 VA Chesapeake Bay Bridge Tunn              |  0.634975 | 0.137229  |             0.357743  |
|  8762075 LA Port Fourchon Belle Pass                |  0.572463 | 0.0636869 |             0.248839  |
|  8638610 VA Sewells Point                           |  0.571141 | 0.145734  |             0.429348  |
|  8770475 TX Port Arthur                             |  0.567437 | 0.0665068 |             0.163197  |
|  8571421 MD Bishops Head                            |  0.546008 | 0.124255  |             0.220904  |
|  8662245 SC Oyster Landing (N Inlet Es              |  0.545056 | 0.152445  |             0.330326  |
|  8635750 VA Lewisetta                               |  0.511213 | 0.0788477 |             0.180457  |
|  8577330 MD Solomons Island                         |  0.497736 | 0.0860068 |             0.211296  |
|  8573364 MD Tolchester Beach                        |  0.483866 | 0.107001  |             0.312795  |
|  8775283 TX Port Inglesid                           |  0.477422 | 0.0416499 |             0.0800903 |
|  9468756 Nome AK                                    |  0.462041 | 0.175147  |             0.435874  |
|  952 USA - Nome_AK                                  |  0.443485 | 0.178455  |             0.446922  |
|  UH729 SOUS00 GL192 Mar del Plata Argentina         |  0.441324 | 0.289598  |             0.591083  |
|  9468132 St. Michael                                |  0.383309 | 0.348248  |             0.777338  |
|  9497645 Prudhoe Bay AK                             |  0.373139 | 0.0888854 |             0.193074  |
|  UH348 SOUS00 GL326 Hamada Japan                    |  0.358979 | 0.0683626 |             0.114633  |
|  UH579 SOUS00 GL151 Prudhoe Bay AK United States o  |  0.358001 | 0.0901208 |             0.193902  |
|  8761305 LA Shell Beach                             |  0.339369 | 0.10615   |             0.207923  |
|  8774770 TX Rockport                                |  0.329287 | 0.0292557 |             0.0720767 |
|  8652587 NC Oregon Inlet Marina                     |  0.327165 | 0.0886346 |             0.242724  |
|  9468333 Unalakleet AK                              |  0.312376 | 0.411314  |             0.862939  |
|  8654467 NC USCG Station Hatteras                   |  0.307299 | 0.0386183 |             0.129696  |
|  8774513 TX Copano Bay                              |  0.22794  | 0.0298147 |             0.0634557 |
|  8636580 VA Windmill Point                          |  0.180886 | 0.0871494 |             0.16705   |
|  UH804 SOUS00 GL321 Tregde Norway                   | -0.417247 | 0.0642007 |             0.123357  |
|  UH818 SOUS00 Smogen Sweden                         | -0.849486 | 0.0777886 |             0.144389  |
|  9491094 Red Dog Dock AK                            | -0.98406  | 0.249918  |             0.379356  |
|  UH819 SOUS00 GL233 Goteborgorsh. Sweden            | -1.35833  | 0.0861948 |             0.197229  |
|  8761927 LA New Canal Station                       | -1.42712  | 0.0885268 |             0.169785  |
|  UH826 SOUS00 GL341 Stockholm Sweden                | -1.60811  | 0.0479952 |             0.123528  |


### Disclaimer
This program is under experimental development. The results should not be used for navigational purposes or emergency planning under any circumstances. Please do not duplicate and use the result figures from this website without permission.
