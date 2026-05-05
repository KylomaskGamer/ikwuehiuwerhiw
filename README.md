# ikwuehiuwerhiw

acronym for "i know weird users eat hamburgers in unknown wacky epic rooms how is wurger"

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

UPDATE: cors proxy is ass and now returns 403s when it attempts to fetch something greater than A SINGLE FLIPPING MEGABYTE

UPDATE: so i connected my domain to this luckily, you may now fetch from https://gh.kylomaskgamer.ca

## i hear copyright music and i want to complain about it / take down your repository

NO, PLEASE DON'T! I tried to organize the issues tab so you can report copyright issues there!

and nintendo if youre merciless enough just do it

### I'm not the one who owns the copyright

ill just act as google and say that you have to be the original copyright holder. attempts to takedown as someone else will count as false

you may still use issues in case that i forgot credit or you want to be claimed as ABSOLUTE SH@#&$POST

### I'm the one who owns the copyright

i want to collaborate together. create an issue for the takedown and let me know which file(s) is breaching copyright. i'll try to take it down, but it wont be instant unless you send me a replacement file (i wont pay money at all for the replacements because i dont get money for this anyways)
