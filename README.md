<h1 align="center">
    Lanx
</h1>

<p align="center">
     <i>A simple, zero-config static file server for Arturo</i>
     <br><br>
     <img src="https://img.shields.io/github/license/drkameleon/lanx?style=for-the-badge">
    <a href="https://github.com/arturo-lang/arturo" style="text-decoration: none; display: inline-block;"><img src="https://img.shields.io/badge/language-Arturo-6A156B.svg?style=for-the-badge" alt="Language"/></a>
</p>


---

<!--ts-->

* [What does this package do?](#what-does-this-package-do)
* [How do I use it?](#how-do-i-use-it)
   * [As a CLI tool](#as-a-cli-tool)
   * [As a library](#as-a-library)
* [Function Reference](#function-reference)
* [Contributing](#contributing)
* [License](#license)

<!--te-->

---

### What does this package do?

Lanx is a minimal static file server for Arturo. Point it at a folder and it will serve its contents over HTTP - with automatic MIME type detection, directory listings, and `index.html` support; no configuration needed! 😉

### How do I use it?

#### As a CLI tool

Just run it from any directory:
```red
lanx              ; serves the current directory
lanx ./public     ; serves a specific folder
```

#### As a library

Embed it in your own Arturo project:
```red
import'lanx!

server: to :lanx []!
server\root: "./public"
server\port: 8080
server\start
```

> [!TIP]
> Drop an `index.html` in any folder to have it served automatically instead of the directory listing.

### Function reference

#### `:lanx` type

| Field | Default | Description |
|---|---|---|
| `root` | current directory | path to serve |
| `port` | `18966` | port to listen on |

#### `start`

Start the server using the configured `root` and `port`.
```red
server: to :lanx []!
server\start
```

### Contributing

All contributions/ideas/suggestions are 100% welcome! 

Noticed something? Open an issue.  
Want to add/fix something? Just make a PR and I'll be more than glad to merge it! 🚀

<hr/>

### License

MIT License

Copyright (c) 2026 Yanis Zafirópulos

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
