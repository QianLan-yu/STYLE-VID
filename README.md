# STYLE-VID
A synthetic video dataset for long-term person re-ID

## Two Samples of the dataset
![image](./picture/Samples.png)

## Comparison with other datasets

As analyzed in the paper, long-term Re-ID in video is closer to human awareness in real-world Re-ID scenarios. Moreover, the rich spatio-temporal information in video is helpful for long-term Re-ID. However, Research on long-term Re-ID in video is still in its infancy. To our knowledge, CCVID is the unique existing publicly available long-term video dataset. Nevertheless, the dataset size is fairly small and all videos are captured from a frontal perspective, which cannot satisfy our research on a generalized long-term Re-ID model.
![image](./picture/Comparison.png)

## The Process of Dataset Production
In this work, we propose a Style-Transferring sYnthetic Long-tErm Video Re-ID (STYLE-VID) dataset particularly for long-term Re-ID. We perform clothing style migration and pedestrian silhouette extraction on it. Firstly, we use the DG-Net to generate new sequences by performing clothing style migration for each sequence. These sequences were combined with the original data to form the RGB sequence part of the STYLE-VID. Then, to obtain the corresponding silhouette sequences, we used a semantic segmentation model to extract the pedestrian silhouettes from the color image sequences. 
![image](./picture/Generating.png)
