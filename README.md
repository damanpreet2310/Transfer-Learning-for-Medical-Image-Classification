# Transfer-Learning-for-Medical-Image-Classification
Transfer Learning for Medical Image Classification
In this project we leverage transfer learning techniques, which consist of models that are trained on huge amounts of data, with a goal to Improve the performance of diabetic retinopathy detection using transfer learning by fine-tuning models and understanding the classification results with visualizations and explainable AI.

The project consiste of 5 tasks taska) ~taske) and idea is to generate the test_predictions based on each task and check the score on kaggle. 
a) Fine-tune a pretrained model using the DeepDRiD dataset. 
    Fine-tune an ImageNet pretrained model ResNet18 on the DeepDRiD dataset and experiment with different augmentation techniques.
    Note: The reference architecture used in this report is single image.
b) Two stage training with additional dataset(s).
     In stage 1 Fine-tune an ImageNet pretrained model ResNet18(in this case) with large data set (Kaggle DR Resized ) in my case and then save the stage1 model
     In stage2 fine tune the stage1 model on DeepDRiD dataset
     Evaluate the resulting stage2 model and get the test_predictions and eventually check the score on kaggle.
c)  Incorporate attention mechanisms in the model.
     Fine-tune an ImageNet pretrained model ResNet18 on the DeepDRiD dataset but also include the multi head attention trainning with single layer. 
     Explore with / without layer normalization and residual connection
d)  Ensemble learning
     Use bagging technique , by loading the pre-trained weights shared by teacher(efficientnet_b0 , resnet18 and resnet34) and re-train the model on DeepDRiD datase. As a           result, I have three test_prediction.csv file. Use these three test_predictions.csv file and use bagging to generate the final test_prediction.csv file and when i upload       to kaggle.
