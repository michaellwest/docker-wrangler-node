# Docker Demo for Cloudflare Wrangler

Run from the terminal:

```bash
docker exec -it wrangler-node-1 cmd
```

Following the [Getting Started guide](https://developers.cloudflare.com/workers/get-started/guide/) you can create and start working with your new project:

```bash
wrangler init my-worker
cd my-worker
```

Since you are running from a console in the container, you'll need to create an API token before proceeding.

Open the .env and update your Account ID and API Token.

```text
CLOUDFLARE_ACCOUNT_ID=
CLOUDFLARE_API_TOKEN=
```