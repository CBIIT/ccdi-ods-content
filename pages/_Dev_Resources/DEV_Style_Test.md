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

---

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
/* Main container */
.event-carousel {
  position: relative;
  max-width: 900px;
  margin: 20px auto;
  overflow: hidden;
}

/* Hide all images by default */
.event-carousel img {
  width: 100%;
  display: none;
}

/* Show only the active image */
.event-carousel img.active {
  display: block;
}

/* Arrow buttons */
.carousel-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0,0,0,0.6);
  color: white;
  border: none;
  padding: 15px 20px;
  font-size: 24px;
  cursor: pointer;
  z-index: 10;
}
.carousel-btn:hover {
  background: rgba(0,0,0,0.8);
}
.prev-btn { left: 10px; }
.next-btn { right: 10px; }

/* Dot navigation */
.carousel-dots {
  text-align: center;
  padding: 15px 0;
}
.dot {
  height: 12px;
  width: 12px;
  margin: 0 5px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  cursor: pointer;
}
.dot.active {
  background-color: #333;
}
</style>

<!-- ============================================ -->
<!-- IMAGES: Add gallery images here -->
<!-- First image needs class="active" -->
<!-- ============================================ -->
<div class="event-carousel" id="eventGallery">
  <img class="active" 
       src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/latest-updates/Data_Code_01.png" 
       alt="Test image 1">
  <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/latest-updates/Data_Book_01.png" 
       alt="Test image 2">
  <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/latest-updates/Data_Science_01.png" 
       alt="Test image 3">
  <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/icons/cloud_upload_icon.png" 
       alt="Test image 4">
  <img src="https://raw.githubusercontent.com/CBIIT/ccdi-ods-content/main/pages/images/stock/data_magnifying_glass_01_900x300.png" 
       alt="Test image 5">

  <button class="carousel-btn prev-btn" 
          id="prevBtn">❮</button>
  <button class="carousel-btn next-btn" 
          id="nextBtn">❯</button>
</div>

<!-- Dots appear here automatically -->
<div class="carousel-dots" 
     id="dotsContainer"></div>

<!-- ============================================ -->
<!-- JAVASCRIPT: Makes gallery buttons work -->
<!-- ============================================ -->
<script>
(function() {
  let currentIndex = 0;
  const images = document.querySelectorAll(
    '#eventGallery img'
  );
  const dotsContainer = 
    document.getElementById('dotsContainer');
  const prevBtn = 
    document.getElementById('prevBtn');
  const nextBtn = 
    document.getElementById('nextBtn');
  
  // Create dots
  for (let i = 0; i < images.length; i++) {
    const dot = document.createElement('span');
    dot.className = 
      i === 0 ? 'dot active' : 'dot';
    dot.addEventListener('click', function() {
      showSlide(i);
    });
    dotsContainer.appendChild(dot);
  }
  
  // Show specific slide
  function showSlide(index) {
    const dots = 
      document.querySelectorAll('.dot');
    
    images[currentIndex]
      .classList.remove('active');
    dots[currentIndex]
      .classList.remove('active');
    
    currentIndex = index;
    
    images[currentIndex]
      .classList.add('active');
    dots[currentIndex]
      .classList.add('active');
  }
  
  // Move slides
  function moveSlide(direction) {
    let newIndex = currentIndex + direction;
    
    if (newIndex < 0) {
      newIndex = images.length - 1;
    }
    if (newIndex >= images.length) {
      newIndex = 0;
    }
    
    showSlide(newIndex);
  }
  
  // Attach button listeners
  prevBtn.addEventListener('click', function() {
    moveSlide(-1);
  });
  
  nextBtn.addEventListener('click', function() {
    moveSlide(1);
  });
  
})();
</script>

<!-- ============================================ -->
<!-- END: IMAGE GALLERY using HTML -->
<!-- ============================================ -->

---

## Lorem Ipsum

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse consectetur sem eget pharetra euismod. Integer malesuada scelerisque eros in pretium. Cras in nulla non metus ultrices pellentesque vitae a mauris. Phasellus molestie metus sed massa euismod laoreet. Pellentesque id tempus libero. Donec aliquet sagittis odio, sit amet scelerisque lacus lacinia non. Morbi eget dui hendrerit, mollis neque fringilla, tristique quam.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse consectetur sem eget pharetra euismod. Integer malesuada scelerisque eros in pretium. Cras in nulla non metus ultrices pellentesque vitae a mauris. Phasellus molestie metus sed massa euismod laoreet. Pellentesque id tempus libero. Donec aliquet sagittis odio, sit amet scelerisque lacus lacinia non. Morbi eget dui hendrerit, mollis neque fringilla, tristique quam.

&nbsp;  

---

**Updated:** August 7, 2025
