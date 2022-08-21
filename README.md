<h1 align="center">
  <img alt="cgapp logo" src="https://raw.githubusercontent.com/CossyCossy/food-delivery/master/html/img/cgapp_logo%402x.png" width="224px"/><br/>
  Go Stripe Payment
</h1>
<p align="center">Create an implementation of a payment gateway with <b>Stripe Api</b> and <b>Golang</b>.</p>

<p align="center"><a href="https://github.com/Crunch-Garage/go-stripe" 
target="_blank"><img src="https://img.shields.io/badge/Go-1.19+-00ADD8?style=for-the-badge&logo=go" alt="go version" /></a>&nbsp;
<a href="https://github.com/Crunch-Garage/go-stripe" 
target="_blank"><img src="https://img.shields.io/badge/Stripe%20-Stripe Go-red?style=for-the-badge&logo=stripe&logoColor=green" alt="stripe-go version" />
 </p>

 <br />

## 🧐 Getting Started 
> Before getting started , let us learn how to install [Golang](https://go.dev/) and investigate what [Stripe](https://stripe.com/docs) is.
>
> As [Edwin Kimani](https://github.com/edugeezu) asks, What is ?, Why ? Golang or Stripe ? Well let's learn why Golang or Stripe

Clone the repository:
```
$ git clone https://github.com/Crunch-Garage/go-stripe.git
```

Get into project directory:
```
$ cd go-stripe/
```

Install the project dependancies:
``` 
$ go mod tidy
```

## 📒 Stripe Authentication

Before running the project, you need to get your stripe Api key. The Stripe Api uses [API keys](https://stripe.com/docs/keys) to authenticate requests. You can view and manage your API keys in [the Stripe Dashboard.](https://stripe.com/login?redirect=/account/apikeys) 

Global API key example:
```
stripe.Key = "sk_test_51LYSmlLmC3rksDIqGzKxI4eqASwBZi4vZnKzwXIUtNXI0NGtBV2tWSyncdTlDZzdyaaaIBpIuAq64WZae9z6RvAA001TmltJWT"
```

Run project:
```
$ go run main.go
```

## 👨‍💻 API requests

Create Customer API example:
```
http://localhost:8080/api/customer/create
```
Method POST

Request Body:
```
{
  "name" : "Jane Doe",
  "phone": "+254712345678",
  "email": "janedoe@example.com",
  "description":"Jane Doe"
}

```

Response Body:
```
{
  "address": {
    "city": "",
    "country": "",
    "line1": "",
    "line2": "",
    "postal_code": "",
    "state": ""
  },
  "balance": 0,
  "created": 1661086328,
  "currency": "",
  "default_source": null,
  "deleted": false,
  "delinquent": false,
  "description": "Jane Doe",
  "discount": null,
  "email": "janedoe@example.com",
  "id": "cus_MHnDA03YgPP9uS",
  "invoice_prefix": "807DC757",
  "invoice_settings": {
    "custom_fields": null,
    "default_payment_method": null,
    "footer": ""
  },
  "livemode": false,
  "metadata": {},
  "name": "Jane Doe",
  "next_invoice_sequence": 1,
  "phone": "+254712345678",
  "preferred_locales": [],
  "shipping": null,
  "sources": {
    "has_more": false,
    "total_count": 0,
    "url": "/v1/customers/cus_MHnDA03YgPP9uS/sources",
    "data": []
  },
  "subscriptions": {
    "has_more": false,
    "total_count": 0,
    "url": "/v1/customers/cus_MHnDA03YgPP9uS/subscriptions",
    "data": []
  },
  "tax_exempt": "none",
  "tax_ids": {
    "has_more": false,
    "total_count": 0,
    "url": "/v1/customers/cus_MHnDA03YgPP9uS/tax_ids",
    "data": []
  }
}

```
