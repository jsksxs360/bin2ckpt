# bin2ckpt

Convert Huggingface Pytorch checkpoint to Tensorflow checkpoint

详细说明可以参见[《将 PyTorch 版 bin 模型转换成 Tensorflow 版 ckpt》](https://xiaosheng.run/2021/04/12/pytorch-model-to-tensorflow-ckpt.html)

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

## Converted Models (ckpt)

- [SpanBERT](https://github.com/facebookresearch/SpanBERT)
  - SpanBERT (base & cased): 12-layer, 768-hidden, 12-heads , 110M parameters
  - SpanBERT (large & cased): 24-layer, 1024-hidden, 16-heads, 340M parameters

  Download: [GoogleDrive](https://drive.google.com/drive/folders/1W8MT99_SvECIaJ2rSthwCraSvM5XkGwH?usp=sharing) | [BaiduDrive](https://pan.baidu.com/s/1-VMYZ7KKxoCveokwIu_27g) (Code: wtyr) | [CTDrive](http://file.xiaosheng.run/d/4096332-43294170-42b59d)

- [SimCSE](https://github.com/princeton-nlp/SimCSE)
  - supervised SimCSE (base & uncased)
  - supervised SimCSE (large & uncased)

  Download: [GoogleDrive](https://drive.google.com/drive/folders/1rDB259UIU2mIq52EfluSHdav1tPt2UQf?usp=sharing) | [BaiduDrive](https://pan.baidu.com/s/139lR2DzkkR35ds1ErrbqyA) (Code: gnq3) | [CTDrive](http://file.xiaosheng.run/d/4096332-43488940-1d8a39)
