#### JSON URL VIEW 
https://raw.githubusercontent.com/HanX-ID/quote-jepang/refs/heads/main/data.json

#### MY CASE BOT
```javascript
case "quote": {
  try {
    let res = await fetch("https://raw.githubusercontent.com/HanX-ID/quote-jepang/refs/heads/main/data.json");
    let data = await res.json();
    let keys = Object.keys(data);
    let random = keys[Math.floor(Math.random() * keys.length)];
    let quote = data[random];

    m.reply(`*${quote.kata}*\n*${quote.arti}*`);
  } catch (e) {
    console.error(e);
    m.reply("gagal mengambil kata bijak.");
  }
}
break;
```
