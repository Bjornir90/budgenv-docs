
# BudgEnv API



## Indices

* [Ungrouped](#ungrouped)

  * [Affectations by month](#1-affectations-by-month)
  * [Create affectation](#2-create-affectation)
  * [Create category](#3-create-category)
  * [Create transaction](#4-create-transaction)
  * [Default budget](#5-default-budget)
  * [Request token](#6-request-token)
  * [Transaction by ID](#7-transaction-by-id)


--------


## Ungrouped



### 1. Affectations by month



***Endpoint:***

```bash
Method: GET
Type: 
URL: {{host}}/affectations/month/2021-12
```



***More example Requests/Responses:***


##### I. Example Request: Affectations by month



##### I. Example Response: Affectations by month
```js
[
    {
        "affectation": {
            "amount": 25,
            "categoryId": "PizycT3DRqDrZoMMCJFkrgRG"
        },
        "date": "2021-12",
        "key": "u9ec9zb59i20"
    }
]
```


***Status Code:*** 200

<br>



### 2. Create affectation



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{host}}/affectations
```



***Body:***

```js        
{
    "date": "2021-12",
    "affectation" : {
        "categoryId": "PizycT3DRqDrZoMMCJFkrgRG",
        "amount": 25
    }
}
```



### 3. Create category



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{host}}/categories
```



***Body:***

```js        
{
    "name": "Savings",
    "amount": 350,
    "goal": {
        "amount": 3000,
        "goalType": "SAVEAMOUNT"
    }
}
```



### 4. Create transaction



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: http://localhost:3000/transactions
```



***Body:***

```js        
{
    "date": "2021-12-01",
    "amount": "500",
    "memo": "This is 5 euros",
    "payee": "Starbucks LLC"
}
```



### 5. Default budget



***Endpoint:***

```bash
Method: GET
Type: 
URL: {{host}}/budgets/default
```



***More example Requests/Responses:***


##### I. Example Request: Default budget



##### I. Example Response: Default budget
```js
{
    "categories": [
        {
            "amount": 0,
            "name": "Gas"
        },
        {
            "amount": 0,
            "goal": {
                "amount": 150,
                "goalType": "SPENDMONTHLY"
            },
            "name": "Groceries"
        },
        {
            "amount": 375,
            "goal": {
                "amount": 3000,
                "goalType": "SAVEAMOUNT"
            },
            "id": "PizycT3DRqDrZoMMCJFkrgRG",
            "name": "Savings"
        }
    ],
    "key": "DEFAULT"
}
```


***Status Code:*** 200

<br>



### 6. Request token



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: {{host}}/token
```



***Body:***

```js        
{
    "username": "{{username}}",
    "password": "{{password}}"
}
```



### 7. Transaction by ID



***Endpoint:***

```bash
Method: GET
Type: 
URL: {{host}}/transactions/hl43qgdi9kkn
```



***More example Requests/Responses:***


##### I. Example Request: Transaction by ID



##### I. Example Response: Transaction by ID
```js
{
    "amount": "500",
    "date": "2021-12-01",
    "key": "hl43qgdi9kkn",
    "memo": "This is 5 euros",
    "payee": "Starbucks LLC"
}
```


***Status Code:*** 200

<br>



---
[Back to top](#budgenv-api)
> Made with &#9829; by [thedevsaddam](https://github.com/thedevsaddam) | Generated at: 2021-12-10 19:17:51 by [docgen](https://github.com/thedevsaddam/docgen)
