# PersonaPlex on Google Colab

 このフォルダには、PersonaPlex の Web UI を Google Colab 上で起動するためのノートブックが入っています。

 ## Colabリンク（フォーク向け）

 `{YOUR_GITHUB}` と `{YOUR_BRANCH}` をあなたのフォーク情報に置き換えてください。

 https://colab.research.google.com/github/{YOUR_GITHUB}/personaplex/blob/{YOUR_BRANCH}/colab/PersonaPlex_WebUI_Colab.ipynb

 ## できること

 - Colabノートブックから以下を一括実行します。
   - 依存関係のインストール（Colabで失敗しがちな `sounddevice` は回避）
   - Hugging Face 認証（必須）
   - `moshi.server` を起動し、外部からアクセス可能なトンネルURLを表示

 ## 事前準備（必須）

 - Google Colab のランタイムを **GPU** に設定
   - Runtime → Change runtime type → Hardware accelerator: **GPU**
 - Hugging Face アカウント
 - モデルのライセンス承諾（gated）
   - https://huggingface.co/nvidia/personaplex-7b-v1
   - ページ上で「Agree/Accept/Use」などを押して承諾してください

 ## 実行手順

 以下を開いて上から実行します。

 - `PersonaPlex_WebUI_Colab.ipynb`

 ノートブック内で以下のチェックが走ります。
 - GPUが有効になっているか（CUDAチェック）
 - Hugging Face の gated repo にアクセスできるか（`voices.tgz` の事前チェック）

 サーバ起動後、ログに **public tunnel URL** が表示されるので、そのURLをブラウザで開いて Web UI にアクセスしてください。

 ## 注意

 - このリポジトリのコードは MIT License です。
 - モデル重みは NVIDIA Open Model License で提供されます。このフォークでは重みを同梱せず、実行時に各自の環境でダウンロードします。
 - ノートブック実行時に Hugging Face へのログインが必要です（トークンは各自で用意してください）。
