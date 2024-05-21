
<div align="center">

<img src="https://i.hizliresim.com/of5jlp4.png" height= "100px" width= "300px" > </img>

 A util package developed for Discord.js users 🎉

<a href="https://www.npmjs.com/package/speste-djs"><img src="https://img.shields.io/npm/v/speste-djs.svg?maxAge=3600" alt="npm version" /></a>
<a href="https://www.npmjs.com/package/discord.js"><img src="https://img.shields.io/npm/dt/speste-djs.svg?maxAge=3600" alt="npm downloads" /></a>


Installation

```sh
npm i speste-djs
```



## Example for ProLogs

</div>

```js
const { ProLogs } = require("speste-djs")

const logger = new ProLogs()

logger.info("Exercitation commodo ea duis nulla officia duis culpa magna duis laboris ex.")
logger.success("Nulla enim eiusmod nulla sint magna proident esse dolor.")
logger.warning("Commodo anim proident qui ea excepteur ullamco eiusmod mollit laboris elit.")
logger.error("In elit mollit commodo magna.")


//Underline with info
logger.info( logger.underline("Fusce id velit ut tortor pretium") + " suspendisse potenti nullam." )


//Italic without special log.
const italic = logger.italic("Hello") + " world.";
console.log(italic)



//Bold without special log.
const bold = logger.bold("Tellus molestie nunc") + " on blandit massa enim nec dui nunc..";
console.log(bold)
```


<div align="center">

## Example for ProEmbed

</div>

```js
const { ProEmbed } = require("speste-djs")

const embed = new ProEmbed()

embed.setInteraction(interaction)
embed.setDescription("Vitae elementum curabitur vitae nunc sed velit dignissim sodales.")
embed.setStatus("success")

interaction.reply({ embeds: [ embed.getEmbed() ] })
```

<div align="center">

## Others..

</div>

```js
const { ValidChecker, Random, ConvertTurkishChars, convertMessageToInteraction, convertMemberToInteraction } = require("speste-djs")


/* Convert Turkish chars to English chars.  */

const converted = new ConvertTurkishChars()
    .setString("Bugün hava çok güzel, dışarı çıkıp doğa yürüyüşü yapmayı düşünüyorum.")
    .getConverted()
console.log(converted) // Bugun hava cok guzel, disari cikip doga yuruyusu yapmayi dusunuyorum.



/*  Valid Checker  */
const validChecker = new ValidChecker()

console.log(validChecker.checkEmail("example@gmail.com")) //true
console.log(validChecker.checkEmail("example @gmail .com")) //false, because is not a valid.
console.log(validChecker.checkEmail("Congue mauris rhoncus.")) // false




/* Random */

const arr = ["yellow", "red", "black", "white", "1", "2"] //...

const random = new Random()
    .setArray(arr)
    .getRandom()

console.log(random) //A completely random answer...


/* Convert your message or member object to interaction */
/* In its normal state, ProEmbed does not support message and member objects. */

//member to interaction

client.on("guildMemberAdd", async (member) => {

    const interaction = convertMemberToInteraction(member)

    const embed = new ProEmbed()

    embed.setInteraction(interaction)
    embed.setDescription(`Welcome, ${member.user.username}`)
    embed.setStatus("default")

    member.send({ embeds: [embed.getEmbed()] })

})

// message to interaction

client.on("messageCreate", async (message) => {

    const interaction = convertMemberToInteraction(message)

    const embed = new ProEmbed()

    embed.setInteraction(interaction)
    embed.setDescription(`Message sended. Content: ${message.content}`)
    embed.setStatus("default")

    message.channel.send({ embeds: [ embed.getEmbed() ] })

})
```
