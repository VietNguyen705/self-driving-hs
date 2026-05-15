# Self-Driving High School: Adversarial Attacks on CNNs

A 10-week summer research project for high school students.

**Title:** Evaluating FGSM and PGD Adversarial Attacks on CNN Models for Self-Driving Car Image Classification.

**Research question:** How much do FGSM and PGD adversarial attacks reduce the performance of CNN models on self-driving-related image classification tasks?

## How to start

1. Open [`adversarial_attacks_cnn.ipynb`](adversarial_attacks_cnn.ipynb) -- or launch it directly in Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VietNguyen705/self-driving-hs/blob/main/adversarial_attacks_cnn.ipynb)
2. Switch the runtime to **GPU** (Runtime -> Change runtime type -> T4 GPU).
3. Fill in every `TODO` cell from top to bottom.

Ask your instructor if stuck.

## 10-Week Plan

| Week | Tasks |
|------|-------|
| 1 | Learn CNNs, self-driving perception, adversarial examples, FGSM, PGD |
| 2 | Set up Python + PyTorch + Colab. Load CIFAR-10 |
| 3 | Train baseline CNN on CIFAR-10. Record accuracy, loss, confusion matrix |
| 4 | Implement FGSM. Test accuracy under different epsilon |
| 5 | Implement PGD. Compare with FGSM. Visualize adversarial images |
| 6 | Load and preprocess KITTI. Build a simplified classification task |
| 7 | Train CNN / ResNet-18 transfer on driving images |
| 8 | Apply FGSM and PGD. Measure accuracy drop and attack success rate |
| 9 | Compare CIFAR-10 vs driving dataset vulnerability |
| 10 | Final paper, poster, presentation. Ethical discussion |

## Datasets

- **CIFAR-10** -- auto-downloaded by torchvision.
- **KITTI** -- register and download from <http://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=2d>. Use `data_object_image_2.zip` and `data_object_label_2.zip`. Simplify to classes `car`, `pedestrian`, `cyclist`, `road scene`, or `non-road object`.

## Key references

- Goodfellow et al., "Explaining and Harnessing Adversarial Examples" (FGSM): <https://arxiv.org/abs/1412.6572>
- Madry et al., "Towards Deep Learning Models Resistant to Adversarial Attacks" (PGD): <https://arxiv.org/abs/1706.06083>
- PyTorch FGSM tutorial: <https://pytorch.org/tutorials/beginner/fgsm_tutorial.html>
- `torchattacks` library: <https://github.com/Harry24k/adversarial-attacks-pytorch>
