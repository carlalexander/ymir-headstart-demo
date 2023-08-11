# Ymir + HeadstartWP

This is a demo repository for creating a serverless headless WordPress site using [HeadstartWP](https://headstartwp.10up.com/) deployed to [Vercel](https://vercel.com) and WordPress deployed with [Ymir](https://ymirapp.com).

You can find the demo site at [https://ymir-headstart-demo.vercel.app/](https://ymir-headstart-demo.vercel.app/).

## Getting Started

The project is divided into two parts: the WordPress site and the frontend application. Each part has its own directory at the root of the project. `headstart` contains the frontend application and `wordpress` contains the WordPress site.

The WordPress site uses [bedrock](https://github.com/roots/bedrock). This allows the WordPress site to be managed via [composer](https://getcomposer.org/). The WordPress site gets deployed with Ymir using GitHub Actions. You will need to deploy the WordPress site once to get the URL to set for the `NEXT_PUBLIC_WORDPRESS_URL` environment variable in the frontend application.

The frontend application is the HeadstartWP Next.js application. It's deployed automatically to Vercel. The deployment gets triggered via the Vercel GitHub integration that you have to configure inside your Vercel project. Make sure you do the following: 

 * Set the root of the project to the `headstart` directory.
 * Ensure the Vercel build is for Next.js
 * Set the `NEXT_PUBLIC_WORDPRESS_URL` environment variable to the URL of your WordPress site.

## Acknowledgements

Thank to [10up](https://10up.com/) for creating HeadstartWP so that I have headless application I can create a demo of. 😅 