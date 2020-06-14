# Electronics Club-Coord Stuff

# Title: Camera Stack in Mobile phones:

## What I am going to discuss?
About the concept of smartphone camera working and what are the factors important for better quality images.

__Why do cameras have higher megapixels than screen resolutions?__


Consider a phone with fullHD display which has 12MP camera. Also consider it has a display resolution of 1920 x 1080 pixels. What 12Mp camera means the phone can be able to capture a maximum of 12MP shots. Take a photo each with 12MP and less than 12MP. Take a look at both of the phones. Well you may not notice considerable difference in the image quality when viewed in 100%.

 _Why this is so?_ Well, since our mobile has resolution of 1920 x 1080 pixels, it can display images of almost 2MP(1920 x 1080 = approx 2million).

_So more megapixels have nothing to do with the quality of images._


### Minimum megapixels for quality prints:__
| Max Print Size(in inch) | Maximum MP |    Resolution   |
|              ---        |     ---    |      ---        |
|        4 x 6″           |    2 MP    |   1600 x 1200   |
|        5 x 7″           |    3 MP    |   2048 x 1536   |
|        8 x 10″	      |    5 MP    |   2560 x 1920   |
|       11 x 14″	      |    6 MP    |   2816 x 2112   |
|       16 x 20″	      |    8 MP    |   3264 x 2468   |
|       16 x 24″	      |   12 MP    |   4200 × 2800   |



__Then what is the use of higher megapixels?__


This will be useful if we present in bigger screens like a projector or laptops which has a higher resolution without having to zoom.

__So, are higher MegaPixels waste?__


Not really. More megapixels will be able to zoom more in the images. Now let us again look at the two images taken. You will be able to see noticeable difference in the image quality when you zoom it over and see. The maximum amount of zoom acheives in both the images will be different. The one with higher MegaPixels is able to zoom more than the one with relatively low MegaPixels.

_So how to improve the quality of image. Here comes the sensor part._
## Digital Camera Sensor:
A digital camera uses an array of millions of tiny light cavities or "photosites" to record an image. When you press your camera's shutter button and the exposure begins, each of these is uncovered to collect photons and store those as an electrical signal. Once the exposure finishes, the camera closes each of these photosites, and then tries to assess how many photons fell into each cavity by measuring the strength of the electrical signal. However this will convert to only greyscale images, since these cavities are unable to distinguish how much they have of each color. In order to capture coloured images, a filter has to be placed over each cavity that permits only particular colors of light.The most common type of color filter array is called a "Bayer array," shown below.

![Bayer filter](https://cdn.hswstatic.com/gif/digital-camera-bayer.jpg)

From the image above we can see that the number of green pixels is equal to the sum of red and blue. This is because the human eye is more sensitive to green light than both red and blue light. Redundancy with green pixels produces an image which appears less noisy and has finer detail than could be accomplished if each color were treated equally.

### Bayer Demosaicing Algorithm:
Bayer "demosaicing" is the process of translating this Bayer array of primary colors into a final image which contains full color information at each pixel. To acheive this, each 2 x 2 array of red, green and blue can be averaged into a single full color activity._Thus the true color of a single pixel can be determined by averaging the values from the closest surrounding pixels(2 x 2 array)._


![Bayer Demosaicing](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.cambridgeincolour.com%2Fimages%2Ftutorials%2Fsensors_bayer2_new.png&f=1&nofb=1)

### Normalisation:
Normalisation reallocates RGB values to negate the green cast created in the image by having twice as much green information as red and blue.




![Normalisation](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.ytimg.com%2Fvi%2FELIJHe9mZVo%2Fmaxresdefault.jpg&f=1&nofb=1)




![Normalisation](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.ok.sc.e.titech.ac.jp%2Fres%2Ftoppicture%2FDM.png&f=1&nofb=1)


## Software part:
The image that we obtained above is a RAW image(just the output of every pixel one by one). Some software algorithms are used to compress the image by discarding all redundant pixels and keep only the useful ones. GPU will be used to render all this because that would be faster instead of using CPU.
_For example if we take a video with a camera for a longer time, it starts to heat too much. This is bcoz GPU is used heavily in the background to proceesing the instanatneous image to a readable format._

__After all these process, our image finally attains readable format.__

__Advantages of Large Sensor:__
- Better Depth of Field performance.
- Better low light performanace.
- Better dynamic range.
- Lower diffraction.

__Disadvantages of Large Sensor:__
- Expensive.
- Big and heavy.
- Expensive equipment.

Smartphones are not only made for camera. It has other jobs as well. It should be compact and light weight. Thats why it has a small sensor placed thereby occupying less space and weight.




# References:

1. https://newatlas.com/camera-sensor-size-guide/26684/
2. https://www.youtube.com/watch?v=eSp8XS9jp0U
3. [Camera Sensor-article](https://www.cambridgeincolour.com/tutorials/camera-sensors.htm)
3. [Raw file Demosaicing-youtube video](https://www.youtube.com/watch?v=9cPxEFpg3Eg&feature=youtu.be)
