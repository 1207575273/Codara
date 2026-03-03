# Codara

AI 驱动的终端代码编辑器。

## 技术栈

- Bun + TypeScript + React

## 开发

```bash
# 安装依赖
bun install

# 代码检查
bun run lint

# 代码格式化
bun run format

# 构建
bun run build
```

## 测试

```bash
# 运行全部测试
bun test

# 运行 provider 单元测试
bun test tests/unit/provider

# 运行 DeepSeek 真实集成测试
bun test tests/integration/provider/deepseek-hello.e2e.test.ts
```

注意：

- 测试文件使用 `bun:test`，请使用 `bun test` 执行，不要使用 `bun run <test-file>`。
- DeepSeek 集成测试会真实发起网络请求，需要在 `.env` 配置 `DEEPSEEK_API_KEY`。

### Provider 单测一对一映射

- `config/parser.ts` -> `tests/unit/provider/parser.test.ts`
- `config/loader.ts` -> `tests/unit/provider/loader.test.ts`
- `runtime/api-key.ts` -> `tests/unit/provider/api-key.test.ts`
- `runtime/resolver.ts` -> `tests/unit/provider/resolver.test.ts`
- `runtime/model-manager.ts` -> `tests/unit/provider/model-manager.test.ts`

## License

MIT
