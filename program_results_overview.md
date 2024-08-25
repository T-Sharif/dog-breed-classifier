This document provides an overview of the performance of three CNN architectures—AlexNet, VGG, and ResNet—using the Dog Breed Classifier program. The program classifies images to determine if they depict a dog and, if so, identifies the breed. The results are compared based on two datasets: one with 40 pre-uploaded pet images for training and another with 4 images used for testing.

# Results from Training Set
## Overview
The following results summarize the performance of each CNN architecture when classifying a set of [40 images of various animals](pet_images). The metrics include the total number of matches, the accuracy in identifying dog versus non-dog images, and the breed classification accuracy for identified dogs. 

*Click the architecture name for the full results file.*

### [AlexNet](alexnet_pet-images.txt)
<img width="500" alt="image" src="https://github.com/user-attachments/assets/96c31228-8f07-4e23-b817-a0f3e230f4ff"> </br>
<img width="550" alt="image" src="https://github.com/user-attachments/assets/625a7344-e865-41f2-8b2f-57c37746bc38">

Summary: AlexNet performs well in distinguishing between dogs and non-dogs but struggles with breed accuracy, achieving an 80% success rate in breed classification.

### [VGG](vgg_pet-images.txt)
<img width="500" alt="image" src="https://github.com/user-attachments/assets/ad7a2e05-4df5-460d-85c5-59ca275c07d4"> </br>
<img width="550" alt="image" src="https://github.com/user-attachments/assets/4315092a-f29f-4e6d-96bf-bc14c760c3d6">

Summary: VGG excels in both dog identification and breed classification, with a high breed classification accuracy of 93.3%. However, it has a longer processing time compared to AlexNet.

### [ResNet](resnet_pet-images.txt)
<img width="500" alt="image" src="https://github.com/user-attachments/assets/ddcac90a-0084-4f1d-a98a-61543cd06836"> </br>
<img width="880" alt="image" src="https://github.com/user-attachments/assets/26fd8cc5-df59-43d9-bfe2-71e0a786f988">

Summary: ResNet provides a good balance between classification accuracy and computational time, with a 90% success rate in breed classification. It correctly identifies dogs and non-dogs but has some misclassifications in breed and non-dog images.

# Results from Testing Set
## Overview
The following results summarize the performance of each CNN architecture when classifying a smaller [set of 4 images](uploaded_images)—a [coffee mug](Coffee_mug_01.jpg), a [golden retriever](Dog_01.jpg), a [mirrored version of the golden retriever](Dog_02.jpg), and a [panda](Panda_01.JPG). This includes the accuracy in identifying dogs versus non-dogs and breed classification accuracy for the identified dogs (**there was an error in the format of the 4 uploaded images, so while the dog breed is correctly identified, the program assigns the image as a breed mismatch**).

*Click the architecture name for the full results file.*

### [AlexNet](alexnet_uploaded-images.txt)
<img width="500" alt="image" src="https://github.com/user-attachments/assets/70e6099a-2118-4181-a6ca-70b75efa04c8"> </br>
<img width="550" alt="image" src="https://github.com/user-attachments/assets/3eb150cf-e487-4013-b793-d3f98bbb01ad">


Summary: AlexNet struggles with breed identification in the testing set, achieving no correct breed classifications despite accurate identification of dogs and non-dogs.

### [VGG](vgg_uploaded-images.txt)
<img width="500" alt="image" src="https://github.com/user-attachments/assets/f999208d-baf4-4770-b198-9ed592e25afa"> </br>
<img width="550" alt="image" src="https://github.com/user-attachments/assets/bf672db3-a308-4981-8d2f-b52b11af034b">

Summary: VGG also fails to identify the breed correctly in the testing set, similar to AlexNet, but processes images faster.

### [ResNet](resnet_uploaded-images.txt)
<img width="500" alt="image" src="https://github.com/user-attachments/assets/b06b2c22-217c-4bd4-8c7d-21c3966d845e"> </br>
<img width="550" alt="image" src="https://github.com/user-attachments/assets/74990390-1d3d-4345-bef9-fb9b786240d1">

Summary: ResNet performs similarly to AlexNet and VGG on the testing set, with fast processing but no correct breed classifications.

# Conclusion
## Summary of Performance
### Accuracy
1. **Breed Classification:** VGG performed the best in classifying the breed with 93.3% accuracy on the 40-image dataset, while AlexNet and ResNet achieved 80.0% and 90.0%, respectively. </br>
2. **Dog Classification:** All architectures correctly identified 100% of dog images, but there were occasional errors in breed classification. </br>
3. **Test Images:** All models exhibited a 50% match rate and 100% accuracy in distinguishing between dogs and non-dogs. However, breed classification accuracy was 0% across all architectures, indicating that improvements are needed, particularly for smaller datasets.

### Efficiency
1. **Runtime:** AlexNet was the fastest for both datasets, taking 23 seconds for the 40-image dataset and 0 seconds for the 4-image dataset. ResNet followed with 44 seconds for the 40-image dataset and 2 seconds for the 4-image dataset. VGG, while delivering the highest accuracy, had the longest runtime.

## Best Architecture
1. **For Accuracy:** VGG had the highest accuracy in breed classification for the 40-image dataset. </br>
2. **For Speed:** AlexNet is optimal for scenarios where processing speed is critical, offering the fastest runtimes but with lower breed classification accuracy.</br>
3. **For a Balance:** ResNet provides a good compromise with reasonable accuracy and runtime, making it suitable for applications where a balance between speed and accuracy is necessary. </br>
4. **For Testing with Limited Data:** All architectures had similar performance on the 4-image dataset, demonstrating their robustness in dog classification but showing limitations in breed classification.

This analysis indicates that while VGG is superior in breed classification accuracy, AlexNet offers the advantage of faster processing time. ResNet provides a balanced approach with a reasonable trade-off between accuracy and computational efficiency.

## Recommendations
1. For applications requiring high breed classification accuracy, VGG is preferred despite its longer processing time.
2. For faster processing with reasonable accuracy, ResNet is a good choice.
3. AlexNet is suitable for applications where classification is less critical, and processing time is a priority.
