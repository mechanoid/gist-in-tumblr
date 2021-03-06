Embed Gists in Tumblr
=====================

Tumblr says you can't paste Github Gists into your blog.

Use this hack to do it anyway.


Credits
-------

This is mostly a hack-job of
[writeCapture](https://github.com/iamnoah/writeCapture), and
inspired by [this gist](https://gist.github.com/2506180).

gist-in-tumblr requires [jQuery](https://github.com/jquery/jquery).


Fast Installation
-----------------

Copy these scripts into the &lt;head&gt; of the blog:

```html
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
<script type="text/javascript" src="https://github.com/downloads/bobbydavid/gist-in-tumblr/gist-in-tumblr-full.v0.1.1.min.js"></script>
```

Note that you are linking directly to Github. If you prefer, you can download
your own copy and link to it on Tumblr.

To active a Gist, put it in a &lt;p&gt; tag with the class "gist" by itself:

```html
<p class="gist">https://gist.github.com/2553077</p>
```

Done!


More Detailed Installation
--------------------------

Copy these scripts into the &lt;head&gt; of the blog:

```html
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
<script type="text/javascript" src="https://github.com/downloads/bobbydavid/gist-in-tumblr/gist-in-tumblr-full.v0.1.1.min.js"></script>
```

For most Tumblr themes, this can be accomplished by clicking "Customize"
and then pasting the script tags your "Description" field.

To active a Gist, put it in a &lt;p&gt; tag with the class "gist" by itself.
For instance, you start with the Gist on its own paragraph in your blog:

```html
Here is my latest Gist:

https://gist.github.com/2553077

Text continues here...
```

Then modify the HTML source and add the class 'gist' to the paragraph tag:

```html
<p>Here is my latest Gist:</p>
<p class="gist">https://gist.github.com/2553077</p>
<p>Text continues here...</p>
```

The Nitty Gritty. And Misc.
---------------------------

Note that gist-in-tumblr currently expects gist URLs to take the form
`https://gist.github.com/[0-9]+(\?file=.+)?`. This means you should not put
your own username in the URL. In other words, don't do
`https://gist.github.com/bobbydavid/12345`.

If you want to link just a single file, do
`https://gist.github.com/12345?file=filename.txt`.

Download and Build
------------------

As part of the build process, you must install
[uglify-js](https://github.com/mishoo/UglifyJS):

    $ git clone git@github.com:bobbydavid/gist-in-tumblr.git
    $ cd gist-in-tumblr
    $ npm install uglify-js
    $ make

The files show up in the `out/` directory.


License
-------

Owing to writeCapture being licensed under GPL, this software is under the same.

