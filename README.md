# インストール
cudaやハードウェアアクセラレータが有効な状態で様々な機能を利用したいので、anacondaは用いず、生pythonでインストールする（老害感）

```console
$ sudo pip3 install jupyter
```

# Jupyterをスタートする
```console
$ jupyter notebook
```

# jupyter特有問題点の対処法

## beautifulsoup
xmlをパースする際に、必要とされるが、html5libをエラーが起きた際に、ダウングレードする必要があり、注意
```console
$ sudo pip3 install --upgrade html5lib==1.0b8
```

# jupyterでrubyを利用する（素晴らしい）
rubyの2.4以上が入った状態で、irubyをgemでインストールして、パスを通す
```console
$ gem install iruby
# add .bashrc
export PATH=$PATH/.gem/ruby/2.4.0/bin:$PATH
```
jupyterがirubyを認識できるようにする
```console
$ iruby register
```
これをやったら、jupyterを再起動する

## エラーの特定の困難さ

import module errorなどでおかしくなった時、適切な表示がでない

この際、ローカルのpyファイルでデバッグする
