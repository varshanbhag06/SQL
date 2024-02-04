# SQL
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

QUESTION 2 : What is the average trip duration in minutes for each bike type?
```sql
SELECT
  bike_type,
  AVG(duration_minutes) AS avg_duration
FROM
  `bigquery-public-data.austin_bikeshare.bikeshare_trips`
GROUP BY
  bike_type
```
![q2](https://github.com/varshanbhag06/SQL/assets/153843798/36d9f31f-dbe9-42e6-b576-3a2f70e7e04f)


QUESTION 3: What are the top 3 stations with the highest total trip duration?
```sql
SELECT
  s.name,
  SUM(t.duration_minutes) AS total_duration
FROM
  `bigquery-public-data.austin_bikeshare.bikeshare_trips` t
JOIN
  `bigquery-public-data.austin_bikeshare.bikeshare_stations` s
ON
  t.start_station_id = s.station_id
GROUP BY
  s.name
ORDER BY
  total_duration DESC
LIMIT
  3;
```
![q3](https://github.com/varshanbhag06/SQL/assets/153843798/3f7b0712-71e7-42fc-82f5-3526b06dd9dd)


QUESTION 4: How many trips start at each station?
```sql
SELECT
  stations.name,
  COUNT(*) AS trip_count
FROM
  `bigquery-public-data.austin_bikeshare.bikeshare_stations` AS stations
JOIN
  `bigquery-public-data.austin_bikeshare.bikeshare_trips` AS trips
ON
  stations.station_id = trips.start_station_id
GROUP BY
  stations.name;
```
![q5](https://github.com/varshanbhag06/SQL/assets/153843798/8d5153cc-fd20-476e-bc97-a152f8765317)


QUESTION 5: What are the stations with more docks than the average number of docks across all stations?
```sql
WITH
  AvgDocks AS (
  SELECT
    AVG(number_of_docks) AS avg_docks
  FROM
    `bigquery-public-data.austin_bikeshare.bikeshare_stations` )
SELECT
  s.name, s.station_id, s.city_asset_number, s.number_of_docks
FROM
  `bigquery-public-data.austin_bikeshare.bikeshare_stations` s
JOIN
  AvgDocks a
ON
  s.number_of_docks > a.avg_docks;
```
![q4](https://github.com/varshanbhag06/SQL/assets/153843798/a1eba6ca-b763-4fcb-8768-d18079374d0b)



