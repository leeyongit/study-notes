# Git Commit 消息规范指南

## 基本格式

commit 信息的基本格式如下:

```bash
<type>(<scope>): <subject>

<body>

<footer>
```

## 类型(type)说明

- feat: 新功能(feature)
- fix: 修复bug
- docs: 文档更新
- style: 代码格式调整，不影响代码运行的变动
- refactor: 重构代码，既不是新增功能，也不是修改bug的代码变动
- perf: 性能优化
- test: 新增测试或更新现有测试
- chore: 构建过程或辅助工具的变动

## 范围(scope)说明

scope用于说明 commit 影响的范围，如:
- 组件名称
- 模块名称
- 功能名称
- 或者不填(可选)

## 主题(subject)说明

- 用简洁的语言描述本次提交的主要内容
- 不超过50个字符
- 以动词开头，使用第一人称现在时，如"change"而不是"changed"或"changes"
- 首字母不要大写
- 结尾不加句号

## 正文(body)说明

- 对本次提交的详细描述
- 可以分成多行
- 说明代码变动的动机，以及与以前行为的对比

## 尾部(footer)说明

- 用于关闭 Issue 或说明破坏性变更
- 如果当前代码与上一个版本不兼容，则 Footer 以 BREAKING CHANGE 开头

## 示例

```
feat(login): 添加用户登录功能

- 实现用户名密码登录
- 添加手机验证码登录
- 集成第三方登录(微信、支付宝)

Close #123
```

```
fix(database): 修复数据库连接池泄露问题

- 修复连接未及时释放的问题
- 优化连接池配置参数
- 添加连接超时处理

解决了生产环境中数据库连接数过多的问题
关联 issue #456
```

## 提交信息检查清单

提交代码前，可以检查以下几点：
1. commit 信息是否符合规范格式
2. type 是否正确选择
3. scope 是否明确
4. subject 是否清晰简洁
5. body 是否详细说明了改动原因
6. 是否需要在 footer 中关联 Issue