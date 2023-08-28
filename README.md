"# NE-BJ500-for-BasicTS" 
将NE-BJ数据集用于交通流MTS预测，基于Traffic-Benchmark中公开数据，以BasicTS格式呈现。
1. Download https://github.com/zezhishao/BasicTS and https://github.com/tsinghua-fib-lab/Traffic-Benchmark/tree/master/methods/GMAN/BJ500/data
2. copy BJ500.h5(unzip BJ500.7z)   to datasets\raw_data\BJ500\BJ500.h5
3. copy Adj(BJ500).txt             to datasets\raw_data\BJ500\Adj(BJ500).txt
4. copy generate_training_data.py  to scripts\data_preparation\BJ500\generate_training_data.py
5. copy DCRNN_BJ500.py             to examples/DCRNN/DCRNN_BJ500.py
6. run python scripts\data_preparation\BJ500\generate_training_data.py
7. check datasets\BJ500\adj_mx.pkl
8. run model run.py on examples/DCRNN/DCRNN_BJ500.py

Result:

data_file_path = datasets/raw_data/BJ500/BJ500.h5             
dom = True                                         
dow = True                                         
graph_file_path = datasets/raw_data/BJ500/Adj(BJ500).txt       
history_seq_len = 12                                           
norm_each_channel = False                                        
output_dir = datasets/BJ500                               
target_channel = [0]                                          
tod = True                                         
train_ratio = 0.7                                          
valid_ratio = 0.1                                          
raw time series shape: (6624, 500, 1)
number of training samples:4621
number of validation samples:660
number of test samples:1320
mean (training data): 52.12267299942433
std (training data): 20.76980173577049

test_time: 15.08 (s), test_MAE: 4.5578, test_RMSE: 8.5757, test_MAPE: 0.1573, test_WAPE: 0.0917, test_MSE: 73.5423
