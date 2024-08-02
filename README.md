<p align="center">
  <img src="https://i.hizliresim.com/c0hz8n9.png" width="500px" />
</p>
<h4 align="center" >A module with many facilitators that you can use in your Discord.js bot 🥳</h1>

## 🚀 Updates
- ProWeb class added.
- Option function added

## 🏅 Five usage examples.
```js
const { ProLogs, ProEmbed, EmbedStyle, ProWeb, SpesteDB, Option, OptionType } = require("resthaven");

const logger = new ProLogs();
const web = new ProWeb();
const db = new SpesteDB({ path: "./src/your-database-path.json" });

logger.success("User game success worked.");
logger.info("User joined the game.");

db.set("user", { money: 300, inventory: ["Box"] }); // "user": { money: 300, inventory: ["Box"] }
const moneydata = db.get("user").money; // 300

web.get(`https://example.com`) // Response
const data = { userMoney: db.get("user").money }  // { userMoney: 300 }

web.post(
`https://example.com/api/newJoinUser`,
JSON.stringify(data),
"Content-Type": "application/json"
) // Response

const option = Option("inventory-item", "Please select an inventory item", OptionType.String, choices: [
{ name: "Box", value: "box"  },
{ name: "Sword", value: "sword"  },
])

const embed = new ProEmbed()
.setInteraction(<Interaction>) // Your interaction.
.setTitle("User Info") // Optional
.setDescription(`Money: ${moneydata}`) // Required
.setThumbail("https://example.com/thumbailUrl") // Optional
.setStatus(EmbedStyle.Default) // Required

<Interaction>.reply({ embeds: [embed.getEmbed()] }) // Reply
```

## 🕷️ I found a bug!
📱 You need contact me from
[discord.](https://discord.com/users/788725011955318784)
