# Getting Started

### Contents
[The JAMstack](#the-jamstack)
[Front-end](#front-end)
[Cloud Functions aka Serverless](#cloud-functions)
[Deployment & Continuous Integration](#deployment)


# The JAMstack
The JAMstack is a powerful new approach for deploying fast, highly scalable sites and applications that don't require backend infrastructure. Thanks to recent advancements in the web platform, developers can now run any web property, from simple sites to complex applications, on global CDNs and without a single web server. Learn more about how the JAMstack works [here](https://jamstackconf.com/what-is-jamstack).

# Front-end
The JAMstack really shines when you leverage a modern front-end library or framework such as React, Angular, or Vue. What's more, you can get set up almost instantaneously with the incredible static site generators (SSGs) that are available today.

You can use whatever framework and SSG you please (or even Vanilla JS if you fancy), but here are a few that we like and recommend:

## React

### Education
1. Beginners: [Thinking in React](https://reactjs.org/docs/thinking-in-react.html)
2. Beginners: [ES6 Guide](https://mrzepinski.gitbooks.io/es6-guide/content/)
3. Beginner - Advanced: [Official React Docs](https://reactjs.org/docs/hello-world.html)
4. Intermediate: [Official Redux Docs](http://redux.js.org/)

### Static Site Generators
Many of today's static site generators have gone above and beyond the humble "boilerplate" label to establish a platform that, paired with a JAMstack architecture, is taking on the monoliths and behemoths such as Wordpress, Drupal, Ruby on Rails, and more.  

Here are a few static site generators that we like and recommned:

#### [Gatsby](https://gatsbyjs.org/docs)
```
npm install --global gatsby-cli
gatsby new gatsby-site https://github.com/gatsbyjs/gatsby-starter-default
cd gatsby-site
gatsby develop
```

#### [Create-React-Native-App](https://github.com/react-community/create-react-native-app)
```
$ npm install -g create-react-native-app
$ create-react-native-app my-app
$ cd my-app/
$ npm start
```

#### What about create-react-app?

For JAMstack sites, even the create-react-app maintainers recommend Gatsby:
> If your website is mostly static (for example, a portfolio or a blog), consider using Gatsby instead. Unlike Create React App, it pre-renders the website into HTML at the build time.

Source: https://github.com/facebook/create-react-app

## Vue
Resources for getting started with Vue coming soon.

### Education

### Static Site Generators

#### Vuepress
A popular static-site generator for Vue. Get started [here](https://vuepress.vuejs.org/).


## Angular
Resources for getting started with Angular coming soon

### Education

### Static Site Generators


# Cloud Functions
Popularly known as "serverless", this is a clever method of integrating backend infrastructure without serving backend code. Your backend code lives on another service, such as AWS Lambda or Microsoft Azure, and links up with your front-end code via JavaScript functions. This architecture not only makes your websites faster, more secure, and really cool -- it also saves you a substantial amount of money. While traditional server-side code will run indefinitely, Lambda functions will only run when called, and charge you per hundred-millisecond. AWS Lambda is currently the most popular of these providers, and you can see their pricing guide [here](https://aws.amazon.com/lambda/pricing/).  

Despite its popularity, if you've ever interacted with AWS services, you'll probably agree that it's not the most user friendly or intuitive. Fortunately there are plenty of services out there that can help you get started with Lambda functions without ever seeing their GUI.

## Netlify Functions
Netlify lets you deploy Lambda functions without an AWS account, and with function management handled directly within Netlify. Your functions are version-controlled, built, and deployed along with the rest of your Netlify site, and we will automatically handle service discovery through our built-in API gateway. This eliminates overhead and brings the power of Deploy Previews and rollbacks to your functions.  

Get set up [here](https://www.netlify.com/docs/functions/).

## Serverless
With the Serverless Framework you can define your entire Serverless application, utilizing popular Serverless technologies like AWS Lambda, with a simple yaml configuration file. You can deploy from a simple CLI interface to popular cloud platforms including AWS, Microsoft Azure, Google Cloud Platform and more.

Get started [here](https://serverless.com/framework/docs/)


# Deployment

With the JAMstack, the promise of a truly modern web architecture is not just limited to development, performance, and security. It also extends to the often-frustrating user experience of deployment, hosting, and continuous integration.  

What if you could do all of that with a simple `git push`? What if you didn't have to worry about FTP, https, url configuration, SSL, or dealing with the AWS console for your Lambda functions?  

That is what Netlify does for you and more. You can learn more about how to work and deploy with Netlify here: https://www.netlify.com/docs/
