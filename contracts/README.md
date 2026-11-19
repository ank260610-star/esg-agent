# 共享接口约定 v0.1

以[实现交接文档第2—3节](../docs/superpowers/plans/2026-11-19-esg-agent-implementation.md)为基线。此目录里的JSON是模拟数据，不是API实现或真实模型提取结果。

工具清单：parse_report、search_evidence、get_rulebook、save_metric_candidates、validate_metrics、compare_years、save_check_proposals、calculate_score、get_task_results、export_analysis。

统一返回字段：ok、data、error、task_id、revision。数值用十进制字符串，缺失用null；PDF物理页从1开始，印刷页单独存。后端生成ID并验证所属任务；错误需code/message/retryable。用户上传和人工复核不开放为Agent工具。

修改接口时在同一PR更新说明、模拟结果和相关测试，并让另一端成员检查。尚未实现的接口明确标记，不自行宣称可调用。

第一轮联调：检索原文→模型整理候选→提交校验→读取结果。示例见examples/search-evidence.mock.json和examples/error.mock.json。
