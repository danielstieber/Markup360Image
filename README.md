# Markup360Image
Module for ProcessWire that let you render 360° images via the WebVR engine a-frame.
Learn more about a-frame on the [offical website](https://aframe.io/).
I have only tested it with PHP7.x and Processwire 3.x.

## How To Install
1. Download the [zip file](https://github.com/danielstieber/Markup360Image/archive/master.zip) at Github or clone directly the repo into your `site/modules`
2. If you downloaded the `zip file`, extract it in your `sites/modules` directory.
3. You might have to change the folders name to 'Markup360Image'.
4. Goto the modules admin page, click on refresh and install it.

## How to use
```PHP
$m360 = $modules->get("Markup360Image"); // load module

$m360->render('my360image.jpg'); // render 360° image 

$m360->render('my360image.jpg', 'Hello World'); // render image and place text in the virtual room

$m360->render('my360image.jpg', 'Hello World', 'roboto'); // choose a font (use one of these or load your own: https://aframe.io/docs/0.8.0/components/text.html#stock-fonts)

$m360->render('my360image.jpg', 'Hello World', 'roboto',  80%, 600); // choose width & height of the scene. Default is width:100%, height:800px

$m360->render($page->image->url); // use with Processwire imagefield
```

## FAQ
### My text is not visible
You probably used a font, that is not working with a-frame. Learn more about it [here](https://aframe.io/docs/0.8.0/components/text.html#fonts)
