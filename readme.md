https://stackoverflow.com/questions/37893755/tensorflow-set-cuda-visible-devices-within-jupyter

```
import os
os.environ["CUDA_DEVICE_ORDER"]="PCI_BUS_ID"   # see issue #152
os.environ["CUDA_VISIBLE_DEVICES"]="1"
import torch
print(torch.__version__)
import timm
from tqdm import tqdm
current_device = torch.cuda.current_device()
# Get the name of the GPU
gpu_name = torch.cuda.get_device_name(current_device)
print(f"Current CUDA device: {current_device}")
print(f"GPU name: {gpu_name}")
```

