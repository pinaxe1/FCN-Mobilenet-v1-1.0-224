# fcn-mobilenet
It is a copy of https://github.com/vietdoan/fcn-mobilenet
mobilenet_v1_1.0_224 <BR>
MODEL_URL = 'http://download.tensorflow.org/models/mobilenet_v1_1.0_224_2017_06_14.tar.gz'<BR>

The project implments Fully Convolutional Network based on MobileNet v1  image_squeeze 1.0 image_size 224

To run the program you should have about a hundred annotated images stored in<BR>
Data_zoo/camvid/train  ../trainannot<BR>
Data_zoo/camvid/test   ../testannot<BR>
Data_zoo/camvid/val    ../valannot<BR>
Annotated image means a pair of images. An image itself and it's annotation.
It makes a pair of PNG images with the same names. 
Images would sit in "train/" folder their annotations in "trainannot/" folder. Same for "test/" and "val/" folders.
Label image is an image painted color #000000 for a background, color #000001 for objects of class 1, color #000002 for class 2 and so on up to NUM_OF_CLASSES = 12
Labeling could be conveniently done with Pixel Annotation tool see https://github.com/abreheret/PixelAnnotationTool<BR>

The programm has 3 modes "train", "test", "visualise"<BR>

To train the network. In Fcn.py set variable mode = "train".<BR>
It took about 6 hours on a GTX1080 to converge the network on my dataset of 100 images.  
  
To validate the network. Set "mode" to "validate"  <BR>
It'll print out average losses for each class.
  
To see how the network will label images set "mode" to "visualize"  <BR>
It'll take a few images from Validation set and then create a few result images in a "logs/" folder.
