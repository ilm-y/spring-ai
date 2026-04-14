Phase 1：Week 1（4.14-4.21）- 学习Spring AI官方examples
学习目标
Code
完成后，你应该能：
  ✅ 理解ChatClient是什么（最简单的方式调用LLM）
  ✅ 理解ChatModel、EmbeddingModel、VectorStore的概念
  ✅ 能跑通官方的一个完整RAG example
  ✅ 理解RAG的5个核心步骤（分块→Embedding→存储→检索→生成）
  ✅ 能改官方代码的参数，看效果变化
  ✅ 不要求：理解源码，理解Spring AI内部实现
具体任务
Day 1-2（4.14-4.15，周一二）：查找 + 理解官方documentation

Code
任务：在网页上看Spring AI官方文档（不用Clone）

步骤1：打开Spring AI官方文档
  https://docs.spring.io/spring-ai/reference/
  
步骤2：找到这些部分并快速浏览（不需要深入）
  [ ] Introduction（了解Spring AI是什么）
  [ ] Getting Started（了解基本用法）
  [ ] ChatClient（最关键，要理解）
  [ ] Embedding Models（理解Embedding怎么用）
  [ ] Vector Stores（理解向量库怎么用）

步骤3：找官方的RAG相关文档
  搜索文档中的"RAG"或"Retrieval"关键字
  找到RAG的章节，快速读一遍（了解大概）

学习方式：
  ✅ 边看文档边记笔记（用Markdown或纸笔）
  ✅ 记录"什么是ChatClient"、"什么是VectorStore"等概念
  ✅ 画一个流程图："Spring AI怎么工作"

时间：2-3小时
Day 3-5（4.16-4.18，周三到周五）：找 + 运行官方examples

Code
任务：找到Spring AI官方的代码示例，在本地跑起来

步骤1：找官方examples（有两个方式）
  方式A（推荐）：
    - 打开GitHub：https://github.com/spring-projects/spring-ai
    - 在网页上（不Clone）找到examples文件夹
    - 看有哪些examples（点进去看README）
  
  方式B（如果网络好）：
    - Clone官方项目的一个小example
    - git clone --depth=1 --filter=blob:none --sparse https://github.com/spring-projects/spring-ai.git
    - cd spring-ai
    - git sparse-checkout set spring-ai-examples
  
  如果都失败，就直接网页看代码

步骤2：选择最简单的example
  通常叫 "simple-chat" 或 "basic-chatclient"
  这个应该是最简单的例子，就是调用LLM回���问题

步骤3：复制这个example的代码到本地
  （不是Clone，而是手动复制关键代码）
  
  核心文件应该有：
    - pom.xml（Maven配置，看依赖是什么）
    - application.yml（配置OpenAI API key等）
    - ChatService.java（或类似的服务类）
    - 一个main方法或Spring Boot Application

步骤4：在你的环境里运行
  [ ] 创建一个新的Spring Boot项目
  [ ] 加入Spring AI的依赖（从pom.xml复制）
  [ ] 复制代码（ChatService等）
  [ ] 创建application.yml，配置API key
  [ ] 运行程序
  [ ] 看能否得到LLM的回答

步骤5：如果成功，改一个参数看效果
  比如：改system prompt，看回答有什么不同
  比如：改model名称（如果支持多个模型）

时间：3天
Day 6-7（4.19-4.21，周六日）：理解 + 总结

Code
任务：总结Week 1的学习，为Week 2做准备

步骤1：画一个"Spring AI RAG流程图"
  输入：用户提问
  ↓
  处理：Spring AI怎么调用LLM
  ↓
  输出：LLM的回答

步骤2：找一个官方的RAG example
  （比simple-chat更复杂）
  包含：文档上传 → Embedding → 向量库 → 检索 → 生成
  
  跑通这个example

步骤3：理解RAG的5个步骤
  写下来，每个步骤一句话解释：
  1. 文本分块（Chunking）：
     为什么要分块？因为...
  
  2. Embedding（向量化）：
     为什么要向量化？因为...
  
  3. 向量存储（Vector Store）：
     为什么要存向量？因为...
  
  4. 检索（Retrieval）：
     怎么检索最相关的文档？用...
  
  5. 生成（Generation）：
     怎么用检索出的文档 + 用户提问生成回答？用...

步骤4：列出"我现在清楚的" 和 "我还不明白的"
  清楚的：ChatClient、VectorStore、RAG流程...
  不明白的：Embedding模型怎么选、怎么优化检索精度...

时间：1-2天

产出：
  ✅ 运行过的Spring AI examples（至少2个）
  ✅ 理解了RAG的完整流程
  ✅ 一张流程图 + 学习笔记
  ✅ 清楚了Week 2要做什么
Week 1的验收标准
Code
✅ 你能用Spring AI写一个最简单的程序：接收用户输入 → 调用LLM → 返回回答
✅ 你能解释"什么是RAG"（用自己的语言，不是背概念）
✅ 你理解了"分块、Embedding、检索、生成"这4个步骤
✅ 你知道官方examples在哪里、大概怎么用
❌ 你不需要：理解Spring AI的源码，理解所有的配置选项，精通所有的框架API
Phase 2：Week 2-4（4.22-5.12）- 自己搭一个"完整的问答系统"
学习目标
Code
完成后，你应该能：
  ✅ 从零创建一个Spring Boot项目，集成Spring AI
  ✅ 自己写代码实现"上传文件 → 分块 → Embedding → 存向量库"
  ✅ 自己写代码实现"提问 → 检索 → LLM生成答案"
  ✅ 用Vue或React写一个简单的前端
  ✅ 用Docker打包，能部署到云或本地server
  ✅ 写一篇600字的技术博客讲"我怎么做的"
  ✅ ���讲15分钟说清楚"这个项目的架构和核心难点"
  ❌ 不需要：看参考项目，看别人怎么做
Week 2（4.22-4.28）：FAQ机器人 - 后端开发
任务：从零写一个Spring Boot应用，实现RAG的核心逻辑

Code
项目需求（最简版本）：
  1. 用户上传一个FAQ文本文件
  2. 系统自动分块、Embedding、存入向量库
  3. 用户提问
  4. 系统检索相关文档，用LLM生成回答

技术栈：
  - Spring Boot 3.x
  - Spring AI（ChatClient、EmbeddingModel、VectorStore）
  - 向量库：Chroma或PgVector（简单，本地）
  - 数据库：MySQL或H2（存元数据）

Day 1-2（4.22-4.23）：项目骨架 + 依赖配置

[ ] 创建Spring Boot项目
    mvn archetype:generate -DgroupId=com.faq -DartifactId=faq-bot

[ ] 加入依赖（pom.xml）
    ```xml
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    
    <dependency>
        <groupId>org.springframework.ai</groupId>
        <artifactId>spring-ai-openai-spring-boot-starter</artifactId>
    </dependency>
    
    <dependency>
        <groupId>org.springframework.ai</groupId>
        <artifactId>spring-ai-chroma-store-spring-boot-starter</artifactId>
    </dependency>
    ```

[ ] 配置application.yml
    ```yaml
    spring:
      application:
        name: faq-bot
      ai:
        openai:
          api-key: ${OPENAI_API_KEY}
          model: gpt-3.5-turbo
    
    server:
      port: 8080
    ```

[ ] 建立项目结构
    src/main/java/com/faq/
      ├── FaqBotApplication.java
      ├── controller/
      │   └── DocumentController.java
      │   └── QAController.java
      ├── service/
      │   └── DocumentService.java
      │   └── QAService.java
      └── model/
          └── Document.java

[ ] 写一个测试接口，确保Spring Boot能启动
    @RestController
    @RequestMapping("/api/health")
    public class HealthController {
        @GetMapping
        public String health() {
            return "OK";
        }
    }

时间：4小时

产出：
  ✅ Spring Boot项目能启动
  ✅ Spring AI依赖配置好
  ✅ 项目结构清晰
Day 3-4（4.24-4.25）：实现文档上传 + 分块 + Embedding

Code
核心逻辑：文件上传 → 读取内容 → 分块 → Embedding → 存向量库

[ ] 实现DocumentService（核心服务）
    
    @Service
    public class DocumentService {
        private VectorStore vectorStore;
        private EmbeddingModel embeddingModel;
        
        public void uploadDocument(MultipartFile file) throws IOException {
            // Step 1：读取文件内容
            String content = new String(file.getBytes());
            
            // Step 2：分块（这是关键！）
            List<String> chunks = chunkText(content);
            
            // Step 3：转换为Spring AI的Document对象
            List<Document> documents = chunks.stream()
                .map(chunk -> new Document(chunk))
                .collect(Collectors.toList());
            
            // Step 4：存向量库
            vectorStore.add(documents);
        }
        
        // 分块函数（简单版本）
        private List<String> chunkText(String text) {
            List<String> chunks = new ArrayList<>();
            int chunkSize = 1000;
            int overlap = 100;
            
            for (int i = 0; i < text.length(); i += (chunkSize - overlap)) {
                int end = Math.min(i + chunkSize, text.length());
                chunks.add(text.substring(i, end));
            }
            return chunks;
        }
    }

[ ] 实现DocumentController（接收上传请求）
    
    @RestController
    @RequestMapping("/api/documents")
    public class DocumentController {
        @Autowired
        private DocumentService documentService;
        
        @PostMapping("/upload")
        public ResponseEntity<String> upload(@RequestParam MultipartFile file) {
            try {
                documentService.uploadDocument(file);
                return ResponseEntity.ok("Document uploaded and indexed");
            } catch (IOException e) {
                return ResponseEntity.badRequest().body(e.getMessage());
            }
        }
    }

[ ] 测试上传功能
    用PostMan或curl测试：
    curl -F "file=@test.txt" http://localhost:8080/api/documents/upload

时间：8小时（包括理解、写代码、测试、debug）

产出：
  ✅ 能上传文本文件
  ✅ 文件被自动分块
  ✅ 分块被存入向量库
  ✅ 理解了"分块"和"Embedding"在代码中怎么实现
Day 5-6（4.26-4.27）：实现提问 + 检索 + 回答

Code
核心逻辑：用户提问 → 向量库检索 → LLM生成答案

[ ] 实现QAService（核心服务）
    
    @Service
    public class QAService {
        private ChatClient chatClient;
        private VectorStore vectorStore;
        
        public String askQuestion(String question) {
            // Step 1：从向量库检索相关文档
            List<Document> relevantDocs = vectorStore.similaritySearch(question);
            
            // Step 2：组织Prompt
            String context = relevantDocs.stream()
                .map(Document::getContent)
                .collect(Collectors.joining("\n\n"));
            
            String prompt = "根据以下信息回答问题：\n\n" + context + 
                          "\n\n问题：" + question;
            
            // Step 3：调用LLM生成答案
            return chatClient.prompt()
                .user(prompt)
                .call()
                .content();
        }
    }

[ ] 实现QAController（接收提问请求）
    
    @RestController
    @RequestMapping("/api/qa")
    public class QAController {
        @Autowired
        private QAService qaService;
        
        @PostMapping("/ask")
        public ResponseEntity<String> ask(@RequestBody QARequest request) {
            String answer = qaService.askQuestion(request.getQuestion());
            return ResponseEntity.ok(answer);
        }
    }
    
    class QARequest {
        private String question;
        // getter and setter
    }

[ ] 测试问答功能
    curl -X POST http://localhost:8080/api/qa/ask \
         -H "Content-Type: application/json" \
         -d '{"question":"什么是常见问题？"}'

时间：8小时

产出：
  ✅ 能提问并得到回答
  ✅ 回答是基于上传的文档（RAG工作了！）
  ✅ 理解了"检索"和"生成"怎么工作
Day 7（4.28）：整理 + Git提交

Code
[ ] 代码清理
    - 加注释
    - 加logger
    - 加异常处理
    - 改变量名字

[ ] 写README
    # FAQ机器人
    
    ## 功能
    - 上传FAQ文档
    - 自动建立知识库
    - 用户提问，自动回答
    
    ## 如何运行
    1. git clone ...
    2. 配置application.yml（填入OpenAI API Key）
    3. mvn spring-boot:run
    4. 访问 http://localhost:8080
    
    ## 技术栈
    - Spring Boot 3.x
    - Spring AI
    - Chroma（向量库）
    
    ## API
    - POST /api/documents/upload：上传文档
    - POST /api/qa/ask：提问

[ ] Git提交
    git add .
    git commit -m "Complete FAQ backend with RAG"

时间：2小时

产出：
  ✅ 完整的、有文档的Spring Boot项目
  ✅ 可以提交到GitHub
周验收标准（Week 2）
Code
✅ FAQ机器人的后端完全工作（上传 → 提问 → 回答的完整流程）
✅ 代码质量好（有注释、有异常处理、有README）
✅ 理解了Spring AI的核心用法（ChatClient、VectorStore、EmbeddingModel）
✅ 能讲清楚"我怎么实现分块、Embedding、检索、生成的"
❌ 前端还没做（放在Week 3）
❌ 没看参考项目（还没到那一步）
Week 3（4.29-5.5）：FAQ机器人 - 前端 + 部署
Code
Day 1-3（4.29-5.1）：前端开发
  [ ] 选择前端框架（Vue3或React，你选一个）
  [ ] 写一个简单的UI
      - 文件上传区域
      - 问题输入框
      - 回答显示区域
  [ ] 调用后端API
  [ ] 本地测试前后端联调

Day 4-5（5.2-5.3）：部署
  [ ] Docker打包
  [ ] 部署到云（可选）或本地server获得一个URL

Day 6-7（5.4-5.5）：博客 + GitHub
  [ ] 写第一篇技术博客（600字）
      标题："我用Java + Spring AI做了一个FAQ机器人"
      
      内容：
      1. 项目背景（为什么做这个项目）
      2. 技术选择（为什么选Java+Spring AI而不是Python？）
      3. 核心实现（分块、Embedding、检索、生成各1段）
      4. 遇到的问题（至少提1个技术难点和解决方案）
      5. 学习收获（通过这个项目学到了什么）
      6. 未来改进（怎么优化）
  
  [ ] Push到GitHub
  [ ] 博客发布到掘金或个人博客

产出：
  ✅ 完整的FAQ机器人（前后端 + UI）
  ✅ 可以运行的demo（本地或云端链接）
  ✅ GitHub repo + 完整README
  ✅ 第一篇高质量技术博客（发布到掘金等）
  ✅ 能用15分钟讲清楚这个项目
Week 4（5.6-5.12）：医疗问诊系统 - Phase 1
Code
这是FAQ项目的"升级版"，主要是改知识库和Prompt

Day 1-2（5.6-5.7）：需求分析 + 医学数据准备
  [ ] 确定系统需求
      - 接收患者症状描述
      - 查询医学知识库
      - 给出初步医学建议
      - 强调"这不是诊断，请咨询医生"
  
  [ ] 准备医学知识库
      方式1：从医学网站爬取（需要许可）
      方式2：用开源医学数据集
      方式3：手动编写一些常见疾病信息
      
      内容应该包括：症状、可能的疾病、建议等

Day 3-5（5.8-5.10）：后端实现
  [ ] 照着FAQ的代码改（知识库换成医学内容）
  [ ] 改进Prompt（医疗专用）
      医疗Prompt应该：
      - 明确身份（医学助手，不是医生）
      - 基于知识库（根据以下信息...）
      - 有免责声明（这不是诊断...）
      - 给出建议（建议用户...）
  
  [ ] 测试系统
      输入：发烧、咳嗽
      输出：应该基于知识库给出合理的建议

Day 6-7（5.11-5.12）：前端 + 优化
  [ ] 改造前端（医疗主题，不用太复杂）
  [ ] 部署

产出：
  ✅ 医疗问诊系统的初版（后端工作）
  ✅ 准备Week 5继续优化和深化

🎯 每个阶段学到什么程度
Phase 1（Week 1）学到的程度
Code
能做到：
  ✅ 解释"什么是ChatClient"
  ✅ 解释"什么是RAG"
  ✅ 跑通一个官方的RAG example
  ✅ 改官方代码的参数，看效果
  
能讲出来：
  ✅ RAG有5个步骤，分别是...
  ✅ Embedding是把文字转成...
  ✅ 向量库是用来...
  
不需要：
  ❌ 理解Spring AI的源码
  ❌ 精通所有的框架API
  ❌ 能自己设计RAG系统的架构
Phase 2（Week 2-4）学到的程度
Code
能做到：
  ✅ 从零创建Spring Boot项目 + 集成Spring AI
  ✅ 自己写代码实现分块、Embedding、存向量库
  ✅ 自己写代码实现检索和生成
  ✅ 写一个完整的REST API
  ✅ 写一个简单的前端
  ✅ 部署项目到云或本地
  
能讲出来：
  ✅ 我怎么实现分块的，为什么这样分块
  ✅ 我怎么选择Embedding模型的
  ✅ 我怎么优化检索精度的
  ✅ 我遇到了什么问题，怎么解决的
  ✅ 这个项目的优点和缺点是什么
  
写得出来：
  ✅ 高质量的技术博客（讲清楚核心实现）
  
不需要：
  ❌ 理解参考项目
  ❌ 学习最佳实践
  ❌ 优化到完美




📋 总结：你现在要做的（这一周）
Code
4月14-4.21（Week 1）：

Day 1-2（4.14-4.15）：
  [ ] 打开Spring AI官方文档网页
  [ ] 快速浏览Introduction + Getting Started + ChatClient部分
  [ ] 记笔记："什么是ChatClient""什么是RAG"
  [ ] 时间：2-3小时

Day 3-5（4.16-4.18）：
  [ ] 在GitHub网页上找官方的简单example（不Clone）
  [ ] 手动复制代码到本地
  [ ] 运行起来
  [ ] 改参数，看效果
  [ ] 时间：6-8小时

Day 6-7（4.19-4.21）：
  [ ] 画流程图："Spring AI RAG怎么工作"
  [ ] 理解5个步骤
  [ ] 跑官方的RAG example
  [ ] 整理笔记
  [ ] 时间：4-6小时

产出：
  ✅ 理解了Spring AI基础
  ✅ 跑通了官方examples
  ✅ 清楚了Week 2要做什么

然后进入Week 2，开始自己写FAQ项目（不看任何参考项目）
