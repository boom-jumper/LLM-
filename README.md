# prompt engineering

## GPT原理
> 基于已有的token，去预测下一个token的概率分布

## prompt
> 包含传递到模型的指令或问题等信息，也可以包含其他详细数据，如上下文、输入或者示例

## temperature
> 1. temperature的参数值越小，模型返回越稳定。
> 2. 如果调高该参数值，模型返回更随机，会带来更多样化或更具创造性的产出。
> 3. 实际应用，如质量保障需要设置更低的temperature，保证输出更真实；如创造性任务，可适度调高temperature。

## top_p
1. top_p的工作方式：按照概念分布对所有的token排序，挑选出`累计概率`[token的累计概念](images/token的累积概念.png)大于设定阈值p的最小token集合，并从中随机选择一个作为输出。
2. top_p与temperature一起称为核采样(nucleus sampling)技术。
3. top_k的数量是固定的，top_p的数量是不固定的
4. top_p的值越小，模型返回越稳定。

## max length
> 调整max_length可控制LLM生成的token数，避免生成冗长或不相关的文本。

## frequency penalty
> penalty与token的频率成比例，penalty越高，token再次出现的概率越低。


