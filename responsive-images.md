## Responsive Images

The internet is not just viewed on a single browser. Optimizing the image for one user isn't enough. Let's make sure that the images we serve are optimized for every screen size.

We've seen how to each image individually for the width, but we can also do so programmatically. By enclosing the img tag in a picture tag, we can adjust the image that is delivered based on the viewport size:

```
<picture>
<img src="http://res.cloudinary.com/hackchallenge/image/upload/w_2500/v1521063217/MyVacation/IMG_20160619_173136306.jpg"
	srcset="http://res.cloudinary.com/hackchallenge/image/upload/w_500/v1521063217/MyVacation/IMG_20160619_173136306.jpg 500w,
		http://res.cloudinary.com/hackchallenge/image/upload/w_1000/v1521063217/MyVacation/IMG_20160619_173136306.jpg 1000w,
		http://res.cloudinary.com/hackchallenge/image/upload/w_1500/v1521063217/MyVacation/IMG_20160619_173136306.jpg 1500w"
			 
	sizes = "100vw"/>
</picture>
```

Test this out on the [picture](https://dougsillars.github.io/picture.html) page. Resize the screen, and the check the url of the image! \(If you have cloned this repo, and the images do not load, you'll see a security error in the URL bar. Allow unsafe scripts for this image to load\).

The srcset paramater lists 3 additional images for loading that are 500, 1000 and 1500 pixels wide \(you can verify this in the url, and also the parameter after the url\).

In this case, I have provided just 3 additional responsive images. For smaller screens, the smaller image will load - and this is great. But there was no science behind my selections - I just winged it. Jason Grigsby has suggested  [images that are 20KB apart](https://cloudfour.com/thinks/responsive-images-101-part-9-image-breakpoints/)to minimize pixel loss, and to maximize image caching. \(This is part 9 of a 10 part series, and I recommend the entire set of posts\). To calculate the dimensions of these different images, there are a number of different tools. In this exercise, we'll use [Responsive Breakpoints](http://www.responsivebreakpoints.com/), a service from Cloudinary.

[![](https://github.com/dougsillars/dougsillars.github.io/raw/master/img/ResponsiveBreakpoints.png)](https://github.com/dougsillars/dougsillars.github.io/blob/master/img/ResponsiveBreakpoints.png)

The site allows you to pick the pixel range of the enw images, the size jump \(in KB\) and the max number of images. Once you upload an image, it gives you the breakpoints:

[![](https://github.com/dougsillars/dougsillars.github.io/raw/master/img/responsiveAlps.png)](https://github.com/dougsillars/dougsillars.github.io/blob/master/img/responsiveAlps.png)[![](https://github.com/dougsillars/dougsillars.github.io/raw/master/img/breakpointsAlps.png)](https://github.com/dougsillars/dougsillars.github.io/blob/master/img/breakpointsAlps.png)

You also get the code you need to display the different image sizes. You can see the results on the &lt;a href="responsive.html&gt;responsive images page. Open this page, and change the size of your browser window. So that you can see that the images are changing, I made every other image load with sepia effects \(another modification possible with Cloudinary\).

[![](https://github.com/dougsillars/dougsillars.github.io/raw/master/img/responsive.gif)](https://github.com/dougsillars/dougsillars.github.io/blob/master/img/responsive.gif)

Aside: The "sizes" parameter is also really cool. In the example above, all images are sized to 100% of the view window. However, in some cases, you could do something like:

```
sizes ="(min-width: 500px) 32vw, 100vw"

```

In this case, if the screen is greater than 500 pixels wide, the image will take up just 1/3 of the screen, and below 500px, it will use 100% of the screen. This is a great way to build multiple layouts for different device screen sizes.

Also note that you have to specify the viewport in the HTML, and remove the width tags

```
<meta name="viewport" content="width=device-width" />
```

## 

  




