# Acne-detection-and-removal

> Final Project in "Computer Vision and Deep Learning" course in IIT Kanpur, 2025.  
> Authors: [Raj](https://github.com/rahulkumarmeena29)
>

<p float="left">
  <img alt="Image 1" src="/image_1.jpg" width="400" />
  <img alt="Image 2" src="/image_2.jpg" width="600" />
</p>


## Problem statement

Acne is one of the most spread skin diseases, that most of the population is affected at some point. However, having beautiful and healthy skin is popular and influenced by society nowadays, and for this reason many people use different apps to remove pimples from their photos manually to post them on social media. We decided to create an automatic pipeline to remove acne from photos to save valuable time spent on image processing.

## Datasets

In this task we tried two approaches and two datasets were used. The first one was a FFHQ dataset link(https://drive.google.com/drive/folders/1u2xu7bSrWxrbUxk-dT-UvEJq8IjdmNTP) created and markuped by us. It consists of 30 images and corresponding acne masks. The second one was [ACNE04](https://drive.google.com/drive/folders/18yJcHXhzOv7H89t-Lda6phheAicLqMuZ) dataset. For each image there was a corresponding xml file containing bounding boxes for pimples.

## Description

Deep Learning System for Automatic Acne Detection and Removal

This project introduces a comprehensive deep learning solution designed to automatically identify and eliminate acne lesions in facial photographs. The pipeline is tailored for use in skincare visualization, professional photo editing, and dermatology applications.

Main Highlights:

Accurate Detection: The system leverages a DLIB-based detection model, trained on the ACNE04 dataset, achieving a mean Average Precision (mAP) of 95%. This enables precise detection of pimples of various sizes and shapes.

Realistic Inpainting: To reconstruct smooth, natural-looking skin, a deep learning network built on gated convolutional layers is used. This approach avoids the over-smoothing and visible artifacts commonly produced by traditional inpainting techniques.

Two-Stage Workflow: The process includes:

Detection: Locating acne regions through bounding boxes.

Removal: Converting bounding boxes to binary masks and filling them with an inpainting network trained on healthy skin patches.

Optimized Performance: Compared to conventional methods and Faster R-CNN baselines, this system shows superior results in both detection accuracy and visual quality, with 90% user satisfaction.

Technical Details:

Detection Model: A DLIB detector using an anchor-free architecture and Complete IoU (CIoU) loss for precise bounding box regression.

Inpainting Network: A UNet-based architecture guided by predicted masks, trained on paired masked and clean skin images from the FFHQ dataset.

Preprocessing: Includes face alignment, HSV color normalization, and non-maximum suppression (NMS) to filter overlapping detections.

Evaluation Metrics: Assessed using PSNR, SSIM, and user survey ratings.

Future Enhancements: Planned improvements include supporting real-time video processing and deploying optimized models on mobile devices.

📊 Detection Performance
Model	mAP@0.5	Precision	Recall
DLIB	0.95	0.93	0.96
Faster R-CNN	0.89	0.88	0.91

