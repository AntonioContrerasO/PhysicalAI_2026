# PhysicalAI

For this hackathon, we explored multiple ideas, some of which were discarded as we encountered different challenges during the event. We ultimately decided to focus on a simple but direct approach. After reviewing the relevant papers and implementations, we found that the ACT approach was well suited to the small amount of data provided.

For our solution, we designed a simple set of experiments, as shown in the following images. Our initial goal was to generate 50 samples; however, calibration issues and problems with the solo-cli tool arose, which affected this process.

![Demo image](images/image-1.jpeg)

We made multiple attempts to gather data and were able to create a small dataset of 20 samples, which is slightly below the amount recommended by the ACT algorithm to achieve optimal results.

While generating the data, we realized that recording new samples was a time-consuming process, so we explored ways to generate additional data more efficiently. For this purpose, we experimented with multiple approaches:

1. Using the recorded videos, we randomly sampled frames and applied modifications to selected frames based on a predefined probability.

2. We also experimented with a video editing model to alter aspects of the environment, such as colors and visual attributes, which produced some interesting results.

see the video in assets folder

[![Demo video](images/image-1.jpeg)](assets/test_chunk.mp4)
