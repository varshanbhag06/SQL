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
