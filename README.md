# 音声のデータセットのクラスタリング・データセット作成のノートブック

[**voice-clustering.ipynb**](voice-clustering.ipynb)

大量のwavファイルから（複数話者が混じっていても可）、[pyannote/embedding](https://huggingface.co/pyannote/embedding) の特徴量でクラスター分けを行い、**特定話者**の**標準的な**発話データを抽出して、与えられた合計時間内に収まるように標準的なものから順に番号づけしてコピーするノートブックです。
自分がデータセット作りのときに使っています。


以下の用途で使えます：
1. 多数の話者が混じったデータセットから、特定話者のデータセットを作成する（話者識別）
2. 一人の話者のデータセットから、標準的な発話を抽出する（感情やトーン等が違う場合も）

jupyter notebookやjupyter labで動かすことを想定しています。
必要ライブラリは [requirements.txt](requirements.txt) に記載しています。

また、wavファイルから特徴量を取り出す [pyannote/embedding](https://huggingface.co/pyannote/embedding) を使うために、hugging faceアカウントを作成して [pyannote/embedding](https://huggingface.co/pyannote/embedding) の規約に同意し、またhugging faceのアクセストークンを [`hf.co/settings/tokens`](https://hf.co/settings/tokens) から発行する必要があります。
