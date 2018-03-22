#Tools
We would like to take these images, and modify them to get the page to load faster. To benchmark these tests, we'll use 2 tools:

<ul>
<li>[Website Speed Test](https://webspeedtest.cloudinary.com/) to test the performance of the images on the page.</li>
<li>[WebPageTest](https://webpagetest.org/) to measure the load time of the page.</li>
<ul>
> NOTE: that these two tools are synced, if you run a WebPageTest run, you can access the Website Speed Test results from the "Image Analysis" link at the top of the page.

Here are links to the initial results (unoptimized):

[WebsiteSpeedTest](https://webspeedtest.cloudinary.com/results/180315_AS_9dc54a8880a3415473c2f1fd03ea3895) The initial page scores "mediocre" in WbSite Speed Test, but we can see that the page has 10MB of images, and Cloudinary can reduce the files to 732 KB - a data savings of 92%! 

![](https://camo.githubusercontent.com/6f8f9a3f37f886aee41c47aef22e6ba34709d336/68747470733a2f2f646f756773696c6c6172732e6769746875622e696f2f6f726967696e616c5f73636f72652e706e67)