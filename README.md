# Brain Tumor Detection

## Aim:
The primary aim of this project is to assess and implement some techniques based on the research paper "[Image Processing Techniques for Brain Tumor Detection: A Review.](https://d1wqtxts1xzle7.cloudfront.net/40014067/IJETTCS-2015-10-01-7-libre.pdf?1447569226=&response-content-disposition=inline%3B+filename%3DImage_Processing_Techniques_for_Brain_Tu.pdf&Expires=1694783027&Signature=AJSZIggBcEaIh-06G5UtwdYRPTPek5phwL4UexlYCwwrmjfx2U2Eh2npRTfgsqI9syTnU9dQJzz1QDNQpYEUW06z8psYhKkiJjWm8dXITsLZfWbReRQJ4CH~0GyjEdnAxQjNb5q4QOJ0MfTgw7auhb4gY1eQKpdqbZhX6g7yPjbPFVfk~vlWYUWTZPjC2IB1lRUg6-WSd0ACGAMdxCgp8mk9hLuCieNOZafod1cq4v2f82aOu4Ko1SARn-t62iNr39UMgM7usdSBh1jaBdPm6m9p1A0~wup2PAL6wCSwpbfdxh7q3jf1BV~uhy4glQzzRRCIisAsWramAZ5do7MbLg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)" to enhance the accuracy of brain tumor detection within magnetic resonance imaging (MRI) scans.

## Abstract:
In particular, the project focus on two key methods highlighted in the paper: median filtering and thresholding. These straightforward yet effective techniques are applied meticulously to preprocess brain MRI images, significantly improving their quality and clarity. In conjunction with these preprocessing methods, leverage a deep learning model, specifically a Convolutional Neural Network (CNN), to evaluate their impact on brain tumor detection accuracy. Findings demonstrate a noteworthy achievement—an accuracy rate of 82.5%, underscoring the potential of these image processing techniques when integrated with advanced machine learning approaches. This project serves as a crucial step towards advancing the early diagnosis of brain tumors, ultimately benefiting both patients and healthcare practitioners in clinical settings. Further research and validation will be instrumental in the full integration of these techniques into practical medical applications.


## About Dataset:

The **[Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)** dataset is sourced from Kaggle and is available for public use. This dataset is primarily used for the task of brain tumor detection using magnetic resonance imaging (MRI) scans.

**1.Tumor MRI Images:**

![tumor](https://github.com/Rajwaghela369/Brain-MRI/blob/adba717331396c5445731455c0e1842a87275470/Sample%20Images/Y4.jpg)

**2.Non-Tumor MRI Images:**

![no tumor](https://github.com/Rajwaghela369/Brain-MRI/blob/adba717331396c5445731455c0e1842a87275470/Sample%20Images/8%20no.jpg)

## Image Preprocessing:
It include application of few image processing methods which are used in tumor detection in medical. Methods are as follows:
1. **Median filtering:**

  Median filter is a non-linear filtering technique used for noise removal. 

2. **Threshold:**

  Image threshold is a simple, effective, way to isolates objects.

**1. Preprocessed Tumor Images:**

![yes](https://github.com/Rajwaghela369/Brain-MRI/blob/adba717331396c5445731455c0e1842a87275470/Preprocessed%20images/Y4.jpg.jpg)

**2.Preprocessed Non-Tumor MRI Images:**

![no](https://github.com/Rajwaghela369/Brain-MRI/blob/adba717331396c5445731455c0e1842a87275470/Preprocessed%20images/8%20no.jpg.jpg)

## Image augmentation:
Image augmentation in deep learning involves applying various transformations (e.g., rotation, scaling, flipping, cropping) to training images to increase dataset diversity, improve model robustness, and prevent overfitting.

## Convolutional Neural Network Evaluation:
![model](https://github.com/Rajwaghela369/Brain-MRI/blob/284b754b9338ed2f46dfa5b40a0c0315d0f2240b/Results/result1.png)

## Results:
![result](https://github.com/Rajwaghela369/Brain-MRI/blob/284b754b9338ed2f46dfa5b40a0c0315d0f2240b/Results/result2.png)

## Conclusion: 
Results underscores the effectiveness of the combined approach of image preprocessing and deep learning in improving the early diagnosis of brain tumors. While further research and validation are necessary to fully integrate these techniques into clinical practice, this project represents a significant step towards enhancing medical professionals' ability to detect brain tumors with precision and efficiency.

### References:
1. Vipin Y. Borole, Vipin Y. Borole, Dr. Seema S. Kawthekar - I JETTCS - Image Processing Techniques for Brain Tumor Detection: A Review, 2015 ([link](https://d1wqtxts1xzle7.cloudfront.net/40014067/IJETTCS-2015-10-01-7-libre.pdf?1447569226=&response-content-disposition=inline%3B+filename%3DImage_Processing_Techniques_for_Brain_Tu.pdf&Expires=1694783027&Signature=AJSZIggBcEaIh-06G5UtwdYRPTPek5phwL4UexlYCwwrmjfx2U2Eh2npRTfgsqI9syTnU9dQJzz1QDNQpYEUW06z8psYhKkiJjWm8dXITsLZfWbReRQJ4CH~0GyjEdnAxQjNb5q4QOJ0MfTgw7auhb4gY1eQKpdqbZhX6g7yPjbPFVfk~vlWYUWTZPjC2IB1lRUg6-WSd0ACGAMdxCgp8mk9hLuCieNOZafod1cq4v2f82aOu4Ko1SARn-t62iNr39UMgM7usdSBh1jaBdPm6m9p1A0~wup2PAL6wCSwpbfdxh7q3jf1BV~uhy4glQzzRRCIisAsWramAZ5do7MbLg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA))
