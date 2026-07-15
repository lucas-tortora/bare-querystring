# bare-querystring

URL query strings utilities.

```
npm i bare-querystring
```

## Usage

```js
const querystring = require('bare-querystring')

querystring.decode('name=ferret') // `{ name: "ferret" }`

querystring.encode({ name: 'ferret' }) // `name=ferret`
```

## License

Apache-2.0

<!-- bare-refgen:api start -->
## API

### Functions

#### `parse(input: string, separator?: string, delimiter?: string): Record<string, string | string[]>`

[source](https://github.com/holepunchto/bare-querystring/blob/v1.1.0/index.d.ts#L1)

Parse a query string into an object, splitting pairs on `separator` (default `&`) and key/value on `delimiter` (default `=`). `+` decodes to a space, keys and values are percent-decoded, and repeated keys collect into an array.

**Parameters**

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| `input` | `string` | — | Query string to parse. |
| `separator?` | `string` | — | Substring that separates key/value pairs (default `'&'`). |
| `delimiter?` | `string` | — | Substring that separates a key from its value (default `'='`). |

**Returns** `Record<string, string | string[]>` — An object (with a `null` prototype) mapping decoded keys to decoded values; repeated keys collect into an array.

#### `decode(input: string, separator?: string, delimiter?: string): Record<string, string | string[]>`

[source](https://github.com/holepunchto/bare-querystring/blob/v1.1.0/index.d.ts#L7)

Alias for `parse`.

**Parameters**

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| `input` | `string` | — | Query string to parse. |
| `separator?` | `string` | — | Substring that separates key/value pairs (default `'&'`). |
| `delimiter?` | `string` | — | Substring that separates a key from its value (default `'='`). |

**Returns** `Record<string, string | string[]>` — The parsed parameters, exactly as `parse` returns them.

#### `stringify(params: {}, separator?: string, delimiter?: string): string`

[source](https://github.com/holepunchto/bare-querystring/blob/v1.1.0/index.d.ts#L13)

Serialize an object into a query string, joining pairs with `separator` (default `&`) and key/value with `delimiter` (default `=`). Array values produce one pair per element.

**Parameters**

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| `params` | `{}` | — | Object whose enumerable entries become key/value pairs; array values produce one pair per element. |
| `separator?` | `string` | — | Substring used to join key/value pairs (default `'&'`). |
| `delimiter?` | `string` | — | Substring used to join a key to its value (default `'='`). |

**Returns** `string` — The percent-encoded query string.

#### `encode(params: {}, separator?: string, delimiter?: string): string`

[source](https://github.com/holepunchto/bare-querystring/blob/v1.1.0/index.d.ts#L15)

Alias for `stringify`.

**Parameters**

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| `params` | `{}` | — | Object whose enumerable entries become key/value pairs; array values produce one pair per element. |
| `separator?` | `string` | — | Substring used to join key/value pairs (default `'&'`). |
| `delimiter?` | `string` | — | Substring used to join a key to its value (default `'='`). |

**Returns** `string` — The percent-encoded query string, exactly as `stringify` returns it.
<!-- bare-refgen:api end -->