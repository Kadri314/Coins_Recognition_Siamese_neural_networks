# Coins_Recognition_Siamese_neural_networks
A common problem in Numismatics, the study of currency, is to detect whether two coins have been struck by the same die. Striking a coin refers to pressing an image into the blank metal disc of the coin. To produce a coin, one must use two dies: one for the observe side (head) and another for the reverse side (tail). Our goal in this problem is to automatically predict given two coins, each as a pair of images representing observe and reverse sides, 1)whether the observe sides of those two coins have been struck by the same die, and 2) whether the reverse sides of those two coins have been struck by the same die.  To do this, we are providing you with a dataset consisting of 91 images of ancient coins of the Roman emperor Caracalla minted in Damascus. Each images depicts the observe and reverse sides of a coin. Also provided is an excel sheet that describes which observe sides and reverse sides of which coins have been struck by the same die. For example, given the following two rows from the excel sheet:  1 O1 R1 2 O1 R2  This indicates that the observe sides of the two coins 1 and 2 have been struck by the same die, whereas their reverse sides were struck by different dies.  You should build a deep learning model to solve the above problem. Once trained, your model should take two images representing two coins, and output whether their observe sides have been struck by the same die or not, and whether their reverse sides have been struck by the same die or not. You should submit your code as well as a write-up describing how you modeled the problem, what architecture and loss function you used, how did you split your data for training, validation, etc and finally some performance evaluation. Make sure you also submit your trained model so we can test it on other datasets.

I solved the coins problem  as following:
1- I Divided each image into two equal halfs, where the left side is the observe side and the right is the reverse side

2- I used Siamese neural networks to solve this task . I  trained the network on the coins so that it give small distances for the coins that are struck by the same die and big distances for coins that are struck by different dies

3- Finally, once the network is trained well on the coin images, I will use one shot learning to tell if two halfs (images) are struck by the same die or not based on a threshold 

4- I wrote a code where you feed a function two coins (file_path) and the function predicts whether the heads and tails are struck by same die or not .

5- Model’s accuracy :

heads accuracy:  0.5516483516483517 (55% of the predicted heads are predicted correct)

tails accuracy:  0.8105006105006105 (81% of the predicted tails are predicted correct)

The performance can be easily enhanced by picking a better threshold.
