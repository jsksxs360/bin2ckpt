# bin2ckpt

Convert Huggingface Pytorch checkpoint to Tensorflow checkpoint

详细说明可以参见[《将 PyTorch 版 bin 模型转换成 Tensorflow 版 ckpt》](https://xiaosheng.run/2021/04/12/article186/)

## Environment

- torch
- tensorflow
- transformers

## Usage

```python
bin_path = './pretrained_model/pytorch_model/'
bin_model = 'pytorch_model.bin'
ckpt_path = './pretrained_model/tensorflow_model/'
ckpt_model = 'bert_model.ckpt'

convert(bin_path, bin_model, ckpt_path, ckpt_model)
```

- **bin_path**: pytorch model path
- **bin_model**: pytorch model name
- **ckpt_path**: path to save tf ckpt
- **ckpt_model**: tf ckpt name

**Notice**: this script only supports to convert the BERT model. If you need to convert other models, please modify the function `to_tf_var_name()` and variable `tensors_to_transpose`.
