# ESG业务后端

负责PDF登记解析、逐页证据索引、结构化指标校验、跨年确定性计算、自建评分、复核和导出。当前只有目录骨架。

建议Python代码位于backend/src/esg_app，依赖和安装配置在根目录pyproject.toml。原实施方案中的src/esg_app映射到本目录；根目录tests和rules保持不变。接手实现时同步包发现配置，不并行创建两套后端。

先与插件成员确认contracts中的字段，然后实现search_evidence与指标校验。模型负责候选与解释，后端不能相信任意证据ID、分数或人工确认状态。
