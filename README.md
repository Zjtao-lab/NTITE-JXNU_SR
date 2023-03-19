# Requirements
XXX

# Train
## 1. Prepare training data 
```matlab
run(GenerateTrainingPatchs.m)
```



## 2. Begin to train
```python
python -m torch.distributed.launch --nproc_per_node=1 --master_port=4321 basicsr/test.py -opt ./options/test/NAFSSR/NAFSSR-S_x4.yml --launcher pytorch
```

# Test
## 1. Prepare test data 
```matlab
run(rename_to_NTIRE.m)
```

## 2. Begin to test
```python
python -m torch.distributed.launch --nproc_per_node=1 --master_port=4321 basicsr/test.py -opt ./options/test/NAFSSR/NAFSSR-S_4x.yml --launcher pytorch
```

