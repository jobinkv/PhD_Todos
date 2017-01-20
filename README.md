# PhD Todos

## Table of condent
* **[Introduction](#introduction)**
* **[Document segmentation](#document-image-segmentation)**
* **[Current work in progress](#current-work-in-progress)**

## Indroduction

This file is to monitor and guide my PhD work at IIIT Hyderabad
In my PhD I am mainly focusing three problems they are:

## Current work in progress

- [x] Write code for deep feature based segmentation and put it for running.(19/Jan). Insprided from [link](https://arxiv.org/pdf/1411.6836v1.pdf)
      - [X] Checked the results and find all image are segment as a background! :(
      - [ ] Do the parameter tweaking
      - [x] Rerun the code with 50 patch size and 7 training image so that the number of sample is grater than the feature dimensuion 4096.
      - [ ] Check the above!
            
- [ ] Get the result with other features like SIFT SURF HOG LBP 

## My on going experiments
- [ ] Run the [work](https://github.com/mcimpoi/deep-fbanks) deep-filter banks. 
- [ ] Run the [work](https://github.com/HyeonwooNoh/DeconvNet) at atom need to check.
- [ ] 
      - [x] Status (Because of the caffe instalation issue the process is in hold)

## Need to fix items
- [x] Running multiple versions of opencv in PC
More reference from [link](http://code.litomisky.com/2014/03/09/how-to-have-multiple-versions-of-the-same-library-side-by-side/)
#### For installed version
```bash
g++ opencvtest.cpp -o test `pkg-config --cflags opencv` 
```
#### For older version
```bash
PROJECT(test)
SET(CMAKE_BUILD_TYPE Release)
CMAKE_MINIMUM_REQUIRED( VERSION 2.6 )
ADD_DEFINITIONS(-D CPU_ONLY)
LINK_DIRECTORIES(/home/jobin/installs/opencv_2.4.8/lib)
INCLUDE_DIRECTORIES(/home/jobin/installs/opencv_2.4.8/include)
ADD_EXECUTABLE(out opencvtest.cpp)
TARGET_LINK_LIBRARIES(out)


```


## Document image segmentation

### Problem statement

### Previous approaches

### Propposed approach

### Results

### Conclusion




