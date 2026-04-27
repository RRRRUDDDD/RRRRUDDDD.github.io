# RRRRUDDDD Hugo Site

这个仓库已经清理为一个干净的 Hugo 站点，并使用主题：
- https://github.com/CaiJimmy/hugo-theme-stack

## 1. 安装 Hugo（extended）

请安装 Hugo extended 版本（建议与 CI 一致使用最新稳定版）。

macOS (Homebrew):

```bash
brew install hugo
```

Windows (Scoop):

```bash
scoop install hugo-extended
```

Linux (手动下载二进制):

```bash
# 示例：0.157.0
HUGO_VERSION=0.157.0
curl -LO "https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_Linux-64bit.tar.gz"
tar -xzf "hugo_extended_${HUGO_VERSION}_Linux-64bit.tar.gz"
sudo mv hugo /usr/local/bin/hugo
hugo version
```

## 2. 安装并启用 Stack 主题

本仓库已通过 Hugo Modules 启用主题（见 `config/_default/module.toml`）。

更新主题：

```bash
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v4
hugo mod tidy
```

## 3. 本地运行

```bash
hugo server
```

## 4. 构建

```bash
hugo --gc --minify
```
