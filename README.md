
<div align="center">

<img src="https://i.hizliresim.com/of5jlp4.png" height= "100px" width= "300px" > </img>

 A util package developed for Discord.js users 🎉

<a href="https://www.npmjs.com/package/speste-djs"><img src="https://img.shields.io/npm/v/speste-djs.svg?maxAge=3600" alt="npm version" /></a>
<a href="https://www.npmjs.com/package/speste-djs"><img src="https://img.shields.io/npm/dt/speste-djs.svg?maxAge=3600" alt="npm downloads" /></a>


Installation

```sh
npm i speste-djs
```

Defines

```sh
const {
SpesteDB,
ProLogs, ProEmbed,
ConvertTurkishChars, TDKGlossary, ValidChecker, Random,
viewFile, ms,
convertMemberToInteraction,
convertMemberToInteraction 
} = require("speste-djs")
```

<div align="center">

### Example for SpesteDB

</div>

```js

```



## Example for ProLogs

</div>

```js

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
Ouput: <br>
<img src="https://i.hizliresim.com/4rind9r.png" height= "120px" width= "500px" > </img> 

<div align="center">

## Example for ProEmbed

</div>

```js

const embed = new ProEmbed()

embed.setInteraction(interaction)
embed.setDescription("Vitae elementum curabitur vitae nunc sed velit dignissim sodales.")
embed.setStatus("success")

interaction.reply({ embeds: [ embed.getEmbed() ] })
```


<div align="center">

### Example for Random

</div>

```js
const arr = ["yellow", "red", "black", "white", "1", "2"] // ..

const random = new Random()
    .setArray(arr)
    .getRandom()

console.log(random);
```


<div align="center">

### Contact with developer: [Discord](https://discord.com/users/788725011955318784)

</div>
