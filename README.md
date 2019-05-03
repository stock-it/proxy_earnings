Proxy server
------

| Endpoints | Description | Ports |
| ------ | ------ | ------|
| `/stocks/:tickerID` | On startup, the static `index.html` served by the proxy server at PORT 3000 will request `:3002/bundle.js`, from the Earnings microservice | from `3000/endpoint` |
| `/api/earnings/:tickerID` | The `:3002/bundle.js` from the Earnings microservice then makes a GET request to the Earnings microservice `server running on :3002` and is routed to correct database controller | `3000/endpoint` to `3002/endpoint` |
