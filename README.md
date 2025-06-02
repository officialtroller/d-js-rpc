# Discord.js RPC Extension++

This Discord RPC package allows you to set activity types in your Discord Rich Presence.
Everything else works as normal.

### __Simple__ Example using types:
```js
const RPC = require('d-js-rpc')
const clientId = 'your_client_id';
const client = new RPC.Client({ transport: 'ipc' });
client.on('ready', () => {
  console.log('Authed for user', client.user.username);

  client.setActivity({
    details: 'Example Presence',
    state: 'Im listening',
    type: 2 // for listening
  });
});

client.login({ clientId });
```
