## Preview Images

In the last few sections, we have resized the images to balance the size and quality of the images, and to fit the painted area of the screen. In this section, we are going to create placeholder images for each file. You may have seen this in apps like Facebook, Pinterest or Google Image search where a placeholder image appears nearly immediately, and then the final image loads in later.

I have created SVG images to load in the background before the larger image can be downloaded. This is great on slower connections, as the screen is populated with color indicating an image is coming. I used[SQIP](https://github.com/technopagan/sqip)to create these thumbnails.

SVG files are vector graphics, and are stored as XML, so they can be added right to the HTML of your document. For example, here is the original image, and the SVG created from it:[![](https://camo.githubusercontent.com/ac915514e0f5839d1df598c514dd00a0d26dd80b/687474703a2f2f7265732e636c6f7564696e6172792e636f6d2f6861636b6368616c6c656e67652f696d6167652f75706c6f61642f775f323530302f76313532313036333231372f4d795661636174696f6e2f494d475f32303136303631395f3137333133363330362e6a7067)](https://camo.githubusercontent.com/ac915514e0f5839d1df598c514dd00a0d26dd80b/687474703a2f2f7265732e636c6f7564696e6172792e636f6d2f6861636b6368616c6c656e67652f696d6167652f75706c6f61642f775f323530302f76313532313036333231372f4d795661636174696f6e2f494d475f32303136303631395f3137333133363330362e6a7067)[![](https://camo.githubusercontent.com/4397252dd8f1be9896152135374fe4b8a599e978/68747470733a2f2f646f756773696c6c6172732e6769746875622e696f2f696d672f706c6974766963652e737667)](https://camo.githubusercontent.com/4397252dd8f1be9896152135374fe4b8a599e978/68747470733a2f2f646f756773696c6c6172732e6769746875622e696f2f696d672f706c6974766963652e737667)![](/assets/import.png)

Using this code, we use the SVG as a background image. Since the code is right ni the HTML, it loads immediately while the larger image continues to load:

```
<img width = "100%" src = "http://res.cloudinary.com/hackchallenge/image/upload/w_4000,q_auto,f_auto/v1521063217/MyVacation/IMG_20160619_173136306.jpg"
    style="background-size: cover; background-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAzNjE2IDY2NCI+PGZpbHRlciBpZD0iYiI+PGZlR2F1c3NpYW5CbHVyIHN0ZERldmlhdGlvbj0iMTIiIC8+PC9maWx0ZXI+PHBhdGggZmlsbD0iIzgyOTk3NiIgZD0iTTAgMGgzNjE2djY2M0gweiIvPjxnIGZpbHRlcj0idXJsKCNiKSIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNyA3KSBzY2FsZSgxNC4xMjUpIiBmaWxsLW9wYWNpdHk9Ii41Ij48ZWxsaXBzZSBmaWxsPSIjYzBkNWRkIiByeD0iMSIgcnk9IjEiIHRyYW5zZm9ybT0ibWF0cml4KC0yMC41Nzg1NSAtOTkuOTUxNSAyMC42NTg5NiAtNC4yNTMzOCAxMjUuMyAyOC4yKSIvPjxlbGxpcHNlIGZpbGw9IiMzZjUzMzAiIHJ4PSIxIiByeT0iMSIgdHJhbnNmb3JtPSJtYXRyaXgoMTMuMzM4MTggLTE1LjM2NTc5IDI3LjI0ODkzIDIzLjY1MzI2IDU2LjggMjEuNCkiLz48ZWxsaXBzZSBmaWxsPSIjNDg2MjE5IiByeD0iMSIgcnk9IjEiIHRyYW5zZm9ybT0icm90YXRlKC02NS42IDExMS4yIC0xNTQuMikgc2NhbGUoMTMuNzY5MTkgMzEuNzUwMDkpIi8+PGVsbGlwc2UgZmlsbD0iI2I2Y2ViNCIgY3g9IjE4NCIgY3k9IjQ1IiByeD0iNjUiIHJ5PSIyMCIvPjxwYXRoIGZpbGw9IiMyYTQzMmEiIGQ9Ik0xNjQgMS45bC0xNS4yIDQzLjMgMS0yMi4zIDU5LjgtMTMuNXoiLz48cGF0aCBmaWxsPSIjYjNjMTk0IiBkPSJNOC4xIDYybDY3LjMtNDItNTkuNSAxMS42TC0xMi4zIDYyeiIvPjxwYXRoIGZpbGw9IiM0ODRlM2IiIGQ9Ik0yNyA1aDYydjIySDI3eiIvPjxwYXRoIGZpbGw9IiNkNWQ0YTIiIGQ9Ik0yMDkgMjJsLTMyLTExLTMwIDMweiIvPjwvZz48L3N2Zz4=);"
    />
```

Here are the [SVG images](https://dougsillars.github.io/svglist.txt) with names for referencing an external file, or the code to use inside the html.

When considering inlining images into html, you should consider tings like cache life of the htm vs. the image.

