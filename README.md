# multi-path-residual-neural-network-Based-IVIF
# A Deep Learning Based Relative Clarity Classification Method for Infrared and Visible Image Fusion
Abstract: Infrared and visible image fused results (IVIF) normally suffer from detail loss,noise occurrence, low contrast, and blurred edges. In this paper, a new method is proposed for IVIF problem. Specifically, visible images are enhanced by guided filter and high dynamic range compression. Infrared images are normalized by linear transformation. Then we use blur and clear discrimination to detect salient pixels between infrared and visible images. A fully weight shared multi-path residual neural network is proposed for blur discrimination between infrared and visible image pixels in the same position. Clear pixels are treated as salient pixels which contribute to fused images more than blur pixels. The output of our proposed network is a binary classification map for blur and clear discrimination and is treated as our fusion weight map in fusion stage. To deal with the discontinuous problem, we compute the two distance transformed maps of the binary classification map and its complementary map. The two distance transformed maps are used as weight map to fuse the enhanced infrared and visible images. Finally, we use single scale retinex (SSR) to further enhance our fused images. The experimental results in public IVIF datasets demonstrate the superior performance of our proposed approach over other state-of-the-art methods in terms of both subjective visual quality and objective metrics.

# Experimental setup
Our computation platform is Linux Ubuntu OS, Intel(R) Xeon(R) CPU E5-2687W v3 @ 3.10GHz, and Nvidia GeForce RTX 2080 TI GPU. Pytorch framework is used for our implementation. We train with stochastic gradient descent (SGD) with the learning rate of 0.0002, the momentum of 0.9, and the weight decay of 0.0005. The step learning rate schedule is implemented with a 225 step size of 1 and the gamma value of 0.9. The Cross-Entropy Loss is used for loss criterion, and batch normalization is used. The training is fast about 12 hours with 30 epoches.

# proposed network architecture.

![1](https://user-images.githubusercontent.com/57870274/212557583-352cf3ad-bcb6-478c-a3c2-c62f82220c2d.jpg)
![2](https://user-images.githubusercontent.com/57870274/212557591-6d2ec696-e5d0-4997-965a-62fc3a91576e.jpg)

# Experimental Results
1.  Quantitative comparison 

![Objective evaluation with SOTA methods](https://user-images.githubusercontent.com/57870274/212557885-c368721a-3ad2-4358-a593-0b5196f5ad95.JPG)


3.  Qualitative results
![TNO_21](https://user-images.githubusercontent.com/57870274/212557919-8c7ee4a6-c957-498d-9d96-c8322ea38f6d.jpg)
![subjective eval](https://user-images.githubusercontent.com/57870274/212557926-eb682baa-cf70-4bc5-a1c3-95ed62e65fa3.jpg)



