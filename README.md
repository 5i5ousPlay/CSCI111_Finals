# CSCI 111 Finals Project: Comparative Analysis of Gradient Boosting and Neural Networks in Classifying Stellar Bodies

*Submitted by Raul Jarod C. Conanan BSMS Computer Science in fulfillment of the finals project for CSCI 111 - Introduction to Artificial Intelligence*

## Running the Notebook

The provided notebook was run locally and requires additional configuration for platforms such as Google Colab or Amazon Sagemaker Lab.
Most of the required libraries / dependencies likely come by default with Colab and Sagemaker Lab instances. 
For libraries / dependencies that are not installed please see the provided `requirements.txt` file.

If you are running on Colab, you may or may not need to include:
`!pip install xgboost` in a cell to ensure that XGBoost is installed on the compute instance.

If you are running locally, create a virtual environment in the same directory where the notebook is (the default Python `venv` works just fine)
and run the command `pip install -r requirements.txt` to install all the needed dependencies for running the notebook.

**IMPORTANT:** If you plan on running the notebook locally, please note that it is fairly computationally intensive.
Some systems may struggle to run the notebook. Some cells are coded to utilize 100% of all your cores and may 
significantly slow down your machine's performance. The provided notebook takes around 45-50 minutes to run in full
on a machine with an i7 10750H and 32GB. 

## Loading Pretrained Models

Provided alongside the notebook, are the pretrained models if you wish to test it on a separate notebook
or script without having to go through the entire project just to have a functioning model you can use.

To load the models into your separate notebook or script add the following line to your code:

**For the Tensorflow DNN:**
`dnn_model = tf.keras.models.load_model('path/to/file/stellar_class_dnn.keras')`

**For the XGB Classifier:**
`xgb_model = XGBClassifier().load_model('path/to/file/stellar_class_xgb.json')`

## Running Pretrained Models

After loading the pretrained models into your script / notebook, using it is as simple as using
the same methods associated with the particular model.

**For the Tensorflow DNN:** `dnn_model.predict(scaled_feature_data)` 

**For the XGB Classifier:** `xgb_model.predict(feature_data)`

