# MUCNumbers

Collected Munich and Bavaria Corona numbers from 2020-02-28 until today. Updated daily.

### DOI

[![DOI](https://zenodo.org/badge/507026399.svg)](https://zenodo.org/badge/latestdoi/507026399)

### License

**Creative Commons Zero v1.0 Universal**

### History

The Numbers file was originally created by [Georg Zoche](https://twitter.com/georgzoche). He shared it with me in June 2020, so I could try some more things I wanted to do with the numbers. Since then I have more or less completely changed the file to its current state by adding a lot of new columns, data, formulas and graphs. I have been sharing these graphs on Twitter since July 2020 and continue to do so every day, now under the [@CoronaMUC](https://twitter.com/CoronaMUC) Twitter account. The Numbers file is freely (CC0 licensed) available at [this page](https://www.icloud.com/numbers/0tPTegqlj4Q2SZ7PysUbTt-gQ#MUCNumbersCorona), which also offers export as Excel file and other formats.

### Sources

These numbers are sourced from

- RKI
  - [Source 1 for recovered numbers](https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/45258e51f57d43efb612f700a876ae8f_0/explore?filters=eyJMYW5ka3JlaXMiOlsiU0sgTfxuY2hlbiJdfQ%3D%3D) Updated daily in the morning. Only contains rows for days with new cases. So I have to manually add empty rows for 2020-02-29, 2020-03-01, 2020-03-07, 2020-03-08, 2020-06-01, 2020-12-25, 2022-06-11 every time.
  - [Source 2 for total case numbers](https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/6d78eb3b86ad4466a8e264aa2e32a2e4_0/explore?filters=eyJCdW5kZXNsYW5kSWQiOls5LDldLCJBZG1Vbml0SWQiOls5MTYyLDkxNjJdfQ%3D%3D) Updated daily in the morning
  - [Source 3 for vaccination numbers](https://github.com/robert-koch-institut/COVID-19-Impfungen_in_Deutschland) Updated monday-saturday around 10:00 in the morning
  - [Source 4 for hospitalisation numbers](https://github.com/robert-koch-institut/COVID-19-Hospitalisierungen_in_Deutschland) updated daily after midnight
- [LGL](https://www.lgl.bayern.de/gesundheit/infektionsschutz/infektionskrankheiten_a_z/coronavirus/karte_coronavirus/index.htm#) for hospital and test numbers - updated daily 8:00 for new 7 day sum of hospitalisation and ICU, monday-friday 14:00 for total bed numbers
- [City of Munich](https://stadt.muenchen.de/infos/corona-fallzahlen-muenchen.html) for Munich specific hospital and vaccination numbers - updated monday-friday around 14:00
- [LMU StaBLab](https://corona.stat.uni-muenchen.de/nowcast/) for Nowcast, R(t) and detailed hospitalisation data with corrections (no updates since 2022-06-10, new numbers earliest 2022-06-29)

The daily CSV is exported from [this spreadsheet](https://www.icloud.com/numbers/0tPTegqlj4Q2SZ7PysUbTt-gQ#MUCNumbersCorona) which contains all the formulas and adds a lot of nice looking graphs.

At around 15:00 CET (earlier on weekends) all updates should be added and the export is run. The new file will be committed here and the previous file will be moved to the folder **archive**. 

### ChangeLog

| DATE | CHANGE |
| --- | --- |
| 2023-04-08 | RKI stops publishing daily vaccination numbers |
| 2023-04-01 | LGL stops publishing IVENA number of total hospital beds |
| 2023-03-06 | City of Munich stops publishing hospitalisation numbers |
| 2022-12-28 | City of Munich stops publishing vaccination numbers |
| 2022-12-16 | No more internal case numbers from City of Munich |
| 2022-07-12 | New columns New Hosp Day BAV, New Hosp Nowcast, Diff Hosp % |
| 2022-07-06 | Added new column R(t) with LMU number |
| 2022-07-04 | Added new column with corrected 7D Hospitalisation incidence |
| 2022-07-03 | Added new column LGL 7D CORR with corrected 7 day hospitalisation numbers from RKI |
| 2022-07-01 | New formula for a better R(t) 4 days and R(t) 7 days |
| 2022-06-29 | New column and graph with ratio of ICU on total hospital beds |
| 2022-06-25 | Changed Naive R4 column to Naive R(t) with new formula to estimate R(t) |
| 2022-06-22 | By adding quarterly numbers of health insurances, a big jump in vaccination numbers |
| 2022-06-21 | Added more 7d hospital numbers from RKI |
| 2022-06-13 | City no longer reports own numbers, only RKI numbers. No more numbers on Active Cases, recovered, corrections. So it has become impossible to calculate a 7 day incidence with the city numbers. |
| 2022-05-02 | LGL no longer offers daily test numbers, only weekly updates on Thursday |
| 2022-05-01 | RKI no longer offers granular data in their excel sheet, only total sums of vaccinations |
| 2022-04-29 | LGL no longer reports numbers to RKI on weekend and bank holidays.  |
| 2022-04-28 | RKI changed method of counting for vaccinations, shifting numbers from first to 2nd/3rd vaccination. RKI also added data on 4th vaccination |
| 2022-04-10 | City of Munich adds 4th vaccination |
| 2021-08-31 | LGL adds hospital numbers |
| 2021-01-09 | City of Munich adds vaccination numbers |
| 2020-12-27 | LGL adds vaccination numbers |
| 2020-09-30 | City of Munich adds hospital numbers |
| 2020-06-01 | LGL added daily test numbers |

### Columns in the CSV File

| COLUMN | DESCRIPTION |
| --- | --- |
| Date | Date |
| Day | Readable date |
| MUC Total | Total cases based on numbers from the City of Munich, switched 2022-06-10 to RKI Total |
| Active Cases | Current active cases |
| MUC Recovered | Total sum of recovered people |
| Deaths (sum) | Total number of deaths |
| MUC New Infections | New infections per day from City of Munich (no more updates since 2022-06-10) |
| Correction | (obsolete) |
| RKI New Infections | New infections per day from RKI |
| Diff MUC RKI | Difference between Munich and RKI numbers (no more updates since 2022-06-10) |
| Diff same day last week | Difference between same day this and last week (%) |
| Active Cases (change) | Change in active cases compared to day before |
| Recovered (change) | Change in recovered compared to day before |
| Death (change) | Change in # of deaths compared to day before |
| MUC 7 Day sum | 7 day sum with numbers of City of Munich (no more updates since 2022-06-10) |
| RKI 7 day sum | 7 day sum using RKI new infection |
| DIFF 7DI | Difference 7 Day Incidence corrected/uncorrected |
| RKI 7 Day Incidence | Corrected RKI Incidence |
| Official RKI 7D Inc | Official (uncorrected) RKI Incidence |
| To 10, To 35, To 50, To 100 | Cases needed to get below/above specific incidence |
| Test Pos Rate BY | Positivity rate of PCR tests Bavaria |
| Daily Tests BY | PCR tests daily Bavaria |
| Daily Test BY Pos | # of positive tests in Bavaria, daily |
| Daily test avg 7 days | 7 day average pf daily PCR tests in Bavaria |
| Beds | # of hospital beds with COVID patients in Munich |
| IMC | # of intermediate medical care beds with COVID patients in Munich |
| ICU | # of intensive care beds with COVID patients in Munich |
| Diff 7 Day Incidence | Difference between Munich and RKI 7 day incidence (no more updates since 2022-06-10) |
| Naive R(t) 4D | Total cases of last 4 days divided by total of 4 days before |
| Naive R(t) 7D | Total cases of last 7 days divided by total of 7 days before moved by 3 days |
| Diff 7D DoD | Change of 7 day sum compared to day before (%) |
| Diff 7D WoW | Change of 7 day sum compared to week before (%) |
| Var Lab WoW | Difference in PCR Tests compared to week before |
| Active WoW | Change in Active Cases compared to week before |
| RKI Total | Total sum of infected with RKI numbers |
| Diff Total | Difference between infection numbers Munich and RKI (no more updates since 2022-06-10) |
| RKI 7D Diff last week | Difference current 7 Day Sum to week before |
| 7D avg weekly chg | 7 Day average of weekly change |
| BAV 1st Vacc Total | Total of 1st vaccination Bavaria |
| BAV 2nd Vacc Total | Total of 2nd vaccination Bavaria |
| BAV 3rd Vacc Total | Total of 3rd (booster)  vaccination Bavaria |
| BAV 4th Vacc Total | Total of 4th (2nd booster) vaccination Bavaria |
| BAV 1st Vacc % | Percentage of poulation with 1st vaccine in Bavaria |
| BAV 1st Vacc Day | 1st vaccination administered per day in Bavaria |
| BAV 1st Vacc Avg | 7 day average of 1st vaccination in Bavaria |
| BAV 1st Vacc 7D | 7 day sum of 1st vaccination in Bavaria |
| BAV 2nd Vacc % | Percentage of poulation with 2nd vaccine in Bavaria |
| BAV 2nd Vacc Day | 2nd vaccination administered per day in Bavaria |
| BAV 2nd Vacc Avg | 7 day average of 2nd vaccination in Bavaria |
| BAV 2nd Vacc 7D | 7 day sum of 2nd vaccination in Bavaria |
| BAV 3rd Vacc % | Percentage of poulation with 3rd vaccine in Bavaria |
| BAV 3rd Vacc Day | 3rd vaccination administered per day in Bavaria |
| BAV 3rd Vacc Avg | 7 day average of 3rd vaccination in Bavaria |
| BAV 3rd Vacc 7D | 7 day sum of 3rd vaccination in Bavaria |
| BAV 4th Vacc % | Percentage of poulation with 4th vaccine in Bavaria |
| BAV 4th Vacc Day | 4th vaccination administered per day in Bavaria |
| BAV 4th Vacc Avg | 7 day average of 4th vaccination in Bavaria |
| BAV 4th Vacc 7D | 7 day sum of 4th vaccination in Bavaria |
| MUC 1st Vacc Total | Total of 1st vaccination Munich |
| MUC 1st Vacc Day | 1st vaccination administered per day in Munich |
| MUC 1st Vacc% | Percentage of poulation with 1st vaccine in Munich |
| MUC 2nd Vacc Total | Total of 2nd vaccination Munich |
| MUC 2nd Vacc Day | 2nd vaccination administered per day in Munich | Percentage of poulation with 2nd vaccine in Munich |
| MUC 2nd Vacc% | Percentage of poulation with 2nd vaccine in Munich |
| MUC 3rd Vacc Total | Total of 3rd vaccination Munich |
| MUC 3rd Vacc Day | 3rd vaccination administered per day in Munich |
| MUC 3rd Vacc% | Percentage of poulation with 3rd  vaccine in Munich |
| MUC 4th Vacc Total | Total of 4th vaccination Munich |
| MUC 4th Vacc Day | 4th vaccination administered per day in Munich |
| MUC 4th Vacc % | Percentage of poulation with  4th vaccine in Munich |
| LGL 7D Hospital | 7 day sum of new hospitalisations in Bavaria |
| Hospital Incidence | 7 day incidence of new hospitalisation in Bavaria |
| LGL ICU | Daily # of ICU beds with COVID patients in Bavaria |
| IVENA Total | Total occpupied hospital beds with COVID patients in Bavaria |
| % 7D SUM of IVENA | 7 day sum in relation to total beds (%) |
| YELLOW % | Old yellow traffic light (max 1200 7 day sum) |
| RED % | Old red traffic light (max 600 ICU beds in total) |
| 7D DIFF TOTAL | Difference total compared to week before |
| ICU to Total % | COVID positive ICU beds compared to total hospital beds with COVID positive patients |
| LGL 7D CORR | corrected 7 day hospitalisation numbers from RKI |
| Hosp 7D Inc Corr | corrected 7 day hospitalisation incidence |
| R(t) LMU | Reproduction number R(t) for Munich from LMU StaBLab |
| New Hosp Day BAV | Daily new hospitalistions in Bavaria from LMU StaBLab |
| New Hosp Nowcast | Nowcast for Daily new hospitalistions in Bavaria from LMU StaBLab |
| Diff Hosp % | % diff between daily new hospitalisations and nowcast |