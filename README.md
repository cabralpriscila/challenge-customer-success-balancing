# Customer Success Balancing

## The Challenge - Customer Success Balancing

This challenge consists of a balancing system between customers and Customer Success (CS) Managers, who are responsible for the strategic follow-up of customers.

Depending on the size of the customer - referring to the size of the company - we have to assign more experienced CSs to serve them.

A CS can handle more than one customer, and CSs can also take vacations, days off, or even get sick. These criteria must be taken into account when running the distribution.

Given this scenario, the system distributes customers to CSs with the closest (highest) capacity to serve customers.

### Example

If we have 6 customers with the following levels: 20, 30, 35, 40, 60, 80, and two CSs with levels 50 and 100, the system should distribute them as follows:

- 20, 30, 35, 40 to the CS with level 50
- 60 and 80 to the CS with level 100

With `n` being the number of CSs, `m` the number of customers, and `t` the number of CS absences, calculate which customers will be served by which CSs according to the rules presented.
Assumptions

- All CSs have different levels
- There is no limit to the number of customers per CS
- Customers can go without being served
- Customers can have the same size
- 0 < n < 1,000
- 0 < m < 1,000,000
- 0 < CS id < 1,000
- 0 < customer id < 1,000,000
- 0 < CS level < 10,000
- 0 < customer size < 100,000
- Maximum value of t = n/2 rounded down

### Input

The `customerSuccessBalancing()` function receives 3 parameters:

- CS id and experience level
- Customer id and experience level
- Unavailable Customer Success ids

### Output

The expected result should be the id of the CS that serves the most customers. With this value, the company can develop a plan of action to hire more CSs of an approximate level.

In case of a tie, return `0`.

### Example

In the example input, CSs 2 and 4 are on vacation, so CS 1 will serve customers up to size 60 (customers 2, 4, 5, 6), while CS 3 will serve customers 1 and 3.

For this example, the return should be `1`, which is the id of the CS serving 4 customers:

```
1
```

## How to run the tests

In the terminal, run the commands:

```
cd challenge-customer-success-balancing
ruby customer_success_balancing.rb
```
