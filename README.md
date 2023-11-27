# A Quick Look at B-cos Nets' Adversarial Robustness

Repository containing checkpoint weights and jupyter notebook for generating results in [A Quick Look at B-cos Nets' Adversarial Robustness](https://mhmoodlan.github.io/blog/b-cos-robustness).

Work based on [B-cos networks](https://github.com/B-cos/B-cos-v2) (see paper: Böhle, M., Singh, N., Fritz, M., & Schiele, B. (2023). [B-cos Alignment for Inherently Interpretable CNNs and Vision Transformers. arXiv preprint arXiv:2306.10898.](https://arxiv.org/abs/2306.10898)).

# Adversarial robustness against PGD attacks

Evaluation of the attacks done using the [Robustness](https://github.com/madrylab/robustness) package, from which the pretrained (Adv-)ResNet-50 models were used.

Table 1: CIFAR-10 test accuracy against PGD $\ell_\infty$ attacks:
|Table 1|Standard Accuracy|$\epsilon=8/255$|$\epsilon=16/255$|
|-------|-----------------|------------------------------------|-------------------------------------|
| ResNet-50  |**95.25%**|0.0% / 0.0%|0.0% / 0.0%|
| Adv-ResNet-50 |87.03%|**53.49% / 53.29%**|**18.13% / 17.62%**|
| Bcos-ResNet-56 |88.06%|0.03% / 0.03%|0.0% / 0.0%|
| Bcos-ResNet-50 |87.42%|19.79% / 19.10%|8.33% / 7.68%|

Table 2: CIFAR-10 test accuracy against PGD $\ell_2$ attacks:
|Table 2| Standard Accuracy | $\epsilon=0.25$ | $\epsilon=0.5$ | $\epsilon=1.0$ | $\epsilon=2.0$ |
|------|-----|------------|-------------|---------|--------|
| ResNet-50  |**95.25%**|8.66% / 7.34%|0.28% / 0.14%|0.0% / 0.0%|0.0% / 0.0%|
| Adv-ResNet-50  |90.83%|**82.34% / 82.31%**|**70.17% / 70.11%**|**40.47% / 40.22%**|5.23% / 4.97%|
| Bcos-ResNet-56 |88.06%|35.06% / 34.75%|13.64% / 13.20%|9.02% / 8.91%|0.0% / 0.0%|
| Bcos-ResNet-50 |87.42%|65.64% / 65.71%|50.19% / 49.96%|33.16% / 32.04%|**15.01% / 14.57%**|

