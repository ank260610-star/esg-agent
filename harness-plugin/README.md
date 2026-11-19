# Harness工具插件与智能体

负责官方DeepSeek Harness接入、工具注册、后端客户端和智能体编排。当前只有提示词与文档，尚无插件代码。

- 系统提示词：[prompts/esg-agent.md](prompts/esg-agent.md)
- 使用说明：[智能体提示词使用说明](../docs/prompts/智能体提示词使用说明.md)
- 工具契约：[contracts](../contracts/README.md)

先用明确标记的模拟结果验证工具调用流程；真实接入后替换模拟返回，禁止以模拟运行宣称业务已实现。官方运行版本、加载配置和模型ID要记录并锁定。
