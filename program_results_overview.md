This document provides an overview of the performance of three CNN architectures—AlexNet, VGG, and ResNet—using the Dog Breed Classifier program. The program classifies images to determine if they depict a dog and, if so, identifies the breed. The results are compared based on two datasets: one with 40 pre-uploaded pet images for training and another with 4 images used for testing.

Results from Training Set
Overview
The following results summarize the performance of each CNN architecture when classifying a set of 40 images of various animals. The metrics include the total number of matches, the accuracy in identifying dog versus non-dog images, and the breed classification accuracy for identified dogs.

AlexNet
Summary: AlexNet performs well in distinguishing between dogs and non-dogs but struggles with breed accuracy, achieving an 80% success rate in breed classification.

VGG
Summary: VGG excels in both dog identification and breed classification, with a high breed classification accuracy of 93.3%. However, it has a longer processing time compared to AlexNet.

ResNet
Summary: ResNet provides a good balance between classification accuracy and computational time, with a 90% success rate in breed classification. It correctly identifies dogs and non-dogs but has some misclassifications in breed and non-dog images.

Results from Testing Set
Overview
The following results summarize the performance of each CNN architecture when classifying a smaller set of 4 images—a coffee mug, a golden retriever, a mirrored version of the golden retriever, and a panda. This includes the accuracy in identifying dogs versus non-dogs and breed classification accuracy for the identified dogs.

AlexNet
Summary: AlexNet struggles with breed identification in the testing set, achieving no correct breed classifications despite accurate identification of dogs and non-dogs.

VGG
Summary: VGG also fails to identify the breed correctly in the testing set, similar to AlexNet, but processes images faster.

ResNet
Summary: ResNet performs similarly to AlexNet and VGG on the testing set, with fast processing but no correct breed classifications.

Conclusion
Summary of Performance
Accuracy
Breed Classification: VGG performed the best in classifying the breed with 93.3% accuracy on the 40-image dataset, while AlexNet and ResNet achieved 80.0% and 90.0%, respectively.
Dog Classification: All architectures correctly identified 100% of dog images, but there were occasional errors in breed classification.

Efficiency
Runtime: AlexNet was the fastest for both datasets, taking 23 seconds for the 40-image dataset and 0 seconds for the 4-image dataset. ResNet was the second fastest overall, with 44 seconds for the 40-image dataset and 2 seconds for the 4-image dataset.

Best Architecture
For Accuracy: VGG had the highest accuracy in breed classification for the 40-image dataset.
For Speed: AlexNet was the fastest, making it suitable for real-time applications where speed is crucial.
For Testing with Limited Data: All architectures had similar performance on the 4-image dataset, demonstrating their robustness in dog classification but showing limitations in breed classification.

This analysis indicates that while VGG is superior in breed classification accuracy, AlexNet offers the advantage of faster processing time. ResNet provides a balanced approach with a reasonable trade-off between accuracy and computational efficiency.

Recommendations
For applications requiring high breed classification accuracy, VGG is preferred despite its longer processing time. For faster processing with reasonable accuracy, ResNet is a good choice. AlexNet is suitable for applications where classification is less critical, and processing time is a priority.


Conclusion
Summary of Performance

Accuracy:

Breed Classification: VGG achieved the highest breed classification accuracy at 93.3% on the 40-image dataset. In comparison, ResNet and AlexNet achieved 90.0% and 80.0% accuracy, respectively.
Dog Classification: All architectures identified 100% of dog images correctly. However, there were occasional errors in breed classification.
Efficiency:

Runtime: AlexNet was the fastest overall, with processing times of 23 seconds for the 40-image dataset and negligible time for the 4-image dataset. ResNet followed with 44 seconds for the 40-image dataset and 2 seconds for the 4-image dataset. VGG, while delivering the highest accuracy, had the longest runtime.
Performance on Test Images:

For test images, all models exhibited a 50% match rate and 100% accuracy in distinguishing between dogs and non-dogs. However, breed classification accuracy was 0% across all architectures, indicating that improvements are needed, particularly for smaller datasets.
Best Architecture:

For Accuracy: VGG is the best choice for applications requiring high breed classification accuracy, despite its longer processing time.
For Speed: AlexNet is optimal for scenarios where processing speed is critical, offering the fastest runtimes but with lower breed classification accuracy.
For a Balance: ResNet provides a good compromise with reasonable accuracy and runtime, making it suitable for applications where a balance between speed and accuracy is necessary.
Recommendations:

High Accuracy Needs: VGG is preferred for tasks where accurate breed classification is crucial and where longer processing time is acceptable.
Speed Prioritization: AlexNet is recommended for real-time applications where speed is more important than breed classification accuracy.
Balanced Approach: ResNet is advisable for applications needing a balance between speed and accuracy, especially when handling larger datasets.
This integrated analysis highlights the strengths and trade-offs of each architecture, providing clear guidance on their suitability based on specific application requirements and dataset sizes.


Conclusion
Summary of Performance

Accuracy:

Breed Classification: VGG achieved the highest accuracy for breed classification with 93.3% on the 40-image dataset, outperforming AlexNet (80.0%) and ResNet (90.0%). However, VGG had the longest runtime.
Dog Classification: All architectures correctly identified 100% of dog images, though breed classification accuracy on test images was 0% across all models, highlighting an area needing improvement.
Efficiency:

Runtime: AlexNet was the fastest, with a runtime of 23 seconds for the 40-image dataset and negligible time for the 4-image dataset. ResNet was the second fastest, taking 44 seconds for the 40-image dataset and 2 seconds for the 4-image dataset.
Best Architecture:

For Accuracy: VGG is the best choice for applications requiring high breed classification accuracy, despite its longer processing time.
For Speed: AlexNet is ideal for scenarios where processing time is critical, offering the fastest performance but with lower breed classification accuracy.
For a Balanced Approach: ResNet provides a good trade-off between accuracy and efficiency, making it suitable for applications needing a balance of both.
Performance on Test Images:

On test images, all architectures performed similarly in distinguishing dogs from non-dogs with 100% accuracy. However, breed classification accuracy was significantly lacking (0%), indicating that further improvements are needed in this area, especially for smaller datasets.
Recommendations:

High Breed Classification Accuracy: Use VGG for applications where accurate breed classification is crucial despite longer processing times.
Speed Priority: Choose AlexNet for scenarios where quick processing is more important than breed classification accuracy.
Balanced Needs: Opt for ResNet if you need a compromise between accuracy and computational efficiency.
Improvement Focus: Address the breed classification issues observed on test images to enhance the models' performance in real-world scenarios with limited data.
This analysis underscores that while VGG excels in breed classification accuracy, AlexNet offers superior speed. ResNet strikes a balance between these factors, and all models need refinement for better breed classification on smaller test datasets.
