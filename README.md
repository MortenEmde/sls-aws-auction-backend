# Serverless AWS and Microservice back-end with authentication and notification service

Serverless backend for an auction service app that I deployed to AWS following Ariel Winberger's Udemy course: [Serverless Framework Bootcamp: Node.js, AWS & Microservices](https://www.udemy.com/course/serverless-framework/)

## Endpoints
You will be able to hit the following endpoints in postman or curl:
### Crate auction:
* POST - https://psdcipmhpf.execute-api.eu-west-1.amazonaws.com/dev/auction

Make sure to include at a JSON object with "title" in the request body:
```
{
    "title": "My awesome auction item"
}
```

### Get all auctions:
* GET - https://psdcipmhpf.execute-api.eu-west-1.amazonaws.com/dev/auctions

### Get auction by ID:
* GET - https://psdcipmhpf.execute-api.eu-west-1.amazonaws.com/dev/auction/{id}

### Place a bid:
* PATCH - https://psdcipmhpf.execute-api.eu-west-1.amazonaws.com/dev/auction/{id}/bid
Make sure to include at a JSON object with "amount" in the request body:
```
{
    "amount": 10
}
```

### Add/update auction picture:
* PATCH - https://psdcipmhpf.execute-api.eu-west-1.amazonaws.com/dev/auction/{id}/picture
Make sure to include at a Raw Text Base64 image in the request body

You can generate a Base64 from a .jpg image useing [this tool.](https://codingly-io.github.io/base64-encoder/)

## Note:
For all endpoints, an accesstoken is required.

If you would like to test the application. Please contact me on mortenemdec@gmail.com and I can generate you a 24 hour development token.

The token need's to be included in postmans "Auth" tab as a "Bearer Token" to access the requests. 