


# Rust Course 项目说明

本项目用于系统性学习和实践 Rust 编程语言，目标是通过构建高质量、符合工程规范的代码，掌握 Rust 的核心特性与工程化能力。

## 📌 项目目标

- 掌握 Rust 基础语法、所有权、生命周期等核心概念
- 理解并实践错误处理、trait、泛型、模块等进阶特性
- 学习 Rust 工程化规范（模块布局、clippy、格式化、pre-commit 等）
- 构建真实可维护的项目，而不仅仅是能运行的示例

## ✅ 环境准备

确保已安装以下工具：

- Rust 工具链（推荐使用 rustup）
- rustfmt：代码格式化工具
- clippy：静态分析与规范检查工具
- pre-commit（可选）：自动执行格式化与规范检查
- git（用于版本控制）

推荐执行以下命令：

```bash
rustup component add rustfmt clippy
cargo fmt --all
cargo clippy --all-targets --all-features -- -D warnings
```

## 🔧 Pre-commit 推荐配置

你可以在根目录添加 `.pre-commit-config.yaml` 文件：

```yaml
repos:
  - repo: https://github.com/doublify/pre-commit-rust
    rev: v1.0
    hooks:
      - id: fmt
      - id: cargo-check
      - id: clippy
```

然后运行：

```bash
pre-commit install
```

即可实现提交前自动检查和格式化。

## 🧱 项目结构（待完善）

```
rust_course/
├── src/
│   └── main.rs
├── Cargo.toml
└── README.md
```

## 📖 学习笔记（可选）

你可以在 `/notes` 目录记录自己的学习笔记、踩坑记录与进度总结。

---

**Rust 不是语法糖，而是系统设计的哲学。**  
你将不仅写出能运行的程序，更要写出性能、安全与可维护性兼顾的工程代码。