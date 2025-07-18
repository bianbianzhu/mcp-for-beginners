<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "b59b477037dc1dd6b1740a0420f3be14",
  "translation_date": "2025-07-16T23:05:05+00:00",
  "source_file": "02-Security/mcp-security-controls-2025.md",
  "language_code": "zh"
}
-->
# 最新 MCP 安全控制 - 2025 年 7 月更新

随着模型上下文协议（MCP）的不断发展，安全依然是关键考量。本文档概述了截至 2025 年 7 月，安全实施 MCP 的最新安全控制措施和最佳实践。

## 认证与授权

### OAuth 2.0 委托支持

MCP 规范的最新更新允许 MCP 服务器将用户认证委托给外部服务，如 Microsoft Entra ID。这大大提升了安全性，具体体现在：

1. **避免自定义认证实现**：降低自定义认证代码中出现安全漏洞的风险  
2. **利用成熟的身份提供商**：享受企业级安全功能  
3. **集中身份管理**：简化用户生命周期管理和访问控制  

## 令牌透传防护

MCP 授权规范明确禁止令牌透传，以防止绕过安全控制和责任追踪问题。

### 关键要求

1. **MCP 服务器不得接受非为其签发的令牌**：验证所有令牌的受众声明是否正确  
2. **实施正确的令牌验证**：检查签发者、受众、过期时间和签名  
3. **使用独立的令牌签发**：为下游服务签发新令牌，而非透传现有令牌  

## 安全会话管理

为防止会话劫持和固定攻击，应实施以下控制措施：

1. **使用安全且非确定性的会话 ID**：通过密码学安全的随机数生成器生成  
2. **将会话绑定到用户身份**：将会话 ID 与用户特定信息结合  
3. **实施适当的会话轮换**：在认证变更或权限提升后进行  
4. **设置合理的会话超时**：在安全与用户体验之间取得平衡  

## 工具执行沙箱

为防止横向移动并限制潜在的安全破坏：

1. **隔离工具执行环境**：使用容器或独立进程  
2. **施加资源限制**：防止资源耗尽攻击  
3. **实施最小权限访问**：仅授予必要权限  
4. **监控执行模式**：检测异常行为  

## 工具定义保护

为防止工具被篡改：

1. **使用前验证工具定义**：检查是否包含恶意指令或不当模式  
2. **使用完整性校验**：对工具定义进行哈希或签名，检测未授权更改  
3. **实施变更监控**：对工具元数据的异常修改发出警报  
4. **对工具定义进行版本控制**：跟踪变更并在需要时回滚  

这些控制措施协同作用，为 MCP 实现构建了坚实的安全防线，既应对了 AI 驱动系统的独特挑战，也保持了传统安全实践的严谨性。

**免责声明**：  
本文件使用 AI 翻译服务 [Co-op Translator](https://github.com/Azure/co-op-translator) 进行翻译。虽然我们力求准确，但请注意，自动翻译可能包含错误或不准确之处。原始文件的母语版本应被视为权威来源。对于重要信息，建议采用专业人工翻译。对于因使用本翻译而产生的任何误解或误释，我们不承担任何责任。