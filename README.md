# Tensorflow distributed example

An example of distributed Tensorflow training based on [Between-graph](https://www.tensorflow.org/deploy/distributed) replication strategy.

## Usage example

To run a distributed training process:

1. Start a parameter server:

```
python train_dist.py --job_name ps --task_index 0 --worker_list worker_1:2222,...,worker_n:2222 --ps_host ps_host:2223 --epochs 10
```

2. Start as many workers as you need on appropriate hosts:

```
python train_dist.py --job_name worker --task_index INDEX --worker_list worker_1:2222,...,worker_n:2222 --ps_host ps_host:2223 --epochs 10
```

After the training stage is finished, trained model will be saved to _checkpoint_dir_. Then, you will be able to evaluate model and visualize model predictions in [visualize_predictions.ipynb](https://github.com/ebochkov/tf_dist_example/blob/master/visualize_predictions.ipynb).


