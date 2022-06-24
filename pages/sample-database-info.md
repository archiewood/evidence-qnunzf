# Sample database

This project is connected to a sample database with data from a fictional ecommerce store, Needful Things Inc.

## The Needful Things Dataset

The data is stored in a **SQLite database**, a local database that is stored in a file.

The file `needful_things.db` contains 4 tables:

- **ORDERS:** data on customer orders

- **MARKETING_SPEND:** shows how much Needful Things has spent on each paid marketing channels per month

- **REVIEWS:** stores customers reviews for some orders, which are Net Promoter Scores (NPS) on a scale of 0-10

- **DELIVERIES:** tracks when deliveries where meant to, and actually, happened

## Sample

10 rows of data for each are show below

```orders
select * from orders limit 10
```

```marketing_spend
select * from marketing_spend limit 10
```

```reviews
select * from reviews limit 10
```

```deliveries
select * from deliveries limit 10
```
