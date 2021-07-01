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

`echo "192.168.1.25" | awk -F ',' {printf "%s.%s\n", $1, $2}`{{execute}}

## 講義資料p.70

- seqコマンドを試してみましょう。

`seq 1 2 10`{{execute}}

- sortコマンドを試してみましょう。

`echo -e "ccc\nbbb\naaa"`{{execute}}

`echo -e "ccc\nbbb\naaa" | sort`{{execute}}

## 講義資料p.71

 
