# Tsinghua-Daimler Urban Pose Dataset
***Note: The official website (www.urbanpose-dataset.com) is still under construction. There will be a fantastic dataset soon!***

## Introduction

**Tsinghua-Daimler Urban Pose Dataset (TDUP)**  is a large-scale human pose estimation dataset focusing on vulnerable road users (VRUs) in urban traffic scenes. There are around 90K VRU instances manually labelled with bounding boxes, including nearly 40K pedestrians and 50K riders. All these instances whose bounding boxes height are greater than 60 pixels are carefully labelled with skeleton joint points. Instance attributes like occlusion and truncation are also provided. All the  images were collected with high-resolution (at least 1920 x 1024 pixels) on-board camera in Chinese urban streets, where the situations are complex and various. With these 21K labelled images, TDUP is expected to play an important role in studying VRUs action for  autonomous driving or other related fields.

The dataset is coming soon and the certain statistics will be updated with its publication.

## Statistics Analysis

#### Dataset Overview

|                   | Train | Val  | Test  | All   |
| ----------------- | ----- | ---- | ----- | ----- |
| Image number      | 15000 | 2000 | 4417  | 21417 |
| Instance number   | 68258 | 7998 | 17201 | 93457 |
| pedestrian number | 29787 | 3387 | 6831  | 40005 |
| rider number      | 38077 | 4569 | 10256 | 52902 |
| co-rider number   | 387   | 42   | 109   | 538   |
| other VRU number  | 7     | 0    | 5     | 12    |

#### Statistics

We compare our TDUP dataset with other popular skeleton datasets including MSCOCO, AI Challenger and MPII. VRU instances in traffic scenes are characterized with small size, regular aspect ratio and frequent occlusions in images. Some figures of statistics are shown as follows.

##### 1. Person Size Frequencies

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/statistics/all_bbox_height_histogram.png" alt="bbox_height" style="zoom:50%;" />

*Note: Only bboxes whose height>60px are took into consideration.*

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/statistics/all_tight_bbox_aspect_histogram.png" alt="bbox_aspect" style="zoom:50%;" />

*Note: Tight bbox aspect ratio. 'Tight bbox' means the smallest rectangle frame contains all the human keypoints.*

##### 2. Person Densities

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/statistics/all_bbox_density_histogram_d.png" alt="person_density" style="zoom:50%;" />

*Note: Frequency-axis refers to the proportion of qualified frames accounting for the overall frames.*

##### 3. Keypoints Visibility

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/statistics/all_kps_visibility_histogram.png" alt="person_density" style="zoom:50%;" />

## Preview

Several labelled images are displayed as examples.

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/examples/2017-02-24-14-19-45_14-26-50-000.jpg" alt="example_1" style="zoom:50%;" />

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/examples/2017-03-04-09-56-25_09-56-35-000.jpg" alt="example_2" style="zoom:50%;" />

<img src="https://github.com/OpenICV-THU/TDUP-dataset/blob/master/examples/2017-04-25-17-12-35.jpg" alt="example_3" style="zoom:50%;" />