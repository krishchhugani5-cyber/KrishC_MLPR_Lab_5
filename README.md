# KrishC_MLPR_Lab_5
The aim of this project is to implement an unsupervised learning approach to cluster detected faces based on their color features and classify a new template image into one of these clusters. The project utilizes computer vision techniques for face detection and machine learning algorithms for clustering.

Methodology:
1)For face detection I used OpenCV's Haar Cascade Classifier (haarcascade_frontalface_default.xml) to identify faces in the source image.

2)For Feature Extraction I Converted detected face regions from BGR to HSV (Hue, Saturation, Value) color space. Then Calculated the mean Hue and Saturation values for each face to serve as feature vectors.

3)For Clustering I Applied the K-Means algorithm (k=2) to group the faces into two distinct clusters based on their features. Then Calculated centroids for each cluster.

4)to classify the Template I Processed a new test image (Dr_Shashi_Tharoor.jpg) through the same feature extraction pipeline. Then Predicted the cluster label for the new image to determine similarity with existing groups.

Key-Findings:
![image alt](https://github.com/krishchhugani5-cyber/KrishC_MLPR_Lab_5/blob/a8818721b13acc0fb54d82287494517010f91395/Screenshot%202026-02-16%20004247.png)
![image alt](https://github.com/krishchhugani5-cyber/KrishC_MLPR_Lab_5/blob/a665b1ba6dc6b031180ee759ffb8fccc186a5c6e/Screenshot%202026-02-16%20004322.png)
![image alt](https://github.com/krishchhugani5-cyber/KrishC_MLPR_Lab_5/blob/62d8d13cabf40822362b7fc9d5324dad6e549ba2/Screenshot%202026-02-16%20004754.png)
![image alt](https://github.com/krishchhugani5-cyber/KrishC_MLPR_Lab_5/blob/76e04917d37d768047c3236556e5744e0716b46a/Screenshot%202026-02-16%20004806.png)
![image alt](https://github.com/krishchhugani5-cyber/KrishC_MLPR_Lab_5/blob/f884d41b6a88f43357216c21329eee033d097984/Screenshot%202026-02-16%20004820.png)
![image alt](https://github.com/krishchhugani5-cyber/KrishC_MLPR_Lab_5/blob/f884d41b6a88f43357216c21329eee033d097984/Screenshot%202026-02-16%20004833.png)

The initial scatter plot reveals the distribution of faces based on Hue and Saturation levels.
The K-Means algorithm successfully separated the faces into two clusters (Cluster 0 and Cluster 1), indicated by the distinct centroids.
The test image was classified into Cluster 1, indicating it shares closer feature similarity with that specific group.

Conclusion: The experiment demonstrated that simple color-based features (Hue and Saturation) combined with K-Means clustering can effectively group faces with similar lighting or skin tone properties. The classification of the template image validates the model's ability to assign new data points to learned clusters based on distance metrics.
