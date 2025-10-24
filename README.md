# ikwuehiuwerhiw

game jam stuff. do **not** steal. grab it from the original source if you need it

## i don’t hear music! why??? :(

tl;dr: blame it all on [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CORS/Errors)

ntl;wtr, sometimes the content just… refuses to work
like some server out there decided `'that request is MAYBEEEE bad'`
don’t be mean to the poor server though, it’s just doing its thing 😅
also, staying under the 32MB upload limit for PenguinMod can be annoying
(i haven’t donated yet, but i probably should… forgot lol)

here’s a simple workaround if you want to avoid hitting the upload limit:

1. upload your files to GitHub
2. link them in your project
3. use a pseudocode script like this:

```py
from pm_Project import Stage
    
songlist = ["poop","pee","pooppoop","peepee"]
    
for i, v in songlist:
    Stage.add_sound(src="https://github.com/KylomaskGamer/ikwuehiuwerhiw/" + v)
```

sometimes PenguinMod’s `fetch()` complains with `"nu uh, lacks a header thingy i forgot"`
so here’s the ULTIMATE workaround in a **chaotic pseudoscript**
(mix of Python, JS, Lua, and maybe stuff i made up):

```py
from pm_Project import Stage
import cors

songlist = ["poop","pee","pooppoop","peepee"]
req = fetch("https://github.com/KylomaskGamer/ikwuehiuwerhiw")
cors_required = str(req.error).includes("NetworkError")

for i, v in songlist:
    if cors_required:
        Stage.add_sound(src=cors.proxy("https://github.com/KylomaskGamer/ikwuehiuwerhiw/" + v))
    else:
        Stage.add_sound(src="https://github.com/KylomaskGamer/ikwuehiuwerhiw/" + v)
```

the cors extension comes from PenguinMod’s [extension library](https://extensions.penguinmod.com), specifically:
[`https://extensions.penguinmod.com/extensions/NamelessCat/corsproxy.js`](https://extensions.penguinmod.com/extensions/NamelessCat/corsproxy.js)

this was reforamtted by chatgpt

for firefox suers, in case it happens heres the extension i use https://addons.mozilla.org/en-US/firefox/addon/cors-unblock/
