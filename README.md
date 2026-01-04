```mermaid graph TD
    A[客户反馈 Critical 问题] --> B[客户支持: 尝试临时方案解决现场问题]
    B --> C[研发: Jira 接收问题并修复]
    C --> D[提交 PR 至 2.6-test 分支]
    D --> E[交付/QA: 在 test 分支验证]
    E --> F[通知研发合并至 2.6-release 分支]
    F --> G[交付/QA: 在 release 分支二次验证]
    G --> H{验证通过?}
    H -- 是 --> I[临时发布 Bug-fix 版本]
    I --> J[1. 版本号+1]
    J --> K[2. 记录三个仓库 Commit ID]
    K --> L[3. 发送全员版本通知邮件]
```
