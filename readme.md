## Traffic Sign Generation with CVAE, GANs, and Diffusion Models

This project explores multiple generative modeling approaches using TensorFlow and modern diffusion models.

Implemented approaches:
- Convolutional Variational Autoencoder (CVAE)
- Deep Convolutional GAN (DCGAN)
- Fully Connected GAN (MLP-GAN)
- Stable Diffusion (text-to-image generation)

## Dataset

- **Dataset:** German Traffic Sign Recognition Benchmark (GTSRB)
- Real-world traffic sign images

A subset of the dataset was used for efficient training.

## Models

### CVAE (Variational Autoencoder)

- Convolutional encoder and decoder  
- Gaussian latent space  
- ELBO loss (reconstruction + KL divergence)  

**Behavior:**
- Smooth but blurry outputs  
- Stable training  
- Structured latent representation  

### DCGAN (Convolutional GAN)
- Convolutional generator and discriminator  
- Noise input (100-dimensional)  
- Adversarial training  

**Behavior:**
- Sharp and realistic images  
- Captures spatial features effectively  

### MLP-GAN (Fully Connected GAN)

- Fully connected generator and discriminator  
- Same training setup as DCGAN  

**Behavior:**
- Noisy outputs  
- Weak spatial structure  
- Demonstrates limitation of dense layers for images  

### Stable Diffusion 

- Pretrained text-to-image diffusion model  
- Generates images from textual prompts  

**Behavior:**
- High-quality, detailed images  
- Strong generalization without task-specific training  

## 📊 Comparison

| Model            | Output Quality | Structure | Control Type       |
|-----------------|--------------|----------|--------------------|
| CVAE            | Smooth       | Good     | Latent space       |
| DCGAN           | Sharp        | Strong   | Random noise       |
| MLP-GAN         | Noisy        | Weak     | Random noise       |
| Stable Diffusion| Very High    | Excellent| Text prompt        |


## Key Insights

- Convolutional architectures significantly improve image generation  
- GANs produce sharper outputs due to adversarial learning  
- VAEs provide structured latent representations but blur details  
- Fully connected networks are not suitable for image generation  
- Diffusion models enable high-quality generation with semantic control via text  


## Tech Stack

- TensorFlow / Keras  
- TensorFlow Probability  
- NumPy, Matplotlib  
- Stable Diffusion (pretrained model)

## Project Structure
- cvae_traffic_signs.ipynb
- dcgan_traffic_signs.ipynb: both dcgann and mlp gan
- stable_diffusion_examples.ipynb
- README.md
