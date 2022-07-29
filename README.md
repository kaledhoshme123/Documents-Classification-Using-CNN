# Documents Classification Using CNN
Proposing the structure of a convolutional neural network, to identify the type of images of documents, the proposed structure of the convolutional neural network includes dividing the image of the document into four main regions and passing those regions to the convolutional neural network as a sequence of single images, and the goal of this methodology is the ability to facilitate the work of The convolutional neural network is able to extract the basic characteristics included in each of the four regions, and then use the GlobalAveragePooling1D layer in order to reach the general characteristics that distinguish the document, and thus the ability of the neural network to easily find the general characteristics that characterize each type of document.

We know that the type of document is determined according to many specifications, such as the design of the document, the header and footer, the body of the document and how the writing is formatted within the document, all of these factors help in the process of identifying the type of document.

Thus, we divided into the head of the document, the bottom of the document, the body of the document and it was divided into two regions (the right body and the left body).
Using the TimeDistributed layer, we are able to pass the images to the neural network as a set of four sub-images, where the properties are extracted from each part and then the common general properties are extracted.

## References:
Adam W. Harley, A. U. (2015). Evaluation of Deep Convolutional Nets for Document Image Classification and Retrieval. Toronto, Ontario: Ryerson University.

The study, which was my main reference, includes the same process of dividing the document into four sections, but with a difference in how to collect the common features. PCA & Conca was used in the study, while it was used in the GlobalAveragePooling1D code.

Another difference is the study used multiple convolutional neural structures for each part extracted from the images of the document, while in my notebook, one convolutional neural network was used, and the network input was considered to be 4 parts representing one complete image.
# Results:

![download (43)](https://user-images.githubusercontent.com/108609519/181709882-5b788f55-db16-4059-9723-302ede054f1a.png)

![download (44)](https://user-images.githubusercontent.com/108609519/181709929-f09a53e8-2151-4be0-a271-378242538492.png)

![download (45)](https://user-images.githubusercontent.com/108609519/181709989-e6c811d5-e52e-4bc1-a6a0-9102b31e1843.png)
