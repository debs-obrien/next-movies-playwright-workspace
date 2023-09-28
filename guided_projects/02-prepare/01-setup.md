# Project overview

<!-- describes the project and how they'll build it at a high level. -->

The project is a movies application which has been built using the Next.js framework. 

![next movies site](./../assets/01-Movies-Site.png)

We will setup Playwright and create end to end tests for this project. We will do this by running the app locally and using the built in dev server to test our application. 

We will use Playwright's tooling to generate tests and run tests in UI mode so we can see a full trace of our tests and use watch mode to watch for any changes in our test files and automatically re run the test.

Once we have written our tests we will then push our changes to GitHub and have our tests run on Continuous Integration and learn how to generate HTML reports, debug on CI and use sharding to help with scaling, meaning our tests will run faster on CI.

## Pre-requisites

### Check Node version

Make sure you have [Node v18 or above](https://nodejs.org/en/download). You can check this by running:

```bash
node -v
```

### Check npm is installed

You should also have [`npm`](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) installed. 

You can check the latest version of npm by running:

```bash
npm -v
```

### Check git is installed

Make sure you have [Git](https://git-scm.com/downloads) installed.

```bash
git
```

### Create a GitHub account

If you don't already have a [GitHub account](https://github.com/) you should go ahead and create one.

### Install VS Code

[Install VS Code](https://code.visualstudio.com/) if you don't already have it. You can use any editor when working with Playwright however VS Code has a Playwright extension which makes for a great developer experience when writing and running tests. 

## Setup

<!-- walks them through the setup of all needed tools, installations, accounts, etc. -->

### Get API Keys

1.Get your [API keys from website](https://www.themoviedb.org/signup)

1.Add your API keys to the `.env.local.example` file

1.Rename the file to `.env.local`

### Install dependencies for the Next app

Clone the next-movies repo from GitHub and open it in VS Code. Open the terminal and cd into the 'next-movies' directory. Install the dependencies.

```bash
npm i --legacy-peer-deps
```

### Running the Next app

Run the dev server

```bash
npm run dev
```

You should see the following message in your terminal

```bash

> movie-app@0.1.0 dev
> next dev -p 8080

ready - started server on 0.0.0.0:8080, url: http://localhost:8080
```

Open the URL, [http://localhost:8080](http://localhost:8080) in your browser where you should now see the movies app running.

![next movies site](./../assets/01-Movies-Site.png)

## Option 1: Local setup

### Installing Playwright

Open up another terminal window and install Playwright inside the 'next-movies' directory. When running the command below it will ask you some questions. Mostly you can just press enter to accept the default values however we do want to add a GitHub actions so press `y` when asked about that.

```bash
npm init playwright@latest
```

If you run into any errors run the command again with the following flag `--legacy-peer-deps`.

Once Playwright has been installed you should see the following message in the terminal.

```bash
✔ Success! Created a Playwright Test project at /Users/xxxxxxxx/next-movies

Inside that directory, you can run several commands:

  npx playwright test
    Runs the end-to-end tests.

  ...

Visit https://playwright.dev/docs/intro for more information. ✨

Happy hacking! 🎭
```

## Option 2: Codespaces setup

From GitHub choose the open in Code Spaces option.
Open the codespaces secrets and create two secrets for:
- NEXT_PUBLIC_TMDB_API_KEY
- NEXT_PUBLIC_TMDB_API_READ_ACCESS_TOKEN


## Option 3: Docker setup

Start by having Docker desktop running on the containers tab
Clone this repo and then click the blue menu at bottom left and choose open folder in container.

Copy the .env.local.exmaple file and rename it to .env.local
Add in the API Key and token from site

On the bottom left of VS Code you will see you are using a Dev Container.
