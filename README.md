<p align="center">
  <a href="https://www.medusa-commerce.com">
    <img alt="Medusa" src="https://user-images.githubusercontent.com/7554214/129161578-19b83dc8-fac5-4520-bd48-53cba676edd2.png" width="100" />
  </a>
</p>
<h1 align="center">
  gatsby-source-medusa
</h1>
<p align="center">
Medusa is an open-source headless commerce engine that enables developers to create amazing digital commerce experiences. This is a Gatsby source plugin for building websites using Medusa as a data source.
</p>
<p align="center">
  <a href="https://github.com/medusajs/medusa/blob/master/LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="Medusa is released under the MIT license." />
  </a>
  <a href="https://github.com/medusajs/medusa/blob/master/CONTRIBUTING.md">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat" alt="PRs welcome!" />
  </a>
  <a href="https://discord.gg/xpCwq3Kfn8">
    <img src="https://img.shields.io/badge/chat-on%20discord-7289DA.svg" alt="Discord Chat" />
  </a>
  <a href="https://twitter.com/intent/follow?screen_name=medusajs">
    <img src="https://img.shields.io/twitter/follow/medusajs.svg?label=Follow%20@medusajs" alt="Follow @medusajs" />
  </a>
</p>

## Quickstart

This takes you through the minimal steps to see your Medusa data in your Gatsby site's GraphiQL explorer.

<div id="install"></div>

### 1. Installation

Install the source plugin to your Gatsby project using your favorite package manager.

```shell
npm install gatsby-source-medusa
```

```shell
yarn add gatsby-source-medusa
```

### 2. Configuration

Add the plugin to your `gatsby-config.js`:

```js:title=gatsby-config.js
require("dotenv").config()

module.exports = {
  plugins: [
    {
      resolve: "gatsby-source-medusa",
      options: {
        storeUrl: process.env.MEDUSA_URL,
      },
    },
    ...,
  ],
}
```

## You are ready to query your data

You should now be able to view your stores `products` and `regions` in your [Gatsby site's GraphiQL explorer](http://http://localhost:8000/__graphiql).
