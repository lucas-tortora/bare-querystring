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

## API

See the [full API reference](https://docs.pears.com/reference/bare/modules/bare-querystring).
