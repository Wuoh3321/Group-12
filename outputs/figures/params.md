# 计量图谱基线参数文档（匹配 outputs 全部图表）
## 基础信息
数据源：Web of Science Core Collection
检索配置：config/query.yaml v0.3-final
分析工具：VOSviewer 1.6.20

## 1. 作者合作网络（author_collaboration.png）
1. 数据来源：tables/Author_Collaboration/vos_output_author_collaboration_v0.3.csv
2. 筛选阈值：最低合作频次 ≥2
3. 网络构建：以作者为节点、合作发文次数为边权重
4. 可视化设置：节点大小=总发文量，连线粗细=合作频次，Louvain聚类着色
5. 输出指标文件：nodes_v0.2.csv（作者发文量、中心性）、edges_v0.2.csv（合作强度）

## 2. 关键词共现网络（keyword_cooccurrence.png）
1. 数据来源：tables/Keywords_Cooccurrence/vos_output_keyword_cooccurrence_v0.3.csv
2. 筛选阈值：关键词共现最低频次 ≥3
3. 网络构建：关键词为节点、共同出现文献数为边权重
4. 可视化设置：节点大小=出现频次，聚类区分五大医学AI细分方向
5. 配套指标：network_metrics_keyword_v0.3.csv（中介中心性、突现频次、模块度）

## 3. 文献共被引网络 co_citation.png
1. 阈值：最低共被引次数 ≥5
2. 节点：高被引里程碑文献，节点大小=总被引频次
3. 用途：梳理领域经典知识基础、奠基文献集群

## 4. 文献耦合网络 bibliographic_coupling.png
1. 阈值：耦合关联强度 ≥4
2. 节点：前沿研究文献，耦合度越高代表研究主题越相近
3. 用途：识别近年新兴研究热点集群

## 通用质控说明
network_qc_summary_v0.3.txt：记录网络模块度Q值、平均聚类系数，所有图谱Q>0.3，聚类结果具备统计学有效性
