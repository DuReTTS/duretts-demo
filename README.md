# DuReTTS Prosody Demo

ICASSP 投稿配套的试听 demo 页面。每行一个样本，包含 Ref（参考音频）、IndexTTS2、DuReTTS 三列。

## 目录结构

```
icassp-demo/
├── index.html        # demo 页面（GitHub Pages 入口）
└── audio/            # 15 个 wav 文件（5 个样本 × 3 列）
    ├── 14ref.wav / 14index.wav / 14duretts.wav
    └── ...
```

## 部署到 GitHub Pages

1. 在 github.com 新建一个仓库（如 `duretts-demo`，Public）。
2. 在本目录执行：

   ```bash
   git remote add origin https://github.com/<你的用户名>/duretts-demo.git
   git push -u origin main
   ```

3. 仓库页面 → **Settings → Pages** → Source 选 **Deploy from a branch**，
   Branch 选 **main** / **/(root)** → Save。
4. 等 1–2 分钟，访问 `https://<你的用户名>.github.io/duretts-demo/`。

## 本地预览

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```

## 修改提示

- 论文标题：编辑 `index.html` 中 `<h1>` 与 `<title>`。
- 新增样本：把 wav 放进 `audio/`（命名 `{编号}{ref|index|duretts}.wav`），
  在 `index.html` 的 `<tbody>` 里复制一行 `<tr>` 并改编号。
- 添加文本列：`index.html` 里留有注释掉的示例。
