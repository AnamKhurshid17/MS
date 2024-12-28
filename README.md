**Complete Paper is available at:**<br />
https://scholar.google.com/citations?view_op=view_citation&hl=en&user=yx_jn10AAAAJ&citation_for_view=yx_jn10AAAAJ:u-x6o8ySG0sC
<br />
**SNE-UNET: An Efficient and Accurate Model for Skin Lesion Segmentation**
<br />
**_Abstract_**
<br />
Melanoma is the deadest type of skin cancer with the highest incidence rate affecting millions of people worldwide and causing almost 75% of deaths. Early detection of melanoma can significantly improve the survival rate by up to 99%. Many segmentation approaches based on traditional machine learning and deep learning techniques are being used to segment skin lesions. However, skin lesion segmentation is a challenging task due to intrinsic visual complexity and the presence of various artifacts in dermoscopic images such as human blood vessels, human hair, clinical ruler, etc. Deep learning-based approaches have shown promising performance in segmenting skin lesions precisely. U-NET is one of the most popular deep-learning models used to segment medical images. The original UNET faces the issue of vanishing gradient and slower network learning by using the RELU activation function. It also faces the issue in generalization of the network and overfitting due to Batch Normalization. It performs simple normalization that ignores key features at the middle and end layers. Therefore, we proposed an enhanced version of U-NET for robust and precise segmentation of skin lesions. We integrated Switchable Normalization and ELU activation functions to overcome the above mention limitations. The use of SN and ELU not only overcomes the issues of the original UNET but also boost the performance in terms of accurate segmentation of the skin lesions. Experimental results conducted on ISIC 2018 and ISIC 2017 datasets indicate that our proposed approach performed better than the existing state-of-the-art methods in terms of accuracy.
<br />
**PROPOSED METHODOLOGY**
<br />
U-NET architecture is the most commonly used approach
in skin lesion segmentation as it considers the feedback of
each layer from the input to the output, which improves its
overall performance. It comprises two main segments which
are encoder and decoder blocks. The encoder section
comprises various stacks of max pooling and convolutional
layers with RELU activation functions. While the decoder
section includes transposed convolutions for exact
localization by up-sampling the feature maps. In our proposed
methodology, we used U-NET as a basic or backbone
architecture however, enhanced it by incorporating
Switchable Normalization (SN) and Exponential Linear Unit
(ELU) activation function instead of RELU. In our method,
Switchable Normalization is used to overcome the issue of
overfitting. We selected Switchable Normalization instead of
Batch Normalization as BN is comparatively too much
expensive concerning computation and extremely reliant on
batch sizes. Additionally, it affects the independence among
the training sample inside the mini-batches and bounds the
competency of the deep learning model. Thus, we integrated
the Switchable Normalization layer into the U-NET
architecture as it considers all the dimensions and utilizes
diverse normalizers on different convolutional layers while
performing normalization operations that boost the
performance of the training models. Moreover, it has the
ability to balance learning and generalization of deep learning
models while training. The dying RELU problem arises in the
original U-NET architecture. Therefore, we used the ELU
activation function as it convergence the models faster and
provide both linearity and non-linearity simultaneously as
compared to the RELU activation function.
The framework of SNE-UNET is presented in Fig. 1. Each
encoder block comprises the following structure:
Fig. 1. SNE-UNET Architecture.Convolutional layer (Con), Switchable Normalization (SN),
ELU, Con, SN, ELU, and Max pooling (Max_pool) layer with
a pool size of [2×2]. Similarly, the decoder block initially uses
Transposed Convolution (Conv2DTranspose) layer for the
upsampling purpose which means it increases the resolution
of activation maps and constructs the image. Afterward, we
concatenated these activations maps with the activations maps
of encoder blocks having a similar size. Thus, each decoder
block consists of Conv2DTranspose, Concatenate, Con, SN,
ELU, Con, SN, and ELU layer. In addition to that, we used an
association layer to link the encoder and decoder section that
contains Con, SN, ELU, Con, SN, and ELU layer. The stride
and padding of all convolutional layers used in our approach
are fixed to 1 and the same respectively.
With consecutive convolutional and max pooling layers,
the encoding section extracts useful contextual and semantic
information. It detects the expedient features and resultantly
reduces the resolution. While the Transposed Convolution
(Conv2DTranspose) layer performs the opposite operation of
the pooling layer which means that the feature map’s
resolution is expanded. The probability of every pixel is
computed in the last convolutional layer to produce the final
output prediction mask. End-to-end training of the proposed
model was performed on training data

![image](https://github.com/user-attachments/assets/42b31136-91cf-4121-b6f6-90b947fb6c9d)
<br />

****Results and Analysis****
<br />

To validate the effectiveness and robustness of our SNEUNET model, we conducted multiple experiments on two
benchmark datasets. We computed DC, JAX, RC, and 𝑃𝑅𝐸𝐶
scores pixel-wise of the images present in the test dataset and
presented the results in Fig. 2 and Fig. 3. For comparing the
segmentation performance of the detected skin lesion area, a
precise melanoma boundary is needed. The proposed SNEUNET model acquired the boundary of the melanoma region
by grouping together the pixels belonging to the melanoma
into one region while the other pixels are gathered separately
<br />
Our proposed SNE-UNET model has accomplished
average score of 0.858 and 0.923 for Recall and Precision,
respectively on ISIC 2018 dataset. Similarly, average score
of DC and JAX were computed for all the images of the test
dataset. Our SNE-UNET method has shown remarkable
segmentation performance as the average DC and JAX score
of segmentation were calculated as 0.889 and 0.801,
respectively. Our method has shown outstanding
performance as it accurately locates the melanoma affected
region.

<br />
While on ISIC 2017 dataset, the SNE-UNET model has
achieved an average score of 0.899 and 0.912 for Recall and
Precision, respectively. Our proposed SNE-UNET model has
shown tremendous skin lesion segmentation performance on
ISIC 2017 dataset as it has accomplished an average score of
0.904 for DC and 0.825 for JAX which indicates that it has
accurately segmented the skin lesions. Our proposed
methodology has shown exceptional performance on ISIC
2017 dataset as it produced accurate results by determining
the accurate melanoma boundaries.



















