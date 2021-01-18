# Al-DDoS Attack Detector

## Incentive
 With growing usage of the World Wide Web and the internet, the concern for security of your data as well as protection from cyber attacks posses a question open to research. The rise in DDoS attacks has led to an increasing interest in the cybersecurity area and many methods of security-data analytics have been applied in order to prevent such occurences and to secure the data.

## Basic concepts

>At the very basic level, we learn that network is basically a connection set between two different computers/servers to exchange information, which is done through sending mere binary data over the transmission lines, which may be wired or wireless (voltage along the conductor is varied at a high frequency to emit radio waves which are captured by a receiver). This data is sent as an encoding and is decoded on the reciever end. 
### Open Systems Interconnection (OSI model)
>This is a conceptual model/ framework which describes the various functions of a network system by categorizing it into 7 layers, namely physical, Data Link, Network, Session, Presentation, and Application layer. There are various ways in which the different layers of the OSI model are exploited to start DDoS, LDDoS, DRDoS, ALDDos, worm and other flooding attacks.
In our project, we focus specifically on the AL-DDoS attacks called Slowloris and Hulk.

>### Slowloris attack
>>Slowloris is an application layer DDoS attack which uses partial HTTP requests to open connections between a single computer and a targeted Web server, then keeping those connections open for as long as possible, thus overwhelming and slowing down the target.

>### Hulk Flood attack
>>HULK flood, is a DDoS attack named by its creators “HTTP Unbearable Load King” is similar to an HTTP flood and is designed to overwhelm web servers’ resources by continuously requesting single or multiple URL’s from many source attacking machines.

## Methods of Security-Data analysis:

>* **Statistical methods**: Network traffic activity is captured during normal conditions and a profile is generated which is then compared to real time conditions, and a threshold is marked. If the _anomaly score_ passes the threshold, an alarm of anomaly is generated.
>* **Machine learning methods**: This method is further classified into supervised, unsupervised and semi-supervised learning algorithms in order to train a model based on data obtained in order to detect a real-time flooding attack.
>* **Knowledge-based methods**: Network or host events are matched with predefined attack rules or certain signatures which would have been analyzed from previously collected data in order to examine them for the presence of attack instances.

## Information about the project

>In our project, we shall be using the **machine learning** method to train different models in order to predict or detect such types of attacks. We will be using the [Application-Layer DDoS Dataset](https://www.kaggle.com/wardac/applicationlayer-ddos-dataset) which has a total of **78 features**. We filter out the data, convert the categorical columns to numeric and also throw in some graphs to support our statistical findings. 
### In total, 3 models were trained with the following accuracies:

* **Deep Neural Network**
A Keras model with input layer of 77 units with 3 subsequent dense layers of sizes 128, 64 and 8 respectively. We use the **RELU** activation function in the first two layers and the **SIGMOID** activation function in the third and output layer. A **dropout** of 0.4 is applied to prevent overfitting. The model performed with 71% accuracy.
This model was outperformed by the **Tensorflow DNN Clasifier** with similar hidden layers and an **RMSProp** optimizer and **SIGMOID** activation function throughout to achieve 93.3% accuracy.

* **Gaussian Naive Bayes Classifier**
A Naive Bayes classifier was used which only needed to estimate the mean and the standard deviation from your training data and thus gave an accuracy  ot about 94.8% on the test data. 

* **Decision Tree Classifier**
A Decision Tree classifier with the **gini** criterion funtion was used to classify the attacks into 3 categories and the model performed the best compared to the rest with an accuracy of 99.9%.

## Future expansions
>With a rising complication factor attached to each attack, we plan to add features such as **Self-adaptive Detection** which will allow the model to adaptive to the changes of current network behaviors, **Protocol Independent** and the feature to make it able to deal with **Flash Crowds** where traffic might increase suddenly with legitimate users and the model might predict it to be a DDoS attack.

---

## References
* [ Security Data Collection and Data Analytics in the Internet: A Survey by Xuyang Jing, Zheng Yan and Witold Pedrycz](https://ieeexplore.ieee.org/iel7/9739/5451756/08428412.pdf)
* https://www.netscout.com/what-is-ddos/application-layer-attacks 
* https://mazebolt.com/what-is-ddos-attack
* 
