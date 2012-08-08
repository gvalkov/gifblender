gifblender
==========

*gifblender* extracts and blends the frames of an animated gif.


Usage
-----

    Usage: gifblender [options] <img.gif>|<img1> <img2> ...

    Options:
      -h, --help               show this help message and exit
      -o, --outdir <arg>       output directory
      -s, --steps <arg>        number of steps
      -t, --transition <arg>   transition timing
      -b, --blend-last         blend first and last frame

    Available transition timings:
      linear (default)
      ease
      ease-in
      ease-out
      ease-in-out


Transition
----------

The `-t|--transition` option specifies the rate at which the
transition between two frames is carried out:

![ease][ease]
![ease-in][ease-in]
![ease-out][ease-out]

![ease-in-out][ease-in-out]
![linear][linear]
![source][source]


Requirements
------------

*gifblender* requires the [ImageMagick][1] suite.

```bash
# Debian compatible OS
$ apt-get install imagemagick

# Redhat compatible OS
$ yum install ImageMagick

# Mac OS with macports
$ port install ImageMagick
```


License
-------

*gifblender* is released under the terms of the `New BSD License`_.


[1]: http://www.imagemagick.org/script/index.php
[source]: https://raw.github.com/gvalkov/screenshots/master/gifblender/demo.gif
[ease]: https://raw.github.com/gvalkov/screenshots/master/gifblender/ease.gif
[ease-in]: https://raw.github.com/gvalkov/screenshots/master/gifblender/ease-in.gif
[ease-out]: https://raw.github.com/gvalkov/screenshots/master/gifblender/ease-out.gif
[ease-in-out]: https://raw.github.com/gvalkov/screenshots/master/gifblender/ease-in-out.gif
[linear]: https://raw.github.com/gvalkov/screenshots/master/gifblender/linear.gif
