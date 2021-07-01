# シェルの概要 パート

## 講義資料p.7

- 以下のコマンドを実行してみましょう。

`echo "Hello World"`{{execute}}

## 講義資料p.15

- どのユーザでログインしているかを確認してみましょう。

`whoami`{{execute}}

- /etc/passwdファイルを確認して


サンプルのステップ1

シェルスクリプトを作って実行してみる。

`touch test.sh`{{execute}}  
`echo 'echo "Hello World"' > test.sh`{{execute}}  

スクリプトを実行してみる

`bash test.sh`{{execute}}

出力結果として、以下が出ていれば成功です。

```
Hello World
```

