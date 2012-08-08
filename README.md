gifblender
==========

*gifblender* blends the frames of animated gifs and other image sequences.


Usage
-----

    Usage: gifblender [options] <img.gif>|<img1> <img2> ...

    Options:
      -h, --help               show this help message and exit
      -o, --outdir <arg>       output directory
      -s, --steps <arg>        number of steps
      -t, --transition <arg>   transition timing
      -b, --blend-last         blend first and last frames

    Available transition timings:
      linear (default)
      ease
      ease-in
      ease-out
      ease-in-out


```bash

# for looping gifs, the -b|--blend-last option lets you blend the last
# and first frames (this creates a seemlessly looping gif)
$ gifblender -o /tmp/frames/ -s 20 -t ease -b source.gif

# you can also blend arbitrary image sequences if they have the same
# dimensions
$ gifblender -o /tmp/frames/ -s 20 img1.jpg img2.jpg img3.jpg *.jpg
```

[Example output][3]

**Note:** *gifblender* only creates intermediary frames - it does not
create gifs. Use a program like [gifsicle][2] to animate
*gifblender*'s results.

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

*gifblender* is released under the terms of the New BSD License.


[1]: http://www.imagemagick.org/script/index.php
[2]: http://www.lcdf.org/gifsicle/
[3]: https://raw.github.com/gist/3295600/3ff0e9ec916c1275841d96cc3f52fe9de43a6af4/gistfile1.txt
[source]: https://raw.github.com/gvalkov/screenshots/master/gifblender/demo.gif
[ease]: https://raw.github.com/gvalkov/screenshots/master/gifblender/ease.gif
[ease-in]: https://raw.github.com/gvalkov/screenshots/master/gifblender/ease-in.gif
[ease-out]: https://raw.github.com/gvalkov/screenshots/master/gifblender/ease-out.gif
[ease-in-out]: https://raw.github.com/gvalkov/screenshots/master/gifblender/ease-in-out.gif
[linear]: https://raw.github.com/gvalkov/screenshots/master/gifblender/linear.gif
