# Data-Structure
## 二分木
全てのノードの子が2個以下である木
## プライオリティキュー・ヒープ
### プライオリティキュー
次の操作が行えるデータ構造。
* 値を追加
* 最小の値を取り出し
### ヒープ
二分木を用いて、プライオリティキューを効率的に実装したもの。

Pythonではheapqをインポートすることにより、リストをヒープとして扱える。
```
import heapq
a = [1,5,3,2,7,9]

# リストをヒープとして扱えるように変換
heapq.heapify(a)

# (順序関係を保ったまま)要素の追加
heapq.heappush(a,5)

# (順序関係を保ったまま)要素の取り出し
heapq.heappop(a)
```

## 問題1：Expedition(POJ 2431)
トラックで距離Lの道を移動する。はじめガソリンがP積まれていて、距離1ごとにガソリンが1消費される。
途中でガソリンが0になると移動失敗となる。
途中にはN個のガソリンスタンドがあり、ガソリンスタンドiは道のスタート地点から距離$A_i$の地点にあり、$B_i$だけガソリンの補給ができる。
ガソリンタンクの容量に制限はない。
トラックは移動完了できるか、また、ガソリン補給が最小で何回必要となるか。

### 制限
* $1\le N \le 10000$
* $1 \le L,P \le 1000000$
* $1 \le A_i \le L, 1 \le B \le 100$

### 入力
$N,L,P$とAとBがそれぞれ次のように渡される。
```
4 25 10
10 14 20 21
10 5 2 4
```

### 出力
移動完了できる場合は最小の補給回数、できない場合は-1を出力。

## 問題2：Fence Repaier (PKU 3253)
一枚の長い板からN枚の板を切り出そうとしています。
切り出す長さは$L_1,...,L_n$であり、元の板の長さはこの合計である。
板を切断するとき、その板の長さ分のコストがかかる。
全ての板を切り出すための最小のコストを求めよ。
### 制約
* $1\le N \le 20000$
* $1 \le L_i \le 50000$
### 入力
次のように渡される。
```
3
8 5 8
```
### 出力
全ての板を切り出すための最小のコスト。