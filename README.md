# Aster memo

## Datetime

* Extract year, month, date, day of week from log date
```sql
, cast(extract(year  from log_date) as int) as log_year
, cast(extract(month from log_date) as int) as log_month
, cast(extract(day   from log_date) as int) as log_day
, to_char(log_date, 'day') as log_day_of_week
```
* Extract hour from unix timestamp
```sql
, cast(extract(hour from to_timestamp(unix_timestamp)) as int) as log_hour
```

