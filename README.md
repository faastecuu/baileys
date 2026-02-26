# Modified Baileys By Faastecuu
<p align='center'>
  <img src="https://files.catbox.moe/6rnx3e.mp4" width="172">
</p>

--- 

## Usage
```json
"depencies": {
  "@whiskeysockets/baileys": "faastecuu/Baileys"
}
```
## Import
```javascript
const {
  default:makeWASocket,
  // Other Options 
} = require('@whiskeysockets/baileys');
```

---
# How To Connect To Whatsapp
## With QR Code
```javascript
const {
  default: makeWASocket
} = require('@whiskeysockets/baileys');

const client = makeWASocket({
  browser: ['Ubuntu', 'Chrome', '20.00.1'],
  printQRInTerminal: true
})
```

## Connect With Number
```javascript
const {
  default: makeWASocket,
  fetchLatestWAWebVersion
} = require('@whiskeysockets/baileys');

const client = makeWASocket({
  browser: ['Ubuntu', 'Chrome', '20.00.1'],
  printQRInTerminal: false,
  version: fetchLatestWAWebVersion()
  // Other options
});

const number = "628XXXXX";
const code = await client.requestPairingCode(number.trim) /* Use : (number, "YYYYYYYY") for custom-pairing */

console.log("Ur pairing code : " + code)
```

# Sending messages

## send orderMessage
```javascript
const fs = require('fs');
const Fareldestroyer = fs.readFileSync('./faastecuuimg');

await client.sendMessage(m.chat, {
  thumbnail: faastecuu,
  message: "Gotta get a grip",
  orderTitle: "pdfFile",
  totalAmount1000: 72502,
  totalCurrencyCode: "IDR"
}, { quoted:m })
```

## send pollResultSnapshotMessage
```javascript
await client.sendMessage(m.chat, {
  pollResultMessage: {
    name: "faastecuu",
    options: [
      {
        optionName: "poll 1"
      },
      {
        optionName: "poll 2"
      }
    ],
    newsletter: {
      newsletterName: "faastecuu Information",
      newsletterJid: "1@newsletter"
    }
  }
})
```

## send productMessage
```javascript
await client.relayMessage(m.chat, {
  productMessage {
    title: "faastecuudestroyer",
    description: "zZZ...",
    thumbnail: { url: "./faastecuu" },
    productId: "EXAMPLE_TOKEN",
    retailerId: "EXAMPLE_RETAILER_ID",
    url: "https://t.me/faastecuu",
    body: "Nak Tido",
    footer: "Footer",
    buttons: [
      {
        name: "cta_url",
        buttonParamsJson: "{\"display_text\":\"Faastecuu\",\"url\":\"https://t.me/Fareldestroyer\"}"
      }
    ],
    priceAmount1000: 72502,
    currencyCode: "IDR"
  }
})
```
