# README

This is a repository for recording techniques that can speed up your training in pytorch.

Includes some tricks and demos.

I sincerely hope that you will submit pull requests


## `torch.compile()`

[https://pytorch.org/docs/stable/generated/torch.compile.html#torch-compile](https://pytorch.org/docs/stable/generated/torch.compile.html#torch-compile)

```python
model = GPT()
model = torch.nn.compile(model)
```

`torch.compile()` need the torch's version >= 2.0

Torch.compile is the python equivalent of gcc for c++. 
A model running in torch.compile can speed things up significantly. 
The acceleration comes mainly from reduced Python overhead and GPU read/write


# Reference

- [nanoGPT](https://github.com/karpathy/nanoGPT)
- [pytorch 提速指南（持续更新）](https://zhuanlan.zhihu.com/p/119364172)