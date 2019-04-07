
![title](hike.png)
# ML Hikeathon

## Problem Statement

**Link Prediction on Hike’s Social Network**
Social networks are highly dynamic; they grow and change quickly over time through the addition of new edges, signifying the appearance of new interactions in the underlying social structure. The fundamental computational problem underlying social-network evolution is the Link Prediction problem:
 

Hike is a social platform and predicting links in their network forms the basis for recommending new friends to our users with whom they can possibly start a chat. High-quality recommendations help in strengthening the network by aiding the creation of new social connections between existing users. It also helps in the retention of new users by helping them find friends as they join the platform.

Can you develop an algorithm to predict whether a Hike user will chat another Hike user who is part of his/her phone contact book?

 
![title](pic.png)


## Data Description
The data for this competition i
s a subset of the Hike’s social graph and the anonymised features of users. Explicitly, the training data is of the following form:
train.zip contains 2 files namely **train.csv, user_features.csv**

**train.csv**
**node1_id, node2_id, is_chat**
Where node1_id and node2_id are anonymised identifiers for users who are in each other’s phone address book. is_chat signifies their chat relationship. is_chat is 1, if the first user sends a chat message with the second user, and 0 otherwise.

 

**user_features.csv**
**node_id, f1, f2, f3, f4, f5, f6, f7, f8, f9, f10, f11, f12, f13**
This file contains some anonymised features for all nodes/users. Here node_id (corresponding to node1_id and node2_id in train/test files) represents the user for whom we have features from f1 to f13

Mostly these features convey information around how active the users are in the app for the given time period - different slices of user engagement metrics. f13 is a categorical feature, f1-f12 are ordinal features each representing no. of days a user did some specific activity on the app in the last 31 days.

**test.csv (contained in test.zip)**
Build a model that can learn to predict probability of a node-pair in the test set to have a chat relation. The test set contains an id and a pairs of nodes
**id, node1_id, node2_id**

for which participants are required to predict is_chat on the test set. (Note that id is just here to identify a unique row in test set and is used in the submission format section)

 
## Submission Format
Submission file must be in a zipped format containing only one csv corresponding to the submission. The format to be followed is:
 

|id|is_chat|
|---|---|
|1|0.25|
|2|0.26|
|3|0.69|
|4|0.27|
|5|0.22|

## Evaluation Metric
The submitted output will be evaluated by the **AUC-ROC score**

## Competition [Link](https://datahack.analyticsvidhya.com/contest/hikeathon/)

## Leaderboard

* **[Public LB](https://datahack.analyticsvidhya.com/contest/hikeathon/lb)** : **17th Rank**
* **[Private LB](https://datahack.analyticsvidhya.com/contest/hikeathon/pvt_lb)** : **23th Rank**

 
