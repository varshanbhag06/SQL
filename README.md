[bquxjob_27427f34_18d726a5430.csv](https://github.com/varshanbhag06/SQL/files/14155576/bquxjob_27427f34_18d726a5430.csv)# SQL
QUESTION 1 : What is the average trip duration for each station?
```sql
SELECT
  s.name AS station_name,
  AVG(t.duration_minutes) AS avg_duration
FROM
  `bigquery-public-data.austin_bikeshare.bikeshare_stations` s
JOIN
  `bigquery-public-data.austin_bikeshare.bikeshare_trips` t
ON
  s.station_id = t.start_station_id
GROUP BY
  s.name;
```

![q1](https://github.com/varshanbhag06/SQL/assets/153843798/1a1d2598-1c08-4a01-b8fd-6959581c95ed)
[Uploading bquxjob_27427f34_18d726a5430.csstation_name,avg_duration
ACC - West & 12th Street,23.503572251670906
ACC - Rio Grande & 12th,24.90557184750735
Lavaca & 6th,40.305220505088549
Toomey Rd @ South Lamar,26.504621606008111
Capital Metro HQ - East 5th at Broadway,32.47699757869249
Rainey @ River St,26.007082476582074
Henderson & 9th,33.094237004497394
11th & San Jacinto,29.494282991900928
5th & Campbell,31.696550602017538
Pease Park,30.744525547445246
Lake Austin Blvd @ Deep Eddy,40.653797628059479
Dean Keeton & Speedway,21.24001387181195
State Capitol @ 14th & Colorado,30.438464747601124
6th & Chalmers,35.727762803234484
11th & Salina,49.625343511450431
10th & Red River,35.827775598273817
Hollow Creek & Barton Hills,35.398488664987369
16th/San Antonio,30.014853977844922
Zilker Park West,26.718701700154543
East 7th & Pleasant Valley,32.584392014519068
Red River/Cesar Chavez @ The Fairmont,43.471023427866733
Lakeshore & Pleasant Valley,51.56890329233255
South Congress @ Bouldin Creek,31.135457227138666
Rosewood & Chicon,46.250412768299391
8th & Lavaca,42.448979591836789
Rosewood & Angelina,33.872981230903562
Lake Austin & Enfield,40.4478962818004
Congress & Cesar Chavez,43.866397867832951
Nash Hernandez @ RBJ South,46.415123696903791
East 5th/Shady @ Eastside Bus Plaza,41.502164502164511
13th & San Antonio,34.443455691509058
Republic Square,29.577272727272756
OFFICE/Main/Shop/Repair,36.916666666666671
Nueces @ 3rd,8.643564356435645
2nd & Congress,33.878842676311081
4th & Congress,27.096046949924769
8th & Congress,30.650108758378938
Capitol Station / Congress & 11th,37.473424013254679
4th/Sabine,19.296488220990923
City Hall / Lavaca & 2nd,31.318692954406014
5th & Bowie,22.510592850915465
Barton Springs & Riverside,35.268069727891159
South Congress & James,35.548637807120038
South Congress & Elizabeth,37.531028568849571
Waller & 6th St.,23.874639249639181
West & 6th St.,30.869755201350507
Bullock Museum @ Congress & MLK,29.083649534322149
Convention Center / 3rd & Trinity,34.623358204353352
17th & Guadalupe,32.122333478450066
Plaza Saltillo,29.362473674133657
East 6th & Pedernales St.,33.575677966101765
Guadalupe & 21st,22.202590769334257
UT West Mall @ Guadalupe,22.192843480457611
Long Center @ South 1st & Riverside,36.135656250000231
4th/Guadalupe @ Republic Square,22.396666666666697
3rd & West,25.724234438043677
State Capitol Visitors Garage @ San Jacinto & 12th,37.554586808187985
San Jacinto & 8th Street,36.650235251538327
Rainey/Driskill,34.861841142912866
5th & San Marcos,21.346090534979449
Trinity & 6th Street,39.123992155153509
Pfluger Bridge @ W 2nd Street,34.376299031792243
Palmer Auditorium,33.847308520455258
East 11th St. at Victory Grill,32.68785215235517
East 11th St. & San Marcos,26.622370379959815
South Congress & Academy,31.091497148693527
Red River & 8th Street,39.0671793711831
Barton Springs Pool,39.327525738205644
Zilker Park,43.80780113600639
Riverside @ S. Lamar,40.414002568070366
Rainey St @ Cummings,39.887696133070477
Barton Springs @ Kinney Ave,34.633650997608576
East 6th at Robert Martinez,27.604671280276875
East 4th & Chicon,33.473882945248647
East 2nd & Pedernales,34.037943966468085
MoPac Pedestrian Bridge @ Veterans Drive,47.648554112554166
Brazos & 6th,40.349851712051787
Republic Square @ 5th & Guadalupe,33.573393553685065
South Congress & Barton Springs at the Austin American-Statesman,38.871196800143814
6th & Congress,35.293075472525658
Nueces & 3rd,27.02990529335478
Medina & East 6th,29.472231243910368
Sterzing at Barton Springs,43.553760789149109
Boardwalk West,40.24367767945963
22nd & Pearl,15.819861156630823
Rio Grande & 28th,19.857569284697139
Dean Keeton & Whitis,14.430975306580459
21st & University,19.262036260590495
21st & Speedway @PCL,17.78172629257535
23rd & San Jacinto @ DKR Stadium,22.043710410241239
Nueces & 26th,17.964071373257582
23rd & Rio Grande,18.319844241425763
Lakeshore @ Austin Hostel,50.214443802925459v…]()

