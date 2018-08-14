# Challenge 2
For this challenge, you will be accessing data from a PostgreSQL database. To
get everything running, you will need Docker installed and from this directory
run:
1. `docker build --tag bi-test .`
2. `docker run --name bi-test -p 5432:5432 --rm bi-test`

The database will be available on `localhost` port `5432`. If you already have
something running on this port (like an existing database instance) then replace
`-p 5432:5432` with `-p <port>:5432` using a different port number `<port>`.

When you are finished, you can `CTRL-C` in the window running the docker container
to shut it down, or `docker stop bi-test` from another window to stop and remove
the container.

The username `postgres` with no password can be used to login, and you should
connect to the `marketing` database.

In this database, there is a table named `regional_purchases` that
shows distributor information for the region. The rows we are interested in are:
* `brand_label` - the name of the product
* `wholesaler_name/wholesaler_serial_number` - the distributor carrying the product

## Task 1
We would like to see how many of the highest rated products and premium products
are actually currently available to us.

Provide a list of all products found in Task 1 of the previous challenge that
are also carried by a distributor in the `regional_purchases` table. We would like
to see the product name, price, rating, and distributor name.

## Task 2
We would like to identity the distributors that have the most relationships with
top producers. By this, we mean a distributor has a relationship with a producer
if they carry any of their products.

Provide a list of the distributors that have the most relationships with the top
producers identified in Task 2 of the previous challenge.

Do the same for the most premium producers identified in Task 3 of the previous
challenge.

## Task 3
We would like to present this at the next investors meeting. Please create a
report identifying the best distributors for us to partner with that we can show
our investors.
