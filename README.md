
https://github.com/user-attachments/assets/2ede8a8f-5179-4c56-bfd5-9b2d3f4fe91a

# Enhanced Video Lip-Synchronization with Wav2Lip and GFPGAN

This repository provides an integration of Wav2Lip and GFPGAN to enhance the resolution and quality of lip-synchronized videos. This combination leverages the lip-syncing capabilities of Wav2Lip and the image enhancement power of GFPGAN to produce high-quality results. Additionally, a user-friendly interface (UI) notebook is provided for easier interaction with the tools.

-------------------------------------------------------------------------------------

|📑 Original Paper|📔 Colab Notebook |📔 UI Colab Notebook 
|:-:|:-:|:-:|
[Paper](http://arxiv.org/abs/2008.10010) |  [Colab Notebook](https://colab.research.google.com/drive/1A2lF-OfXBu1k2SsGnQiCZBTmpi-PSDZR?usp=sharing)| [UI Collab Notebook](https://colab.research.google.com/drive/1_6DpJnzU35Rew0LHUJUL2lKD4o-biY5M?usp=sharing)

-------------------------------------------------------------------------------------

## Introduction
Lip synchronization in videos is crucial for creating realistic and engaging content. While Wav2Lip provides state-of-the-art lip-syncing capabilities, the visual quality of the output can sometimes be lacking. This project aims to address this by integrating GFPGAN, which enhances the resolution and overall visual quality of the generated videos. The provided UI notebook makes it easier for users to interact with the tools.

![image](https://github.com/user-attachments/assets/693225f3-ad94-41fa-9302-126e947d91dd)

--------------

## Features
- High-Quality Lip Synchronization: Utilizes Wav2Lip for accurate lip-syncing.
- Enhanced Visual Quality: Applies GFPGAN to improve the resolution and clarity of videos.
- User-Friendly Interface: Includes a UI notebook for easier interaction.
- Preprocessing Enhancements: Implements preprocessing steps like freezing mouth movements and trimming audio to enhance the final result.
- Easy Integration: Seamlessly combines both models to provide a streamlined workflow.
-----------------------------
## Preprocessing Enhancements
To improve the results, several preprocessing steps are implemented:

- Freeze Mouth Movements(This step helps in stabilizing the mouth movements in the video):
* *  Extract the mouth region from the first frame of the video and use it as a static mouth image for frames where the audio is silent.
- Audio Preprocessing: Trims the audio with the pydub library to include only the part where the voice begins and ends. , for ensuring better synchronization.
    
-------------------------
## Prerequisites

- `Python 3.6` 
- ffmpeg: `sudo apt-get install ffmpeg`
- Install necessary packages using `pip install -r requirements.txt`. 
-------------------------------------------------------------
## Usage
This repository contains two notebooks:

1- Enhanced Video Lip-Synchronization:

- Open the Wav2Lip.ipynb notebook in your preferred environment (recommended Google Colab for GPU).
- Load your video and audio files.
* - Follow the steps to process your video and apply enhancements.
    
2- User-Friendly Interface:

- Open the Wave2Lip UI.ipynb notebook for a more interactive experience.
- Load your video and audio files.
- Use the provided UI to easily process and enhance your videos.

----------------------------------------
## Examples
Here are some examples of the results you can achieve with this integration:


https://github.com/user-attachments/assets/a05ee9cb-ef06-427f-bc2a-a16995774b39


**original:**

https://github.com/user-attachments/assets/c68ddc0a-bdb5-4711-9829-6c8c96add1c5

**After Enhancement:**



https://github.com/user-attachments/assets/b77b1de0-4f10-4b63-a5de-ae6f56f34c10




## Conclusion 
The lip-syncing pipeline using Wav2Lip provides a robust solution for synchronizing lip 
movements in videos with given audio tracks. By following the methodology outlined above, 
one can achieve high-quality lip synchronization. Integrating additional models like GFPGAN can 
further enhance the visual quality of the generated videos.






