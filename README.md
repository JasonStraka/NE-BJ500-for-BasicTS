"# NE-BJ500-for-BasicTS" 
1. Download https://github.com/zezhishao/BasicTS and https://github.com/tsinghua-fib-lab/Traffic-Benchmark/tree/master/methods/GMAN/BJ500/data
2. copy files to /BasicTS
3.   BJ500.h5(unzip BJ500.7z)   to datasets\raw_data\BJ500\BJ500.h5
4.   Adj(BJ500).txt             to datasets\raw_data\BJ500\Adj(BJ500).txt
5.   generate_training_data.py  to scripts\data_preparation\BJ500\generate_training_data.py
6.   DCRNN_BJ500.py to examples/DCRNN/DCRNN_BJ500.py
7. run python scripts\data_preparation\BJ500\generate_training_data.py
8. check datasets\BJ500\adj_mx.pkl
9. run model on examples/DCRNN/DCRNN_BJ500.py
Result:
----------------------------------------------------------------------
|      data_file_path = datasets/raw_data/BJ500/BJ500.h5             |
|                 dom = True                                         |
|                 dow = True                                         |
|     graph_file_path = datasets/raw_data/BJ500/Adj(BJ500).txt       |
|     history_seq_len = 12                                           |
|   norm_each_channel = False                                        |
|          output_dir = datasets/BJ500                               |
|      target_channel = [0]                                          |
|                 tod = True                                         |
|         train_ratio = 0.7                                          |
|         valid_ratio = 0.1                                          |
----------------------------------------------------------------------
raw time series shape: (6624, 500, 1)
number of training samples:4621
number of validation samples:660
number of test samples:1320
mean (training data): 52.12267299942433
std (training data): 20.76980173577049
