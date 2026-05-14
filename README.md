# Comparative-Analysis-of-Pre-trained-CNN-Models-for-Custom-Image-Classification
https://colab.research.google.com/drive/14YfcwgwI2rKiR5e7AXVWajHBiNg4zIrE?usp=sharing

A. Model Performance
1. Highest Accuracy: MobileNetV2 achieved the highest accuracy, reaching 95.00% on the test set. It likely performed best due to its efficient architecture that balances depth and parameter count, making it highly effective at capturing botanical features in smaller datasets.

2. Lowest Performance: ResNet50 had the lowest performance, with a test accuracy of only 17.10%. This could be due to the model being too deep for the specific dataset, leading to convergence issues or "vanishing gradients" if not tuned correctly for this specific task.

3. Loss Values: MobileNetV2 had the lowest test loss at 0.2312, whereas ResNet50 had the highest at 2.8035. VGG16 sat in the middle with a loss of 1.4574.

B. Evaluation Metrics
4. Accuracy Limitations: Accuracy can be misleading if classes are imbalanced; it doesn't show if the model is failing specifically on one type of cactus while succeeding on others.

5. Best F1-score: MobileNetV2 achieved the best F1-score (implied by its 0.99 ROC AUC and high accuracy). This indicates a strong balance between Precision and Recall, meaning it rarely misses a class and rarely makes false identifications.

6. Precision and Recall: MobileNetV2 showed high consistency in both, while ResNet50 struggled significantly, failing to reliably identify most classes.

C. Confusion Matrix Analysis
7. Misclassifications: Based on the Grad-CAM analysis, models like ResNet50 frequently misclassified images because they failed to focus on the cactus itself.

8. Patterns: A successful pattern was seen in MobileNetV2, where activations were centered on the plant body. Unsuccessful patterns in ResNet50 showed activations in the background or corners of the image.

D. ROC and AUC
9. Highest AUC: MobileNetV2 had the highest AUC score of 0.99.

10. AUC Significance: AUC tells us the model's ability to distinguish between classes; a score of 0.99 indicates the model has a 99% chance of correctly distinguishing between a positive and negative class.

E. Explainability (Grad-CAM)
11. Decision-Making: Grad-CAM revealed that MobileNetV2 focused on the texture and shape of the cactus.

12. Focus: MobileNetV2 focused on relevant regions (the plant), while ResNet50 focused on irrelevant background noise.

13. Meaningful Heatmaps: MobileNetV2 produced the most meaningful heatmaps, showing clear alignment between the heat intensity and the cactus features.

F. Model Comparison & Improvement
14. Recommendation: MobileNetV2 is recommended for deployment because it provides the highest accuracy (95%) with the lowest loss and best visual explainability.

15. Improvement: Performance could be further improved by fine-tuning the top layers of the pre-trained model or using data augmentation to help the model generalize even better.

G. Real-World Application
16. Scenarios: This can be used for automated botanical surveys, helping enthusiasts identify cactus species, or monitoring plant health in nurseries.

17. Risks: Deploying an inaccurate model (like the ResNet50 version) could lead to the misidentification of rare species or incorrect care instructions for specific plants.

18. Integration: The saved .keras files (shown being saved to Google Drive) can be exported and loaded into a TensorFlow.js or TensorFlow Lite framework for use in web and mobile applications.

<img width="1262" height="107" alt="image" src="https://github.com/user-attachments/assets/b2322766-35fb-49ac-9ed5-ea5c87c900b6" />


<img width="1686" height="458" alt="image" src="https://github.com/user-attachments/assets/15043f81-0bb9-44c7-9995-825a0abd4113" />
<img width="1690" height="562" alt="image" src="https://github.com/user-attachments/assets/f3291875-b080-453b-a43e-fae4ce16a03e" />
<img width="1685" height="583" alt="image" src="https://github.com/user-attachments/assets/af4a20ea-e872-4adb-b2bb-4b670fe7e93c" />
<img width="1062" height="678" alt="image" src="https://github.com/user-attachments/assets/b33120df-c5e9-4b99-84a0-29adb28b6430" />

