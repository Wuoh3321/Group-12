# 数据集说明
## 1. 基础信息
数据源：Web of Science Core Collection
检索配置：参考 ../config/query.yaml (v0.3-final)
检索执行时间：2026-XX-XX
时间范围：2020 - 2026年
文献类型：Article、Review Article
语言：英文

## 2. 数据存放
原始数据：./raw/ （WoS原始导出文件）
清洗数据：./processed/ （去重、筛选后标准化数据）

## 3. 数据规模
原始文献总数：XXX 条
清洗后有效文献：XXX 条
去重率：XX%

## 4. 核心保留字段
标题、作者、作者机构、关键词、摘要、参考文献、DOI、发表年份、期刊名称

## 5. 补充说明
数据清洗规则详见 ../docs/cleaning_rules.md
文献筛选流程详见 ../reports/screening_rules.md
