# [Free Online Gel Analyzer](https://svgpubs.github.io/FreeOnlineGelAnalyzer/)

# [![yt image](yticon_35x25.png) Quick-Start Tutorial](https://www.youtube.com/watch?v=8xcbzyapMgU&t=2s)

### This Free Online Gel Analyzer App offers scientists a quick way to analyze SDSPAGE, Agarose and Western gels.

## Easily measure:

- ## band area
- ## intensity
- ## molecular weight.

### Create a custom figure to save in your lab notebook. Label lanes, name bands, save sequence information, and more.

# General Advice

The program works best on a computer with updated [Chrome](https://www.google.com/chrome/) or [Firefox](https://www.mozilla.org/en-US/firefox/new/) web browser.

Although not required, it is recommended to follow these steps in order:

1. Create Lanes
2. Draw Bands
3. Add Band Data
4. Download

# Frequently Asked Questions

# App Security

## Is it safe to upload my scientific images onto the Free Online Gel Analyzer App?

**Yes.** None of the data are ever sent across the internet or stored (the data being, for example, the uploaded file, the text input, and all intermedieate and resulting calculations of your gel). If the data never enters the internet, it cannot be accessed by any third party, including me. Your browser only uses the internet to initially load the program. Once initially loaded, all processing occurs on your computer, inside your individual browser.

## Does it collect or sell my personal information?

**No.** This app uses Google Analytics to track how many times and from what regions of the world it is visited. I followed [How To Make Google Analytics GDPR-Compliant (No Consent Required)](https://rankmath.com/blog/google-analytics-gdpr/) to disable cookies and personally identifiable information collection. Although no lawyers were involved, this was done with the intent of achieving [General Data Protection Regulation (GDPR) Compliance](https://gdpr.eu/).

## Still concerned about data security?

If you or your laboratory are still not comfortable uploading scientific results onto an online application, no worries. Soon an liscened desktop version (with additional features!) will be available. The link to this desktop program will be added here likely before September 2021 for Mac, Windows and Linux operating systems.

# Technical

## What is the best image resolution?

The user can upload high or low resolution images. However, to ensure performance, large images are compressed so that the longest dimension of the cropped image (width or height) is a maximum of 800 pixels.

## How is band area calculated?

The band area is the total number of pixels inside the band. Image resolution will affect the reported area.

## How is band intensity calculated?

The band intensity is the sum of inverted pixel values. Non-inverted grey-scale pixel values range from 0 (black) to 255 (white). In order for darker bands to report larger intensities, each pixel is mathematically inverted by subtracting the pixel value from 255, and then they are all added together. Image resolution, gel staining method, and image lighting will affect the reported intensity.

## What calculation is used to convert colored pixels into grey-scale pixels?

Colored pixels contain red, blue and green channels. Each color channel has a value between 0 and 255 (none to highest possible color value).

`Greyscale `=` 0.16`x`(Red-Channel) `+` 0.34`x`(Green-Channel) `+` 0.5`x`(Blue-Channel`

Then, each pixel's color channel value is replaced with the calculated Greyscale value.

Example: [100,10,40] `==>>` [39, 39, 39]

## How is the molecular weight best-fit line calculated?

I followed these [BioRad instructions](https://www.bio-rad.com/webroot/web/pdf/lsr/literature/Bulletin_6210.pdf).

To used the [linear least squares](https://en.wikipedia.org/wiki/Linear_least_squares) method to generate the molecular weight `y=mx+b` calculation.

I assume the gel is cropped so that the top is where the molecules enter the separation layer of the gel and the bottom is the dyefront. However, don't stress out trying to achieve 100% accuracy: small changes in gel image cropping does not significantly alter molecular weight estimates.

## How is percent intensity calculated for each pixel in the pixel hover tool?

`percent intensity = (255 `-`pixel-value)`x`(1/255)`x` 100`

where pixel-value is the greyscale value.

## Can I compare band areas and intensities between two different gels?

By default, no. Because the images may have different resolutions, staining intensity, and lighting conditions, you cannot assume band areas and intensities from different gels are comparable.

However, if you want to compare two different gel images, you can with careful controls. In an ideal senario, if both images contain gels that have the same dimension IN PIXELS, were run under identical conditions (including staining and washing steps) and were imaged with the same camera with the same lighting, then the areas and intensities measured between two different images will be comparable.

However, even without these strict experimental controls in place, there are several things you can do to make inter-gel comparisons. First, you can use the manual Draw A Band tool to create a control or background band that you can use to measure the image background. Secondly, you can add identical samples to both gels (for example, an identical ladder) and use the differences between those bands in the two images to scale relationships.

# Troubleshooting

## It is slow or stalling.

Try updating your internet browser to a new version of either [Chrome](https://www.google.com/chrome/) or [Firefox](https://www.mozilla.org/en-US/firefox/new/). This app relies on recent advancements that not all browsers support yet. Do not use Safari or Internet Exporer for now.

## What is that number following my cursor in the gel image?

You are likely seeing the hover value indicating pixel intensity. At the bottom right of your gel image, there are three buttons. Deselect them to make the numbers dissappear.

## How do I report issues/bugs?

If you have watched the [Tutorial](https://www.youtube.com/watch?v=8xcbzyapMgU&t=2s) AND are using decent computer AND you are using a recent version of either Chrome or Firefox, but are still having issues, please report it here. You must share your operating system (Mac, Windows or Linux), operating system version, browser and browser version number, and then what leads to the issue. The better you describe the way for me to reproduce the error you are getting, the better the chances that I can fix it quickly! I won't respond to issues that lack information.
