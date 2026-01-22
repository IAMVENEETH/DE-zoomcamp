# DE-zoomcamp
Codespace for DE-zoomcamp

## Homework-Module-1

### Question 1

**Answer:docker run -it --entrypoint=bash --rm python:3.13.11**

### Question 2

**Answer: db:5432**

### Question 3

**Answer:**

'''sql
select count(*)
from green_taxis
where (lpep_pickup_datetime > '2025-11-01' and lpep_pickup_datetime <= '2025-12-01') 
and trip_distance <= 1
