# Video-Resolution-Enhancer
## Using Super Resolution to Enhance the resolution of a Video frame-by-frame

![Comparison](https://user-images.githubusercontent.com/28367168/55273188-133d7680-52ee-11e9-88ce-b73e8a9e1ab1.jpg)
*A snapshot of the input and output videos to compare the difference in resolution*

The goal of this project was to explore how video resolution can be improved using super resolution. 
This project Keras implementations of different Residual Dense Networks for Single Image Super-Resolution (ISR) referenced through an already existing
github repository, Read the full documentation at: https://idealo.github.io/image-super-resolution/.

The basic steps of this project can be summarized as follows : 
1. Extract video frame by frame
2. Run frames through ISR Model to obtain enhanced frames
3. Stitch enhanced frames together to produce output Video

## About the Files in this Project

1. **data** - Contains four sub-folders
   - frames : folder containing the extracted frames from input video
   - input : folder containing the input videos
   - output : contains the enhanced frames
   - output_videos : contains the final stitched output videos
2. **weights** - Folder containing .hdf5 files for different ISR Model weights
3. **Comparision.mp4** - Video showing the quality comparision between original and enhanced video
4. **VideoCreate.ipynb** - Jupyter Notebook for stitching enhanced frames together and saving the output video
5. **VideoExtract.ipynb** - Jupyter Notebook for extracting the frames from input video
6. **enhance.ipynb** - Jupyter Notebook that enhances extracted frames 

## Results

The input video was a 144p (256×144) Youtube video. The average time for enhancing each video frame was 45.0 seconds. The input video was taken uptil
60. The output video frame had a resolution of (512x288) which is double the initial resolution. This difference is visible in the comparision.mp4
video. It is to be noted that the process of enhancing this video quality was time-consuming as can be seen that with an average 45.0 seconds
processing 60 frames takes up around 45 Minutes. 

## Applications <br>

Given that a better and faster method is developed, such a technique can be used to real-time process frames from a video-streaming website
such as Youtube. This would enable us to view the video content at a better resolution without the added cost of bandwidth. The only delay
factor to be accounted for could be the processing time of enhancing each frame.

## Citations

```
@misc{cardinale2018isr,
  title={ISR},
  author={Francesco Cardinale et al.},
  year={2018},
  howpublished={\url{https://github.com/idealo/image-super-resolution}},
}
```

