# lighttool

一个零第三方依赖的轻量级目录文件统计 CLI 工具。

## 功能

- 统计文件数、目录数、总大小
- 按扩展名汇总占用空间
- 列出最大的 Top N 文件
- 支持 JSON 输出，方便脚本集成
- 默认忽略隐藏文件/目录，可用 `--include-hidden` 包含

## 安装

```bash
git clone https://github.com/<你的用户名>/lighttool.git
cd lighttool
python -m pip install -e .
```

## 使用

```bash
# 扫描当前目录
lighttool

# 扫描指定目录，显示 Top 10
lighttool ./src --top 10

# 包含隐藏文件
lighttool . --include-hidden

# JSON 输出
lighttool . --json
```

示例输出：

```text
扫描目录: /path/to/project
文件数: 42
目录数: 7
总大小: 1.2 MB

按扩展名汇总（Top 5）:
  .py          800.0 KB
  .md          200.0 KB
```

## 测试

```bash
python -m unittest discover -s tests -v
```

## License

MIT