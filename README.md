# Tiny ML Occupancy Detection

The aim of this study is explain the different types of quantization methods of TensorFlow Lite and make a comparison 
with Neuton.AI platform. I would like to thank [Neuton.AI](https://neuton.ai/) for their help during the project. 

**The source of data is here:** [occupancy_detection_dataset](https://archive.ics.uci.edu/ml/datasets/Occupancy+Detection+#)

**The problem is:** Recognize whether someone is in the room or not based on measurements of temperature, humidity, 
light, and CO2. Ground-truth occupancy was obtained from time stamped pictures that were taken every minute.

**Features and Target**
- Temperature Humidity
- Light
- CO2
- Humidity Ratio
- Occupancy – 0 - not occupied; 1 - occupied status.

There are two colab notebooks:

- [Occupancy_TFLite_Models.ipynb](Occupancy_TFLite_Models.ipynb): includes all types of quantization methods of 
  TensorFlow Lite.
- [Occupancy_TFLite_vs_NeutonAI.ipynb](Occupancy_TFLite_vs_NeutonAI.ipynb): includes the comparison with Neuton.AI

You can find the results below:

Model | Parameters | Accuracy | Size_kb
------|------------|----------|--------
TensorFlow Model|57.0|0.974729|25.750000
TensorFlow Model_2|3553.0|0.990975|79.601562
TFLite_no_quantization|-|0.974729|1.632812
Dynamic_range_quantization|-|0.974729|1.734375
Representative_Dataset_Float_Fallback|-|0.974729|2.085938
Neuton_AI|60.0|0.981279|0.140000
