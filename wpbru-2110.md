# WPBRU 21/10/2014

## How to speed up your Wordpress Site (Gilbert)

You have to figure
- things you control,
- things you **may** control,
- things you have **no control** over.

Optimization is about figuring out :
- what is **relevant** to you
- what **matters** to you
- what you can **afford**

### Start by gathering data

- Either use YSlow (on Firefox)
- Or [PageSpeed](https://developers.google.com/speed/pagespeed/insights/)

### Start with the basics : Images

- **Images** (think about your home slider ;) ) : Use things like [ImgOptim](https://imageoptim.com) or [Shrink-o-matic](http://toki-woki.net/p/Shrink-O-Matic/), restrain the numbers of images, check that the images are in RVB and compressed (JPG, 70% quality, ...), ...

- Think about **what you want to achieve** on each page, and make logical decisions (is this Google Map really needed or can we use a simple image ?)

- Are your images **really responsives** ? Go over the basic max-width:100%, responsive images is using different images sizes depending on the device, thus allowing to load lighter images for mobile devices.

- Is the **image format** correctly used ? Do you need a PNG or a JPG or a GIF ? Avoid using PNG for everything, at it'll result in larger file sizes.

### Now Web Fonts

Think well before using WebFonts. If you use them, sets your **parameters correctly** to avoid loading the entire font (for example, avoid loading the italic if you don't need it). Some parameters even allows to load only some glyphs of a specified font.

### Now Social!

Sharing buttons come with a **heavy loading cost**, as they're loaded through heavy javascripts. There are ways to put sharing buttons [without using scripts](http://danielmiessler.com/blog/social-media-buttons-no-javascript/). If you want the share numbers, then you have to rely on some heavy and external javascripts. Think that you don't really need those numbers until you have a serious audience (or the numbers will be low and useless).

### Now it gets a bit tricky

- Reduce the http requests : have a look on the **external depedencies of the plugins** you use, check the plugins you use, minifie your javascripts and css, ...

- Assets on a separate domain (with no cookies)

- Inline style : good or bad. Generally you should avoid inline CSS, but things are changing recently, as some people spotted perceived performances with inline css

- Render blocking JS

- Heave JS with slow external response

- Ditch MySQL, ditch Apache