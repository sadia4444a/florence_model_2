## Task Document

### Task Overview

### Title: Extract Frame and Find Detailed Caption from the Image and Use that Caption for Caption-to-Phrase Grounding

### Objective
To process frames extracted from a video, generate detailed captions for each frame, and use these captions to perform caption-to-phrase grounding. This involves drawing bounding boxes around relevant objects and labeling them based on the generated captions.

### Key Concepts
CAPTION_TO_PHRASE_GROUNDING: Caption-to-phrase grounding is a task that involves linking textual descriptions (captions) to specific regions in an image. This means associating parts of the image with the phrases in the caption. For instance, if a caption describes "a cat sitting on a mat," grounding would involve identifying and marking the bounding box around the cat and the mat in the image. The grounding process allows for the extraction of specific object locations and their relationships based on the textual description.

### Steps
#### Extract Frames from Video
 1. Load the video file.
 2.Process each frame at a specified interval (e.g., every 10th frame).
#### Generate Detailed Caption
  1. Use the Florence model to generate a detailed caption for each selected frame.
  2.Process the frame through the model to obtain the caption.
#### Perform Caption-to-Phrase Grounding
  1.Use the generated caption to perform a caption-to-phrase grounding task.
  2.Extract bounding boxes and labels from the frame based on the grounding results.
### Implementation Details
#### Initialization
  1.Define the tasks and text prompts.
  2.Create a directory to save processed images if it doesn’t already exist.
#### Video Processing
  1.Open the video file and read frames.
  2.Process every specified interval of frames (e.g., every 10th frame).
#### Caption Generation
   1.Use the Florence model to generate detailed captions for each selected frame.
   
   2.Store the captions along with frame numbers.
#### Caption-to-Phrase Grounding
  1.Use the detailed captions to perform grounding.
  
  2.Extract bounding boxes and labels from the image.
#### Draw bounding boxes and labels on the frame.
   1.Saving Processed Frames
   2.Save each processed frame with bounding boxes and labels in the specified output directory.


## Some Output:

### Caption : 7: 'In this image we can see a mobile on the surface. We can also see some text on it.'
### Caption-to-Phrase Grounding :![frame_7](https://github.com/user-attachments/assets/96fc23f4-5ed0-41c6-a298-2c175aaf2eb0)

### Caption : 96: 'In this image we can see a person holding a rope. In the background there is a blur background and there is some text on the image.',
### Caption-to-Phrase Grounding :![frame_96](https://github.com/user-attachments/assets/1c7abf18-d033-4bb6-87ed-2df65381b94a)

### Caption :  122: 'In this image we can see a man and a woman standing. In the background there is a wall with lights. On the right side there are flower vases and some other objects on the table.',
### Caption-to-Phrase Grounding :![frame_122](https://github.com/user-attachments/assets/efdf28cb-2c51-4085-acdf-7e12c08620e2)



### Caption : 124: 'In this image we can see a cake placed on the table. We can also see some glasses and the background is blurred.',
### Caption-to-Phrase Grounding :![frame_124](https://github.com/user-attachments/assets/2901f1c0-a997-4d62-84d3-2d36501672f1)


### Caption : 142: 'In this image we can see two mobiles and some text on the image.', 
### Caption-to-Phrase Grounding :![frame_142](https://github.com/user-attachments/assets/1f299d36-629d-4243-9db4-72e019899b89)







