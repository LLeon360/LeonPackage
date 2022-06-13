# UNetBiomedicalDiagnosis
Contains a module for functions that build and evaluate a U-Net Model which is a modified auto-encoder image-to-image architecture that includes skip connections from encoder to decoder layers with matching input dimensions to retain features from the encoded image. The model is designed for image segmentation and produces a mask based off x-ray data. The model is used with lung x-rays to segment out lungs, brain scans to segment out brain tumors, and pictures of a room to segment out a human figure. With the MD.ai chest x-ray dataset for lung segmentation, it is able to manage 98% accuracy with a wide range of 3,4,5 encoding block of Conv2D and MaxPooling and BatchNormalization + 1 latent layer without pooling and the mirrored number of decoding layers that do Conv2DTranspose for deconvolution and UpScaling to reverse MaxPooling making 7,9,11 layers with doubling filters/kernels in each encoding block from 16,32,64,80 that double with each block like in a traditional CNN and then half with each decoding block.
