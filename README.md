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
  s.name;```

![q1](https://github.com/varshanbhag06/SQL/assets/153843798/1713cc71-7f2a-4e6d-8347-bea2dba9c91b)
