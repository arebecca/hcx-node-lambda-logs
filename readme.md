### Usage
```javascript
const logs = require('logs');

logs.init(process.env.SENTRY_DSN);

const server = new ApolloServer({
  plugins: [logs.apolloPlugin],
  // ...
});

exports.handler = logs.wrapHandler(server.createHandler());

```