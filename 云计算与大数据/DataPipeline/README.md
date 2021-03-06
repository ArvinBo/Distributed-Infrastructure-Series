# DataPipeline 实时数据集成平台

数据源变化捕获是数据集成的起点，结合日志的解析、增量条件查询模式和数据源主动 Push 模式，最终构建出一个数据汇集层。在这个阶段，推荐考虑 Kafka Connect 这类面向数据集成的专有框架，可以有效缩短研发周期和成本。

数据汇集层建议构建在消息队列之上，为后继的加工处理提供便利。如果需要全量持久化长期保存，建议结合使用消息队列和分布式文件系统分别做实时数据和全量数据的存储。

流式处理能力是实时数据集成平台必要的组件。结合企业技术栈特点，选用包括 Flink、Spark Streaming、Kafka Streams 等流行的引擎在多数情况下都能够满足要求。

端到端数据的 EOS 是数据集成中的一个难题，需要用户根据业务实际需求、数据本身的特性、目的地特点 case by case 去解决。
