# cybralist.js
<a href="https://cybralist.com/dc" target="_blank"><img src="https://logos-world.net/wp-content/uploads/2020/12/Discord-Logo.png?size=512" alt="Join our discord" width="256"></a><br>
**Support:** [https://cybralist.com/discord](https://cybralist.com/discord) <br>
**NPM:** [npmjs.com/package/cybralist.js](https://www.npmjs.com/package/cybralist.js)<br>

## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://cybralist.com/discord) address.*
- `npm i cybralist.js`

# Define Module & Client
```js
const Discord = require("discord.js");
const client = new Discord.Client();
const cybralist = require("cybralist.js");
const dbl = new cybralist("TOKEN-HERE", client);

client.login("BotToken");
```

# Server Count & Shard Count Posting
```js
client.on("ready", async () => {
  dbl.serverCount();
  /* 
  -> Server count posted. 
  or 
  -> Server count & shard count posted.
  */

});
```

# Vote Checking
```js
let hasVote = await dbl.hasVoted("714451348212678658"); // -> User ID
  if(hasVote === true) {
      console.log("Voted")
    } else {
      console.log("Vote please.")
  }
// -> Vote please.
```

# Search on cybralist
```js
let botFind = await dbl.search("779641401482805289");
console.log(botFind.username) // -> Allegro
```
