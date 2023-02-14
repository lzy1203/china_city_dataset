# RocketQAv2

## 算法描述
提出统一的联合训练优化方法，首次实现召回和精排的联合训练: 改进精排模型训练目标，提出动态软蒸馏方法，增强的负例采样方式。

## 环境 & 安装

```shell
Python 3.7
PaddlePaddle 1.8 (Please refer to the Installation Guide)
cuda >= 9.0
cudnn >= 7.0
faiss
```

## 使用

```shell
# Download data
- sh wget_data.sh

# Download the trained models
- sh wget_trained_model.sh

# Joint Model Training
cd model
sh script/run_joint-model_train.sh $TRAIN_SET $MODEL_PATH $nodes $epochs $instance_num

# Dual-encoder inference
sh script/run_retrieval.sh $TEST_SET $MODEL_PATH $DATA_PATH $TOP_K

# Cross-encoder inference
sh script/run_reranking.sh $TEST_SET $MODEL_PATH

```

## 论文/专利引用

