---
layout: post
title: Hello World
author: caspervonb
redirect_from: /blog/2017/03/21/hello-world
---

This is Web Reload, a spiritual successor and drop-in replacement for
[Live Reload](https://livereload.com){:target="_blank"}.

<!---->

Now for those who are not familiar with Live Reload, it is a browser script
that talks to a file monitor running on a remote server or your local machine
via web sockets, reloading the files that change, as: they change.

So, the obvious question now then is, wh:y does Web Reload exist if Live Reload
already does this? Isn't Live Reload fine the way it is? Well perhaps it is
but it has issues on the bug tracker that has been open for years at this point
with no reply from the author, the last commit was in 2015.

Web Reload fixes a bunch of these issues, requires less permissions, adds
support for `.svg`, `.webp`, `.bmp`, `.ico`, image formats, `<link>`,
`<picture>`, `<track>`, `<video>`, `<audio>` and `<source>` tags, it also
considers `srcset` attributes in addition to `src` and `href` when searching
the document for modified resources.

Aditionally it also has a fallback to a polling mode when no socket server is
available, but will connect to reload compatible servers on port *35729* like
Live Reload does which is more effecient than hammering the server with *HEAD*
requests.

Release versions of the web extensions and universal script will be made
available soon, until then the [source code is available on
GitHub](https://github.com/webreload/webreload), feel free to browse, submit an
issue or just star the repository.
