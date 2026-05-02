原因：
	每个token都和其他所有token交互：
		复杂度为O（n^2)
			计算瓶颈
			显存瓶颈（kv cache过多）
			超过模型训练长度
解决方案：
	Flashattention
		更多在ram中进行计算防止爆显存
	GQA
		kv cache 压缩，多头同时使用一组key和value
	pageattention
		将kv cache放在非连续的内存中
	通过插值法等使模型认为长文本在训练长度内

总结：
	长文本处理变慢的原因是O(n^2)的复杂度和IO瓶颈