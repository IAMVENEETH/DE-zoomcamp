# DE-zoomcamp
Codespace for DE-zoomcamp

## Homework-Module-1

### Question 1

**Answer:docker run -it --entrypoint=bash --rm python:3.13.11**

### Question 2

**Answer: db:5432**

### Question 3

**Answer:select count(*) from green_taxis where (lpep_pickup_datetime > '2025-11-01' and lpep_pickup_datetime <= '2025-12-01') and trip_distance <= 1**

### Question 4

**Answer:select CAST(lpep_dropoff_datetime AS DATE) AS "day",sum(trip_distance) from green_taxis where trip_distance <= 100 group by 1 order by 2 desc:**

### Question 5

**Answer:select z."Zone",sum(total_amount) from green_taxis g join zones z on g."PULocationID" = z."LocationID" WHERE CAST(lpep_dropoff_datetime AS DATE) = '2025-11-18' group by 1 order by 2 desc LIMIT 1:**

### Question 6

**Answer:select "Zone",MAX(t.tip) From zones JOIN (select g."DOLocationID" as D,tip_amount as tip from green_taxis g  join zones z on "PULocationID" = z."LocationID" Where z."Zone" = 'East Harlem North') t on "LocationID" = t.D group by 1 order by 2 desc LIMIT 1**
