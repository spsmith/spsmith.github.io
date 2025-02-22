---
layout: page
title: 3D CSI
description: 3D Technology for Crime Scene Investigation
---

# 3D Technology for Crime Scene Investigation

![Crime scene house dataset]({{'images/WID-VE/CSI/csh.png' | absolute_url}})
*Sample image of one of our datasets, showing the UW Platteville Crime Scene House*

This two-year NIJ-funded project focused on the use of 3D capture technology for crime scene investigation. Using a LiDAR scanner, datasets of various mock crime scenes were captured. Working with the **Dane County Sheriff's Office** and the **UW-Madison LaFollette School of Public Affairs**, a cost benefit analysis was created determining the efffectiveness of this technology for crime scene investigators. I was one of three developers on this project, focusing on algorithm design as well as data collection.

I assisted with data collection at the University of Wisconsin-Platteville Crime Scene House and the Fox Valley Technical College Public Safety Training Center, two facilities with mock crime scene setups avaialable for scanning. Additionally, I visited crime scenes under investigation along with members of the sherriff's office to capture real world datasets.

![Crime scene house dataset side by side example]({{'images/WID-VE/CSI/csh_2.jpg' | absolute_url}})
*3D point cloud data showing the interior and exterior of the Crime Scene House*

The 3D scanning process results in very large datasets, containing hundreds of millions to billions of individual 3D data points. The analysis of these datasets also required our team to design new point cloud processing algorithms. I implemented these algorithms in C++ to speed up our lab's existing data processing pipeline, resulting in a much faster processing workflow.

A team from the LaFollette School of Public Affairs conducted a cost-benefit analysis using our data. I ported the R code they wrote to a web interface, creating an interactive web tool where crime scene investigators can input their own statistics to determine whether 3D scanning is an ideal technology for their department. [This web tool can be viewed here.](https://3d-csi-app.discovery.wisc.edu/)

Three focus groups were held alongside the **University of Wisconsin Survey Center**. Each focus group featured a brief overview of the project and its technology, and asked participants how the technology would change their work process. Focus groupmembers consisted of law enforcement officers, attorneys, and members of the general public serving as mock jurors. I assisted the survey center project director with each focus group, providing the technology overview and answering any questions focus group members had during the discussion.

*For more information, visit the project website at <https://3d-csi.discovery.wisc.edu/>.*

### Publications

The following publications resulted from this project:
- [A Cost-Benefit Analysis of 3D Scanning Technology for Crime Scene Investigation](https://www.sciencedirect.com/science/article/pii/S2665910719300258) *(Forensic Science International: Reports, Volume 1, November 2019)*
- [Methods for Detecting Manipulations in 3D Scan Data](https://www.sciencedirect.com/science/article/pii/S1742287619301793) *(Digital Investigation, Volume 30, September 2019)*

### Tools Used

*[CloudCompare](https://www.danielgm.net/cc/)*
- CloudCompare is an open source program designed for the analysis and editing of point cloud datasets.

*Programming languages used: C++, R*