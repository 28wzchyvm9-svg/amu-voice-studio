# AMU VOICE STUDIO

ブラウザだけで動く、端末内完結の音声合成＆文学キネティックタイポグラフィ動画アプリです。
サーバーへ文章を送らず、すべての合成・書き出しは開いた端末の中で行います。

- **AMU TALK** — テキストを読み上げて MP3 で保存
- **AMU NOVEL** — 縦書き原稿＋ナレーション同期の文学系タイポグラフィ動画（MP4 書き出し）

公開ページ: https://28wzchyvm9-svg.github.io/amu-voice-studio/

## 仕組み

- 音声合成: Style-BERT-VITS2（JP-Extra）を ONNX Runtime Web で端末内実行
- 音響モデル・DeBERTa・辞書・BGM は Hugging Face（AiMu1215）の公開リポジトリから取得し、
  初回読み込み時に端末へ保存します（このリポジトリにはテキストファイルのみを置いています）

## クレジット

- 歌声・音声モデル: JVNV Corpus（CC BY-SA 4.0）由来の JVNV F2 / itoolsjp Style-Bert-VITS2 Voice Assets（東部湯の丸・さくら徳次郎・横浜青葉）
- BGM ピアノ音源: Salamander Grand Piano（Alexander Holm、CC BY 3.0）
- ライブラリ: onnxruntime-web（MIT）、mp4-muxer（MIT）、lamejs（LGPL-2.1）、Comlink（Apache-2.0）
