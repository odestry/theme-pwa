# theme-name

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat&colorA=338fbb&colorB=1c1c1c&logoColor=ffffff)](https://github.com/odestry/contribute)
[![Discord Shield](https://img.shields.io/discord/983602196493004820?style=flat&colorA=338fbb&colorB=1c1c1c&label=discord&logo=discord&logoColor=ffffff)](https://discord.gg/blanklob-community-983602196493004820)

[Usage](#usage) |
[Tools](#tools) |
[Contributing](#contributing) |
[License](#license)

An opinionated lightweight theme starter for all projects.

## Usage

To get started clone the template by clicking the **Use this template** button or by running the following command:

```bash
git clone https://github.com/odestry/theme-starter.git
```

### Running the development server

To run the development server, you'll need to have [Shopify CLI](#shopify-cli) as well as [Node.js](https://nodejs.org) installed on your machine.

1. Install the dependencies

```bash
npm install
```

2. Connect to your store

To connect your store update the `shopify.theme.toml` file with your store's information.

```toml
[environments.development]
store = "john-apparel.myshopify.com"
```

3. Start the development server

```bash
npm run dev
```

After authenticating, this will start a local development server running at `https://localhost:9292` that you can use to preview your changes.

## Tools

There are a number of really useful tools that the Shopify Themes team uses during development. This theme is already set up to work with these tools.

### Shopify CLI

[Shopify CLI](https://github.com/Shopify/shopify-cli) helps you build Shopify themes faster and is used to automate and enhance your local development workflow. It comes bundled with a suite of commands for developing Shopify themes—everything from working with themes on a Shopify store (e.g. creating, publishing, deleting themes) or launching a development server for local theme development.

You can follow this [quick start guide for theme developers](https://github.com/Shopify/shopify-cli#quick-start-guide-for-theme-developers) to get started.

### Tailwind CSS

[Tailwind CSS](https://tailwindcss.com) is a utility-first CSS framework for rapidly building custom storefront interfaces. It's a great way to build Shopify themes and sections quickly. You can find the configuration file at `tailwind.config.ts`. We use Vite to compile Tailwind CSS.

### Theme Check

We recommend using [Theme Check](https://github.com/shopify/theme-check) as a way to validate and lint your Shopify themes.

Theme Check is a command line tool that runs a series of tests against your theme code to surface errors, deprecations, and potential bugs. It's a great way to ensure your theme is up to date with the latest best practices and that you're not using any deprecated Liquid or JSON fields.

You can also run it from a terminal with the following Shopify CLI command:

```bash
shopify theme check
```

### Continuous Integration

This theme uses [GitHub Actions](https://github.com/features/actions) to maintain the quality of the theme. [This is a starting point](https://github.com/odestry/theme-starter/blob/main/.github/workflows/ci.yml) and what we suggest to use in order to ensure you're building better themes. Feel free to build off of it!

#### Shopify/lighthouse-ci-action

We love fast websites! Which is why we created [Shopify/lighthouse-ci-action](https://github.com/Shopify/lighthouse-ci-action). This runs a series of [Google Lighthouse](https://developers.google.com/web/tools/lighthouse) audits for the home, product and collections pages on a store to ensure code that gets added doesn't degrade storefront performance over time.

#### Shopify/theme-check-action

This theme runs [Theme Check](https://github.com/Shopify/theme-check-action) on every commit via [Shopify/theme-check-action](https://github.com/Shopify/theme-check-action).

## Contributing

We'd love your help! Please read our [contributing guide](https://github.com/odestry/contribute) to learn about our development process, how to propose bug fixes and improvements.

## License

Copyright (c) 2023-present Odestry. See [LICENSE](/LICENSE.md) for further details.
