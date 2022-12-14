# Using_GAN_to_generate_Brain_Tumor_MRI_Images
One of the application of GANs is Image Augmentation. One of the challenge in Deep learning based Medical Imaging is that we have less data that could be used for training models. The images generated by Generative Adversarial Networks could be a solution to this problem. In this notebook I have used GAN to generate Brain Tumour MRI images. 

# Generative Adversarial Networks

<p style="font-size:20px">Generative adversarial networks are implicit likelihood models that generate data samples from the statistical distribution of the data. They’re used to copy variations within the dataset. They use a combination of two networks: generator and discriminator.</p>
<br>
<img src="https://debuggercafe.com/wp-content/uploads/2020/07/gan.png" />



## <u> The Generator: </u>
<p style="font-size:20px"> The generator is a part of GAN that learns to create fake data by incorporating feedback from the discriminator. A generator network takes a random normal distribution (z), and outputs a generated sample that’s close to the original distribution. It learns to make the discriminator classify its output as real.</p>

## <u> The Discriminator: </u>
<p style="font-size:20px">The discriminator in a GAN is simply a classifier. It tries to distinguish real data from the data created by the generator. It could use any network architecture appropriate to the type of data it's classifying.</p>

## <u> A Complete GAN model: </u>

<br><img src="https://www.mdpi.com/applsci/applsci-11-02913/article_deploy/html/images/applsci-11-02913-g001.png">

## <u> How do GANs work ? </u>

<p style="font-size:20px">Both the generator and the discriminator are neural networks. The generator output is connected directly to the discriminator input. Through backpropagation, the discriminator's classification provides a signal that the generator uses to update its weights.<br>
The generator learns to generate plausible data. The generated instances become negative training examples for the discriminator.
The discriminator learns to distinguish the generator's fake data from real data. The discriminator penalizes the generator for producing implausible results. <br>
When training begins, the generator produces obviously fake data, and the discriminator quickly learns to tell that it's fake. As training progresses, the generator gets closer to producing output that can fool the discriminator. Eventually, if generator training goes well, the discriminator gets worse at telling the difference between real and fake. It starts to classify fake data as real, and its accuracy decreases. That means the output generated by Generator is so good that the Discriminator could no longer differentiate between real and fake.
</p>
