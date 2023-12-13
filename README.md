## Customer Segmentation

A) table for question 1 containing all columns needed. created a temporary table  #RFM  by selecting specific
column from the salesoOrderheader and salesOrderDetail. which includes CustomerId,OrderDate,SalesOrderID,ProductID
OrderQty,UnitPrice,LineTotal for each sales*/

```
SELECT 
    a.[CustomerID],
    a.[OrderDate],
    a.[SalesOrderID],
    b.[ProductID],
    b.[OrderQty],
    b.[UnitPrice],
    b.[LineTotal]
INTO #RFM
FROM [Sales].[SalesOrderHeader]a 
INNER JOIN [Sales].[SalesOrderDetail] b 
ON a.[SalesOrderID] = b.[SalesOrderID]

SELECT * 
FROM #RFM
```
