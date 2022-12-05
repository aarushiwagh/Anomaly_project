# Anomaly_project
This project aims to create a meta-ensemble based classifier approach for attack detection in multi-tenant distributed systems.
Distributed systems in a network have always been vulnerable to cyber attacks due to exposure of vulnerabilities in shared memories, configurations, and network access.
Being co-holders in the same server provides attackers with an opportunity to track the activities of other users and accordingly make an attack when the security of the latter is in peril.
Traditionally, the effort has been to build full proof network architectures free from any threats and attacks. 
However, owing to its open-ended nature, it is impossible to come up with a completely secure architecture.
A common factor that can always be observed irrespective of the type of attacks is the specific values and configuration of the system through which the attack is instantiated. 
The rise in the use of machine learning algorithms and data collection facilities provides us with an opportunity to use network parameter values for modeling any anomaly and subsequent possibility of attacks.
The results obtained on this data demonstrate that machine learning coupled with ensembling can be used as a good aid for network attacks analysis. 
We use decision trees, random forest, SVM, Naive bayes and MLP Classifier techniques to classify attacks as "Inliers" or "Outliers". We also perform weighted average to get an ensemble model.
