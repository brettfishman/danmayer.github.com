---
layout: posttail
authors: ["Dan Mayer"]
title: "Emacs swap buffer window method"
category:
tags: []
---
{% include JB/setup %}

So I really like split screen in emacs. I am in that mode pretty much all the time. One thing that annoyed me was opening a file on the side of the screen I wanted. Sometimes I want code left, tests right others it is project A left project B right or often server code left, client code right. Anyways I often opened a file on the wrong side of the screen and wanted to move the buffer. Previously I always closed the buffer, then switched to the other emacs window (C-x o) then reopened the file. This annoyed me to know end, so I finally went looking for a solution. I found something that was close, but not what I wanted, which [swaps two buffers positions left and right](http://stackoverflow.com/questions/1774832/how-to-swap-the-buffers-in-2-windows-emacs), so I started with that code and modified it to do just what I want. I then bound the function to "C-x /" which wasn't in use and I can now swap buffer windows with ease. Also, kind of fun to do a bit of lisp/emacs hacking and breaking out of my Ruby world a bit.

        <script src="https://gist.github.com/1009137.js?file=swap_buffer_window.el"> </script>

If you notice I have it also close the current tab for the buffer and move the cursor context to the new buffer on the other side of the screen. Most people hate and don't use tabs in emacs so that one tab closing could be commented out. I love tabs because I am a very spacial person and the tabs let me keep the physical location of the buffers in my head. This was written to run in Aquamacs, but will work equally well in standard emacs. Just drop it in your .emacs file or emacs config directory.     Code can be found at this gist, [Emacs swap buffer window](https://gist.github.com/1009137)