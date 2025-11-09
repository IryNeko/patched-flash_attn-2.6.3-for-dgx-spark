# patched-flash_attn-2.8.3-for-dgx-spark
precompiled flash_attn wheel for dgx spark, arm archtecture

** DO NOT USE IT ON JETSON, YOU MAY BREAK IT **

system:
DGX spark GB10 sm201
using torch 2.9.0, cp312, cu130:
https://download.pytorch.org/whl/cu130/torch-2.9.0%2Bcu130-cp312-cp312-manylinux_2_28_aarch64.whl.metadata

modified the flash_attn 2.8.3, adjusted setup.py to add sm_121 to use the 80 set of instructions, so it works on gb10
no longer a workaround, it works now

if you think I want to mine some crypto with your machine, then do it yourself, 
make the changes base on my post then compile them from source
https://github.com/Dao-AILab/flash-attention/issues/1969

tested on wan 2.2 it works

<img width="808" height="384" alt="QQ_1762153070869" src="https://github.com/user-attachments/assets/5e5bb515-b400-45ed-9674-98a56766fead" />

If you have any questions, feel free to post them as issues, I would help. 

Also included the arm64 decord package, well, this is also needed for wan2.2, compiled from source, in case you are also trying wan2.2<br>
if you are not using wan2.2, you don't need that decord wheel
