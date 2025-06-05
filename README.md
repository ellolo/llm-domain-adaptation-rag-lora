# cthulhu_fine_tuning



## Fine tuning results

All runs use the following configuration:
- quantization: 4-bit, BitsAndBytes
- LoRA r: 16
- LoRA alpha: 32
- rLoRA: used
- max sequence length: 256


### Runs statistics

| Run id | Model | Parameters | GPU | Time taken | Memory usage (GB) | Google Compute Units | 
| -------- | ------- | -------- | ------- |  -------- | -------- |  -------- |
| 1 | Llama-3.2-1B-Instruct | lr=0.0001 b=64  | A100 40GB | 25m   | NA | NA |
| 2 | Llama-3.2-8B-Instruct | lr=0.0001 b=16  | A100 40GB | 2h25m | pre-trained model: 7.2<BR> Llora adapters: 0.16<BR>training (excl model): 13.8  | 16 |
| 3 | Llama-3.2-8B-Instruct | lr=0.00003 b=32 | A100 40GB | 3h11m | pre-trained model: 7.2<BR> Llora adapters: 0.16<BR>training (excl model): 7.1 | 22 |

### Model evaluation

Evaluation is performed a manually created set of 20 questions related to the manual.\
For each question we evaluate:
- correctness: [0,1]
- readability: [0,5]
