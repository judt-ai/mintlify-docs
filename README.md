# judt docs

The source of the judt documentation site, built with [Mintlify](https://mintlify.com).

## Layout

The site has three tabs, and each tab has its own directory:

| Directory | Tab | Covers |
|---|---|---|
| `manage/` | Manage Apps | Operating Apps: the API, the MCP server, the in-product agent, tokens, sandboxes, deployments, and Secrets. |
| `build/` | Build Apps | Writing the code inside an App: `wrangler.json`, bindings, storage, background work, and the celld runtime. |
| `api-reference/` | API Reference | One page for each endpoint, generated from `api-reference/openapi.json`. |

The `docs.json` file sets the navigation and the site configuration.

## Update the API reference

The `api-reference/openapi.json` file is a copy of `docs/openapi/public.json` from the `judt-ai/judt` repository. After the API changes, copy the file again. If an endpoint is added or removed, also update the API Reference groups in `docs.json`.

## Preview locally

Install the [Mintlify CLI](https://www.npmjs.com/package/mint), and then start the preview server in this directory:

```bash
pnpm dlx mint dev
```

## Writing style

Write in the Google developer documentation style. Name the runtime "celld, the judt runtime" on its first mention in a page, and "celld" after that.
