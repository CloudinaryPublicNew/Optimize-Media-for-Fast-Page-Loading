## Pixels

AS you have been following along, you've probably noticed the 'w\_2500' parameter. This parameter tells Cloudinary to resize the image to 2500 pixels wide. Now, even on a laptop, an image that only uses 25-30% of the screen does not need to be 2500 pixels wide.

When a device has a large image, it will resize the image, shedding unnecessary pixels from the image before it appears on the screen. In some ways, this is double taxation - it costs time to download the large image, and then additional time for the device to resize the file. \(This is further compounded on low end mobile devices, where the low powered processor takes longer, and draws more power to resize the image\)

To resize these images, you can adjust the width parameter in the url. Open the image in a new tab, and adjust the number - and you'll see that a smaller \(or larger\) image is delivered to the browser:

[http://res.cloudinary.com/hackchallenge/image/upload/w\_2500,q\_auto,f\_auto/v1521063280/MyVacation/IMG\_20160526\_135242148\_HDR.jpg](http://res.cloudinary.com/hackchallenge/image/upload/w_2500,q_auto,f_auto/v1521063280/MyVacation/IMG_20160526_135242148_HDR.jpg)

