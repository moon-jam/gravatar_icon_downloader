# Gravatar 頭像下載器

> **注意：** 這個專案的所有內容，包括此 README 文件和腳本本身，都是由 Gemini CLI 創建的，用於測試其酷酷功能。

這個腳本可以根據提供的文字檔案中的使用者列表下載他們的 Gravatar 頭像。

## 授權

本專案採用 MIT 授權。詳情請見 [LICENSE](LICENSE) 文件。

## 環境需求

- `curl`：一個用於傳輸 URL 資料的命令列工具。
- `md5`：一個用於計算 MD5 雜湊值的命令列工具。
- `python3`：用於對預設圖片參數進行 URL 編碼。

## 使用方法

### 1. 準備列表檔案

建立一個文字檔案（例如 `users.txt`）。每一行必須包含一個名字和一個電子郵件地址，並以 **Tab** 字元分隔。

**重要提示**：必須使用 Tab 作為分隔符。不支援使用空格，否則會導致錯誤。

**`users.txt` 檔案範例：**
```
範例一	example1@example.com
範例二	example2@example.com
```

### 2. 讓腳本可執行

```bash
chmod +x download
```

### 3. 執行腳本

此腳本使用具名參數。

**A) 基本用法（必需）：**
```bash
./download --file=users.txt
```

**B) 指定自訂尺寸：**
```bash
./download --file=users.txt --size=512
```

**C) 使用遠端 URL 作為預設圖片：**
```bash
./download --file=users.txt --default=https://example.com/my-avatar.png
```

如果使用者沒有 Gravatar 頭像，腳本將會使用本地的 `default.png` 檔案（如果存在），除非您透過 `--default` 指定了遠端的 URL。

### 4. 獲取幫助

您可以顯示幫助訊息以獲取使用說明：
```bash
./download --help
```

---

# Gravatar Icon Downloader

> **Note:** This entire project, including this README and the script itself, was created by Gemini CLI as a test of its cooooool capabilities.

This script downloads Gravatar icons for a list of users provided in a text file.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Prerequisites

- `curl`: A command-line tool for transferring data with URLs.
- `md5`: A command-line tool to compute MD5 hashes.
- `python3`: For URL encoding the default image parameter.

## Usage

### 1. Prepare the List File

Create a text file (e.g., `users.txt`). Each line must contain a name and an email address, separated by a **Tab** character.

**IMPORTANT**: You must use a Tab separator. Spaces are not supported and will cause errors.

**Example `users.txt` file:**
```
example1	example1@example.com
example2	example2@example.com
```

### 2. Make the Script Executable

```bash
chmod +x download
```

### 3. Run the Script

The script uses named arguments.

**A) Basic usage (required):**
```bash
./download --file=users.txt
```

**B) With a custom size:**
```bash
./download --file=users.txt --size=512
```

**C) With a remote URL as the default image:**
```bash
./download --file=users.txt --default=https://example.com/my-avatar.png
```

**D) With a local file path as the default image:**
```bash
./download --file=users.txt --default=./my-default-avatar.png
```

If a user does not have a Gravatar, the script will use the local `default.png` file (if it exists) unless a remote `--default` URL or a local `--default` path is specified.

### 4. Get Help

You can display the help message with usage instructions:
```bash
./download --help
```

