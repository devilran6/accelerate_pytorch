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

Important: `torch.compile()` need the torch's version >= 2.0

Torch.compile is the python equivalent of gcc for c++. 
A model running in torch.compile can speed things up significantly. 
The acceleration comes mainly from reduced Python overhead and GPU read/write

## Gradient Checkpoint

[https://pytorch.org/docs/stable/checkpoint.html](https://pytorch.org/docs/stable/checkpoint.html)

```python
model = nn.Sequential(...)
input_var = checkpoint_sequential(model, chunks, input_var)
```

Time => GPU memory

Try this to "slow down" when you speed up too much to run out of memory.

# Reference

- [nanoGPT](https://github.com/karpathy/nanoGPT)
- [pytorch 提速指南（持续更新）](https://zhuanlan.zhihu.com/p/119364172)