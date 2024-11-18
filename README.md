# wrangler secret bulk put repro

Run the following to repro this issue:

```shell
pnpm install
# create the worker with a text binding "MY_VAR"
pnpm wrangler deploy

# try to set MY_VAR to a secret using bulk command:
pnpm wrangler secret bulk ./secrets.json
```

This will result in the following unhelpful error:

```
$ pnpm wrangler secret bulk ./secrets.json

 ⛅️ wrangler 3.87.0
-------------------

🌀 Creating the secrets for the Worker "wrangler-action-example-bulk-failing"

Finished processing secrets JSON file:
✨ 0 secrets successfully uploaded

✘ [ERROR] 🚨 1 secrets failed to upload


If you think this is a bug then please create an issue at https://github.com/cloudflare/workers-sdk/issues/new/choose
```
