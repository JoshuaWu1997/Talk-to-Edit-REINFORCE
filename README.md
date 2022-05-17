# Talk-to-Edit with RL extension

![Python 3.7](https://img.shields.io/badge/python-3.7-green.svg?style=plastic)
![pytorch 1.6.0](https://img.shields.io/badge/pytorch-1.6.0-green.svg?style=plastic)

This repository is a reinforcement learning based extension of this paper:
> **Talk-to-Edit: Fine-Grained Facial Editing via Dialog**<br>
> Yuming Jiang<sup>∗</sup>, Ziqi Huang<sup>∗</sup>, Xingang Pan, Chen Change Loy, Ziwei Liu<br>
> IEEE International Conference on Computer Vision (**ICCV**), 2021<br>

## Our Code Structure
We aggregate our code base into two notebooks:
1. Editing with simulator (demo/qualitative results): <a href="https://colab.research.google.com/drive/1YfUQVqAf3XD3EECCwuiScVP_TJU9QBih?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="google colab logo"></a>
2. RL based editing with simulator (training): <a href="https://colab.research.google.com/drive/1lzBaysfO_B9v03xetq1HTKpfQbBKQNXn?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="google colab logo"></a>

The code written as scripts is structured:
* `utils/dialog_edit_utils.py`:
  * `EditTracker`: Gaussian Policy + State Tracker
    * `supervised_loss`: Supervised feature distance loss
    * `reinforce_loss`: REINFORCE loss
  * `gen_simulated_query`: User simulator
  * `dialog_with_simulator`: Interactive simulation environment (demo/test)
  * `train_with_simulator`: Interactive simulation environment (training)
* `policy_network.pth`: Our pretrained policy.

## Qualitative Results

### Running examples of interactive editing
edit images for multiple fields

![result](./assets/example_2.png)


edit images for multiple degree

![result](./assets/example_3.png)

### Comparison results of baseline and ours
![result](./assets/examples.png)

## Quantitative Results
### Feature Preservation
We shows the quantitative results of the feature distances of multi-round
interactive image editing. For the baseline method, We observe a trend of increasing feature distance
between its edited image and the target image. This observation may imply that while the baseline
method is editing the semantic attribute of the facial image, some other characteristics (e.g. facial
identity, background, colors, etc.) of the source image are not well preserved. In practice, such
deviation from the source image can be magnified in longer user sessions since the bias is accumulated
through multiple rounds.

![result](./assets/q1.png)

### Semantic Attribute Preservation
![result](./assets/q2.png)

## CelebA-Dialog Dataset

[**CelebA-Dialog Dataset**](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/CelebA_Dialog.html) is available for [Download](https://drive.google.com/drive/folders/18nejI_hrwNzWyoF6SW8bL27EYnM4STAs?usp=sharing).

**CelebA-Dialog** is a large-scale visual-language face dataset with the following features:
- Facial images are annotated with rich **fine-grained labels**, which classify one attribute into multiple degrees according to its semantic meaning.
- Accompanied with each image, there are **captions** describing the attributes and a **user request** sample.

The dataset can be employed as the training and test sets for the following computer vision tasks: fine-grained facial attribute recognition, fine-grained facial manipulation, text-based facial generation and manipulation, face image captioning, and broader natural language based facial recognition and manipulation tasks.

The codebase is maintained by [Junda Wu](https://github.com/JoshuaWu1997).

Part of the code is borrowed from [Talk-to-Edit](https://github.com/yumingj/talk-to-edit).
[[Paper](https://arxiv.org/abs/2109.04425)]
[[Project Page](https://www.mmlab-ntu.com/project/talkedit/)]
[[CelebA-Dialog Dataset](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/CelebA_Dialog.html)]