# Solution

```javascript
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
  for (let i = 0; i < enc.length; i++) {
      const modi = enc[i];
      let result;
      
      if (modi < 100) result = modi + 50;
      else if (modi % 69 == 0) result = modi / 69;
      else result = modi / 1337;
      
      dec += String.fromCharCode(result);
  }
  
  return dec;
}
```
