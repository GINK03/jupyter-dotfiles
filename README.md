# jupyter特有問題点

## beautifulsoup
xmlをパースする際に、必要とされるが、html5libをエラーが起きた際に、ダウングレードする必要があり、注意
```console
$ sudo pip3 install --upgrade html5lib==1.0b8
```

## エラーの特定の困難さ

import module errorなどでおかしくなった時、適切な表示がでない

この際、ローカルのpyファイルでデバッグする
