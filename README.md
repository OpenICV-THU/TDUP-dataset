# Tsinghua-Daimler Urban Pose Dataset
***Note: The official website (www.urbanpose-dataset.com) is still under construction. There will be a fantastic dataset soon!***

## Introduction

**Tsinghua-Daimler Urban Pose Dataset (TDUP)**  is a large-scale human pose estimation dataset focusing on vulnerable road users (VRUs) in urban traffic scenes. **To our best knowledge, it will be the first published human skeleton datasets with reasonable amounts for VRU perception in autonomous driving.** 

There are around 90K VRU instances manually labelled with bounding boxes, including nearly 40K pedestrians and 50K riders. All these instances whose bounding boxes height are greater than 60 pixels are carefully labelled with skeleton joint points. Instance attributes like occlusion and truncation are also provided. All the  images were collected with high-resolution (at least 1920 x 1024 pixels) on-board camera in Chinese urban streets, where the situations are complex and various. With these 21K labelled images, TDUP is expected to play an important role in studying VRUs action for  autonomous driving or other related fields.

The dataset is coming soon and the certain statistics will be updated with its publication.

## Preview

Several labelled images are displayed as examples.

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/examples/2017-02-24-14-19-45_14-26-50-000.jpg" alt="example_1" style="zoom:50%;" />

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/examples/2017-03-04-09-56-25_09-56-35-000.jpg" alt="example_2" style="zoom:50%;" />

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/examples/2017-04-25-17-12-35.jpg" alt="example_3" style="zoom:50%;" />

## Statistics Analysis

#### Dataset Overview

|                     | Train | Val  | Test  | All   |
| ------------------- | ----- | ---- | ----- | ----- |
| # Image number      | 15000 | 2000 | 4417  | 21417 |
| # Instance number   | 68258 | 7998 | 17201 | 93457 |
| # Pedestrian number | 29787 | 3387 | 6831  | 40005 |
| # Rider number      | 38077 | 4569 | 10256 | 52902 |
| # Co-rider number   | 387   | 42   | 109   | 538   |
| # Other VRU number  | 7     | 0    | 5     | 12    |

#### Statistics

We compare our TDUP dataset with other popular skeleton datasets including MSCOCO, AI Challenger and MPII. VRU instances in traffic scenes are characterized with small size and frequent occlusions in images. A table of comparisons and figures of statistics are shown as follows.

|                          | TDUP               | MSCOCO        | AI Challenger           | MPII           |
| ------------------------ | ------------------ | ------------- | ----------------------- | -------------- |
| # Domain                 | Autonomous driving | General       | General                 | General        |
| # Collection             | On-board camera    | Flickr images | Internet search engines | YouTube videos |
| # Keypoints              | 17                 | 17            | 14                      | 16             |
| # Images                 | 21K                | 200K          | 300K                    | 25K            |
| # Humans                 | 90K                | 250K          | 700K                    | 40K            |
| # Humans per image       | ≈4.29              | 1.25          | ≈2.33                   | 1.6            |
| # Average bbox height    | 152 px             | 204 px        | 568 px                  | 646 px         |
| # Visible body keypoints | 58.8%              | 86.2%         | 76.0%                   | 76.3%          |



##### 1. Person Size Frequencies

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/statistics/all_bbox_height_histogram_d.png" width = "600" height = "400" alt="bbox_height" align=center/>

The figure demonstrates the human bounding box height distribution of different datasets. TDUP has a larger proportion of small-size humans than others because a great number of VRUs in traffic scenes seem very small in images. 

*Note: Only bboxes whose height>60px are took into consideration.*

##### 2. Keypoints Visibility

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/statistics/all_kps_visibility_histogram_d.png" width = "600" height = "400" alt="keypoint visibility" align=center/>

The figure demonstrates the keypoints visibility of different datasets. It is common that VRUs are occasionally occluded by themselves or others visually so there is larger proportion of invisible keypoints in TDUP than in others. We compare them based on the definition of keypoints in TDUP. Facial points are not defined in AI Challenger and MPII so there are no corresponding columns for them. 