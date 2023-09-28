# Setup Environment

Fill in what dev container is and how it works. Then explain how this codespace works.

![next movies site](./../assets/01-Movies-Site.png)

## Get API Keys

Get your API keys from website

## Codespaces

From GitHub choose the open in Code Spaces option.
Open the codespaces secrets and create two secrets for NEXT_PUBLIC_TMDB_API_KEY and NEXT_PUBLIC_TMDB_API_READ_ACCESS_TOKEN


## Docker

Start by having Docker desktop running on the containers tab
Clone this repo and then click the blue menu at bottom left and choose open folder in container

Copy the .env.local.exmaple file and rename it to .env.local
Add in the API Key and token from site

On the bottom left of VS Code you will see you are using a Dev Container.

## Running the Next app

Install dependencies

```bash
npm i --legacy-peer-deps
```

Run the dev server

```bash
npm run dev
```

