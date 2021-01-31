# Object classification in remote sensing images with Machine Learning

## Steps for Data Pre-processing
• First, we downloaded the testing dataset which was for Sentinel 1 – EW satellite for the city of Stockholm, Sweden for the year of 2020 from the respective link which was given to us.
• Then we used QGIS software tool to render the downloaded satellite image.
• Since our Testing satellite picture had only one band which was Gray scale, we have raster the image to get different bands for our Testing Image. (The reason that why we Raster the images, is that first we tried to train our model with the black and white pictures but when we cropped the pictures since everything was in the same color our model did not performed well in the means of accuracy so, we created the raster image with RGB colors to differentiate between the categories)
• With QGIS software we have cropped the satellite image using VRT layer to 500 by 500 Pixels.
• Out of the images that we have created from VRT, we have selected the images which has more categorize (which are Sea, Forest, Urban) with the help of google satellite map on QGIS.
• Further we have reduced the pixels to 10 by 10 for the selected satellite images that has more categorize.
• In the next step we have classified each category image and placed them in their respective classes by comparing each of them in Google Satellite to check that they belong to which category.
• With the help

## Algorithm Used
• Initially we thought of creating our own dataset and label the data using LabelMe and use U-Net CNN algorithm but because of time constraint and upon discussion with you we have decided to do Sliding Window Technique with CNN.
• Since our dataset was Sentinel 1 -EW and it had the resolution of 10m+ so it was so small to detect objects like Ship, Car so, we couldn’t do object
3
detection. Instead, we had to do Semantic Segmentation to detect landmarks and classes like Forest, Sea, and Urban.
• After converting the dataset into np array, we then processed the Numpy array dataset to the pool of CNN-2D and Dense layer activation as Relu' using Keras. We have formed the Dense layer using the activation 'Softmax'.
• Next, we have compiled the model using "Adam" optimizer and used categorical cross entropy for the loss.

## SCREENSHOTS

![ScreenShot](https://raw.github.com/sudeeppereje/ML-645-project/master/screenshots/Testimage.jpg)
