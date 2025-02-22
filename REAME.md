## Spring Boot App - ecommerce
-----------------------------------------------
-----------------------------------------------
#### Wallet Microserivce -p 8000
-----------------------------------------------

##### User register Post(/api/v1/users/register)
```
{
    "name": "randomName",
    "password":"pass",
    "email": "randomName@gmail.com"
}
```
##### User login Post(/api/v1/users/login)
```
{
    "email": "randomName@gmail.com",
    "password":"pass"
}
```
##### User allUsers Get(/api/v1/users)
```
```

##### Wallet create Post(/api/v1/wallet/create/{userId})
```
```

##### Wallet get Get(/api/v1/wallet/{userId})
```
```

##### Transaction cash In Post(/api/v1/transaction/cashin/{walletId}?amount={amount})
```
```

##### Transaction cash Out Post(/api/v1/transaction/cashout/{walletId}?amount={amount})
```
```

##### Transaction Transaction History of A Wallet Get(/api/v1/transaction/{walletId})
```
```
-----------------------------------------------
#### Shop Microserivce -p 8001
-----------------------------------------------
##### Product creation Post(/api/v1/products/create)
```
{
    "name": "randomName",
    "description":"randomDes",
    "price": 50
}
```

##### Get all products Get(/api/v1/products)
```
```

##### Get one product Get(/api/v1/products/{id})
```
```

##### Create Cart Post(/api/v1/cart/create/{userId})
```
```

##### add item to Cart Post(/api/v1/cart/{userId}/add?productId={productId}&quantity={quantity})
```
```
##### show Cart contents Get(/api/v1/cart/{userId})
```
```

##### clear Cart contents Delete(/api/v1/cart/{userId}/clear)
```
```
##### create Order Post(/api/v1/orders/create/{userId}/{walletId})
```
```
##### get Order by userId Get(/api/v1/orders/user/{userId})
```
```
##### get Order by id Get(/api/v1/orders/{orderId})
```
```
##### updated Order Status Put(/api/v1/orders/{orderId}/status?status={status})
```
```

-----------------------------------------------
#### Inventory Microserivce -p 8002
-----------------------------------------------

##### create Inventory  Post(/api/v1/inventory/create)
```
{
    "productId": randomPrductId(Long),
    "quantity": randomQuantity(int)
}
```
##### get Inventory  by productId Get(/api/v1/inventory/product/{productId})
```
```

##### update Inventory by productId Put(/api/v1/inventory/product/{productId}?quantity={quantity})
```
```

##### delete Inventory by id Delete(/api/v1/inventory/{id})
```
```

-----------------------------------------------
#### api-gateway-p 8765
-----------------------------------------------

```
http://localhost:8765/{name of any microservice registered with eureka}/endpoint
```