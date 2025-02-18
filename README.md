## What is Grokking?

Generalization lies at the heart of machine learning. A good machine learning model should arguably be able to generalize fast, and behave in a smooth/predictable way under changes of (hyper)parameters.

Grokking, the phenomenon where the model generalizes long after overfitting the training set, has raised interesting questions after it was observed on algorithmic datasets by (Power et al., 2022). Training networks on small algorithmically generated datasets can reliably exhibit Grokking phenomenon. Such phenomenon can be quickly reproduced on a single GPU, so these datasets provide a fertile ground for studying a poorly understood aspect of deep learning: generalization of overparametrized neural networks beyond memorization of the finite training dataset.

 
 
## Omnigrok
This is the code repo for the paper: ["Omnigrok: Grokking Beyond Algorithmic Data"](https://openreview.net/forum?id=zDiHoIWa0q1), accpeted in ICLR 2023 as spotlight.  We elucidate [the grokking phenomenon](https://arxiv.org/abs/2201.02177) from the perspective of loss landscapes, and show that grokking can not only happen for algorithmic datasets and toy teacher-students setups, but also for standard machine learning datasets (e.g., MNIST, IMDb movie reviews, QM9 molecules).

The examples used in this paper are relatively small-scale. We make our codes as minimal as possible: each example is self-consistent, kept in a single folder. 
|Examples| Figure in [paper](https://openreview.net/forum?id=zDiHoIWa0q1) | Folder |
|--|--|--|
|Teacher-student|Figure 2| ./teacher-student|
| MNIST handwritten digits | Figure 3 | ./mnist |
| IMDb Movie Reviews | Figure 4 | ./imdb |
| QM9 Molecule properties  | Figure 5 | ./qm9 |
| Modular addition | Figure 6 & 8 | ./mod-addition |
| MNIST Representation | Figure 7 | ./mnist-repr |

For each example, we conduct two kinds of experiments: 
* (1) reduced landscape analysis: the weight norm is fixed during training. 
* (2) grokking experiments: the weight norm is not fixed during training (standard training).

Each folder (except for MNIST representation) contains two subfolders, for (1) "landscape" and (2) "grokking".


