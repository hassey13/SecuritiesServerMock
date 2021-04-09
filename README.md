# Data API

I have created a class to provide you data like a server might.

### Methods:

    import { ServerMock } from 'SecuritiesServerMock/ServerMock';

    ServerMock.getAllSecurities // returns a Promise that resolves to an array of all securities (stocks) supported in the mock server

        [
            { id: 1, name: 'Apple Inc.', symbol: 'AAPL' },
            ...
        ]

    ServerMock.getEquity // returns a Promise that resolves to an object with current user's equity data

        { cash: 3255.23 }

    ServerMock.getPortfolio // returns a Promise that resolves to an array of portfolio securities (stocks)

        [
            { id: 1, name: 'Apple Inc.', symbol: 'AAPL', shares: 4, cost_basis: 102.24 },
            ...
        ]

    ServerMock.getSecurityPrices // returns a Promise that resolves to a lookup security (stock) pricing data

        {
            1: { id: 1, name: 'Apple Inc.', symbol: 'AAPL', current_price: 122.42, current_price_change: 1.12, current_price_change_percent: .0087, },
            ...
        }

### Jargon:
cost_basis = average price the shares of the stock were purchased at
security/securities = stock/s
