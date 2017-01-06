#Shutterfly Customer Lifetime Value

One way to analyze acquisition strategy and estimate marketing cost is to calculate the Lifetime Value (“LTV”) of a customer. Simply speaking, LTV is the projected revenue that customer will generate during their lifetime.

A simple LTV can be calculated using the following equation: `52(a) x t`. Where `a` is the average customer value per week (customer expenditures per visit (USD) x number of site visits per week) and `t` is the average customer lifespan. The average lifespan for Shutterfly is 10 years.  

## Requirements

With working code, design and implement an in memory data structure, code, data quality tests and unit tests on the following operations. You may use one of the following OO languages: Java, Python, Scala. Once you have completed the requirements, submit a link to a Github repo (public is fine, you do not need to pay for a private repo) with your source code.

### Ingest(e, D)
Given event e, update data D

### TopXSimpleLTVCustomers(x, D)
Return the top x customers with the highest Simple Lifetime Value from data D.

## Events

Please use the following sample events the Data Warehouse collects from Shutterfly’s public sites. All events have a `KEY` and `EVENT_TIME`, but are received with no guaranteed order and with fluctuating frequency.

### Customer
* Event Type
  * CUSTOMER
* Verbs
  * NEW
  * UPDATE
* Data
  * KEY(CUSTOMER_ID)
  * EVENT_TIME
  * LAST_NAME
  * ADR_CITY
  * ADR_STATE

### Site Visit
* Event Type
  * SITE_VISIT
* Verbs
  * NEW
* Data
  * KEY(PAGE_ID)
  * EVENT_TIME
  * CUSTOMER_ID
  * TAGS

### Image Upload
* Event Type
  * IMAGE
* Verbs
  * UPLOAD
* Data
  * KEY(IMAGE_ID)
  * EVENT_TIME
  * CUSTOMER_ID
  * CAMERA_MAKE
  * CAMERA_MODEL

### Order
* Event Type
  * ORDER
* Verbs
  * NEW
  * UPDATE
* Data
  * KEY(ORDER_ID)
  * EVENT_TIME
  * CUSTOMER_ID
  * TOTAL_AMOUNT

## Reference
https://blog.kissmetrics.com/how-to-calculate-lifetime-value

## Help
If you have questions, you can email your recruiter. Alternatively, or if you stumbled upon this challenge and have questions you can email ccdwh@shutterfly.com.


