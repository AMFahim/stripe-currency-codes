# stripe-currency-codes

`stripe-currency-codes` is an NPM package that provides a list of currency codes supported by Stripe. This package allows developers to easily access and use Stripe's supported currencies within their applications.

## Installation

To install the package, run:

```bash
npm install stripe-currency-codes
```
## Usage

Here is an example of how to use the `useStripeCurrency` hook from the `stripe-currency-codes` package in a React component:
```js
import React from 'react';
import { useStripeCurrency } from 'stripe-currency-codes';

const App = () => {
  const { stripeCurrencies } = useStripeCurrency();

  console.log(stripeCurrencies);

  return (
    <>
      <ul>
        {stripeCurrencies.map((currency, index) => (
          <li key={index}>{currency}</li>
        ))}
      </ul>
    </>
  );
}

export default App;
```

### Hook: useStripeCurrency

#### Description

The `useStripeCurrency` hook returns an object containing the list of Stripe-supported currency codes.

#### Example
```js
const { stripeCurrencies } = useStripeCurrency();
```
#### Return Value

-   `stripeCurrencies`: An array of currency codes supported by Stripe.

### Example Application

You can integrate the `useStripeCurrency` hook in your React application as shown below:
```js
import React from 'react';
import { useStripeCurrency } from 'stripe-currency-codes';

const CurrencyList = () => {
  const { stripeCurrencies } = useStripeCurrency();

  return (
    <div>
      <h1>Stripe Supported Currencies</h1>
      <ul>
        {stripeCurrencies.map((currency, index) => (
          <li key={index}>{currency}</li>
        ))}
      </ul>
    </div>
  );
}

export default CurrencyList;
```
Note: You can also use it in input fields, dropdown, or any necessery fields. It does not supported in backend api.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have any suggestions or improvements.
## License

This project is licensed under the ISC License.

## Contact

If you have any questions or need further assistance, feel free to contact the package maintainer.