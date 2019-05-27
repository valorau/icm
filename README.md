Rauli Valo

Intelligent Computational Media - 
Generating synth patches using Principal Component Analysis



Project video on Youtube: https://youtu.be/AhfPI4CgHPA
Project video for download: https://tinyurl.com/yxceznoe


[Starting knowledge]

I had some programming experience with Pure Data, zero experience with Python.



[Project]

I wanted to teach computer to generate usable patches for a simple software synthesizer.

I found a Pure Data clone of Roland SH-101 on pdpatchrepo.info coded by pseudonym jersupereq. I modified the program so that it could randomize new patches, save them as .txt files and load patches from a .txt file back into the program.

Then I randomized new sounds until I got about eighty patches that I totally subjectively deemed to be good. In this context “good” means that I could imagine using them as a part of an electronic music composition. Over hundred randomized patches were deemed bad as I couldn't think of any use for them in conventional compositions. Also about a hundred were skipped altogether as they were not good or bad, just boring. The parameters of good patches were saved into one txt file and the parameters of bad ones into another.

Then I imported the good patch parameters (79 sets of 21 parameters) into JupyterLab, scaled them and ran them through Principal Component analysis. I experimented with different numbers of components ending up to using three. 

The variance ratio of the analysis was 0.39151707, 0.3264084, 0.28207453. To my limited understanding this implies that there were some small commonalities between the parameters of the good patches. I ran the analysis also with the bad patches. In them, no such commonalities were found.

After the analysis, new sets of synth patch parameters were generated randomly along the principal axis vectors. (I am not sure if this is the correct way to express it.) These were exported as a txt file that was formatted so that the Pure Data synthesizer could read them.


Results

The patches that were generated by the Python program were more often rhythmical than randomly generated ones. Other than that, I can't say anything certain about them. I had a feeling that they might have been somewhat more suitable for use in music compositions, but the test setting here is extremely vulnerable to many kinds of biases.

Learning outcomes

I got a nice introduction to Python and many great moments when figuring some (very basic) stuff out by myself. I learned how to handle .txt files with Pure Data as that was something that I haven't done before. When randomizing sounds I feel like I gained some intuitive insight on what kinds of synth sounds are usable for what kind of purposes, and which parameters have more effect to overall sound than others.
