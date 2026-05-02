prompt 教模型做什么
context给模型信息
agent：动态prompt ➕ 自动管理context


prompt 技巧：
	思维链：要求模型一步步给出思考过程
	给出范例，包含数据
	角色表演
context engineering：
	token限制：
		rag 先检索材料
		窗口压缩

prompt稳定性问题：
	自动化优化（不稳定
	强制逐步思考，并同时使用不同路径解答并使用最优回答
	重排输入的prompt，将最关键信息放在开头或结尾
	自反思：先让模型判断rag检索是否有效
