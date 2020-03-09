The problem statement: 

A geology research company wants to create a tool for identifying interesting patterns in their imagery data. They will provide an image of interest and the ML model should return the top "N" similar images. 

There are 6 different types of rocks:
•	andesite
•	gneiss
•	marble
•	quartzite
•	rhyolite
•	schist

The complexity lies in the fact that we cannot use Transfer Learning to classify the images. All transfer learning algorithms like ResNet, VGG16 etc. are trained on real world objects, and not on such rock formations. Hence their classification performance is really poor. We would need to create our own CNN architecture.

The approach: 

•	We first need to identify which of the categories the input image belongs to
•	Once that is identified we'll select "N" similar images from the corresponding folder
•	For obtaining similar images we'll use the "Structural Similarity Index" (SSIM) which is conveniently provided as part of the scikit-image package
•	The SSIM values range from 0 to 1, 1 being a perfect match


