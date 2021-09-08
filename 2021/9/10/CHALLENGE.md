# Challenge 9-8-2021

```javascript
function encrypt(str) {
  let enc = [];

  for (let i = 0; i < str.length; i++) {
    const raw = str[i].charCodeAt(0);
    let result;

    if (raw > 100) result = raw - 50;
    else if (raw > 50) result = raw * 69;
    else result = raw * 1337;

    enc.push(result);
  }

  return enc;
}

function decrypt(enc) {
  let dec = '';

  for (let i = 0; i < enc.length; i++) {
    /* solution */
  }

  return dec;
}

const enc = encrypt('...' /* find this key */);
console.log(enc);

const dec = decrypt(enc);
console.log(dec);
```

### Resources/hints
- [String.prototype.charCodeAt() - MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt)
- [String.fromCharCode() - MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
