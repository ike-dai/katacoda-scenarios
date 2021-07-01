## 講義資料p.60

- func1が定義されたfunc1.shを実行し結果を出力してみましょう。

`./tutorial/func1.sh`{{execute}}


## 講義資料p.65

- 配列を定義してみましょう。

`sample=("a" "b" "c")`{{execute}}

- 配列の要素の個数を参照してみましょう。

`echo ${#sample[@]}`{{execute}}

- 配列の要素の中身全てを出力してみましょう。

`echo ${sample[@]}`{{execute}}

## 講義資料p.69

- sedコマンドを試してみましょう。

`cat tutorial/original.txt`{{execute}}

`sed -e "s/Hello/GoodBy/g" tutorial/original.txt > converted.txt`{{execute}}

`cat converted.txt`{{execute}}


- awkコマンドを試してみましょう。

`echo "192.168.1.25" | awk -F '.' '{printf "%s.%s\n", $1, $2}'`{{execute}}

## 講義資料p.70

- seqコマンドを試してみましょう。

`seq 1 2 10`{{execute}}

- sortコマンドを試してみましょう。

`echo -e "ccc\nbbb\naaa"`{{execute}}

`echo -e "ccc\nbbb\naaa" | sort`{{execute}}

## 講義資料p.71

- dateコマンドで1週間前の日付を出力してみましょう。
    - TZ環境変数でタイムゾーンを指定して実行する例

`TZ=Asia/Tokyo date +"%Y-%m-%d %H:%M:%S" --date "1 week ago"`{{execute}} 

- findコマンドでtutorialフォルダ以下の.txtのファイルのみを検索してみましょう。

`find ./tutorial -name "*.txt"`{{execute}}

## 講義資料p.72

- grepコマンドで./tutorialフォルダ配下のファイルの内、txtというキーワードを含まないものを出力してみましょう。


`ls -l ./tutorial | grep -v txt`{{execute}}

- curlコマンドでexample.comのトップページhtmlを出力してみましょう。

`curl -XGET http://example.com`{{execute}}

## 講義資料p.74

- cronの定義を確認してみましょう。(現在ログインしているユーザ(root)のcron定義)

`crontab -l`{{execute}}

`cat /var/spool/cron/crontabs/root`{{execute}}

- cronの共通の定義を確認してみましょう。

`cat /etc/crontab`{{execute}}

## 講義資料p.77

- tutorial/var_echo.shを各種フラグをつけて実行してみましょう。

`bash -u tutorial/var_echo.sh`{{execute}}

`bash -v tutorial/var_echo.sh`{{execute}}

`bash -x tutorial/var_echo.sh`{{execute}}


実践編の講義部分は以上で終了です。お疲れさまでした。


