# APIs
Listed here are the APIs for your use.
* Browse the APIs here. Visit docs etc.
* Meet with the API sponsors at the hackathon, particularly on Saturday morning
* Communicate with the API sponsors via their dedicated Discord channel.
* Deploy your apps with Netlify. 

# Fauna
#### Quick Description
Cloud database with generous free plan and distributed ACID transactions for global data integrity. Get started easily and scale to worldwide success.

### Purpose
Stores transactional data like account balances, user profiles, social media content, shopping cart orders, etc.

##### API endpoint:
Install with the netlify command line tool after you have linked your checkout to your app, by running `netlify addons:create fauna` and you can access your database with environment variables like this:

```js
const client = new faunadb.Client({
  secret: process.env.FAUNADB_SERVER_SECRET
});
```

### Challenges

A common pattern with Single Page Apps is for the browser to query a cloud database directly. FaunaDB access control supports apps like this. A [demo app using the Netlify Identity service and login widget to authenticate with FaunaDB is available here.](https://github.com/fauna/netlify-faunadb-todomvc) Follow the eight steps in the README and you'll be ready to build your own app.

### Docs

The [FaunaDB Query API docs](https://app.fauna.com/documentation/reference/queryapi) are a good reference.

For [getting started with the data model, this tutorial is good.](https://app.fauna.com/documentation/howto/crud) And when you log into fauna.com (not required to get started) you can [learn more about the Fauna Shell and other tools here.](https://app.fauna.com/account)

### Video tutorial

I'll walk through these steps live during the Hackathon keynote.

### Presentation slides

Coming soon.

### Prizes

1st: Apple Watch
2nd: Oculus Go standalone VR headset
3rd: $100 iTunes Gift card


***

# Formspree

https://formspree.io

### Purpose

Formspree is a form backend that emails you when someone submits your forms. It’s the simplest way to add custom contact forms, order forms, or email capture forms to your JAMstack website. Once you connect your form to our endpoint we’ll email you the submissions. No PHP, Javascript or sign up required.

### API endpoint

To use formspree with an existing HTML form you must:

1. change the `action` of your form to point to `https://formspree.io/<YOUR EMAIL>`
2. make sure the `method` is `POST`, and
3. give a `name` attribute to all your `input` tags.

For example:

```html
<form action="https://formspree.io/your@email.com" method="POST">
  <input type="text" name="name">
  <input type="email" name="_replyto">
  <input type="submit" value="Send">
</form>
```

Try playing around with formspree in our sandbox at https://testformspree.com 

### Challenges

Get a "contact us" form set up on your website! 

### Docs
Using formspree is as easy as the `API endpoint` instructions. Try playing around with formspree at https://testformspree.com.

You can have more control of how your forms are handled by formspree by adding special `type="hidden"` inputs. See the docs below for a list of the special input names that you can use. 

https://formspree.io/docs/

You can also find answers to common questions on our help site here:

https://help.formspree.io/

Finally, we will be here at the hackathon and available to help you. Just look for this goofy guy near the big Formspree banner:

<img src="https://lh3.googleusercontent.com/ocJ3qPMgGIJzONipiMk7NADYM2JHtnV25MqdqFrJrheUHMZYbUT3XAxvDHvHGZeTOu4GAyIUVyPmPDpmImwr6sRI0MUENLfAbGNw9B1dLhjh4elL5wR4FipJRCX7qPYPCK1nzD33310=w1274-h1698-no" width="200px">


### Video tutorial
Nothing yet, but maybe we'll have one of these posted soon...


### Prizes

In person participants that use Formspree in their hackathon project are eligible to win a DJI Spark drone!

Off-site participants that use Formspree will be eligible to win an Amazon Gift Card worth $200. If Amazon gift cards aren't available in your country we will work with you to come up with an equivalent prize.

***

# Clarifai
#### Quick Description
Clarifai's API offers image and video recognition capabilities.

The API is built around a simple idea: you send inputs (an image or video) to the service and it returns predictions. The type of prediction is based on what model you choose. For example, if you run your input through the pre-trained 'food' model, the predictions it returns will contain concepts that the 'food' model knows about. If you run your input through the 'color' model, it will return predictions about the dominant colors in your image. The 'General' model covers a broad array of common concepts. A full list of models is available here: https://clarifai.com/models.

### Purpose
Use the Clarifai API if you want to add image understanding to your JAMstack app. Two common use cases are analyzing what is in an image and visual (image-based) search.

Clarifai can recognize over 10,000 concepts out-of-the-box with default settings ("General" model). You can also quickly train a model to recognize new concepts based on images you upload and label. You can see a complete list of pre-trained models you can use here: https://clarifai.com/models

##### API endpoint:
https://api.clarifai.com/v2

We recommend using a client library to access the API (makes it easier). There are clients available for most languages, including JavaScript: https://clarifai.com/developer/reference/

### Challenges
+ Get JSON results from Clarifai's "General" model for an image of your choice.
(Hint: https://clarifai.com/developer/guide/predict#predict)

++ Train your model to recognize a new object or concept (using at least 10 images as labeled examples)
(Hint: https://clarifai.com/developer/guide/train#train)

### Docs
Developer Guide (start here): https://clarifai.com/developer/guide/
Technical Reference and Client Libraries: https://clarifai.com/developer/reference/
JavaScript API endpoint reference: https://sdk.clarifai.com/js/latest/index.html

### Video tutorial
4 minute Intro to Clarifai including an API demo with the Python client: https://youtu.be/YOrrROME2zc


***


# Hasura

Hasura gives you instant, realtime GraphQL APIs for your JAMstack app. With one-click to deploy on Heroku's free tier, you can get started in less than a minute.

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/hasura/graphql-engine-heroku)

You don't need to know how to write a GraphQL schema, resolvers or learn how to use
a database to get started! Head to the deployed app, create a table, and run CRUD + realtime with GraphQL :)

![Hasura demo GIF](https://raw.githubusercontent.com/hasura/graphql-engine/master/assets/demo.gif)

You can also use Hasura to trigger Lambda/Serverless functions such as [Netlify
Functions](https://www.netlify.com/docs/functions/) when an event happens on the
database, for example, send an email when a new user is added.

### Purpose

You should use Hasura if your JAMstack app needs to CRUD data, needs a realtime API,
or if you want to trigger webhooks on data changes.

Here are some examples of how you can use Hasura:
- CRUD operations with GraphQL ([sample app](https://github.com/hasura/graphql-engine/tree/master/community/examples/todo-auth0-jwt))
- Building a realtime app (sample apps: [chat](https://github.com/hasura/graphql-engine/tree/master/community/examples/realtime-chat), [poll](https://github.com/hasura/graphql-engine/tree/master/community/examples/realtime-poll), [location tracking](https://github.com/hasura/graphql-engine/tree/master/community/examples/realtime-location-tracking))
- Sourcing the data for a gatsby site from a postgres database ([sample app](https://github.com/hasura/graphql-engine/tree/master/community/boilerplates/gatsby-postgres-graphql))
- Triggering browser-based notifications if some data changes ([sample app](https://github.com/hasura/graphql-engine/tree/master/community/examples/serverless-push))

### Learn in 5 minutes (video tutorials)

Here are a few short videos to help you get started:

1. Explore GraphQL queries, mutations and subscriptions with a realtime todo app [(video coming soon)]()
2. Send an email when a new user is created using Netlify functions [(video coming soon)]()
3. Integrate authentication/authorization with auth0 [(video coming soon)]()

### Support & help

- Join the [Hasura discord server](https://discord.gg/vBPpJkS). We're super active and someone from the team or the community will help out any time of the day if you have any questions!
- Tanmai will be hanging around at the hackathon if you're present offline! Do say Hi and ask him as many questions as you'd like:

<img src="https://api.react-finland.fi/media/graphql-finland-2018/speakers/tanmai.jpg" alt="Tanmai" width="200px">

### Docs

Hasura docs are available at [`docs.hasura.io`](https://docs.hasura.io).

Here are some quick links to get you started:

- [Deployment guide on Heroku](https://docs.hasura.io/1.0/graphql/manual/getting-started/heroku-simple.html)
- [Making your first GraphQL query](https://docs.hasura.io/1.0/graphql/manual/getting-started/first-graphql-query.html)
- [Creating tables and columns](https://docs.hasura.io/1.0/graphql/manual/schema/index.html)
- [Querying data through GraphQL](https://docs.hasura.io/1.0/graphql/manual/queries/index.html)
- [Modifying data using Mutations](https://docs.hasura.io/1.0/graphql/manual/mutations/index.html)
- [Getting realtime data using Subscriptions](https://docs.hasura.io/1.0/graphql/manual/subscriptions/index.html)
- [Create Gatsby sites using GraphQL and Postgres](https://github.com/hasura/graphql-engine/tree/master/community/boilerplates/gatsby-postgres-graphql)
- [Example applications built using Hasura](https://github.com/hasura/graphql-engine/tree/master/community/examples)
- [Trigger a Lambda function](https://docs.hasura.io/1.0/graphql/manual/getting-started/first-event-trigger.html)

To query data from frontend applications, you can use the [Apollo
Client](https://www.apollographql.com/docs/react/). Here are some popular clients:

- [React](https://www.apollographql.com/docs/react/essentials/get-started.html)
- [Angular](https://www.apollographql.com/docs/angular)
- [Vue](https://www.apollographql.com/docs/react/integrations.html#vue)


### Prizes

TBA


***


# Pilon

Pilon is an **e-commerce platform** designed and built from the ground up for the JAMstack world.  

Our collection of lightweight, API-first, commerce micro-services enable you to quickly build and test innovative commerce experiences that your customers will love. Use Pilon’s pre-built components to make your store whatever you want it to be while still having the flexibility to change it any time you want.

We're **opening** our beta platform to hackathon participants and *we'll be there hacking on Pilon while you're hacking on your projects*.

### Purpose

E-commerce stuff.

Use Pilon to add any of these elements to your project:
* Customer Auth
* Product Catalog / CMS
* Cart + Checkout
* Taking Orders Online

##### API endpoints:
REST
* https://api.pilon.io/v1

GraphQL
* https://api.pilon.io/v1/graphql

### Challenges
Sell something.  Use Pilon's new GraphQL API + Gatsby to build a super fast, super easy, super sweet commerce experience.

To get inspired, [*checkout how fast an e-commerce site can be*](https://rachio.com) when its built with **Gatsby** and a GraphQL API.

### Docs

Pilon's main documentation can be accessed at:
* https://docs.pilon.io/

Pilon's API docs are here:
* https://api.pilon.io/v1/docs

An example project using our REST API can found on GitHub here:
* https://github.com/pilon-io/example-fh

### Video tutorial

### Support & Help

We'll be at a table at the hackathon to provide lots of support and help.  Hit up Garth at our table or in the Pilon channel on Discord.

We'll be there hacking with you the whole time.

### Prizes

First prize will be a Parrot BEBOP 2 FPV drone.  Pretty sweet!

https://www.parrot.com/us/drones/parrot-bebop-2-fpv

![Parrot BEBOP 2 FPV drone](https://www.parrot.com/files/s3fs-public/styles/product_teaser_display/public/compo_bebop_2_fpv_0.png)

***

# Overall Winners
#### The top 6 teams will present to a panel of judges including representatives from freeCodeCamp, Netlify, Formspree, and Fauna.
Note: "Overall" winners are separate from the "API winners". Each API sponsor will have their own challenges and prizes, which you can see above.

### Prizes
* Top 6 teams
  * Demo your product for around 10 minutes in the GitHub Video Booth to be displayed to the other hackers on televisions around the office, and to be recorded to be posted on line and shared via the freeCodeCamp blog!
* Top 3 Teams
  * Present your product on the GitHub stage in front of your fellow hackers! Get your presentation recorded for the livestream, and also recorded for later publication on the freeCodeCamp blog!
  * 3rd place: $200 cash prize
  * 2nd place: $300 cash prize
  * 1st place: $500 cash prize
