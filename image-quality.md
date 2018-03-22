## Image Quality

The images on this page are all JPG images.  JPG is a lossy image format, meaning that as you lower the image quality, pixels are removed from the image - lowering the visual quality of the image.  Google recommends that all images on the web use at least 85% quality to reduce file size.

You can adjust quality of images with any image processing tool. However, to simplify this exercise, we will use Cloudinary's tooling to change the quality on the fly. This is easily done by adjusting parameters in the url:

Here is the full quality image:

![](/assets/IMG_20160526_135242148_HDR %281%29.jpg)[http://res.cloudinary.com/hackchallenge/image/upload/w\_2500/v1521063280/MyVacation/IMG\_20160526\_135242148\_HDR.jpg](http://res.cloudinary.com/hackchallenge/image/upload/w_2500/v1521063280/MyVacation/IMG_20160526_135242148_HDR.jpg)

and here is the image at quality = 50:![](/assets/IMG_20160526_135242148_HDR.jpg)[http://res.cloudinary.com/hackchallenge/image/upload/w\_2500,q\_50/v1521063280/MyVacation/IMG\_20160526\_135242148\_HDR.jpg](http://res.cloudinary.com/hackchallenge/image/upload/w_2500,q_50/v1521063280/MyVacation/IMG_20160526_135242148_HDR.jpg)

If you look at the 2 URLs carefully, there is one small change made to the 2nd.  By simply adding the 'q\_50' parameter, Cloudinary generates an image at quality 50.  You can manually tweak the quality for each image by modifying this value.  However, manually tweaking the image quality for lots of images is not scalable.  Luckily, tools like SSIM allow algorithms to find the perfect balance between pixel savings and image quality.  Cloudinary uses a version of SSIM when the 'q\_auto' parameter is used.

![](/assets/IMG_20160526_135242148_HDR %282%29.jpg)[http://res.cloudinary.com/hackchallenge/image/upload/w\_2500,q\_auto/v1521063280/MyVacation/IMG\_20160526\_135242148\_HDR.jpg](https://www.gitbook.com/book/cloudinary/optimize-media-for-fast-page-loading/edit#)

