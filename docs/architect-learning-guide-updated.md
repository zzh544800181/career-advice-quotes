# 架构学习指南 · 技术动态更新

> 更新日期：2026-04-21
> 目标岗位：美业S2B2C平台技术架构负责人（SaaS多租户架构 + AI智能体 + Spring Cloud + 云原生）

---

## 一、高价值项目发现（2026年4月）

### AI Agent & Spring AI 领域

| 仓库 | Stars | 核心亮点 | 推荐理由 |
|------|-------|---------|---------|
| langchain4j/langchain4j | 11.4k | 2026-04-02 合并 PR#4850 "Introduce optional agents"，正式引入Agent框架 | Java AI Agent 事实标准，Spring AI 深度集成 |
| langgraph4j/langgraph4j | ~2k | 同时支持 LangChain4j 和 Spring AI 的 Agent 执行器，2026-03-25 升级 spring-ai-agent | 构建复杂多步骤AI工作流的最佳选择 |
| langchain4j/langchain4j-spring | 347 | 2026-04-09 发布 1.13.0-beta23，@AiService 注解支持Spring Boot快速集成 | 快速上手LangChain4j的Spring生态入口 |

### 多租户微服务架构

| 仓库 | Stars | 核心亮点 | 推荐理由 |
|------|-------|---------|---------|
| ThomasVitale/spring-boot-multitenancy | 154 | Schema-per-tenant 隔离方案完整，Spring Boot 多租户标杆参考 | 多租户Spring Boot标杆参考 |
| SatinderSinghSall/Full-Stack-Salon-Booking-Web-App | 0 | 2026-03-22 创建，美业预约全栈微服务（8个服务：User/Salon/Booking/Payment/Notification等），Spring Boot + React + RabbitMQ + Keycloak | 美业S2B2C平台最接近的参考实现 |
| IQKV/microservices-platform | - | 2026-04-08 仍有push，schema-per-tenant多租户微服务平台，Spring Cloud | 持续活跃维护的多租户参考 |

### Kubernetes 多租户 SaaS 基础设施

| 仓库 | Stars | 核心亮点 | 推荐理由 |
|------|-------|---------|---------|
| victorpreston/multi-tenant-saas-gateway | 7 | NestJS API Gateway + Kong + PostgreSQL/TimescaleDB + Kafka + Redis，完整EKS + Terraform基础设施 | 生产级多租户SaaS网关参考 |
| clouddrove/k8s-multitenant | 1 | Helm Chart 自动创建 Namespace/RBAC/ResourceQuota/LimitRange/NetworkPolicies | GitOps多租户K8s快速起步 |
| sufyanism/Multi-Tenant-SaaS-Infrastructure | 0 | Terraform + Kubernetes 基础设施即代码，Namespace隔离 + RBAC + CI/CD | 多租户云原生基础设施模板 |

---

## 二、技术趋势变化（2026年4月）

### 1. AI Agent 框架正式标准化
- **变化**：LangChain4j 在 2026-04-02 正式合并 Agent 框架（PR #4850），标志 Java AI Agent 从"社区实验"进入"官方支持"阶段
- **影响**：Spring AI + LangChain4j 的组合正在成为 Java 生态构建 AI Agent 的事实标准
- **建议**：优先掌握 @AiService 注解 + ChatLanguageModel + Agent 的组合模式

### 2. LangGraph4j 成为复杂 Agent 编排关键
- **变化**：LangGraph4j 1.8.11（2026-03-30）同时支持 LangChain4j 和 Spring AI 的 Agent executor
- **影响**：多步骤推理、工具调用、记忆管理需要 LangGraph 范式
- **建议**：学习 LangGraph 的 StateGraph 编排模式，适合美业 AI 助手的多轮对话场景

### 3. 美业 SaaS 微服务架构逐渐成型
- **变化**：2026年新出现的美业项目（Full-Stack-Salon-Booking-Web-App）已采用 8服务拆分 + RabbitMQ + Keycloak 的生产级架构
- **影响**：美业 SaaS 的技术复杂度已对齐泛行业标准，不再是"简单管理系统"
- **建议**：参考其服务拆分策略（User/Salon/Booking/Payment/Notification），这对美业 S2B2C 平台规划很有价值

### 4. 多租户 K8s 基础设施走向成熟
- **变化**：2026年新项目均使用 Namespace + RBAC + NetworkPolicies 的标准隔离方案，Terraform/Helm GitOps 化
- **影响**：多租户 K8s 部署不再是难题，配置模板化降低了落地门槛
- **建议**：使用 clouddrove/k8s-multitenant 或 sufyanism/Multi-Tenant-SaaS-Infrastructure 作为基础设施起点

---

## 三、学习路径更新建议

### 对「AI 智能体」路线的补充
1. **必学**：langchain4j 官方示例 + LangGraph4j StateGraph 编排（优先级：P0）
2. **参考**：spring-ai-alibaba 或 Spring AI 官方参考实现（优先级：P1）
3. **实践**：尝试用 LangChain4j 构建美业场景的 AI 客服 Agent（多轮预约/咨询）

### 对「SaaS 多租户」路线的补充
1. **必学**：ThomasVitale/spring-boot-multitenancy 的 Schema-per-tenant 实现（优先级：P0）
2. **必学**：SatinderSinghSall/Full-Stack-Salon-Booking-Web-App 的服务拆分（优先级：P0）
3. **实践**：结合 victorpreston/multi-tenant-saas-gateway 的 API Gateway 方案设计租户路由

---

## 四、推荐资源汇总

### 项目仓库（按优先级）
1. https://github.com/langchain4j/langchain4j — 11.4k stars，Java AI Agent 标准
2. https://github.com/langgraph4j/langgraph4j — ~2k stars，多步骤Agent编排
3. https://github.com/ThomasVitale/spring-boot-multitenancy — 154 stars，多租户Spring Boot参考
4. https://github.com/SatinderSinghSall/Full-Stack-Salon-Booking-Web-App — 美业微服务最佳参考
5. https://github.com/victorpreston/multi-tenant-saas-gateway — 生产级多租户网关

### 官方文档
- LangChain4j 文档: https://docs.langchain4j.dev/
- Spring AI 文档: https://docs.spring.io/spring-ai/reference/

---
> 本文档由技术动态自动化流程生成（2026-04-21）
