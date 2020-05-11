# Optimal Transport ENSAE

## Summary and results

<p> 
This repository contains all the necessary material used for the implementation of OT-GAN. We tried to replicate the results from Genevay et al's 'Learning Generative Models with Sinkhorn Divergences' (2017) paper. More precisely, we focus on the MNIST experiment. 
  
In this case, the critic is constant and the goal is only to learn the target distribution using the sinkhorn loss derived from the 
  
</p>
 

<p>
Our approach is the following :

<ul>
  <li> We first built a standard GAN and generated some samples, for benchmark </li>
  <li> We implemented from scratch a model and a critic and tried to train this model on the MNIST dataset </li>
</ul>

</p>

<p>

Here are some benchmark images : 

<p align="center">
  <img src="https://github.com/hugothimonier/ENSAE_CycleGan_MNIST_USPS/blob/master/img/Discriminator.png">
</p>

And some samples on our trained model : 

<p align="center">
  <img src="https://github.com/hugothimonier/ENSAE_CycleGan_MNIST_USPS/blob/master/img/Discriminator.png">
</p>

The loss during traning evolved as follows : 

<p align="center">
  <img src="https://github.com/hugothimonier/ENSAE_CycleGan_MNIST_USPS/blob/master/img/Discriminator.png">
</p>

Obviously, the performance of our model can be increased. We present several reasons why our approach failed in the report and the notebook ```sinkhorn_gan.ipynb```

## Organization of the repository 

The main notebook, summarizing our results is ```sinkhorn_gan.ipynb```. Further details on our approach and trials can be found in the notebooks ```autodiff_ot_gan.ipynb``` and ```autodiff_ot_gan_checkpoint.ipynb``` located in the ```draft``` folder. 

The folder ```vanilla_gan.ipynb``` contains the notebook and the necessary helpers to replicate the standard GAN we intended to use as a benchmark. Since training can be long, a pretrained model (```generator.pkl```) and the generated samples (```train_samples.pkl```) can be found in the ```model``` folder. This model was trained with the 

Finally, the folder ```report``` contains our report on this project. This report introduces some theory, presents our approach and describes the architecture of our different networks. 

All notebook feature a link that enables them to be opened in Google Colab. <b> Cuda is mandatory to run the ```sinkhorn_gan.ipynb``` notebook. </b>





