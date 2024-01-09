# Report:

Finally, we get the classification accuracy on its test set,the best model with acc 0.6529865506329114 at 4 epoch!

Training data records can be found last at MAE_Cifar_TASK.ipynb.


# Introduction

In this project, I'll refer to Touvron et al., "Training data-efficient image transformers & distillation through attention, Configuration of the ViT-tiny model in ICML 2021 To train 20 cycles on the CIFAR10 dataset, and fine-tune the pre-trained ViT-tiny encoder on the train set of CIFAR-10 for 5 epochs and report the classification accuracy on its test set.

This is part of my reference paper

Table 1. Variants of our DeiT architecture. The larger model, DeiTB, has the same architecture as the ViT-B (Dosovitskiy et al., 2020). The only parameters that vary across models are the embedding dimension and the number of heads, and we keep the dimension per head constant (equal to 64). Smaller models have a lower parameter count, and a faster throughput. The throughput is measured for images at resolution 224×224.

        Model     embedding_dimension   #heads   #layers   #params  training_resolution  throughput(im/sec)
        DeiT-Ti        192                3       12        5M        224                 2536

lr=base_learning_rate * batch_size / 512     I have modify the denominator 256 to 512

In the following code, we will adopt the parameter configuration of DeiT-Ti.


Title of paper: Masked Autoencoders Are Scalable Vision Learners

Paper site: https://arxiv.org/abs/2111.06377

Code site: https://github.com/facebookresearch/mae

The project reference code address: https://github.com/IcarusWizard/MAE
