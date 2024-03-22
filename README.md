# JavaScript Image to PDF Converter

This is a JavaScript script that utilizes the jsPDF library to convert images on a webpage into a PDF document and save it as "check.pdf".

## How it Works

The script loads the jsPDF library dynamically from the google drive and then creates a PDF document by looping through all the images on the webpage. It filters out images with invalid sources, and for each valid image, it follows these steps:

1. Create a canvas element and draw the image on the canvas.
2. Convert the canvas content to a base64-encoded image data URL.
3. Add the base64 image data to the PDF document using jsPDF's `addImage` method.
4. Add a new page to the PDF for the next image.

Once all the images have been processed, the PDF is saved as "check.pdf" using the `pdf.save()` method.

## How to Use

1. Include the following script tag in your HTML file to load the jsPDF library:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/1.5.3/jspdf.debug.js"></script>
