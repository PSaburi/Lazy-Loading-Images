Lazy Loading Images - The complete guide

What is Lazy loading images?
Lazy loading images is a technique which helps in improving the perceived page load time and user experience by loading images at a later point in time, 
when they are actually needed on a page, rather than loading them upfront.

Why go for lazy loading images?
- Web Performance Improvement
- Cost Reduction (Image Delivery Cost)

Which Images can be Lazy Loaded?
- Images that are not visible to the user up front.

How does lazy loading images work?
- As user scrolls down, image placeholder starts coming into viewport, loading of images are triggered when they become visisble.

Different Techniques for Lazy Loading Images
- Images on websites can be loaded in two ways
1. <img> tag
   Syntax: "<img src="" data-src="https://image-download.com/sample.jpg" />"
   Image loaded using the <img/> tag, the browser uses the 'src' attribute of the tag to trigger the image load.
   Put the image URL in an attribute other than 'src'. When the image enters the viewport pick that image URL and put it in the 'src' attribute.

   Ways to check when image enters the viewports:
	- Trigger Image load using Javascript i.e. Event listeners are used on Scroll, Resize, OrientationChange events in the browser.
	- Using Intersection Observer API to trigger image loads: Intersection Observer API is a relatively new API in browsers. It makes it simple to detect when an 
	element enters the viewport and take action when it does.

2. CSS Background Images
	Syntax: #bg-image.lazy{
		  background-image: none;
		  background-color: #F1F1FA;
		}
		#bg-image{
		  background-image: url("https://image-download.com/sample.jpg")
		}
	Background image is applied only when the element does not have a particular class. Otherwise, there is no background.
	Remove the class when the element enters the viewport.

Thus Lazy loading if implemented correctly will significantly improve the loading performance of your web pages, reduce page size and delivery costs by 
cutting down on unneccessary resources loaded upfront while keeping the necessary content intact on the page.
	



