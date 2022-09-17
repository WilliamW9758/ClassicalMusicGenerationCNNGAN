# Amadeus - A Classical Music Generation CNN GAN
Amadeus is a classical music generation CNN GAN built using Tensorflow Keras. 

## The Approach and Data Structure
The model took a visual approach to music generation, utilizing pianoroll as the medium.

![Pianoroll Example](Assets/pianoroll.png)

In a pianoroll, the vertical axis is the pitch of the note, each pixel up is a halftone higher. The horizontal axis is time. In this case, each pixel to the right denotes 32ms forward in time. 

The pianoroll is stored in an array, with each pixel being a note. If the pixels are connected horizontally, they are treated as a long note. The intensity of the pixel is intended to be the velocity of a note, or, the strength the piano key is pressed down. However, this feature is not currently implemented due to complexity in training the model. 

Pianoroll is great for a CNN model, since each pixel is related in some way to its spacial neighbors - you can form chords by certain vertical composition, and extended notes by adding horizontally. 

## The Model
