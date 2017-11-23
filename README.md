# Tensorflow distributed example

An example of distributed Tensorflow training based on [Between-graph](https://www.tensorflow.org/deploy/distributed) replication strategy.

## Usage example

To start a new process run:

```
python train_dist.py --job_name ps --task_index 0 --worker_list localhost:2222 --ps_host localhost:2223 --epochs 10
```

