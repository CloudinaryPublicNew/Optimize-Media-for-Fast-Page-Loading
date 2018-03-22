#Tools
To speed up this [webpage](https://dougsillars.github.io/), we need to load everything faster.  Simply put, these images need to get smaller, so they download faster. To benchmark these tests, we'll use 2 tools:

1. <a href="https://webspeedtest.cloudinary.com" target = "_blank">Website Speed Test</a> to test the performance of the images on the page.
2. <a href="https://webpagetest.org" target="_blank">WebPageTest</a> to measure the load time of the page.

>Note: These two tools are synced, if you run a WebPageTest run, you can access the Website Speed Test results from the "Image Analysis" link at the top of the page.


Here are links to the initial results (unoptimized):
<a href="https://webspeedtest.cloudinary.com/results/180315_AS_9dc54a8880a3415473c2f1fd03ea3895" target="_blank">WebsiteSpeedTest</a> 
The initial page scores "mediocre" in WebSite Speed Test, but we can see that the page has 10MB of images, and Cloudinary can reduce the files to 732 KB - a data savings of 92%!
<img width = "100%" src="https://dougsillars.github.io/img/original_score.png"/>

<a href = "https://webpagetest.org/result/180315_0S_8d8676cea9714fd1bf6820d70cb139c6/" target = "_blank">WebPageTest</a>
Shows that the load time was 19.6s, and the SpeedIndex (a measurement of speed to paint the screen was 7258.
<img width = "100%" src="https://dougsillars.github.io/img/Webpagetest_screenshot.png"/>


So, what steps can we take to make this page faster?  As I discussed in my Lunch and Learn, there are several steps we can take. So, fork this page and begin Optimizing!

>If you need to host this page, you can use GitHub Pages.  
1. Visit pages.github.com
2. set up a repository named <github username>.github.io
3. once this is created, you are given the option to import from another repository.  Enter:"https://github.com/dougsillars/dougsillars.github.io", and you've essentially cloned this repository into your own GitHub Pages repository.
