# Python入門 はやたす --youtube

2023/10/4 ~  10/7  

## 01_Pythonの特徴とPythonでできること

- 文法がシンプル
- 汎用性が高い
  - Webアプリ開発 ..Django, Flask
  - 機械学習プログラミング(AI開発) ..Scilit-learn, TensorFlow, PyTorch
  - データサイエンス ..Pandas, Matplotlib, Seaborn
  - Excelの自動処理 ..Pandas
  - Webスクレイピング ..BeautifulSoup, Selenium
  - ブロックチェーン開発
  - ゲーム開発
  - FX自動売買 などなど
- ポテンシャルが高い
  - 最近では、基本情報技術者試験でCOBOLに代わって、Pythonが試験内容に盛り込まれました。
  - 更に、プログラミング言語ランキングでは、常に上位にランクインしています。  
    https://xtech.nikkei.com/atcl/nxt/column/18/01068/111100001/  

## 02_Pythonを使える状態に！環境構築の種類と設定方法を紹介

オフライン  

- Python(Pure Python)
- Anaconda  

オンライン  

- Google Colaborator  
- AWS Cloud9 ..無料機関1年間のみ

今回の学習では、Google Colaborator を使う  

Google Colaborator の使い方  
  Shift ＋ Enter -> 実行  

## 03＿プログラミングの基本！変数と出力を学ぼう

変数名 = 代入する値

print() ..()内を出力  
※google labでは、()内の記載だけで出力OK  
  ただし、最後の１行だけしか出力されない

## 04_Pythonの基本！数値と演算・文字列とインデックス・bool値と比較演算子を習得しよう

整数の範囲で割り算をしたいときには、//を使う  

文字列の場合、インデックスを指定することで、特定の文字を取得できる  
s = 'こんにちは'  s[0] --> 'こ'  

## 05_type()関数とキャスト(型変換)を習得しよう

 型の確認 ..type()

キャスト(型変換)  

- str()
- int()

## 06_制御構文のif文を習得しよう

if 条件式 :
    処理
elif 条件式 :
    処理
else :
    処理

## 07_制御構文のfor文を習得しよう

for i in range(以上から,未満まで,ピッチ):処理

## 08_制御構文のwhile文を習得しよう

i = 0  
while i < 100:  
    i += 1  

途中で繰り返し処理を中断したいときには、break  
特定の条件だけ処理をスキップしたい場合には、continue  

## 09_リストの扱い方

enumerate ..リストからindexとvalue両方を取り出す  
l =  ['Python', 'Java' ,'Golang']  
for i,v in enumerate(l):  
    print(i,v)  

## 10_メソッドを習得してリストを自在に操ろう

append() ..リストに要素を追加する  
insert(index, value)..場所を指定して、要素を追加  
extend() ..リストを拡張  
remove() ..リストから要素を削除(該当する先頭の要素のみ)  

## 11_Python独特！リスト内包表記をマスターしよう

リスト内包表記  
l = [i for i in range(10)]  
高速な処理 ..※ %%timeit --処理時間を測定  

## 12_データ構造のタプルを習得しよう

タプル  
タプルでは要素の追加・変更や、要素の削除ができない  
アンパック  
  t = (1,2)  
  a,b = t  

## 13_辞書とメソッドについて、深く学ぼう

辞書  
d = {key1:value1, key2:value2, ..., }  
d[key] ..値を取り出すとき  
d[key] = value ..辞書に新しいkeyとvalueを追加  
d.keys() ..辞書に入っているkeyをすべて取得するには、keys()を使う  
d.values ..valueをすべて取得したいときには、values()を使う  
d.items ..keyもvalueも取得したいといったときには、items()を使う  
d.get(key)を使っても、辞書内の要素を取得できる  
get()とd[key]の違い  
  get() : 指定したkeyがないと、Noneを返す  
  d[key] : 指定したkeyがないと、エラーになる  
pop() ..要素を取得し、元の辞書から要素を消す  

## 14_ 集合と演算を、図解付きで分かりやすく解説

集合(set)  
a = {1,2,3,4,5}  

集合の特徴  
  重複を許さない  
  順序を保たない  

a = {1,2,3,4,5}  
b = {2,3,5,7,9}  
  aとbの差集合  
    a-b ..1,4  
  bとaの差集合  
    b-a ..7,9  
  aとbの積集合 ..共通部分  
    a & b ..2,3,5  
  aとbの和集合  
    a | b ..1,2,3,4,5,7,9  
  aとbの排他的論理和 ..和集合から共通部分を除いた部分  
    a ^ b ..1,4,7,9  
※ベン図を作ると理解しやすい

## 15_組み込み関数と自作関数の基礎を習得しよう

組み込み関数  
Pythonで最初から準備されている関数のことを、組み込み関数という

組み込み関数には、以下のようなものがある

- print()
- type()
- len()
- id()
- range()
- enumerate()
- min()
- max()

[公式ドキュメント](https://docs.python.org/ja/3/library/functions.html)

関数の定義  
def 関数名():  
    処理

関数の呼び出し  
関数名()  

## 16_キーワード引数とlambda関数を習得しよう

キーワード引数  
引数を指定して関数に渡すことで、順番が逆にならずに済む

lambda式(無名関数)  
定義：関数名 = lanmbda 引数 : 返り値 
実行：関数名(引数)

lambda式 x if文
関数名 = lambda 引数 : 真のときの返り値 if 条件式 else 偽のときの返り値  

※データサイエンスで、lambda式は頻出  

## 17_例外処理(エラーハンドリング)を習得しよう

try:
except:エラーの場合の処理  
else:正常な場合の処理  
finally:エラー、正常にかかわらず実行する処理

エラーの原因  
except TypeError as e:  
type(e)

エラーハンドリングは、たとえばスクレイピングするとき、「もしURLにアクセスできなかったら...」といったときに使う  

## 18_クラスの定義とメソッドの使用

help()  
help()関数を使うと、「どんな変数なのか」といった詳細が見れる  

クラスの定義  
Childクラスを作成して、say_hello()メソッドを持たせる

```python
class Child(object):
    def say_hello(self):
        print('Hello!!')
```

クラスのメソッドの利用

```python
# 1. 変数 = クラス名()
child = Child()
# 2. 変数.メソッド名()
child.say_hello()
```

## 19_クラスの初期化__init__()を分かりやすく解説

クラス内で__init__(self)を定義してあげると、オブジェクトを生成するとき常に呼ばれるようになる  

- クラス内のメソッドでは、selfを必ず付ける
- __init__で受け取ったデータ(例えばname)は、self.name = nameのように記述して、そのクラス内で使えるようにする  

## 20_クラスの継承

class クラス名(継承元クラス名):
  pass  

継承を受けた側のクラスをサブクラスと呼ぶ  

## 21_ライブラリのインポート

ライブラリの略称(任意)  

- seaborn : sns
- tensorflow : tf
- matplotlib.pyplot : plt
- pandas : pd
- numpy : np

導入されていないライブラリを使うには、自分でライブラリをインストールします。  
そのときのコマンドは、pip install ライブラリ名  
(google colab内のセルでは頭に ! をつける)  
