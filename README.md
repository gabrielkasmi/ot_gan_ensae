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
  <img src="https://github.com/gabrielkasmi/ot_gan_ensae/blob/master/img/generated_images.png">
</p>

And some samples on our trained model : 

<p align="center">
  <img src="https://github.com/gabrielkasmi/ot_gan_ensae/blob/master/img/generated_ot_gan_mnist.png" width="200">
</p>

The loss during traning evolved as follows : 

<p align="center">
  <img src="https://github.com/gabrielkasmi/ot_gan_ensae/blob/master/img/losses_summary_notebook.png">
</p>

Obviously, despite the loss "converged" after 50 epochs, the performance of our model can be increased. We present several reasons why our approach failed in the report and the notebook ```sinkhorn_gan.ipynb```.

## Organization of the repository 

The main notebook, summarizing our results is ```sinkhorn_gan.ipynb```. Further details on our approach and trials can be found in the notebooks ```autodiff_ot_gan.ipynb``` and ```autodiff_ot_gan_checkpoint.ipynb``` located in the ```draft``` folder. 

The folder ```vanilla_gan``` contains the notebook and the necessary helpers to replicate the standard GAN we intended to use as a benchmark. Since training can be long, a pretrained model (```generator.pkl```) and the generated samples (```train_samples.pkl```) can be found in the ```model``` folder. These pretrained model can be used to generate your own samples in the notebook ```visualize_vanilla_gan.ipynb```without having to train the model again. If you want to train your model, you can use the notebook ```define_train_gan.ipynb```. 

Finally, the folder ```report``` contains our report on this project. This report introduces some theory, presents our approach and describes the architecture of our different networks. The folder ```img``` contains the images generated during training the models. 

All notebook feature a link that enables them to be opened in Google Colab. <b> Cuda is mandatory to run the ```sinkhorn_gan.ipynb``` notebook. </b>





