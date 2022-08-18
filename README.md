TransHawkes
===================================
TransHwakes: Prediction of Social Media Content Popularity Based on Transfomer Integrated Hawkes Process
It is an algorithm for measuring the influence of social media advertisers' advertising posts

# Framework
![image](https://github.com/naminshenren/TransHawkes/blob/master/transHAWKES.PNG)

DataSet
----------------------------------- 
We publish the Sina Weibo Dataset used in our paper,i.e., dataset_weibo.txt. It contains 119,313 messages in June 1, 2016.
Each line contains the information of a certain message, the format of which is:
    
    <message_id>\tab<user_id>\tab<publish_time>\tab<retweet_number>\tab<retweets>
    <message_id>:     the unique id of each message, ranging from 1 to 119,313.
    <root_user_id>:   the unique id of root user. The user id ranges from 1 to 6,738,040.
    <publish_time>:   the publish time of this message, recorded as unix timestamp.
    <retweet_number>: the total number of retweets of this message within 24 hours.
    <retweets>:       the retweets of this message, each retweet is split by " ". Within each retweet, it records 
    the entile path for this retweet, the format of which is <user1>/<user2>/......<user n>:<retweet_time>.
    
This dataset is limited to only use in research. And when you use this dataset, please cite our paper as listed above.

Downlowd link: https://pan.baidu.com/s/1c2rnvJq 

password: ijp6

                                                                                                                                                               
Steps to run TransHawkes
----------------------------------- 

1.split the data to train set, validation set and test set.
command: 

    cd gen_sequence
    python gen_sequence.py
    #you can configure parameters and filepath in the file of "config.py"
 
2.trainsform the datasets to the format of ".pkl"
command:

    cd deep_learning
    python preprocess.py
    #you can configure parameters and filepath in the file of "config.py"
 
3.train TransHawkes
command:

    cd deep_learning
    python run_sparse.py learning_rate learning_rate_for_embeddings l2 dropout
    #exsamples  python -u run_sparse.py 0.005 0.0005 0.05 0.8
    
The pre trained model can be obtained from the following link:
URL: https://pan.baidu.com/s/1yFRhs-wMPtm9LzEIsEalVQ
Password: q5A5
    
## Dependencies

The script has been tested running under Python 3.5.2, with the following packages installed (along with their dependencies):

- `numpy==1.14.1`
- `scipy==1.0.0`
- `networkx==2.1`
- `tensorflow-gpu==1.6.0`

In addition, CUDA 9.0 and cuDNN 7 have been used.

## Acknowledge
This work was supported by the National Key R&D Program of China under Grant No. 2020AAA0103804(Sponsor: <a  href ="https://bs.ustc.edu.cn/chinese/profile-74.html">Hefu Liu</a>) and partially supported by grants from the National Natural Science Foundation of China (No.72004021). This work belongs to the University of science and technology of China.

