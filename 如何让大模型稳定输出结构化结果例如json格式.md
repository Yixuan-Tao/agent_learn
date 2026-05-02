1. 提示词控制：
	1. 给出标准结构和样例数据并放在最后部分提示词防止中间遗忘
2. api原生约束：
	1. json mode
	2. structure output
3. 推理引擎文法：
	1. logit masking
	2. 推理时就屏蔽不符合语法的token概率
4. 工程校验和自修复
	1. pydantic 校验
		1. 数据模型拦截非法字符
	2. retry
		1. 捕获校验错误，反馈给模型并重试