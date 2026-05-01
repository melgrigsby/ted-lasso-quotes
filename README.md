# Ted Lasso quotes API

This repo was forked from [https://github.com/jamesseanwright/ron-swanson-quotes](https://github.com/jamesseanwright/ron-swanson-quotes).  I didn't really do anything exciting with it other than change the quotes and update the dependencies.

---

A Node.js server to serve up quotes from the TV show Ted Lasso.

## Production host

[https://ted-lasso-quotes.onrender.com](https://ted-lasso-quotes.onrender.com)

The `Access-Control-Allow-Origin` header is set to `*` so that you can make requests from any domain.

## APIs

### `GET /v2/quotes`

Returns an array with one quote:

```json
[
   "Doing the right thing is never the wrong thing."
]
```

### `GET /v2/quotes/<count>`

Returns an array with `<count>` quotes e.g. `GET /quotes/2`

```json
[
    "I don't like gossip, but my butt enjoys a little scuttle.",
    "Change isn't about trying to be perfect. Perfection sucks. Perfect is boring."
]
```

### `GET /v2/quotes/search/<term>`

Returns an array of quotes matching `<term>` without case sensitivity e.g. `GET /quotes/search/poopeh`

```json
[
    "Lads, remember, it's just poopeh. Let it flow."
]
```

## OpenAPI 3 Schema

An [OpenAPI](https://swagger.io/docs/specification/about/) 3 schema is available at `/v2/schema`.

## Local development

Once you've cloned this repo, run `npm i` to install the dependencies.

Then you can run:

* `npm run build`: builds the TypeScript source code
* `npm start`: runs the compiled server
