https://github.com/user-attachments/assets/a1aaa77f-961c-4aac-b80c-856d981ef94c

https://github.com/user-attachments/assets/9b4812fd-7af8-462f-9720-1b4550de2c99

https://github.com/user-attachments/assets/afc9da2f-8d0b-4e48-9454-88c47e2bdef6
# Enhanced Video Lip-Synchronization with Wav2Lip and GFPGAN
This repository provides an integration of Wav2Lip and GFPGAN to enhance the resolution and quality of lip-synchronized videos. This combination leverages the lip-syncing capabilities of Wav2Lip and the image enhancement power of GFPGAN to produce high-quality results. Additionally, a user-friendly interface (UI) notebook is provided for easier interaction with the tools.
-----------------------------------
|📑 Original Paper|📰 Project Page|🌀 Demo|⚡ Live Testing|📔 Colab Notebook
|:-:|:-:|:-:|:-:|:-:|
[Paper](http://arxiv.org/abs/2008.10010) | [Project Page](http://cvit.iiit.ac.in/research/projects/cvit-projects/a-lip-sync-expert-is-all-you-need-for-speech-to-lip-generation-in-the-wild/) | [Demo Video](https://youtu.be/0fXaDCZNOJc) | [Interactive Demo](https://bhaasha.iiit.ac.in/lipsync) | [Colab Notebook](https://colab.research.google.com/drive/1tZpDWXz49W6wDcTprANRGLo2D_EbD5J8?usp=sharing) /[Updated Collab Notebook](https://colab.research.google.com/drive/1IjFW1cLevs6Ouyu4Yht4mnR4yeuMqO7Y#scrollTo=MH1m608OymLH)
-------------------------------------------------------------------------------------
# Introduction
Lip synchronization in videos is crucial for creating realistic and engaging content. While Wav2Lip provides state-of-the-art lip-syncing capabilities, the visual quality of the output can sometimes be lacking. This project aims to address this by integrating GFPGAN, which enhances the resolution and overall visual quality of the generated videos. The provided UI notebook makes it easier for users to interact with the tools.

![image](https://github.com/user-attachments/assets/693225f3-ad94-41fa-9302-126e947d91dd)

--------------
# Features
* High-Quality Lip Synchronization: Utilizes Wav2Lip for accurate lip-syncing.
* Enhanced Visual Quality: Applies GFPGAN to improve the resolution and clarity of videos.
* User-Friendly Interface: Includes a UI notebook for easier interaction.
* Preprocessing Enhancements: Implements preprocessing steps like freezing mouth movements and trimming audio to enhance the final result.
* Easy Integration: Seamlessly combines both models to provide a streamlined workflow.
-----------------------------
# Preprocessing Enhancements
To improve the results, several preprocessing steps are implemented:

* Freeze Mouth Movements(This step helps in stabilizing the mouth movements in the video):
* *  Extract the mouth region from the first frame of the video and use it as a static mouth image for frames where the audio is silent.
* Audio Preprocessing: Trims the audio with the pydub library to include only the part where the voice begins and ends. , for ensuring better synchronization.
-------------------------
Prerequisites
-------------
- `Python 3.6` 
- ffmpeg: `sudo apt-get install ffmpeg`
- Install necessary packages using `pip install -r requirements.txt`. Alternatively, instructions for using a docker image is provided [here](https://gist.github.com/xenogenesi/e62d3d13dadbc164124c830e9c453668). Have a look at [this comment](https://github.com/Rudrabha/Wav2Lip/issues/131#issuecomment-725478562) and comment on [the gist](https://gist.github.com/xenogenesi/e62d3d13dadbc164124c830e9c453668) if you encounter any issues. 
- Face detection [pre-trained model](https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth) should be downloaded to `face_detection/detection/sfd/s3fd.pth`. Alternative [link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/prajwal_k_research_iiit_ac_in/EZsy6qWuivtDnANIG73iHjIBjMSoojcIV0NULXV-yiuiIg?e=qTasa8) if the above does not work.
-------------------------------------------------------------
# Usage
This repository contains two notebooks:

1- Enhanced Video Lip-Synchronization:

* Open the Wav2Lip.ipynb notebook in your preferred environment (recommended Google Colab for GPU).
* Load your video and audio files.
* Follow the steps to process your video and apply enhancements.
2- User-Friendly Interface:
* Open the Wave2Lip UI.ipynb notebook for a more interactive experience.
* Load your video and audio files.
* Use the provided UI to easily process and enhance your videos.

----------------------------------------
# Examples
Here are some examples of the results you can achieve with this integration:

original:

https://github.com/user-attachments/assets/c68ddc0a-bdb5-4711-9829-6c8c96add1c5

After Enhancement
- result after freezing:
* *   Uploading result after freezing.mp4…
- result with many languages: 

* * https://github.com/user-attachments/assets/d34039ba-f6de-496a-ac76-a5ced2debfaa
* * Uploading 96_E_result.mp4…
* * Uploading 96_A_result.mp4…

Conclusion 
The lip-syncing pipeline using Wav2Lip provides a robust solution for synchronizing lip 
movements in videos with given audio tracks. By following the methodology outlined above, 
one can achieve high-quality lip synchronization. Integrating additional models like GFPGAN can 
further enhance the visual quality of the generated videos.





