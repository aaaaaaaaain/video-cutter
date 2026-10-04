# 影片分段剪輯

在瀏覽器裡把影片依時間、容量或自訂入點／出點切成多段。影片只在使用者自己的瀏覽器裡處理，不會上傳。

線上使用：https://aaaaaaaaain.github.io/video-cutter/

## 功能

- 每段固定長度、每段不超過容量、自訂入點／出點三種切法
- 快速模式（不重新編碼，切點對齊關鍵影格）與精準模式（重新編碼）
- 即時預覽、縮圖時間軸、每段容量預估
- 多段輸出時打包成 zip，裡面是一個資料夾

快捷鍵：Space 播放、I 入點、O 出點、← → 前後 1 秒（加 Shift 10 秒）

## 第三方元件

| 元件 | 版本 | 授權 | 原始碼 |
|---|---|---|---|
| @ffmpeg/ffmpeg（`vendor/ffmpeg.js`、`vendor/814.ffmpeg.js`） | 0.12.15 | MIT | https://github.com/ffmpegwasm/ffmpeg.wasm |
| @ffmpeg/core（`vendor/ffmpeg-core.js`、`vendor/core.*.wasm`） | 0.12.10 | GPL-2.0-or-later（含 FFmpeg 與 x264） | https://github.com/ffmpegwasm/ffmpeg.wasm 、 https://ffmpeg.org |
| JSZip（`vendor/jszip.min.js`） | 3.10.2 | MIT 或 GPL-3.0 | https://github.com/Stuk/jszip |

`vendor/core.0.wasm`～`core.2.wasm` 是 @ffmpeg/core 的 `ffmpeg-core.wasm` 原檔依序切成三份，網頁載入時再接回去，內容沒有修改。
