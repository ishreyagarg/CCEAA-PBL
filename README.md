# CCEAA-PBL
Brain tumor diagnosis is a critical aspect of healthcare.However, advancements in deep learning offer the potential to automate this process, improving efficiency and accuracy. Our project aims to leverage deep learning techniques on AWS to classify brain MRIs by their clinical diagnosis and identify tumors if present.

Link to deployed website - [https://results-shreya.s3.amazonaws.com/index.html]

Link to kaggle dataset -  [https://www.kaggle.com/sartajbhuvaji/brain-tumor-classification-mri]

Description of attached files-

On Google Collab, run the following scripts:
  1a. Brain_Tumor_Load_Data.ipynb
  1b. Brain_Tumor_ResNet50.ipynb
  1c. Brain_Tumor_VGG16.ipynb
  1d. Brain_Tumor_Xception.ipynb
  1e. Brain_Tumor_Combine_Three_Models.ipynb

These scripts will generate models for various CNN techniques and Random forest classifier (which are also available in the repository, namely ResNet_model.h5, VGG16_model.h5, Xception_model.h5, random_forest.joblib.

We also have made the website which have the following components, index.html, style.css, PhotoViewer.js and loading.gif.

There is a small test dataset also attached for uploading in S3 buckets.

Steps for the proper functioning-
1. Run the 1a to 1e notebooks on Google colab.
2. It generates models to be used later.
3. Create 3 S3 Buckets to store models(4), test images and website pages.
4. Load the models in one bucket.
5. Load the testing images in second bucket.
6. Use AWS Sagemaker to create a jupyter notebook which runs the model that is generating the results.
7. Then load the results in third bucket.
8. Configure AWS Cognito to allow unauth access to the images in the results bucket
9. Configure the results bucket to host static websites.
10. Working website with Brain MRI Classification and Tumor Detection using Deep Learning on AWS SageMaker has been successfully deployed and ready to run.
