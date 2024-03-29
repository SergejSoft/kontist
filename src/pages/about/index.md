---
templateKey: about-page
title: Welcome
---
 Discover all the services of our platform so that you can build or integrate your application with Kontist.

## Getting started

We provide you with a GraphQL API to e.g. fetch transactions or start new transfers.
For exploring the API we recommend the Playground application.
When you are ready for implementation you first need to register your own application with us as an OAuth2 client. 

Then you can use your application to create an access token to access Kontist on behalf of a user. With that access token you can then make requests to our /api/graphql endpoint.
For an easier start we provide you with our SDK.

## 
We suggest the following steps:

* Open your Kontist bank account (if you do not have one yet)
* Explore our API with the Playground
* Read the GraphQL Docs
* Register your own application
* Use our SDK in your application or directly use the /api/graphql endpoint
  Kontist SDK




Our JavaScript SDK helps you easily connect to our services.\
 It was developed for Node.js and the browser and contains TypeScript type definitions.\
Just run 

```
npm install kontist 
```

to install the latest version.
The SDK includes authentication convenience methods and provides methods for the most common use cases, e.g. creating a new transfer:

```

const confirmationId = await client.models.transfer.createOne({
  amount: 1234,
  recipient: "Johnny Cash",
  iban: "DE07123412341234123412",
  purpose: "test transfer",
});
```

```
// wait for sms
const smsToken = "...";
```

```
await client.models.transfer.confirmOne(confirmationId, smsToken);
```


GraphQL Playground
The Playground is an interactive, in-browser application that can be used to explore the GraphQL interface we provide. You may authorize the application with the same credentials that you use for the Kontist mobile app.
