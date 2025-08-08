# OptAPI
OptAPI is an LLM-driven intelligent agent framework designed to transform natural language problem descriptions into structured optimization models and automatically solve them using state-of-the-art Operations Research (OR) techniques. 

OptAPI 是一个 LLM 驱动的智能代理框架， 旨在将自然语言问题描述转换为结构化优化模型 ，并使用最先进的运筹学（OR）技术自动解决这些问题。

## 1. **数学与运筹优化基础**

### 核心内容

* **线性代数基础**

  * 向量、矩阵运算（加减乘、转置、逆、秩）
  * 特殊矩阵（对称矩阵、稀疏矩阵）
* **微积分基础**

  * 函数的极限、导数、梯度（用于理解最优化）
* **优化理论基础**

  * 线性规划（LP）问题的标准形式
  * 整数规划（IP/MILP）的概念
  * 约束、目标函数、可行域
  * 对偶理论（primal-dual）、KKT条件（了解即可）
* **经典运筹问题**

  * 运输问题、背包问题
  * 车辆路径问题（VRP）
  * 作业车间调度（Job Shop Scheduling）
  * 网络流（最大流、最小费用流）
* **基本算法**

  * 单纯形法（理解思路即可）
  * 分支定界法（Branch & Bound）
  * 启发式算法简介（贪心、局部搜索）

### 推荐教材与课程

* 书籍：《运筹学》（哈姆迪·塔哈，中文第3版）
* 线上课程：MIT OpenCourseWare - [Introduction to Operations Research](https://ocw.mit.edu/courses/sloan-school-of-management/15-053-optimization-methods-in-management-science-spring-2013/)
* 线性代数：3Blue1Brown《Essence of Linear Algebra》视频系列
* 优化入门：Stanford CS 97SI 《Convex Optimization I》视频课（听概念即可）

---

## 2. **编程与软件工程基础**

### 核心内容

* **Python 基础**

  * 语法（变量、数据结构：列表、字典、元组）
  * 函数、类和模块化编程
  * 异常处理
* **第三方库使用**

  * Pyomo（建模库）、OR-Tools（求解工具）
  * Requests、FastAPI（HTTP 接口开发）
* **版本控制**

  * Git 基础命令（clone, commit, push, pull, branch, merge）
  * GitHub 仓库操作
* **虚拟环境**

  * 使用 venv 或 conda 管理 Python 依赖
* **测试和调试**

  * unittest/pytest 基础单元测试
  * 调试技巧（断点、打印日志）
* **基础数据结构与算法**

  * 排序算法、查找算法
  * 递归、迭代
  * 简单图论知识（邻接表/邻接矩阵）

### 推荐资源

* 《Python 编程快速上手——让繁琐工作自动化》（Al Sweigart）
* Codecademy / LeetCode Python 练习（算法入门）
* FastAPI 官方文档和教程
* Pyomo 官方教程和示例

---

## 3. **人工智能与大语言模型基础**

### 核心内容

* **LLM 基础知识**

  * Transformer 架构基础（Self-attention 概念）
  * GPT 系列模型特点
  * Token、Prompt、温度、Top-p 等参数含义
* **API 使用**

  * OpenAI API 调用流程（Python SDK）
  * 常用 API 参数调节
  * 设计清晰 Prompt（指令设计、结构化输出）
* **Prompt 工程**

  * 如何引导模型输出 JSON、表格格式
  * 多轮对话的上下文维护
  * 结果校验和纠错策略
* **Agent 框架入门**

  * LangChain 结构（Chains, Agents, Tools）
  * AutoGen 多 Agent 协作思想

### 推荐资源

* OpenAI 官方文档：[https://platform.openai.com/docs](https://platform.openai.com/docs)
* 《The Illustrated Transformer》博客文章
* LangChain 官方教程与示例
* Prompt Engineering Guide（网上开源资料）


## 4. **运筹优化建模与求解实操**

### 核心内容

* **Pyomo 建模基础**

  * 变量定义、约束、目标函数写法
  * 多目标与分段函数
  * 求解器接口调用（Gurobi、CPLEX、CBC）
* **OR-Tools 基础**

  * 路径优化、调度模块
  * 简单示例编写
* **模型调试技巧**

  * 可行性检查
  * 求解失败原因分析
* **问题案例实践**

  * 经典运输模型
  * 车辆路径规划 VRP
  * 作业车间调度 JSSP
* **集成与自动化**

  * 自动生成模型代码
  * LLM 辅助模型构建流程

### 推荐资源

* Pyomo 官方文档和示例
* Google OR-Tools 官方教程
* Gurobi 教程（学术许可免费）
* 优化社区博客（如 NEOS Server）

---

## 5. **软件架构与工程实践**

### 核心内容

* **模块化设计**

  * 职责划分（解析、建模、求解、API）
  * 接口设计
* **API 设计与实现**

  * RESTful API 基础
  * FastAPI 框架深入
  * 文档生成（Swagger/OpenAPI）
* **容器化部署**

  * Docker 基础（Dockerfile 编写）
  * 本地测试与镜像管理
* **持续集成与部署（CI/CD）基础**

  * GitHub Actions 简单流水线
* **安全基础**

  * 输入过滤
  * 基本认证机制

### 推荐资源

* FastAPI 深度教程（官方文档 & 视频）
* Docker 入门教程（官方文档 + 视频）
* GitHub Actions 官方文档
* RESTful API 设计最佳实践文章

---

# 总结与建议

| 领域     | 学习重点                              | 推荐资源                 | 实践建议               |
| ------ | --------------------------------- | -------------------- | ------------------ |
| 数学/运筹  | LP/MILP基础，经典模型，算法思想               | 《运筹学》、MIT OCW        | 纸上写模型，手写算法流程       |
| 编程     | Python，Pyomo，FastAPI，Git          | Sweigart书，官方文档       | 写运输模型代码，做API调用     |
| AI/LLM | Transformer基础，OpenAI API，Prompt设计 | OpenAI文档，LangChain教程 | 设计Prompt，调用API做抽取  |
| 优化实操   | 建模技巧，求解器使用，案例实践                   | Pyomo/Gurobi教程       | 完成VRP/JSSP模型求解Demo |
| 工程实践   | 模块化，API设计，Docker，CI/CD            | 官方文档，教学视频            | 写模块，做Docker镜像      |

---

