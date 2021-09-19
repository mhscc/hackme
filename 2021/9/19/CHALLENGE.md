# Challenge 9-18-2021
![difficulty](https://img.shields.io/badge/Difficulty-Easy-brightgreen)

### Intro

Encryption and decryption (also known as conversion) are a big part of many apps. We use conversions to make storing or transferring data much easier or secure. There are many types of conversion — [Base64](https://en.wikipedia.org/wiki/Base64) for data transfer or encoding and [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) for string encryption, to name a few.

### Reward

Once you write your decryption function, you can use it to reveal the encrypted gift card code. The string returned will be a $5 Google Play gift card code. Redeem it as soon as you can. Please contact us once you solve this challenge; we will announce the winner and reveal the solution after.

### Code

```js
// returns an array of bytes
function encrypt(str) {
  let enc = [];

  for (let i = 0; i < str.length; i++) {
    let result;
    const raw = str[i].charCodeAt(0);

    if (raw > 100) result = raw - 50;
    else if (raw > 50) result = raw * 69;
    else result = raw * 1337;

    enc.push(result);
  }

  return enc;
}

// returns a string
function decrypt(enc) {
  let dec = '';
  
  /* solution */

  return dec;
}
```

Encrypted gift card code:
```
[
  4899, 5658, 4623, 6141,
  5244, 3726, 6210, 3864,
  5244, 3726, 6003, 6141,
  4623, 3864, 3933, 5865
]
```

### Goal

You must write a fully working decryption function. Here is an example of how it should function:

```js
const enc = encrypt('Hello, world!');
console.log(enc);
// [ 4968, 51, 58, 58, 61, 58828, 42784, 69, 61, 64, 58, 6900, 44121 ]

const dec = decrypt([ 4968, 51, 58, 58, 61, 58828, 42784, 69, 61, 64, 58, 6900, 44121 ]);
console.log(dec);
// 'Hello, world!'
```

---

### Code Execution/editing

You can use a code-editor such as [Visual Studio Code](https://code.visualstudio.com/) or even a text-editor such as Notepad. For compiling or debugging, you can use the [developer tools](https://balsamiq.com/support/faqs/browserconsole/) on any web browser. However, we recommend using an editor and compiler service such as [OneCompiler's JS Compiler](https://onecompiler.com/javascript/).

### Resources/hints

- [String.prototype.charCodeAt() - MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt)
- [String.fromCharCode() - MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
