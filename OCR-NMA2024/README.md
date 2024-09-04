# An Investigation on Easy OCR Performance on processing images with different distortions 

Optical Character Recognition (OCR) models have numerous applications ranging from digitising archives to industrial quality assurance. 
Given their significance, understanding the impact of sub-par quality images on their performance is critical, and here we set out to explore
just that: What type of image corruption and/or distortion will have the most impact on an OCR model? 
We hypothesise that the OCR model’s performance will progressively degrade, in a non-linear fashion, as the level of image corruption 
increases. For certain types of transformations, like text skewing, we expect to see a far faster decline in relevant metrics. 
In order to perform the aforementioned model evaluation we decided on a two pronged approach: using an “off-the-shelf” model (EasyOCR) [1], as well as developing our own. Work on the custom model was focused on ResNet-based and visual transformer-based architectures; fine-tuning pre-trained models to mitigate the problem of limited computing resources. Additionally, to have greater control over the dataset that was to be used, we generated it utilising the TRDG module [2] and then corrupting the images as needed. Unfortunately, getting a custom model to work proved more difficult than expected, where, even though our models exhibited normal behaviour during training, they ultimately failed to converge i.e. recognize characters properly. Therefore, we pivoted towards EasyOCR on which front our efforts continue, thus, at 
this point, it is too early to draw conclusions from preliminary results. If afforded more (GPU) time our team would like to pursue finishing
custom OCR models, as the corruptions’ impact will certainly be model-dependent, so evaluating on multiple models would enable us to make a 
far more substantiated claim.

[1]: https://github.com/JaidedAI/EasyOCR
[2]: https://github.com/Belval/TextRecognitionDataGenerator
