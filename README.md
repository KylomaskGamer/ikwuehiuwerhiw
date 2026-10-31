# ikwuehiuwerhiw

Acronym for "I Know Weird Users Eat Hamburgers In Unknown Wacky Epic Rooms How Is Wurger"

Game jam stuff. Do **not** steal. Grab it from the original source if you need it.

> [!IMPORTANT]
> If you believe a file hosted here infringes your copyright, please read [`CONTRIBUTING.md`](CONTRIBUTING.md) for information on reporting it.

## i don’t hear music! why??? :(

TL;DR: blame it all on [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CORS/Errors).

NTL;WR, sometimes the content just dont spawn

Like some server out there decided `'that request is MAYBEEEE bad'`.

Don't be mean to the poor server, though. It's just doing its thing 😅

Also, staying under PenguinMod's 32 MB upload limit can be annoying (56 MB for Donators).

~~(I haven't donated yet, but I probably should… forgot lol)~~ i donated yes i did im a donor now theres a patreon (im still using this because audio files are as big as a double angus cheeseburger at harveys)

Here's a simple workaround if you want to avoid hitting the upload limit:

1. Upload your files to GitHub.
2. Link them in your project.
3. Use a pseudocode script like this:

```py
from pm_Project import Stage

songlist = ["poop", "pee", "pooppoop", "peepee"]

for i, v in songlist:
    Stage.add_sound(src="https://github.com/KylomaskGamer/ikwuehiuwerhiw/" + v)
```

Sometimes PenguinMod's `fetch()` complains with `"nu uh, lacks a header thingy i forgot"`.

So here's the ULTIMATE workaround in a **chaotic pseudoscript** (a mix of Python, JS, Lua, and maybe stuff I made up):

```py
from pm_Project import Stage
import cors

songlist = ["poop", "pee", "pooppoop", "peepee"]
req = fetch("https://github.com/KylomaskGamer/ikwuehiuwerhiw")
cors_required = str(req.error).includes("NetworkError")

for i, v in songlist:
    if cors_required:
        Stage.add_sound(src=cors.proxy("https://github.com/KylomaskGamer/ikwuehiuwerhiw/" + v))
    else:
        Stage.add_sound(src="https://github.com/KylomaskGamer/ikwuehiuwerhiw/" + v)
```

The CORS extension comes from PenguinMod's [extension library](https://extensions.penguinmod.com), specifically:

[`https://extensions.penguinmod.com/extensions/NamelessCat/corsproxy.js`](https://extensions.penguinmod.com/extensions/NamelessCat/corsproxy.js)

This was reformatted by ChatGPT.

For Firefox users, if you run into this issue, here's the extension I use:

https://addons.mozilla.org/en-US/firefox/addon/cors-unblock/

**UPDATE:** The CORS proxy is ass and now returns 403 errors when it attempts to fetch something greater than A SINGLE FLIPPING MEGABYTE.

**UPDATE:** Luckily, I connected my domain to this. You can now fetch files from:

https://gh.kylomaskgamer.ca

## copyright concerns

Hear copyrighted music and want to report it?

Please don't immediately panic or assume you need to file a formal notice. I've organized the Issues tab so copyright concerns can be reported there.

> [!IMPORTANT]
> GitHub Issues are my preferred first point of contact, but you're still welcome to use formal legal procedures.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for the full procedure.

And Nintendo, if you're merciless enough, just do it.

---

## AI assistance

Parts of this document were reformatted and reworded with assistance from ChatGPT (OpenAI). The original ideas, policies, and content are mine.
