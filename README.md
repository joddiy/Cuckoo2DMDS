This is the extracted features from our dataset and the code for [Dynamic Malware Analysis with Feature Engineering and Feature Learning](https://arxiv.org/abs/1907.07352).

Thare are three directories as following:

# !IMPORTANT

Due to the copyright, we cannot offer this code and dataset in public anymore.

If you need the code and dataset, please submit an issue to this project and indicate your name, university and email within the issue. 

# dataset

The data directory contains all the samples and the label.csv provides the labels of these samples.

The _dataset.zip_ file is 331MB, expands to 11.2GB, and has a MD5 of 46cc2fe85037006a26a730ff0f8f9d54.

The original data at the dataset was collected from two months, April 2017 and May 2017. We run these malware at Cuckoo server and then collected their runtime logs. Then we applied the proposed feature engineering method on these logs to get this published dataset.

The summary of the dataset as the following:

|       | Benign | Malicious | Total |
|-------|--------|-----------|-------|
| April | 10160  | 15609     | 25769 |
| May   | 20552  | 11465     | 32017 |
| Total | 30712  | 27074     | 57786 |

Each sample is stored as numpy format, you can load it by ```numpy.load('./data/201704_0.npy')```. The shape of each sample is (LENGTH, 102), and the LENGTH is at most 1000. 102 is the dimension of each API call, please refer to our paper for more details.

# feature

This is the code of a feature engineering method.

Thare are two python scripts. The _Features.py_ containes the core code of the feature engineering method. And the _main.py_ implemented a multi-process function to call the _Features.py_. 

Please refer to _main_ function at each python script about how to run the code.

# model

This is the deep learning model for our proposed approach, which is built within keras platform and the _requriments.txt_ lists the necessary dependent packages.

If you want to run the model, please unzip the _dataset/dataset.zip_, then you can run the model.py by using python.


