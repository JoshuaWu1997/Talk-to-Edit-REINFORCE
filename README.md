# Talk-to-Edit with RL extension

![Python 3.7](https://img.shields.io/badge/python-3.7-green.svg?style=plastic)
![pytorch 1.6.0](https://img.shields.io/badge/pytorch-1.6.0-green.svg?style=plastic)

This repository is a reinforcement learning based extension of this paper:
> **Talk-to-Edit: Fine-Grained Facial Editing via Dialog**<br>
> Yuming Jiang<sup>∗</sup>, Ziqi Huang<sup>∗</sup>, Xingang Pan, Chen Change Loy, Ziwei Liu<br>
> IEEE International Conference on Computer Vision (**ICCV**), 2021<br>

[[Paper](https://arxiv.org/abs/2109.04425)]
[[Project Page](https://www.mmlab-ntu.com/project/talkedit/)]
[[CelebA-Dialog Dataset](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/CelebA_Dialog.html)]
[[Poster](https://drive.google.com/file/d/1KaojezBNqDrkwcT0yOkvAgqW1grwUDed/view?usp=sharing)]
[[Video](https://www.youtube.com/watch?v=ZKMkQhkMXPI)]

You can try our colab demo here. Enjoy!
1. Editing with simulator: <a href="https://colab.research.google.com/drive/1YfUQVqAf3XD3EECCwuiScVP_TJU9QBih?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="google colab logo"></a>

## Qualitative Results

![result](./assets/1024_results_updated.png)


## CelebA-Dialog Dataset

[**CelebA-Dialog Dataset**](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/CelebA_Dialog.html) is available for [Download](https://drive.google.com/drive/folders/18nejI_hrwNzWyoF6SW8bL27EYnM4STAs?usp=sharing).

**CelebA-Dialog** is a large-scale visual-language face dataset with the following features:
- Facial images are annotated with rich **fine-grained labels**, which classify one attribute into multiple degrees according to its semantic meaning.
- Accompanied with each image, there are **captions** describing the attributes and a **user request** sample.

The dataset can be employed as the training and test sets for the following computer vision tasks: fine-grained facial attribute recognition, fine-grained facial manipulation, text-based facial generation and manipulation, face image captioning, and broader natural language based facial recognition and manipulation tasks.


## Citation

   If you find our repo useful for your research, please consider citing our paper:

   ```bibtex
   @InProceedings{jiang2021talkedit,
     author = {Jiang, Yuming and Huang, Ziqi and Pan, Xingang and Loy, Chen Change and Liu, Ziwei},
     title = {Talk-to-Edit: Fine-Grained Facial Editing via Dialog},
     booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision},
     year={2021}
   }
   ```

The codebase is maintained by [Yuming Jiang](https://yumingj.github.io/) and [Ziqi Huang](https://ziqihuangg.github.io/).

Part of the code is borrowed from [stylegan2-pytorch](https://github.com/rosinality/stylegan2-pytorch), [IEP](https://github.com/facebookresearch/clevr-iep) and [face-attribute-prediction](https://github.com/d-li14/face-attribute-prediction).

