## Day1～Day2：吃透官方文档（不是浏览，是精读 + 总结）
必看页面(https://docs.spring.io/spring-ai/reference/)：
  只看这 5 块，其他暂时跳过：
    Introduction
    Getting Started
    ChatClient
    Embedding Models
    Vector Stores

必须输出（不输出 = 白看）：
  一页纸核心笔记（手写 / Markdown 都行）
    ChatClient 是什么、用来干嘛
    ChatModel vs ChatClient 区别
    EmbeddingModel 作用
    VectorStore 作用
    为什么要用 VectorStore 而不是直接存文本
    
  一张架构简图：
    用户请求 → Controller → Service → ChatClient → ChatModel → LLM API → 返回结果
    
3 个必须搞懂的问题：
  Spring AI 帮我们解决了什么麻烦？
  不用 Spring AI 直接调 OpenAI 行不行？
  RAG 在 Spring AI 里大致分成哪几步？
  
极致要求：
  合上书，能对着空气讲 3 分钟
  不懂的词全部查清楚，不模糊放过


## 基本情况
学年：大二下（现在4月14号）
目标终点：秋招（2025年9月）找到AI工程师的工作

时间节点：
  📅 4月14-6月30：2.5个月自由学习（最关键）
  📅 7月1-20：期末复习
  📅 7月20-8月31：腾讯Mini项目 + 等待
  📅 9月中旬：投递实习
  📅 11月-12月：秋招笔试面试
  📅 明年2-6月：大三下实习

技术基础：
  ✅ Java：会Spring Boot + MyBatis + MySQL（能对着敲，不能独立设计）
  ✅ 前端：会ArkTS，能快速学Vue/React
  ✅ Linux/Docker：有基础
  ✅ 算法：每天刷1道Leetcode（有纪律）
  ❌ 不会：系统设计、缓存、分布式等进阶内容
  ❌ 不清楚：怎么用Java做AI应用

网络环境：
  ⚠️ Clone大项目经常失败
  ✅ GitHub网页可以看
  ✅ 官方文档网页可以访问

选择方向：**Java + Spring AI**（不学Python）
  原因：避免"两套系统"，利用已有的Java基础，在Java中嵌入AI能力
  目标：成为"懂AI的Java工程师"（市场稀缺）
## 学习目标
到秋招时（9月中旬），你应该达到的状态：

1️⃣ 项目经历
   ✅ 3个完整的、有GitHub repo的、可以demo的Java + AI项目
     - FAQ机器人（简单）
     - 医疗问诊系统（中等）
     - Mini项目或第三个项目（复杂）
   ✅ 每个项目都有完整README和部署说明
   ✅ 代码质量好（有注释、有测试、有文档）

2️⃣ 技术深度
   ✅ 理解Spring AI怎么工作（不是源码，是API用法）
   ✅ 理解RAG的完整流程（分块、Embedding、检索、生成）
   ✅ 能用代码实现一个完整的RAG系统
   ✅ 理解系统设计的基础概念（缓存、数据库优化等）

3️⃣ 算法能力
   ✅ LeetCode 100道中等题目

4️⃣ 表达能力
   ✅ 能讲清楚"为什么选Java+Spring AI而不是Python"
   ✅ 能讲清楚"我的项目怎么做的，遇到什么问题，怎么解决的"
   ✅ 4-5篇高质量技术博客

5️⃣ 大厂背书（加分项）
   ✅ 腾讯Mini项目的参赛经历
## 学习进度
Spring AI的学习：
  ❌ 还没开始

RAG的理解：
  ⚠️ 知道概念，没有实战过

Java后端能力：
  ⭐⭐⭐ 中等（能对着敲，不能独立设计）

项目经历：
  ⭐⭐ 一个错题本项目（照着做的）

技术博客：
  ❌ 还没写过

算法刷题：
  ⭐⭐⭐ 开始积累（每天刷1道，但还没有明确的计划到100道）

总体：
  你有基础，但没有"AI工程"的实战经验
  需要通过这2.5个月（4月-6月）快速积累3个项目和写作能力
