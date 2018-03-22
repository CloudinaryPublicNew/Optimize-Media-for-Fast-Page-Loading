## Format



There are formats that have better compression algorithms than others. JPEG and PNG are older formats, and formats like Webp or JPEG2000 use newer compression algorithms that save even more data without any loss of quality. Since WebSite Speed Test and WebPageTest use desktop Chrome by default, we try to use Webp on our site during testing.

Rather than creating new images in each format and comparing them, we can again leverage the Cloudinary toolchain, and add the "f\_auto" parameter to the url - and Cloudinary will pick the best format \(based on compatibility, size and quality\) to deliver to the device.

[![](https://camo.githubusercontent.com/b4eb45e157bdfb1f9c50713ac1a69810d350f10f/687474703a2f2f7265732e636c6f7564696e6172792e636f6d2f6861636b6368616c6c656e67652f696d6167652f75706c6f61642f775f323530302c715f6175746f2c665f6175746f2f76313532313036333238302f4d795661636174696f6e2f494d475f32303136303532365f3133353234323134385f4844522e6a7067)](https://camo.githubusercontent.com/b4eb45e157bdfb1f9c50713ac1a69810d350f10f/687474703a2f2f7265732e636c6f7564696e6172792e636f6d2f6861636b6368616c6c656e67652f696d6167652f75706c6f61642f775f323530302c715f6175746f2c665f6175746f2f76313532313036333238302f4d795661636174696f6e2f494d475f32303136303532365f3133353234323134385f4844522e6a7067)

[http://res.cloudinary.com/hackchallenge/image/upload/w\_2500,q\_auto,f\_auto/v1521063280/MyVacation/IMG\_20160526\_135242148\_HDR.jpg](http://res.cloudinary.com/hackchallenge/image/upload/w_2500,q_auto,f_auto/v1521063280/MyVacation/IMG_20160526_135242148_HDR.jpg)

