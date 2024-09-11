# NuxtAuth

A small template to use Nuxt with some features already baked in

## About

This is a small project to be used as a template of sorts. It comes with the
following features:

- PrimeVue, for UI components
- Tailwind, for styling
- Auth0, for authentication
- PostHog, for analytics

More details [here](https://docs.google.com/document/d/1UPcMZHZF0V_bencLmeDzq_7Sn9uIsaa0EP_Xj9qJ6T4/edit)

## Setup

Locally, you just need to setup node like usual:

```bash
npm install
```

That is it, you can run your development application using:

```bash
npm run dev
```

## Configuration

Check the `.env.example` file for the environment variables you need to set.

### PostHog

Create an account on PostHog website and then create a project. You will find your public key in Settings > General > Project ID

### Auth0

Create an account on Auth0 website and then create an application. Inside your applicaiton, in Settings > Basic Information, you will find your keys and credentials.
It's important ot remember that the domain needs to contain the `https://` prefix to work properly.

You also need to set the Allowed Callback URLs in the Application URIs section to `http://localhost:3000/api/auth/callback/auth0` for development.

### Vercel and GitHub Actions

The action is already setup to deploy to Vercel on any push or pull request, but the branch is not specified.
If you want do deploy on a specific branch, you have to change the `build.yml` workflow file.

Also, the repository secrets need to be set in the GitHub repository settings, following the names defined in the workflow file.