---
layout: page
title: 3D CSI
description: 3D Technology for Crime Scene Investigation
---

# 3D Technology for Crime Scene Investigation

![Crime scene house dataset]({{'images/csh.png' | absolute_url}})

This two-year project focused on the use of 3D capture technology for crime scene investigation. Using the lab's LiDAR scanner, datasets of various mock crime scenes were captured. Working with the **Dane County Sheriff's Office** and the **UW-Madison LaFollette School of Public Affairs**, this data was used to construct a cost benefit analysis in order to determine the efffectiveness of this technology for crime scene investigators.

I assisted with data collection at the UW-Platteville Crime Scene House and the Fox Valley Technical College Public Safety Training Center, two facilities with mock crime scene setups avaialable for scanning. Additionally, I visited a few crime scenes under investigation along with members of the sherriff's office to capture real world datasets.

The 3D scanning process results in very large datasets, containing hundreds of millions to billions of individual 3D data points. I wrote code in C++ to speed up our lab's existing data processing pipeline, resulting in a much faster processing workflow. The analysis of these datasets also required our team to design new point cloud processing algorithms, which I assisted in coding.

A team of students from the School of Public Affairs conducted a cost-benefit analysis using data from our team and the sheriff's office. I ported the R code they wrote to a web interface, resulting in a web tool where crime scene investigators can input their own statistics to determine whether 3D scanning is an ideal technology for their department.

A number of focus groups were held through the **University of Wisconsin Survey Center**. Each focus group featured a brief overview of the project and its technology, and asked participants how the technology would change their work process. Focus groups were conducted with law enforcement officers, attorneys, and members of the general public with jury experience. I assisted the survety center project director with each focus group, providing the technology overview and answering any questions focus group members had during the discussion.

For more information, visit the project website at <https://3d-csi.discovery.wisc.edu/>.

### Publications

This project produced the following publications:
- [A Cost-Benefit Analysis of 3D Scanning Technology for Crime Scene Investigation](https://www.sciencedirect.com/science/article/pii/S2665910719300258) *(Forensic Science International: Reports, Volume 1, November 2019)*
- [Methods for Detecting Manipulations in 3D Scan Data](https://www.sciencedirect.com/science/article/pii/S1742287619301793) *(Digital Investigation, Volume 30, September 2019)*

### Tools Used

*CloudCompare*
- CloudCompare is an open source program designed for the analysis and editing of point cloud datasets.

*Programming languages used: C++, R*