- [Getting started](#getting-started)
  - [Install](#install)
  - [Configure](#configure)
  - 🙌 [Retrieving API Information from Shopify](#retrieving-api-information-from-shopify)
    - 🛒 [Enabling Cart and Checkout features](#enabling-cart-and-checkout-features)
  - 🔥 [Fire it up](#fire-it-up)
- 🔌 [Plugin options](#plugin-options)
- 🎨 [Images](#images)
  - 🚀 [Use Shopify CDN](#use-shopify-cdn)
  - 🚥 [Use runtime images](#use-runtime-images)
  - 🖼️ [Download images up front](#download-images-up-front)
- 🚨 [Limitations](#limitations)
- 🛠 [Development](#development)
- 💾 [Migrating from v4 to v5](#migrating-from-v4-to-v5)

# gatsby-source-shopify

A plugin for sourcing data from Medusa to your Gatsby site.

<div id="getting-started"></div>

## Getting started

This takes you through the minimal steps to see your Medusa data in your Gatsby site's GraphiQL explorer.

<div id="install"></div>

### Install

Install this plugin to your Gatsby site.

```shell
npm install gatsby-source-medusa
```
or

```shell
yarn add gatsby-source-medusa
```

<div id="configure"></div>

### Configure

Add the plugin to your `gatsby-config.js`:

```js:title=gatsby-config.js
require("dotenv").config()

module.exports = {
  plugins: [
    {
      resolve: "gatsby-source-medusa",
      options: {
        baseUrl: process.env.MEDUSA_BASE_URL,
        fields: ["products", "regions"],
      },
    },
    ...,
  ],
}
```

<div id="query-data"></div>

### Explore your data

Run your site with `gatsby develop`. When the site builds successfully, you should see output like this:

```
You can now view your-site in the browser.
⠀
  http://localhost:8000/
⠀
View GraphiQL, an in-browser IDE, to explore your site's data and schema
⠀
  http://localhost:8000/___graphql
⠀
Note that the development build is not optimized.
To create a production build, use gatsby build
```

Now follow the second link to explore your Medusa data!
<div id="supported-fields"></div>

## Supported field types

The source plugin currently only supports the fields: products and regions.
