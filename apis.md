# APIs
Listed here are the APIs for your use.
* Browse the APIs here. Visit docs etc.
* Meet with the API sponsors at the hackathon, particularly on Saturday morning
* Communicate with the API sponsors via their [dedicated slack channel](http://bit.ly/reactathon2017-slack)


# OpenTable
#### Quick Description
OpenTable is a leading marketplace for restaurants and diners. We love creating amazing dining experiences and we are expanding globally and across the dining space.

### Purpose
OpenTable’s public API is a means to search for restaurants, availability slots, make reservations, modify or cancel reservations. There are two key forms of public API:

##### REST API endpoint:
A more comprehensive API supporting all features required for interacting with OpenTable.

##### Graph QL endpoint (Alpha):
A work in progress endpoint that provides information on restaurants, cuisines, offers etc. Transaction level capabilities are not yet available at this endpoint.

### Challenge
We are looking for creative ideas and prototypes that are built using React family of technologies leveraging the public APIs thereby providing or enhancing the value for our diners.

### Docs

##### 1. REST API
Functionalities exposed by token(Please refer documentation for details)
1. Get restaurant listings
2. Provision  
3. Single/multi search
4. Make Reservation
5. Cancel reservation
6. Get Reservation
7. Promotions and offers

Visit [this](https://platform.otqa.com/documentation/secure) link with the following credentials
````
PP Client ID / User Id : cpa_5069
PP Secret / Password: aMrmcXH4BuUlLIyN6paPhseSlrzMh6Lz
`````
Documentation [here](https://platform.otqa.com/documentation/secure)

Step 1: Get an access token:

````
curl --user cpa_5069:aMrmcXH4BuUlLIyN6paPhseSlrzMh6Lz -X POST https://oauth-pp.opentable.com/api/v2/oauth/token?grant_type=client_credentials
````

Step 2: Access the API. This example gets availability for restaurant with id - 334879

````
curl -i -X GET -H "Content-Type:application/json" -H "Authorization:bearer TOKEN" "https://platform.otqa.com/availability/334879?start_date_time=2017-03-29T18%3A00&party_size=2&forward_minutes=120&backward_minutes=30"
````

where TOKEN - is the value you retrieve from step 1.

You can get a list of all RIDs that are availability for this user ID through this api:

````
curl -i -X GET -H "Content-Type:application/json" -H "Authorization:bearer TOKEN" 'https://platform.otqa.com/sync/listings'
````

Lat/long based search:

````
https://platform.otqa.com/availability?latitude=42.360082&longitude=71.058880&party_size=2&radius=200&forward_minutes=180&backward_minutes=30&start_date_time=2017-03-13T20%3A00&include_unavailable=true
````

IMPORTANT NOTE: Replace *.opentable.com with *.otqa.com


Few other RIDs that have availability info: 334879,
334882,
334885,
334888,
334891,
334894,
334897,
334900,
334903.

##### 2. Graph QL Endpoint(Alpha):

Quickstart - [here](./opentable/graphql-quickstart.md)

https://www.opentable.com/graphiql – For the API explorer
https://www.opentable.com/graphql – The API endpoint

Getting started with 

### Video tutorial
##### 1. REST API:
Not available yet.
##### 2. Graph QL API:
[Youtube video link](https://www.youtube.com/watch?v=CNL_cgNsJEc)

### Prizes
(Depending on the value of the product and number of winners)
Xbox One S 500GB Console - Battlefield 1 Bundle
Chrome Citizen Messenger Bag Black/Red, One Size
Amazon Tap - Alexa-Enabled Portable Bluetooth Speaker

***

# Netlify
#### Quick Description
Netlify provides [Continuous Delivery](https://www.netlify.com/docs/continuous-deployment), 1-click HTTPS, [Custom Domains](https://www.netlify.com/docs/custom-domains/), integrated prerendering, and a custom global CDN.

### Purpose
[Progressive Web Apps](https://developers.google.com/web/tools/lighthouse/) are user experiences that are fast, secure, and engaging. Netlify helps you get there with our asset optimization and free SSL integration. 

Netlify improves your workflow with Deploy Previews that work by deploying every pull request from your git repository to a unique URL; completely different from the one your main site uses. You and your team can see how those changes look before they’re merged into the main branch and deployed to production.

To help you discover Deploy Previews, we put those links where it helps your team the most, directly in the pull request as commit statuses:

![](https://cdn.netlify.com/4d4d418736774eaea776b4ab08ee07af4a0bc5a9/c6be8/img/blog/deploy-preview-success.png)

We keep this preview up to date as you continue to work, committing new changes to the same branch. Our CDN takes care of invalidating the cache every time for you.

### Challenge
We are looking for the most interesting apps leveraging the [JAMstack](https://jamstack.org/) and have a high [PWA](https://developers.google.com/web/tools/lighthouse/) rating on Google's [Lighthouse](https://jamstack.org/). All projects considered will need to be deployed to Netlify and with [Deploy Previews](https://www.netlify.com/blog/2016/07/20/introducing-deploy-previews-in-netlify/) enabled. 

### Docs
http://netlify.com/docs

### Video tutorial
- [Getting Started with the UI](https://www.youtube.com/watch?v=9sfTsX03UgI&t=4s)
- [Getting Started via the CLI](https://www.youtube.com/watch?v=vFtvhvgmgZE)

### Prizes
$300 + Chromecast & Color-Changing Bluetooth Speakers

***


# Serverless
#### Quick Description

**The Serverless Framework** – Build applications comprised of microservices that run in response to events, auto-scale for you, and only charge you when they run. This lowers the total cost of maintaining your apps, enabling you to build more logic, faster.

The Framework uses new event-driven compute services, like AWS Lambda, Google CloudFunctions, and more. It's a command-line tool, providing scaffolding, workflow automation and best practices for developing and deploying your serverless architecture. It's also completely extensible via plugins.

Serverless is an MIT open-source project, actively maintained by a full-time, venture-backed team.

### Purpose

The framework was created to help developers focus on writing their application code rather than maintaining or scaling servers.

### Challenge
We are looking for the most interesting apps leveraging the [Serverless Framework](https://serverless.com/framework/docs/). 

All projects considered will need to have a least one serverless function deployed via the framework!

Stop by our table if you need help!

### Docs
[Docs link](https://serverless.com/framework/docs/)

### Video tutorial

[About the Serverless framework](https://www.youtube.com/watch?v=bFHmgqbAh4M)

[Getting Started](https://www.youtube.com/playlist?list=PLIIjEI2fYC-C3NJF7a4-Cvh5hjdCmrVmN)

[Setting up your AWS account for Serverless](https://www.youtube.com/watch?v=HSd9uYj2LJA)

[Building a rest API](https://www.youtube.com/playlist?list=PLIIjEI2fYC-B0QxvWI6XnRB_ze0m0BKUj)

### Prizes

- Amex gift card ($700) split between the team members

***

# Overall Winners
#### The top 6 teams will present to a panel of judges including representatives from Real World React, OpenTable, and Netlify.
Note: "Overall" winners are separate from the "API winners". Each API sponsor will have their own challenges and prizes.

### Prizes
* X Box One
* Playstation 4
* Smart TV
* Chrome messenger bag
* Amazon Echo Dot
* Google Home
* Roost Laptop Stands
* Chromebook
* Tickets to React Conf
