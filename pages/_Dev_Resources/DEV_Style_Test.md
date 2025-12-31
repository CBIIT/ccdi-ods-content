---
title: DEV Style Test
author: ZD
date: 2025-06-04
---

# Header 1: Style Test Page

## Header 2

### Header 3

#### Header 4

##### Header 5

###### Header 6

## Banner Image

![Stylized image of colorful DNA molecules on a blue background](https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/stock/dna_art_01_800x335.jpg)

## Style Examples

**Bold** | *Italics* | ***Bold Italics***  

>**Bolded block header**  
>Basic text. **Bold**, *Italics*, ***Bold Italics***

- List Level 1
  - List Level 2
    - List Level 3

&#8505; Info | &#128204; Pushpin | &#128161; Lightbulb

### Standard Table

| Basic Header | **Bold Header** | *Italic Header* | ***Bold Italics Header. This is an example of a header that contains many characters, which will require the header to use multiple lines for display because of text wrapping to accommodate a necessarily verbose table column header that includes a self-referential run-on sentence.*** |
| --- | --- | --- | --- |
| Forced<br>Multi-<br>Line<br>Content | 999 | Empty below | &alpha; &beta; &delta; &gamma; &mu; |
| ABC | 00001 | | Many character word wrap: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse consectetur sem eget pharetra euismod. Integer malesuada scelerisque eros in pretium. Cras in nulla non metus ultrices pellentesque vitae a mauris. Phasellus molestie metus sed massa euismod laoreet. |

### Headerless Table

| | |
| --- | --- |
| ![Data cloud icon](https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/icons/cloud_upload_icon.png) | [External link - cancer.gov](https://cancer.gov) |
| ![Folder icon](https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/icons/folder_icon.png) | [Internal link - This page](/post/_Dev_Resources/DEV_Style_Test) |

## Links

[External link - cancer.gov](https://cancer.gov)  
[Internal link - This page](/post/_Dev_Resources/DEV_Style_Test)  
[Internal link - Nested page](/post/_Dev_Resources/test_nested/test-nested-page)  
[Internal anchor link - This page](#lorem-ipsum)  
[Internal anchor link - Different page](/post/About/About-ODS#who-we-are)  
[PDF link - New Tab Browser View](https://cbiit.github.io/ccdi-ods-content/pages/documents/test/DSHub_test_file.pdf)  
[DOCX link - Direct Download](https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/documents/test/DSHub_test_file.docx)  

## HTML Testing

### Embedded Video

<iframe
  height="458"
  width="845"
  src="https://nci.rev.vbrick.com/embed?id=a938aa7e-3d6e-4dfa-94b5-18ceae3c179a"
  frameborder="0"
  allowfullscreen
  title="Office of Data Sharing, You, and the Data Sharing Lifecycle">
</iframe>

### Style Tags

<style>
.test-gallery { border: 2px solid red; padding: 20px; }
</style>
<div class="test-gallery">
  Test using style tags. This should have a red border if tags not stripped.
</div>

### Image Gallery

<!-- ============================================ -->
<!-- START: IMAGE GALLERY using HTML -->
<!-- ============================================ -->

<style>
/* Hide radio buttons */
.carousel-radio {
  display: none;
}

/* Carousel container */
.css-carousel {
  position: relative;
  max-width: 900px;
  margin: 16px auto 0px auto;
  overflow: hidden;
}

/* Image container - maintain aspect ratio */
.carousel-images {
  position: relative;
  width: 100%;
  min-height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Hide ALL images by default */
.carousel-images img {
  max-width: 100%;
  max-height: 300px;
  width: auto;
  height: auto;
  position: absolute;
  opacity: 0;
  object-fit: contain;
  transition: opacity 0.5s;
}

/* Show ONLY the selected image */
#slide1:checked ~ .carousel-images img:nth-of-type(1),
#slide2:checked ~ .carousel-images img:nth-of-type(2),
#slide3:checked ~ .carousel-images img:nth-of-type(3),
#slide4:checked ~ .carousel-images img:nth-of-type(4),
#slide5:checked ~ .carousel-images img:nth-of-type(5),
#slide6:checked ~ .carousel-images img:nth-of-type(6) {
  opacity: 1;
  position: relative;
}

/* Navigation labels */
.carousel-nav {
  text-align: center;
  margin-top: 12px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 12px;
  padding: 0 8px;
}

.carousel-nav label {
  display: inline-block;
  padding: 8px 16px;
  margin: 0;
  background: #333;
  color: white;
  cursor: pointer;
  border-radius: 4px;
  font-size: 16px;
}

.carousel-nav label:hover {
  background: #555;
}

</style>

<div class="css-carousel">
  <input type="radio"
         name="carousel"
         id="slide1"
         class="carousel-radio"
         checked>
  <input type="radio"
         name="carousel"
         id="slide2"
         class="carousel-radio">
  <input type="radio"
         name="carousel"
         id="slide3"
         class="carousel-radio">
  <input type="radio"
         name="carousel"
         id="slide4"
         class="carousel-radio">
  <input type="radio"
         name="carousel"
         id="slide5"
         class="carousel-radio">
  <input type="radio"
         name="carousel"
         id="slide6"
         class="carousel-radio">
  
  <div class="carousel-images">
    <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/dev/pages/images/stock/conference_crowd_01_900x300.png"
         alt="Image 1">
    <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/latest-updates/Data_Code_01.png"
         alt="Image 2">
    <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/latest-updates/Data_Book_01.png"
         alt="Image 3">
    <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/latest-updates/Data_Science_01.png"
         alt="Image 4">
    <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/icons/cloud_upload_icon.png"
         alt="Image 5">
    <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/stock/data_magnifying_glass_01_900x300.png"
         alt="Test: Image Name 6">
  </div>
  
  <div class="carousel-nav">
    <label for="slide1">1</label>
    <label for="slide2">2</label>
    <label for="slide3">3</label>
    <label for="slide4">4</label>
    <label for="slide5">5</label>
    <label for="slide6">test</label>
  </div>
</div>

<!-- ============================================ -->
<!-- END: IMAGE GALLERY using HTML -->
<!-- ============================================ -->

## Lorem Ipsum

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse consectetur sem eget pharetra euismod. Integer malesuada scelerisque eros in pretium. Cras in nulla non metus ultrices pellentesque vitae a mauris. Phasellus molestie metus sed massa euismod laoreet. Pellentesque id tempus libero. Donec aliquet sagittis odio, sit amet scelerisque lacus lacinia non. Morbi eget dui hendrerit, mollis neque fringilla, tristique quam.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse consectetur sem eget pharetra euismod. Integer malesuada scelerisque eros in pretium. Cras in nulla non metus ultrices pellentesque vitae a mauris. Phasellus molestie metus sed massa euismod laoreet. Pellentesque id tempus libero. Donec aliquet sagittis odio, sit amet scelerisque lacus lacinia non. Morbi eget dui hendrerit, mollis neque fringilla, tristique quam.

&nbsp;  

---

**Updated:** August 7, 2025
