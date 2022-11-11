<script setup>
import ContentBlock from './ContentBlock.vue'
import ImageViewer from './ImageViewer.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
</script>

<template>
  <ContentBlock>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Overview</template>

    When viewing digital images on the internet, there are two common types of files you will come across--raster and vector. This guide will teach you the basics of both, some of the key
    differences, and when you should choose one over the other.

  </ContentBlock>

  <ContentBlock>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Raster Files</template>

    Raster images—also referred to as bitmap images—are made up of many tiny squares of color. These tiny squares are called pixels. In a raster image these pixels are placed on coordinates on a graph that when viewed toegether form a picture. 
    The more pixels an image has, the higher the quality of the image, but this comes at a cost of additional file size. A high quality photo from a modern digital camera could contain millions of pixels.
    While raster files can produce an image of incredible detail and quality, they do suffer from a major downside. Because the number of pixels in a raster image is a fixed amount encompassing a fixed size, if you need to enlarge a raster file your image can become very stretched and distorted. 
    This is when vector images come in handy.

    <div class="extensions">
      Some of the most common raster file formats include:
      <ul>
        <li><span class="accent-text">JPEG</span> - Joint Photographic Experts Group (web-friendly format that provides small file sizes at the cost of some fidelity)</li>
        <li><span class="accent-text">PNG</span> - Portable Network Graphics (popular web format that supports transparent backgrounds, 1:1 reproduction of images, and a wide color palette)</li>
        <li><span class="accent-text">BMP</span> - Bitmap Image File (an older, but still widly supported, format that supports compressed or uncompressed images)</li>
        <li><span class="accent-text">GIF</span> - Graphics Interchange Format (popular web format that supports multiple frames leading to basic animations)</li>
        <li><span class="accent-text">PSD</span> - Adobe Photoshop files (industry standard tool for editing raster graphics)</li>
      </ul>
    </div>
  </ContentBlock>

  <ContentBlock>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Vector Files</template>

    Vector images work very differently than raster ones. While raster images are made up of many, many tiny pixels, vector files create images using mathematical equations. Vector images are made up of a combination
    of different geometric shapes, like points, lines, and curves. By defining how all of these shapes connect and where they should be placed on a plane, you can form an image. It takes a ton of information to store
    the massive number of pixels and their configuration found in a raster file, but since a vector file only needs to save the equations for shapes, the file size is usually much smaller. Additionally, vector
    files can be enlarged without any loss of quality like you would find in a raster file, because the mathematical equations can be adapted perfectly to the new dimensions of your image.

    <div class="extensions">
      Some of the most common vector file formats include:
      <ul>
        <li><span class="accent-text">SVG</span> - Scalable Vector Graphics (web-friendly vector format)</li>
        <li><span class="accent-text">DXF</span> - Drawing Exchange Format (used by engineers and architects for blueprinting and designs)</li>
        <li><span class="accent-text">STL</span> - Standard Triangle Language (mainly for 3d modeling and 3d printing)</li>
        <li><span class="accent-text">AI</span> - Adobe Illustrator vector files (a tool for editing vector graphics)</li>
      </ul>
    </div>


  </ContentBlock>

  <ContentBlock>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Which Should You Choose?</template>

    Both formats have specific use cases, so choosing between the two is usually a straightforward decision. If your image is of mainly solid colors and shapes, and may need to be resized,
    you should be using vector images. If your file requires complex, detailed blends of colors and continous surfaces, such as images of real-life, you should be using raster. Below are
    some common examples of when you would use the two formats.
    
    <div class="extensions">
      Raster Uses
      <ul>
        <li><span class="accent-text">Photography</span> - Digital cameras typically save their photos as raster images. The pixel format of raster graphics allows for incredible detail and color that a vector file cannot match.</li>
        <li><span class="accent-text">Digital Image Editing</span> - Programs like Photoshop work with raster files. Raster files support per-pixel editing allowing for extreme customization and detail.</li>
        <li><span class="accent-text">Scanning</span> - Files scanned from a copier will be in raster format. A scanner will shine a light on an image and collect the reflection using mirrors and sensors in a process not all that different from the principles of a digital camera.</li>
      </ul>
    </div>

    <div class="extensions">
      Vector Uses
      <ul>
        <li><span class="accent-text">Logos</span> - Logos need to be resized often and are typically made up of simple geometric shapes. They are perfect for the vector format.</li>
        <li><span class="accent-text">Clothing Design</span> - Pixels are sometimes very difficult to reproduce on clothing, and the lack of resizing is problematic. Vectors are preferred here.</li>
        <li><span class="accent-text">2D/3D Animation</span> - At a very simplified level, graphics cards render images through the processing of vectors. Animation tools work with vectors.</li>
        <li><span class="accent-text">Architecture Design</span> - blueprints are made up of a series of geometric shapes, so the vector format is clearly the tool for this field. Computer design programs work in vectors.</li>
      </ul>
    </div>

  </ContentBlock>


  <ContentBlock>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>A Visual Representation</template>

    The first image is a <span class="accent-text">raster image</span>. Notice how detailed the photo is and how there are so many diverse lights, colors, surfaces, and blends. Watch as the photo grows; as it extends
    past the initial file size, the image will become more and more distorted to the point where you can see the individual pixels.

    <div class="space">
      The second image is a <span class="accent-text">vector image</span>. Notice how the photo is much less detailed--it is only simplistic shapes, but watch as it grows. The image will retain perfect quality
      as it sizes up well beyond the dimensions of the raster image.
    </div>

    <ImageViewer />
  </ContentBlock>
  
 
</template>

<style scoped>
  .extensions {
    margin-top: 20px;
    line-height: 2em;
  }

  .space {
    margin-top: 15px;
  }

  .accent-text {
    color: var(--color-heading);
  }
</style>
