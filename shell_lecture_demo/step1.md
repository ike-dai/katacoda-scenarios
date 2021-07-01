# シェルの概要 パート

## 講義資料p.7

- 以下のコマンドを実行してみましょう。

`echo "Hello World"`{{execute}}

## 講義資料p.13

- manコマンドでechoコマンドの仕様を確認してみましょう。

`man echo`{{execute}}

## 講義資料p.15

- どのユーザでログインしているかを確認してみましょう。

`whoami`{{execute}}

- /etc/passwdファイルを確認して、上記ユーザのログインシェルの種別を確認しましょう。

`cat /etc/passwd`{{execute}}

- 以下コマンドを実行して実際にどのシェル上にいるかを確認しましょう。

`echo $SHELL`{{execute}}

## 講義資料p.18

- ホームディレクトリ直下の.bashrcファイルの中身を見てみましょう。
    - ※講義資料中に記載の.bash_profileは確認環境上には存在しないので注意

`cat ~/.bashrc`{{execute}}

# シェルスクリプトの基本 パート

## 講義資料p.26

- helpコマンドを実行して組み込みコマンドにどのようなものがあるかを見てみましょう。

`help`{{execute}}

## 講義資料p.27

- coreutilsに含まれるコマンドにどのようなものがあるかを見てみましょう。

`dpkg -L coreutils | grep bin`{{execute}}

## 講義資料p.28

- tutorialフォルダ直下に配置されているsample.shを実行してみましょう。
    - 実行方法1 bashの引数として実行
    `bash tutorial/sample.sh`{{execute}}
    - 実行方法2 直接実行
    `./tutorial/sample.sh`{{execute}}
    - 実行方法3 commandコマンドで実行
    `command tutorial/sample.sh`{{execute}}

## 講義資料p.31

- tutorial/sample.shの実行権限を確認してみましょう。

`ls -l tutorial/sample.sh`{{execute}}

- x権限を外してみましょう。

`chmod a-x tutorial/sample.sh`{{execute}}

- 再度実行してみましょう。
    - 実行方法1 bashの引数として実行
    `bash tutorial/sample.sh`{{execute}}
    - 実行方法2 直接実行
    `./tutorial/sample.sh`{{execute}}
    - 実行方法3 commandコマンドで実行
    `command tutorial/sample.sh`{{execute}}

- x権限を再度付与しましょう。

`chmod a+x tutorial/sample.sh`{{execute}}

## 講義資料p.42

- シェル変数を定義してみましょう。

`VAR1="test"`{{execute}}

- スクリプトの中でシェル変数をechoした結果を見てみましょう。

`cat ./tutorial/var_echo.sh`{{execute}}
`./tutorial/var_echo.sh`{{execute}}

- VAR1シェル変数を環境変数化してみましょう。

`export VAR1`{{execute}}
`./tutorial/var_echo.sh`{{execute}}

## 講義資料p.48

- コマンドの結果をgrepでフィルタしてみましょう。

`ls -l ~/tutorial`{{execute}}
`ls -l ~/tutorial | grep sample`{{execute}}

## 講義資料p.49

- dateコマンドの結果を変数に格納してみましょう。

``VAR=`date```{{execute}}

- 変数に格納された結果を確認してみましょう。

`echo $VAR`{{execute}}

## 講義資料p.50

- dateコマンドの結果をファイルに書き出してみましょう。

`date > output.log`{{execute}}
`cat output.log`{{execute}}

- 再度書き込みましょう。

`date > output.log`{{execute}}
`cat output.log`{{execute}}

- 追記型で再度書き込みましょう。

`date >> output.log`{{execute}}
`cat output.log`{{execute}}

## 講義資料p.52

- 標準出力・標準エラー出力されるスクリプトを実行してみましょう。

`./tutorial/stdout_stderror.sh`{{execute}}

- 標準エラー出力をerror.logに出力してみましょう。

`./tutorial/stdout_stderror.sh 2> error.log`{{execute}}

- 標準出力と標準エラー出力両方をoutput.logに出力してみましょう。

`./tutorial/stdout_stderror.sh > output.log 2>&1`{{execute}}
`cat output.log`{{execute}}

概要編の講義部分は以上で終了です。お疲れさまでした。

