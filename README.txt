Irish Sign Language - Hand Orientation Redundancy Filter (HORF) - Dataset

The refered dataset is part of the main ISL dataset, available at: 
https://github.com/marlondcu/ISL

The ISL dataset contains real hand images composed of 23 hand gestures (English alphabet except ’J’, ’X’ and ’Z’) and 3 dynamic gestures (’J’, ’X’ and ’Z’). The typology is one-handed finger spelling.

To build this dataset, short videos were filmed. In total 6 people (3 males and 3 females) performed the finger spelling ISL alphabets. Each shape was recorded 3 times.

Each static gesture (hand-shape) was performed by moving the arm in an arc from the vertical to the horizontal position. This was performed to simulate rotated gestures that can occur in real word conversations. The videos were converted into frames. Frames were converted to grayscale and the background was removed from the frame using a pixel-value threshold. This produced frames that contain only the arm and the hand.

The number of frames for each video depends on its length. Videos were recorded at 30 frames per second (fps) and a resolution of 640 × 480 pixels. The device used to record the videos was an Apple iPhone 7. The videos were saved with .mov extention. The video format was RGB24. 

From these videos, we selected only the static shapes (23) obtaining a total of 52,688 frames. Using a iterative method we computed the difference among these images and selectected only the 50,000 most different images. This dataset is called ITERATIVE REDUNDANCY FILTER (IRF) dataset and it is available at https://github.com/marlondcu/ISL_50k. However, this dataset still contains quite redundant frames, for this reason we created a new filter, using the computation of Axis of Least Inertia to identify the pose angle of the arm and the hand in each image. This new method is called Hand Orientation Redundancy Filter (HORF).

Directory's structure: Frames are stored into a zip file, containg all the 6 persons, 3 shots, 20 shapes. The file name structure is "Person" + person's number + shape + shot number + frame number, separated by hyphen (-). For example, "Person1-A-1-1.jpg" refers to Person 1, shape A, first shot, first frame. Note that the sequence of frames misses some of them, because they were the "redundant" ones.

The folder DynamicShapes contains the shapes ’J’, ’X’ and ’Z’, not used by the author yet. 

