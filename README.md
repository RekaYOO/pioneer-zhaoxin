# 面试题集合

欢迎来到面试题集合项目！这是一本使用mdBook构建的面试题目汇总，涵盖了硬件部、网络部、办公室、美工部、推广部等多个领域的面试题目。

## 📚 在线阅读

本书已部署到GitHub Pages，可以通过以下链接在线阅读：
- **在线地址**: `https://RekaYOO.github.io/pioneer-zhaoxin/`

## 🏗️ 项目结构

```
pioneer-zhaoxin/
├── .github/
│   └── workflows/
│       └── PublishMySite.yml    # GitHub Actions自动构建配置
├── src/
│   ├── SUMMARY.md               # 书籍目录结构
│   ├── introduction.md          # 介绍页面
│   ├── 硬件部/                  # 硬件部题目
│   ├── 网络部/                  # 网络部题目
│   ├── 办公室/                  # 办公室题目
│   ├── 美工部/                  # 美工部题目
│   └── 推广部/                  # 推广部题目
├── book.toml                    # mdBook配置文件
├── mdbook.exe                   # mdBook可执行文件
└── README.md                    # 项目说明文档
```

## 🤝 如何贡献新章节

### 1. 准备工作

确保你已经安装了以下工具：
- Git
- mdBook（项目中已包含Windows可执行文件,其他系统需要自行安装）

### 2. 克隆项目

### 3. 创建新分支

```bash
git checkout -b feature/add-new-question
```

### 4. 添加新题目

#### 4.1 确定题目分类

根据题目内容，选择合适的部门分类：
- `硬件部/` - 硬件相关题目
- `网络部/` - 网络技术题目
- `办公室/` - 办公软件、项目管理题目
- `美工部/` - 设计、UI相关题目
- `推广部/` - 营销、推广相关题目

#### 4.2 创建题目文件

在对应的部门目录下创建新的Markdown文件，文件命名格式：
```
题目类型.md
```

例如：`操作系统.md`

#### 4.3 题目文件模板

例：

```markdown
# 题目标题

## 题目描述

[详细描述题目要求和背景]


### 子标题1
[具体内容]

### 子标题2
[具体内容]

## 事项

1. [步骤1]
2. [步骤2]
3. [步骤3]

## 相关

- [1]
- [2]
- [3]
```

#### 4.4 更新目录

在 `src/SUMMARY.md` 文件中添加新题目的链接：

```markdown
# 硬件部
- [硬件基础题1](./硬件部/硬件基础题1.md)
- [硬件基础题2](./硬件部/硬件基础题2.md)
- [硬件基础题3](./硬件部/硬件基础题3.md)
- [硬件基础题4](./硬件部/硬件基础题4.md)  # 新添加的题目
```

### 5. 本地预览

在项目根目录运行以下命令预览效果：

```bash
# Windows
./mdbook.exe serve

# Linux/Mac
mdbook serve
```

然后在浏览器中访问 `http://localhost:3000` 查看效果。

### 6. 提交更改

```bash
# 添加文件到暂存区
git add .

# 提交更改
git commit -m "添加[部门名称][题目类型]题目"

# 推送到远程分支
git push origin feature/add-new-question
```

### 7. 创建Pull Request

1. 访问GitHub仓库页面
2. 点击 "Compare & pull request" 按钮
3. 填写PR标题和描述
4. 提交Pull Request等待审核


## 🚀 自动化构建

本项目配置了GitHub Actions自动构建，当代码推送到main分支时会自动：

1. 使用mdBook构建静态网站
2. 部署到GitHub Pages
3. 更新在线版本