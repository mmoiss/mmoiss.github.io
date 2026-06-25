---
title: "Q-Diffusion: Quantizing Diffusion Models"
collection: publications
excerpt: 'Running Stable Diffusion in 4-bit weights with high generation quality for the first time.'
date: 2023-05-01
venue: '*International Conference on Computer Vision* (ICCV), 2023'
paper_url: 'https://arxiv.org/abs/2302.04304'
project_page_url: 'https://xiuyuli.com/qdiffusion'
code_url: 'https://github.com/Xiuyu-Li/q-diffusion'
bibtex_url: 'https://github.com/Xiuyu-Li/q-diffusion#citation'
authors: 'Xiuyu Li, Yijiang Liu, **Long Lian**, Huanrui Yang, Zhen Dong, Daniel Kang, Shanghang Zhang, Kurt Keutzer'
citation:
cover_image: 2023-05-01-QDiffusion.png
---
Diffusion models have achieved great success in image synthesis through iterative noise estimation using deep neural networks. However, the slow inference, high memory consumption, and computation intensity of the noise estimation model hinder the efficient adoption of diffusion models. Although post-training quantization (PTQ) is considered a go-to compression method for other tasks, it does not work out-of-the-box on diffusion models. We propose a novel PTQ method specifically tailored towards the unique multi-timestep pipeline and model architecture of the diffusion models, which compresses the noise estimation network to accelerate the generation process. We identify the key difficulty of diffusion model quantization as the changing output distributions of noise estimation networks over multiple time steps and the bimodal activation distribution of the shortcut layers within the noise estimation network. We tackle these challenges with timestep-aware calibration and split shortcut quantization in this work. Experimental results show that our proposed method is able to quantize full-precision unconditional diffusion models into 4-bit while maintaining comparable performance (small FID change of at most 2.34 compared to >100 for traditional PTQ) in a training-free manner. Our approach can also be applied to text-guided image generation, where we can run stable diffusion in 4-bit weights with high generation quality for the first time.
