# 漢字拆解練習簿

輸入一個漢字，查看筆順動畫與拼音、練習筆順（寫錯會提示）、拆分部首（紅色）與其他部件（藍色），以及 HSK 1–4 級的常見組詞、例句和拼音。可切換繁體／簡體資料庫。

純靜態網頁，不需要建置或後端。

## 放到 GitHub Pages

1. 在 GitHub 建立一個新的公開 repository。
2. 把這個資料夾裡的所有檔案和資料夾（`index.html`、`data/`、`lib/`、`.nojekyll`、`README.md`）上傳到 repository 根目錄。
3. 到 Settings → Pages，Source 選「Deploy from a branch」，Branch 選 `main`、資料夾選 `/ (root)`，儲存。
4. 一兩分鐘後網站會出現在 `https://<你的帳號>.github.io/<repository 名稱>/`。

## 在自己的電腦上開啟

直接雙擊 `index.html` 無法載入資料（瀏覽器會擋 `file://` 的讀取）。請在這個資料夾執行：

```
python3 -m http.server 8000
```

然後打開 <http://localhost:8000>。

## 檔案

- `index.html`：整個網頁（版面、樣式、程式）
- `lib/hanzi-writer.min.js`：筆順動畫與練習的程式庫
- `data/c/*.json`：約 9,500 個字的筆順、拼音、部首與部件資料（分成 48 個檔）
- `data/words.json`：HSK 1–4 級詞語與例句
- `data/conv.json`：繁簡對照表

## 資料來源與授權

- 筆順與字形：[hanzi-writer-data](https://github.com/chanind/hanzi-writer-data)（Arphic Public License）
- 部件拆分、部首：[Make Me a Hanzi](https://github.com/skishore/makemeahanzi)（Arphic Public License／LGPL）
- 繁簡對照：[OpenCC](https://github.com/BYVoid/OpenCC)（Apache-2.0）
- HSK 詞表：[complete-hsk-vocabulary](https://github.com/drkameleon/complete-hsk-vocabulary)（MIT）
- 例句：[hsk-sentences-audio](https://github.com/no7z/hsk-sentences-audio)（CC BY-SA 4.0，重新散布時請保留出處）
- 筆順動畫：[Hanzi Writer](https://hanziwriter.org)（MIT）

繁體字和簡體字共用同一套筆順資料，個別字可能和臺灣教育部的標準筆順不同。
