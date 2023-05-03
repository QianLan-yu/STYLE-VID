# STYLE-VID
A synthetic video dataset for long-term person re-ID

## Two Samples of the dataset
![image](./picture/Samples.png)

## Comparison with other datasets

As analyzed in the paper, long-term Re-ID in video is closer to human awareness in real-world Re-ID scenarios. Moreover, the rich spatio-temporal information in video is helpful for long-term Re-ID. However, Research on long-term Re-ID in video is still in its infancy. To our knowledge, CCVID is the unique existing publicly available long-term video dataset. Nevertheless, the dataset size is fairly small and all videos are captured from a frontal perspective, which cannot satisfy our research on a generalized long-term Re-ID model.
|    Methods     |      Datasets      | Source        | identities        | Cameras | Bboxes    | Origin | CC  | Sequences        |
|----------------|--------------------|---------------|-------------------|---------|-----------|--------|-----------------|------------------|
| Image-based ST | CUHK03             | CVPR2014  | 1,467     | 6     | 14,097    | Real     | NO  | #         |
|                | Market-1501        | ICCV2015  | 1,501     | 6     | 32,668    | Real    | NO  | #         |
|                | DukeMTMC-reID      | ECCVW2016 | 1404      | 8     | 36,411    | Real     | NO  | #         |
|                | MSMT17             | CVPR2018  | 4,101     | 15    | 126,441   | Real     | NO  | #         |
|                | PersonX            | CVPR2019  | 1,266     | 6     | 273,456   | Generated    | NO  | #         |
|                | RandPerson         | ACM2020   | 8,000     | 19    | 1,801,816 | Generated    | NO  | #         |
| Image-based ST | PRID               | SCIA2011  | 200       | 2     | 40,033    | Real     | NO  | 400       |
|                | iLIDS-VID          | ECCV2014  | 300       | 2     | 42,460    | Real     | NO  | 600       |
|                | MARS               | ECCV2016  | 1,261     | 6     | 1,191,003 | Real     | NO  | 20,478    |
|                | DukeMTMC-VideoReID | CVPR2018  | 1,812     | 8     | 815,420   | Real     | NO  | 4,832     |
|                | LS-VID             | ICCV2019  | 3,772     | 15    | 2,982,685 | Real     | NO  | 14,943    |
| Image-based LT | PRCC               | TPAMI2019 | 221       | 3     | 33,698    | Real     | YES | #         |
|         | Real28             | CVPRW2020 | 28        | 4     | 4,324     | Generated    | YES | #         |
|         | VC-Clothes         | CVPRW2020 | 512       | 4     | 19,060    | Real     | YES | #         |
|         | LTCC               | ACCV2020  | 152       | 12    | 17,138    | Real     | YES | #         |
|         | Celeb-reID         | TCSVT2020 | 1,052     | #     | 34,186    | Internet    | YES | #         |
|         | COCAS              | CVPR2020  | 5,266     | 30    | 62,382    | Real     | YES | #         |
|         | DeepChange         | ARXIV2021 | 1,121     | 17    | 178,407   | Real     | YES | #         |
|         | LaST               | ARXIV2021 | 10,862    | #     | 224,721   | Internet    | YES | #         |
|         | NKUP+              | ACMMM2022 | 361       | 29    | #         | Real     | YES | 240       |
| Video-based LT | Motion-ReID        | WACV2018  | 30        | 2     | #         | Real     | YES | 240       |
|         | CVID-reID          | TMM2020   | 90        | #     | #         | Real     | YES | 2,980     |
|         | CCVID              | CVPR2022  | 226       | #     | 347,833   | Real     | YES | 2,856     |
| Gait recognition    | CASIA-B            | ICPR2006  | 124       | 11    | #         | Real     | 部分  | 13,640    |
|         | OU-MVLP            | CVA2018   | 10,307    | 14    | #         | Real     | NO  | 288,596   |
|         | GREW               | ICCV2021  | 26,345    | 882   | #         | Real     | YES | 128,671   |
|         | Gait3D             | CVPR2022  | 4,000     | 39    | #         | Real     | YES | 25,309    |
|         | GaitLU-1M          | TPAMI2022 | 1,035,309 | 1,379 | #         | Real     | YES | 1,035,309 |
| Video-based LT | STYLE-VID          | Ours       | 536       | #     | 485,394   | Generated    | YES | 8,721     |


![image](./picture/Comparison.png)

## The Process of Dataset Production
In this work, we propose a Style-Transferring sYnthetic Long-tErm Video Re-ID (STYLE-VID) dataset particularly for long-term Re-ID. We perform clothing style migration and pedestrian silhouette extraction on it. Firstly, we use the DG-Net to generate new sequences by performing clothing style migration for each sequence. These sequences were combined with the original data to form the RGB sequence part of the STYLE-VID. Then, to obtain the corresponding silhouette sequences, we used a semantic segmentation model to extract the pedestrian silhouettes from the color image sequences. 
![image](./picture/Generating.png)
