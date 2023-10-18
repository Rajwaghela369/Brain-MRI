# Brain Tumor Detection

## Aim:
The primary aim of this project is to assess and implement some techniques based on the research paper "[Image Processing Techniques for Brain Tumor Detection: A Review.](https://d1wqtxts1xzle7.cloudfront.net/40014067/IJETTCS-2015-10-01-7-libre.pdf?1447569226=&response-content-disposition=inline%3B+filename%3DImage_Processing_Techniques_for_Brain_Tu.pdf&Expires=1694783027&Signature=AJSZIggBcEaIh-06G5UtwdYRPTPek5phwL4UexlYCwwrmjfx2U2Eh2npRTfgsqI9syTnU9dQJzz1QDNQpYEUW06z8psYhKkiJjWm8dXITsLZfWbReRQJ4CH~0GyjEdnAxQjNb5q4QOJ0MfTgw7auhb4gY1eQKpdqbZhX6g7yPjbPFVfk~vlWYUWTZPjC2IB1lRUg6-WSd0ACGAMdxCgp8mk9hLuCieNOZafod1cq4v2f82aOu4Ko1SARn-t62iNr39UMgM7usdSBh1jaBdPm6m9p1A0~wup2PAL6wCSwpbfdxh7q3jf1BV~uhy4glQzzRRCIisAsWramAZ5do7MbLg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)" to enhance the accuracy of brain tumor detection within magnetic resonance imaging (MRI) scans.

## Abstract:
In particular, the project focus on two key methods highlighted in the paper: median filtering and thresholding. These straightforward yet effective techniques are applied meticulously to preprocess brain MRI images, significantly improving their quality and clarity. In conjunction with these preprocessing methods, leverage a deep learning model, specifically a Convolutional Neural Network (CNN), to evaluate their impact on brain tumor detection accuracy. Findings demonstrate a noteworthy achievement—an accuracy rate of 82.5%, underscoring the potential of these image processing techniques when integrated with advanced machine learning approaches. This project serves as a crucial step towards advancing the early diagnosis of brain tumors, ultimately benefiting both patients and healthcare practitioners in clinical settings. Further research and validation will be instrumental in the full integration of these techniques into practical medical applications.


## Dataset Description:

The **[Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)** dataset is sourced from Kaggle and is available for public use. This dataset is primarily used for the task of brain tumor detection using magnetic resonance imaging (MRI) scans.
Data Content: The dataset comprises MRI images of the human brain, which are categorized into two main sets:

**Tumor MRI Images:**
1. This subset contains MRI images of the brain where individuals have been diagnosed with brain tumors.
2. These images include various types and sizes of brain tumors.
3. The presence of tumors in these images makes them crucial for training machine learning models to detect and classify brain tumors.

**Non-Tumor MRI Images:**

1. This subset consists of MRI images of the brain where individuals do not have tumors.
2. These images serve as the control or reference group for comparison.
3. Non-tumor images are used to establish a baseline for distinguishing between normal brain structures and abnormal tumor growth.

This dataset It can be employed in the development of image classification algorithms aimed at automating the detection of brain tumors in MRI scans.

The Sample Image are follows:
With Tumor:

![tumor](https://github.com/Rajwaghela369/Brain-MRI/blob/adba717331396c5445731455c0e1842a87275470/Sample%20Images/Y4.jpg)

Without Tumor:

![no tumor](https://github.com/Rajwaghela369/Brain-MRI/blob/adba717331396c5445731455c0e1842a87275470/Sample%20Images/8%20no.jpg)

## Image Preprocessing:
It include application of few image processing methods which are used in tumor detection in medical. Methods are as follows:
1. **Median filtering:**

  Median filter is a non-linear filtering technique used for
  noise removal. Median filtering is used to remove salt
  and pepper noise from the converted gray scale image. It
  replaces the value of the center pixel with the median of
  the intensity values in the neighborhood of that pixel. ([Image Processing Techniques for Brain
  Tumor Detection: A Review, 2015](https://d1wqtxts1xzle7.cloudfront.net/40014067/IJETTCS-2015-10-01-7-libre.pdf?1447569226=&response-content-disposition=inline%3B+filename%3DImage_Processing_Techniques_for_Brain_Tu.pdf&Expires=1694783027&Signature=AJSZIggBcEaIh-06G5UtwdYRPTPek5phwL4UexlYCwwrmjfx2U2Eh2npRTfgsqI9syTnU9dQJzz1QDNQpYEUW06z8psYhKkiJjWm8dXITsLZfWbReRQJ4CH~0GyjEdnAxQjNb5q4QOJ0MfTgw7auhb4gY1eQKpdqbZhX6g7yPjbPFVfk~vlWYUWTZPjC2IB1lRUg6-WSd0ACGAMdxCgp8mk9hLuCieNOZafod1cq4v2f82aOu4Ko1SARn-t62iNr39UMgM7usdSBh1jaBdPm6m9p1A0~wup2PAL6wCSwpbfdxh7q3jf1BV~uhy4glQzzRRCIisAsWramAZ5do7MbLg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA))
2. **Threshold:**

  Image threshold is a simple, effective, way of partitioning
  an image into a foreground and background. This image
  analysis technique is a type of image segmentation that
  isolates objects by converting gray scale images into
  binary images. Image threshold is most effective in images
  with high levels of contrast. ([Image Processing Techniques for Brain
  Tumor Detection: A Review, 2015](https://d1wqtxts1xzle7.cloudfront.net/40014067/IJETTCS-2015-10-01-7-libre.pdf?1447569226=&response-content-disposition=inline%3B+filename%3DImage_Processing_Techniques_for_Brain_Tu.pdf&Expires=1694783027&Signature=AJSZIggBcEaIh-06G5UtwdYRPTPek5phwL4UexlYCwwrmjfx2U2Eh2npRTfgsqI9syTnU9dQJzz1QDNQpYEUW06z8psYhKkiJjWm8dXITsLZfWbReRQJ4CH~0GyjEdnAxQjNb5q4QOJ0MfTgw7auhb4gY1eQKpdqbZhX6g7yPjbPFVfk~vlWYUWTZPjC2IB1lRUg6-WSd0ACGAMdxCgp8mk9hLuCieNOZafod1cq4v2f82aOu4Ko1SARn-t62iNr39UMgM7usdSBh1jaBdPm6m9p1A0~wup2PAL6wCSwpbfdxh7q3jf1BV~uhy4glQzzRRCIisAsWramAZ5do7MbLg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA))

Preprocessed sample image:
With Tumor:

![yes](https://github.com/Rajwaghela369/Brain-MRI/blob/adba717331396c5445731455c0e1842a87275470/Preprocessed%20images/Y4.jpg.jpg)

Without Tumor:

![no](https://github.com/Rajwaghela369/Brain-MRI/blob/adba717331396c5445731455c0e1842a87275470/Preprocessed%20images/8%20no.jpg.jpg)

Apart from this there are various other techniques like edge detction, Image enhacement, etc. This methods are applied in various Image segmentation and object detection related tasks in Deep learning. It is crucial for enhancing data precision and overall model performance. However, the application of these methods should be judiciously chosen, as the effectiveness can vary depending on the nature of the data and the specific task. Striking the right balance is essential, as too many preprocessing steps may lead to overfitting or underfitting. Therefore, the selection of techniques is data-driven, with a focus on optimizing the preprocessing pipeline to achieve the best results for the given project.

## Image augmentation:
Image augmentation in deep learning involves applying various transformations (e.g., rotation, scaling, flipping, cropping) to training images to increase dataset diversity, improve model robustness, and prevent overfitting.

## Convolutional Neural Network Evaluation:
![model](https://github.com/Rajwaghela369/Brain-MRI/blob/284b754b9338ed2f46dfa5b40a0c0315d0f2240b/Results/result1.png)

## Results:
![result](https://github.com/Rajwaghela369/Brain-MRI/blob/284b754b9338ed2f46dfa5b40a0c0315d0f2240b/Results/result2.png)
