# Lazy Loading



"The fastest code is the code that never runs" "the fastest request is the request never made"

When it comes to loading a webpage - the fewer the number of requests, the faster the page will load. So, how can we reduce the number of requests. There are a number of libraries that help you lazy load images.

The idea behind lazy loading is to only load the images that appear on the screen \(or are about to appear on the screen as the user scrolls\). If the user never scrolls to the bottom 1/2 of your webpage - those images will never load - reducing bytes, and the amount of time it takes the page to load.

In this example, I have used[lazysizes](https://github.com/aFarkas/lazysizes)to help me load my images. Lazyizes allows you to use responsive images, and also a preview image with lazy loading your images.

The result is the preview image loads for all images, but only the images in the viewport are downloaded - and they use the responsive image logic to select the correct image.

This is essentially the 'Holy Grail' of image optimization - we can only load the images required, have a preview image while the image loads, and use responsive delivery to ensure that the image is properly sized and formatted for he device. You can see how this works with 2 test pages: [lazyload with external svg references](https://dougsillars.github.io/lazy/index_lazy.html) and [lazyload with inline svg references](https://dougsillars.github.io/lazy/index_lazy_inline_.html).

# 



