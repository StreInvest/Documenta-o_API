![stapi](https://user-images.githubusercontent.com/54999837/118889676-d371e880-b8d3-11eb-8889-73b488ca068b.png)


# Investimentos

## `GET` Investimentos

![image](https://user-images.githubusercontent.com/54999837/120897254-8728e700-c5fb-11eb-979f-355cbf4e0ff3.png)

#### Status `200`

```json
{
    "response": [
        {
            "_id": "60a1aa920d83402158ac8358",
            "investment_name": "teste aberto",
            "status": "Open",
            "risk": "Severe",
            "category": "CDB",
            "consortium": {
                "_id": "6097ffb54ee8cc407bb8109c",
                "consortium_name": "caixa economica federal",
                "created_at": "2021-05-09T15:28:53.477Z",
                "updated_at": "2021-05-09T15:28:53.477Z",
                "__v": 0
            },
            "profitability": {
                "day": "00.01",
                "month": "00.10",
                "year": "01.00",
                "score": "00.05%",
                "minimum_value": "25.00"
            },
            "created_at": "2021-05-16T23:28:18.367Z",
            "updated_at": "2021-05-16T23:53:54.093Z",
            "__v": 0
        },
        {
            "_id": "60a40b55ecfbef0015a29f72",
            "investment_name": "boa para excluir",
            "status": "Close",
            "risk": "Severe",
            "category": "teste",
            "consortium": {
                "_id": "6097ffb54ee8cc407bb8109c",
                "consortium_name": "caixa economica federal",
                "created_at": "2021-05-09T15:28:53.477Z",
                "updated_at": "2021-05-09T15:28:53.477Z",
                "__v": 0
            },
            "profitability": {
                "day": "00.01",
                "month": "00.10",
                "year": "01.00",
                "score": "22.05%",
                "minimum_value": "10.00"
            },
            "created_at": "2021-05-18T18:45:41.232Z",
            "updated_at": "2021-05-18T19:10:37.186Z",
            "__v": 0
        }
    ],
    "paginate": {
        "limit": "2",
        "page": 1,
        "totalCurrentPage": "2"
    },
    "status": 200
}
```
#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```
## `POST` Investimentos

![image](https://user-images.githubusercontent.com/54999837/120897566-3d410080-c5fd-11eb-9e0b-c127e94cc0a3.png)

### body - dados enviados

```json
{
    "investment_name": "bom pra voce",
    "status": "Close",
    "risk": "Moderate",
    "category": "Poupanca",
    "consortium": "60b03825fcf1440015381f38",
    "profitability": {
        "day": "01.00",
        "month": "09.50",
        "year": "20.00",
        "score": "100.00%",
        "minimum_value": "100.00"
    }
}
```
#### Status `201 Created`

```json
{
    "response": {
        "_id": "60bb9ff1f4fe4f0015a33b79",
        "investment_name": "bom pra voce teste",
        "status": "Close",
        "risk": "Moderate",
        "category": "Poupanca",
        "consortium": "60b03825fcf1440015381f38",
        "profitability": {
            "day": "01.00",
            "month": "09.50",
            "year": "20.00",
            "score": "100.00%",
            "minimum_value": "100.00"
        },
        "created_at": "2021-06-05T16:01:53.992Z",
        "updated_at": "2021-06-05T16:01:53.992Z",
        "__v": 0
    },
    "status": 201
}
```
#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```
#### Status `500 Internal Server Error` - param??tros incorreto

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>Error</title>
    </head>
    <body>
        <pre>Internal Server Error</pre>
    </body>
</html>
```

## `GET` Investimento especifico

![image](https://user-images.githubusercontent.com/54999837/120897737-12a37780-c5fe-11eb-9f83-1f84c012063e.png)

#### Status `200 Sucess`

```json
{
    "response": {
        "_id": "60a1aa920d83402158ac8358",
        "investment_name": "teste aberto",
        "status": "Open",
        "risk": "Severe",
        "category": "CDB",
        "consortium": {
            "_id": "6097ffb54ee8cc407bb8109c",
            "consortium_name": "caixa economica federal",
            "created_at": "2021-05-09T15:28:53.477Z",
            "updated_at": "2021-05-09T15:28:53.477Z",
            "__v": 0
        },
        "profitability": {
            "day": "00.01",
            "month": "00.10",
            "year": "01.00",
            "score": "00.05%",
            "minimum_value": "25.00"
        },
        "created_at": "2021-05-16T23:28:18.367Z",
        "updated_at": "2021-05-16T23:53:54.093Z",
        "__v": 0
    },
    "status": 200
}
```

#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```

#### Status `500 Internal Server Error` - ID incorreto

```html
<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="utf-8">
	<title>Error</title>
</head>

<body>
	<pre>Internal Server Error</pre>
</body>

</html>
```

## `PUT` Investimento

![image](https://user-images.githubusercontent.com/54999837/120898223-55664f00-c600-11eb-9afa-1e7e4f7bdc7c.png)

### Body - parametros que deseja ser alterado

```json
{
    "investment_name": "boa para excluir",
    "status": "Close",
    "risk": "Severe",
    "category": "teste",
    "consortium": "6097ffb54ee8cc407bb8109c",
    "profitability": {
        "day": "00.01",
        "month": "00.10",
        "year": "01.00",
        "score": "22.05%",
        "minimum_value": "10.00"
    }
}
```

#### Status `200 Sucess`

```json
{
    "response": {
        "_id": "60a40b55ecfbef0015a29f72",
        "investment_name": "boa para excluir",
        "status": "Close",
        "risk": "Severe",
        "category": "teste",
        "consortium": "6097ffb54ee8cc407bb8109c",
        "profitability": {
            "day": "00.01",
            "month": "00.10",
            "year": "01.00",
            "score": "22.05%",
            "minimum_value": "10.00"
        },
        "created_at": "2021-05-18T18:45:41.232Z",
        "updated_at": "2021-06-05T16:22:53.966Z",
        "__v": 0
    },
    "status": 200
}
```

#### Status `500 Internal Server Error` - ID incorreto

```html
<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="utf-8">
	<title>Error</title>
</head>

<body>
	<pre>Internal Server Error</pre>
</body>

</html>
```

#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```

#### Status `500 Internal Server Error` - param??tros incorreto

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>Error</title>
    </head>
    <body>
        <pre>Internal Server Error</pre>
    </body>
</html>
```
## `DELETE` investimento

![image](https://user-images.githubusercontent.com/54999837/120898637-189b5780-c602-11eb-9ffe-4aca64b96c04.png)


#### status `204 No Content`

* n??o retorna nada (succeso)

#### Status `404Not Found`

```json 
{
    "response": "User already deleted",
    "status": 404
}
```

#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```
#### Status `500 Internal Server Error` - ID incorreto

```html
<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="utf-8">
	<title>Error</title>
</head>

<body>
	<pre>Internal Server Error</pre>
</body>

</html>
```

# Consorcio - emissor do investimento

## `GET` consorcio

![image](https://user-images.githubusercontent.com/54999837/120930410-8196d400-c6c3-11eb-8c77-2739443775fe.png)

#### Status `200 Sucess`

```json
{
    "response": [
        {
            "_id": "6097ffb54ee8cc407bb8109c",
            "consortium_name": "caixa economica federal",
            "created_at": "2021-05-09T15:28:53.477Z",
            "updated_at": "2021-05-09T15:28:53.477Z",
            "__v": 0
        }
    ],
    "paginate": {
        "limit": "1",
        "page": 1,
        "totalCurrentPage": "1"
    },
    "status": 200
}
```

#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```
## `POST` consorcio

![image](https://user-images.githubusercontent.com/54999837/120930629-80b27200-c6c4-11eb-8bd1-62eea36953ad.png)

### Body

```json
{
    "consortium_name": "para ser excluido 2"
}
```
#### Status `201 created`

```json
{
    "response": {
        "_id": "60bcebe1035afd00158ba2ba",
        "consortium_name": "para ser excluido 2",
        "created_at": "2021-06-06T15:38:09.138Z",
        "updated_at": "2021-06-06T15:38:09.138Z",
        "__v": 0
    },
    "status": 201
}
```

#### Status `500 Internal Server Error` - Consorcio j?? existente

```html
<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="utf-8">
	<title>Error</title>
</head>

<body>
	<pre>Internal Server Error</pre>
</body>

</html>
```

#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```


## `PUT` consorcio

![image](https://user-images.githubusercontent.com/54999837/120930851-7349b780-c6c5-11eb-811e-322f2f989e56.png)

### Body

```json
{
    "consortium_name": "casas bahia - atualizado"
}
```

#### Status `200 Sucess`

```json
{
    "response": {
        "_id": "60bcebda035afd00158ba2b9",
        "consortium_name": "casas bahia - atualizado",
        "created_at": "2021-06-06T15:38:02.828Z",
        "updated_at": "2021-06-06T15:45:15.698Z",
        "__v": 0
    },
    "status": 200
}
```

#### Status `400 Bad Request` dados j?? foi alterado ou parametros enviado incorretamente via body

```json
{
    "response": "it was not possible to update, check the data is being sent correctly",
    "status": 400
}
```
#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```

#### Status `500 Internal Server Error` - ID Invalido

```html
<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="utf-8">
	<title>Error</title>
</head>

<body>
	<pre>Internal Server Error</pre>
</body>

</html>
```

## `DELETE` consorcio

![image](https://user-images.githubusercontent.com/54999837/120931046-46e26b00-c6c6-11eb-83f6-eaf55bfbcc65.png)


#### status `204 No Content`

* n??o retorna nada (succeso)

#### Status `404Not Found`

```json 
{
    "response": "User already deleted",
    "status": 404
}
```

#### Status `401 Unauthorized`

```json
{
    "response": "you don't have access",
    "status": 401
}
```
#### Status `500 Internal Server Error` - ID incorreto

```html
<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="utf-8">
	<title>Error</title>
</head>

<body>
	<pre>Internal Server Error</pre>
</body>

</html>
```

