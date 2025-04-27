# DeepReach: A Deep Learning Approach to High-Dimensional Reachability
### [Project Page](http://people.eecs.berkeley.edu/~somil/index.html) | [Paper](https://arxiv.org/pdf/2011.02082.pdf)<br>

Original Repository (https://github.com/smlbansal/deepreach/tree/public_release) Maintainers<br>
[Albert Lin](https://www.linkedin.com/in/albertkuilin/),
[Zeyuan Feng](https://thezeyuanfeng.github.io/),
[Javier Borquez](https://javierborquez.github.io/),
[Somil Bansal](http://people.eecs.berkeley.edu/~somil/index.html)<br>
University of Southern California

Original Authors<br>
[Somil Bansal](http://people.eecs.berkeley.edu/~somil/index.html),
Claire Tomlin<br>
University of California, Berkeley

This code relates to an assessment done with an experiment for a "Dubin2D" system.

## High-Level Structure
The code is organized as follows:
* `dynamics/dynamics.py` defines the dynamics of the system.
* `experiments/experiments.py` contains generic training routines.
* `utils/modules.py` contains neural network layers and modules.
* `utils/dataio.py` loads training and testing data.
* `utils/diff_operators.py` contains implementations of differential operators.
* `utils/losses.py` contains loss functions for the different reachability cases.
* `run_experiment.py` starts a standard DeepReach experiment run.

## Monitoring a DeepReach Experiment
Throughout training, the training loss curves, value function plots, and model checkpoints are saved locally to `runs/experiment_name/training/summaries` and `runs/experiment_name/training/checkpoints` (and to WandB).

## Modifications for DeepReach Assessment
* `dynamics/dynamics.py`: a new "Dubins2D" class was added
* `experiments/experiments.py`: a new plotting case when z-axis = -1 for visualizing a 1x3 plot where columns are for different give time, t.

```
## Citation
@software{deepreach2024,
  author = {Lin, Albert and Feng, Zeyuan and Borquez, Javier and Bansal, Somil},
  title = {{DeepReach Repository}},
  url = {https://github.com/smlbansal/deepreach},
  year = {2024}
}
```

```
@inproceedings{bansal2020deepreach,
    author = {Bansal, Somil
              and Tomlin, Claire},
    title = {{DeepReach}: A Deep Learning Approach to High-Dimensional Reachability},
    booktitle = {IEEE International Conference on Robotics and Automation (ICRA)},
    year={2021}
}
```
