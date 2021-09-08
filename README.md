## Proxying Plausible endpoints through Cloudflare

This is needed as some Ad-blockers prevent scripts from other domains from beeing fetched.

Script is from [Plausible Analytics docs](https://plausible.io/docs/proxy/guides/cloudflare).

## Deployment

You have 3 possibilities to deploy this script to Cloudflare Workers:

1. Copy the code from `index.js` and past it into the Cloudflare Workers Web Editor.
2. Install Cloudflare's CLI tool wrangler globally, login and deploy your script like [here](https://developers.cloudflare.com/workers/get-started/guide).
3. Inject this project into a CI/CD pipeline, inject the wrangler ENV variables `CF_ACCOUNT_ID`, `CF_ZONE_ID` and `CF_API_TOKEN` respectively and run the `yarn publish` command.

It is also possible to configure the associated domain via wrangler or the `wrangler.toml` file like it's documented [here](https://developers.cloudflare.com/workers/get-started/guide#optional-configure-for-deploying-to-a-registered-domain).
