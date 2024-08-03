# 🌿 谷歌生草机 - Google Translate Grass Machine

## 介绍 📖

谷歌生草机利用 Google 翻译的特点，通过多次随机翻译，将文本内容逐渐变得荒谬有趣。这种方法可以有效地生成生草内容，适合用于娱乐和实验。本程序基于 [ReturnZeroGirl/GoogleTranslateMakeGrass](https://github.com/ReturnZeroGirl/GoogleTranslateMakeGrass) 项目，进行了改进和扩展。

## 功能特点 ✨

- **多语言随机翻译**：支持多种语言，随机选择翻译。
- **自定义翻译次数**：可根据需要设置翻译的次数。
- **生成 Excel 文件**：保存详细的翻译过程和结果到 Excel 文件中。
- **自动调整 Excel 格式**：自动换行、自动适应列宽、首行居中。
- **详细日志记录**：记录每次翻译的过程，方便调试和追踪。

## 安装 🔧

### 克隆项目

```sh
git clone https://github.com/happycola233/GoogleTranslateMakeGrass.git
cd GoogleTranslateMakeGrass
```

### 安装依赖

```sh
pip install deep-translator pandas openpyxl colorlog
```

## 配置 ⚙️

首次运行程序时，如果 `config.ini` 文件不存在，程序会自动生成一个默认配置文件。请根据需要修改配置文件中的内容：

```ini
[options]

# 待生草的文件
file_src = src.txt

# 生草结果输出文件
file_out = translation_results.xlsx 

# 编码
encoding = utf-8

# 目标语言（详见源代码内的language_names映射）
target_lang = zh-CN

# 生草次数
frequency = 20
```

### 源文件 ✏️

`src.txt` 文件是待翻译的源文件，请将需要翻译的内容写入该文件。例如：

```
这是需要生草的文本内容。
```

## 使用方法 🚀

运行程序：

```sh
python translator.py
```

程序会读取 `src.txt` 文件中的内容，根据配置文件中的设置进行多次随机翻译，并将结果保存到 `translation_results.xlsx` 文件中。

## 注意事项 ⚠️

由于 Google 翻译服务在中国大陆无法直接访问，大陆用户需要自行准备代理来访问 Google 翻译服务。

## 日志 📜

程序运行时会在 `logs` 目录下生成日志文件，详细记录每次翻译的过程和结果，方便调试和追踪。日志文件示例如下：

```
[2024-08-03 14:17:44,189] -INFO- logs 目录已存在
[2024-08-03 14:17:44,190] -INFO- 配置文件读取成功
[2024-08-03 14:17:44,190] -INFO- 源文件读取成功
[2024-08-03 14:17:44,780] -INFO- 翻译第 1 次: This is a test.
...
[2024-08-03 14:17:52,992] -INFO- 翻译结果已保存为 translation_results.xlsx
```

## 生成的 Excel 文件示例 📊

生成的 `translation_results.xlsx` 文件包含以下列：

| 生草次数 | 目标语言 | 目标语言（中文全称） | 结果 | 结果翻译成中文（简体） |
| -------- | -------- | ------------------- | ---- | --------------------- |
| 1        | en       | 英语                | ...  | ...                   |
| 2        | fr       | 法语                | ...  | ...                   |
| 3        | de       | 德语                | ...  | ...                   |
| ...      | ...      | ...                 | ...  | ...                   |

## 贡献 🤝

欢迎提交 Issue 和 Pull Request，帮助改进本项目。贡献方式如下：

1. Fork 本仓库
2. 创建你的分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开 Pull Request

## 许可证 📝

本项目使用 ![License](https://img.shields.io/badge/license-MIT-blue.svg)，详情请参见 LICENSE。

## 鸣谢 🙏

感谢 [ReturnZeroGirl](https://github.com/ReturnZeroGirl) 提供的原始项目。
