Day1～Day2：吃透官方文档（不是浏览，是精读 + 总结）
必看页面
https://docs.spring.io/spring-ai/reference/
只看这 5 块，其他暂时跳过：
Introduction
Getting Started
ChatClient
Embedding Models
Vector Stores
必须输出（不输出 = 白看）
一页纸核心笔记（手写 / Markdown 都行）
ChatClient 是什么、用来干嘛
ChatModel vs ChatClient 区别
EmbeddingModel 作用
VectorStore 作用
为什么要用 VectorStore 而不是直接存文本
一张架构简图
plaintext
用户请求 → Controller → Service → ChatClient → ChatModel → LLM API → 返回结果
3 个必须搞懂的问题
Spring AI 帮我们解决了什么麻烦？
不用 Spring AI 直接调 OpenAI 行不行？
RAG 在 Spring AI 里大致分成哪几步？
极致要求
合上书，能对着空气讲 3 分钟
不懂的词全部查清楚，不模糊放过
