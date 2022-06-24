# Tutorial

This tutorial covers the basics of Evidence:

1. Markdown
2. SQL queries
3. Chart and other components

_If the server crashes, restart it with `npm run dev` in the terminal_

## Markdown

Evidence pages are just markdown files. The file for this page is `pages/tutorial:-basics.md`

👇 Add some text below and save the file to see it update instantly in the UI.

## Queries

Write queries using markdown code fences ` ``` `:

```orders_by_month
select
substr(order_datetime,1,7) as date,
sum(sales) as sales_usd
from orders
group by date
```

You can see both the SQL and the query results by interacting with the query above.

👉 _Edit the above query to just display 2021 data by adding:_ `where order_datetime>='2021-01-01'`

## Charts

Charts can be included in a single line of code

<BarChart data = {data.orders_by_month} />

👉 _Add a title to the chart by adding `title = 'Sales by Month, USD'` just before the `/>` in the above chart component._

Evidence has support for most common chart types, see them all in our <a href="https://docs.evidence.dev/features/charts/examples" target="_blank">component library</a>.

🎉 Thats it for the basics! 🎉

To work with your own database, you will need to install Evidence locally.

<BigLink href="/tutorial:-logic-and-loops">&larr; Install instructions </BigLink>

## More Powerful Features ⚡

Evidence supports using logic & loops to determine what text and data is diplayed.

<BigLink href="/tutorial:-logic-and-loops">Using Logic & Loops &rarr;</BigLink>

<br>
<br>
