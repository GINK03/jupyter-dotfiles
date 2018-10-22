# 動作イメージ
<div align="center">
  <img src="https://user-images.githubusercontent.com/4949982/47258571-fa779c00-d4d7-11e8-8673-a7b6cf29c9ad.png">
</div>

# JupyterLabインストール
```console
$ conda install jupyterlab
$ conda install -c conda-forge nodejs # 拡張機能を有効にするのに必要
$ jupyter labextension install jupyterlab_vim # vimのバインディング
```

# Jupyterをスタートする
```console
$ jupyter lab
```

# Indent幅の変更

Settings -> Advanced Setting Editorから、`tabSize`の大きさや`insetSpace`などが編集できる 

<div align="center">
  <img src="https://user-images.githubusercontent.com/4949982/47258747-bf2a9c80-d4da-11e8-822f-7f2326ae1fa9.png">
</div>

# jupyter labこのコマンドで、password hashを作成する
```console
In [1]: from notebook.auth import passwd
In [2]: passwd()
Enter password:
Verify password:
Out[2]: 'sha1:67c9e60bb8b6:9ffede0825894254b2e042ea597d771089e11aed'
```
作成したhashは.jupyterの配下のパスワードに入れると認証に利用できる

# color hack
色を以下のファイルを変更することで、変更できる。
`/anaconda3/share/jupyter/lab/themes/\@jupyterlab/theme-dark-extension/index.css`
(デフォルトの色合いはエグいので、おとなしめに変更するなど)

<div align="center">
  <img src="https://user-images.githubusercontent.com/4949982/47275798-71eb1f80-d5ed-11e8-9f32-db71eb818aaa.png">
</div>
コメントを灰色に  

```
--jp-mirror-editor-comment-color: #aeaeae;
```
ストリング（リテラル）をオレンジに  

```
--jp-mirror-editor-string-color: #D39838;
```
