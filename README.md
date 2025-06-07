Impestyst - My Custom BigCommerce Catalyst Storefront



Table of Contents

Overview

Relationship to Original Catalyst

Getting Started

Prerequisites

Installation

Connecting to Your BigCommerce Store

Local Development

Deployment

Contributing

License

Attribution

Contact

Overview

This repository contains a customized version of the BigCommerce Catalyst headless commerce storefront framework. Catalyst is built with Next.js, leverages React storefront components, and is backed by the BigCommerce GraphQL Storefront API.

This custom storefront is designed to showcase skillsets acquired while working with the Senior Support team of BigCommerce, as well as to provide hands-on experience to enhance troubleshooting. 

Relationship to Original Catalyst
This project is a fork of the official BigCommerce Catalyst repository. We regularly aim to pull in updates from the upstream Catalyst project to ensure we benefit from BigCommerce's ongoing development, bug fixes, and performance improvements.

Original Catalyst Description (from their README, for context):

Catalyst is the composable, fully customizable headless commerce framework for BigCommerce. Catalyst is built with Next.js, uses our React storefront components, and is backed by the GraphQL Storefront API. By choosing Catalyst, you'll have a fully-functional storefront within a few seconds, and spend zero time on wiring up APIs or building SEO, Accessibility, and Performance-optimized ecommerce components you've probably written many many times before.

Key Features & Customizations
Here's a summary of the significant changes and additions made in this custom repository:

Getting Started
To get a local copy up and running, follow these simple steps.

Prerequisites
A BigCommerce account.
Node.js version 20 or 22.
Corepack-enabled pnpm: corepack enable pnpm
Installation
Clone this repository:
Bash

git clone https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
Install dependencies:
Bash

pnpm install
Connecting to Your BigCommerce Store
Catalyst requires connection to a BigCommerce store to fetch product data and other storefront information.

Run the Catalyst setup process:

Bash

pnpm create @bigcommerce/catalyst@latest init
Follow the prompts to connect your Catalyst project to your BigCommerce store. This will generate a .env.local file with your store's API credentials.

Note: If you already have a .env.local file from a previous setup, ensure it's configured correctly for your desired BigCommerce store and channel.

Local Development
To run the development server:

Bash

pnpm run dev
This will start the local development server, typically accessible at http://localhost:3000.

Deployment
Deployment instructions will vary depending on your chosen hosting provider (e.g., Vercel, Netlify, AWS Amplify, etc.).

General steps for Vercel (common for Next.js applications):

Create a new project on Vercel.
Connect your GitHub repository.
Configure environment variables (ensure all necessary BigCommerce API credentials from your .env.local are added to Vercel's environment variables).
Vercel will automatically detect that it's a Next.js project and deploy it.
Refer to your chosen hosting provider's documentation for detailed deployment instructions.

Contributing
We welcome contributions to this custom Catalyst storefront! If you have suggestions for improvements, bug fixes, or new features, please open an issue or submit a pull request.

Please ensure your contributions align with the project's goals and adhere to the original BigCommerce Catalyst contribution guidelines where applicable.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Note: The original BigCommerce Catalyst source code is also under the MIT License. Your modifications and any derivative work are subject to the terms of this license.

Attribution
This project is a custom fork and modification of the excellent BigCommerce Catalyst headless commerce framework. We extend our gratitude to the BigCommerce team for creating and open-sourcing this powerful foundation.

Contact
For any questions, feedback, or inquiries, please contact:

Russell Covey
GitHub: https://github.com/RustyFox13
Email: russellcovey@outlook.com



⚠️ **IMPORTANT:** As of January 6, 2025, the `main` branch is frozen. The default branch is now `canary`. Please make sure to work with and submit PRs to the `canary` branch.


<a href="https://catalyst.dev" target="_blank" rel="noopener norerrer">
  <img src="https://storage.googleapis.com/bigcommerce-developers/images/catalyst_readme_banner.png" alt="Catalyst for Composable Commerce Image Banner" title="Catalyst">
</a>

<br />
<br />

<div align="center">

[![MIT License](https://img.shields.io/github/license/bigcommerce/catalyst)](LICENSE.md)
[![Lighthouse Report](https://github.com/bigcommerce/catalyst/actions/workflows/lighthouse.yml/badge.svg)](https://github.com/bigcommerce/catalyst/actions/workflows/lighthouse.yml) [![Lint, Typecheck, gql.tada](https://github.com/bigcommerce/catalyst/actions/workflows/basic.yml/badge.svg)](https://github.com/bigcommerce/catalyst/actions/workflows/basic.yml)

</div>

**Catalyst** is the composable, fully customizable headless commerce framework for
[BigCommerce](https://www.bigcommerce.com/). Catalyst is built with [Next.js](https://nextjs.org/), uses
our [React](https://react.dev/) storefront components, and is backed by the
[GraphQL Storefront API](https://developer.bigcommerce.com/docs/storefront/graphql).

By choosing Catalyst, you'll have a fully-functional storefront within a few seconds, and spend zero time on wiring
up APIs or building SEO, Accessibility, and Performance-optimized ecommerce components you've probably written many
times before. You can instead go straight to work building your brand and making this your own.

## Demo

- [Catalyst Demo](https://catalyst-demo.site)

![-----------------------------------------------------](https://storage.googleapis.com/bigcommerce-developers/images/catalyst_readme_hr.png)

<p align="center">
 <a href="https://www.catalyst.dev">🚀 catalyst.dev</a> •
 <a href="https://developer.bigcommerce.com/community">🤗 BigCommerce Developer Community</a> •
 <a href="https://github.com/bigcommerce/catalyst/discussions">💬 GitHub Discussions</a> •
 <a href="/docs">💡 Docs in this repo</a>
</p>

![-----------------------------------------------------](https://storage.googleapis.com/bigcommerce-developers/images/catalyst_readme_hr.png)


## Deploy on Vercel

The easiest way to deploy your Catalyst Storefront is to use the [Vercel Platform](https://vercel.com/new) from the creators of Next.js.

Check out the [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

<div align="left">
  <a href="https://vercel.com/new/clone?repository-url=https://github.com/bigcommerce/catalyst&root-directory=core&project-name=my-catalyst-storefront&repository-name=my-catalyst-storefront&integration-ids=oac_nsrwzogJLEFglVwt2060kB0y&external-id=catalyst&demo-title=BigCommerce+Catalyst+with+Vercel&demo-description=Create+a+BigCommerce+Catalyst+Storefront+and+Deploy+to+Vercel&demo-url=catalyst-demo.site&demo-image=https://storage.googleapis.com/s.mkswft.com/RmlsZTozODgzZmY3Yy1hNmVlLTQ1MGUtYjRkMS1mMjEyNzgxNjk5MTY%3D/Social-image-Catalyst.png"><img src="https://vercel.com/button" alt="Deploy with Vercel"/></a>
</div>

## Quickstart

Create a new project interactively by running:

```bash
npm create @bigcommerce/catalyst@latest
```

You'll then get the following prompts:

```console
? What would you like to call your project?  my-faster-storefront
? Which would you like?
❯ Link Catalyst to a BigCommerce Store
  Use sample data

? Would you like to create a new channel? y

? What would you like to name the new channel? My Faster Storefront

Success! Created 'my-faster-storefront' at '/Users/first.last/Documents/GitHub/my-faster-storefront'
```

Next steps:

```bash
cd my-faster-storefront && npm run dev
```

Learn more about Catalyst at [catalyst.dev](https://catalyst.dev).

## Resources

- [Catalyst Documentation](https://catalyst.dev/docs/)
- [GraphQL Storefront API Playground](https://developer.bigcommerce.com/graphql-storefront/playground)
- [GraphQL Storefront API Explorer](https://developer.bigcommerce.com/graphql-storefront/explorer)
- [BigCommerce DevDocs](https://developer.bigcommerce.com/docs/build)

![-----------------------------------------------------](https://storage.googleapis.com/bigcommerce-developers/images/catalyst_readme_hr.png)

> [!IMPORTANT]
> If you just want to build a storefront, start with the [CLI](#quickstart) which will install the Next.js application in [/core](/core/).
> If you wish to contribute back to Catalyst or create a fork of Catalyst, you can check the [docs for this monorepo](https://catalyst.dev/docs/monorepo) to get started.
