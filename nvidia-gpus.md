# GPU Info

```bash
nvidia-smi --query-gpu=timestamp,pstate,temperature.gpu,utilization.gpu,utilization.memory,memory.total,memory.free,memory.used --format=csv -l 1
```

```
timestamp, pstate, temperature.gpu, utilization.gpu [%], utilization.memory [%], memory.total [MiB], memory.free [MiB], memory.used [MiB]
2019/08/23 14:41:50.273, P2, 85, 100 %, 55 %, 10989 MiB, 1048 MiB, 9941 MiB
2019/08/23 14:41:51.274, P2, 85, 100 %, 54 %, 10989 MiB, 1048 MiB, 9941 MiB
2019/08/23 14:41:52.275, P2, 85, 100 %, 55 %, 10989 MiB, 1048 MiB, 9941 MiB
```
https://docs.fast.ai/dev/gpu.html#gpu-monitoring

---
Continuously provide time stamped power and clock

`nvidia-smi --query-gpu=index,timestamp,power.draw,clocks.sm,clocks.mem,clocks.gr --format=csv -l 1`
```
index, timestamp, power.draw [W], clocks.current.sm [MHz], clocks.current.memory [MHz], clocks.current.graphics [MHz]
0, 2019/08/23 14:54:47.307, 208.36 W, 1545 MHz, 6800 MHz, 1545 MHz
0, 2019/08/23 14:54:48.310, 249.62 W, 1560 MHz, 6800 MHz, 1560 MHz
0, 2019/08/23 14:54:49.315, 205.51 W, 1545 MHz, 6800 MHz, 1545 MHz
```
https://nvidia.custhelp.com/app/answers/detail/a_id/3751/~/useful-nvidia-smi-queries

# Multi GPU
## Setting GPUs to Use
```bash
export CUDA_VISIBLE_DEVICES=1
export CUDA_VISIBLE_DEVICES=2,3

# Generic Python
import os; os.environ['CUDA_VISIBLE_DEVICES']='2'

# PyTorch
torch.cuda.set_device(1)
```
https://docs.fast.ai/dev/gpu.html#multi-gpu
