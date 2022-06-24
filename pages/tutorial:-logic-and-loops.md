# Logic and Loops

```category_sales
select
category,
round(sum(sales)) as sales_usd
from orders
group by category
order by sales_usd desc
```

## Loops

You can use `{#each}` statements to loop through and generate text and charts.

**Sales by Category:**

{#each category_sales as category_row}

- {category_row.category}: 

{/each}

👉 _Add the following after `- {category_row.category}:` to show the sales per category:_

`$<Value value={category_row.sales_usd}/>`

## Logic

```orders_per_day
select
substr(order_datetime,1,10) as date,
sum(sales) as sales_usd
from orders
group by date
order by date desc
limit 7
```

Use `{#if}` and `{#else}` statements to control what content is show to users based on custom logic.

**Sales vs Target**

{#if data.orders_per_day[0].sales_usd>50}

Met sales target on {data.orders_per_day[0].date}:
${data.orders_per_day[0].sales_usd} / $50

Hooray! 🥳🥳🥳

{:else}

Missed sales target on {data.orders_per_day[0].date} 😞:
${data.orders_per_day[0].sales_usd} / $50

{/if}

👉 _Replace occurences of `[0]` with `[1]` in the page above to see if the sales target was met on 2021-12-30 (the second most recent day in the dataset)_

Loops and logic are often to powerful to combine - loop through data and only display data if certain conditions are met.

<br>
<br>
