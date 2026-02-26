# Pythonについて

### 1. 必須のルール
- 改行して処理を切る！

```python
print("Hello Python") # 改行して切る
print("Hello Programming")
```


- まとまった処理はインデント（字下げ）を作って指定する！
```python
n = 1

if n == 1:
    print(n)
```
- 大文字と小文字は区別されるため使用には気を付ける！
```python
Print("Hello Python")
```

---

### 2. プログラムを書くときに使えるコツ

- コメントを使う（#記号）
- [PEP8](https://pep8-ja.readthedocs.io/ja/latest/)を参考にする
    - Pythonの標準コーディング規約
    - プログラムを書く際のマナー（お作法）みたいなもの

---

### 3．変数について

__変数__:1つのデータを保管しておく入れ物
```python
n = 100

print(n)
```

#### 変数名のルール
- 英小文字（a ~ z）
- 単語の区切りに _
```md
○ name, student_no
```
- 1文字目に数字は使えない
- 使えないキーワードがある
```md
× 1st_number, forなど
```

#### ⚠️"="は「代入」の意味！
```md
# A = B
→ BをAに代入する（右から左へ）
```

#### 参照する：値を見る
```md
# 変数名（→値に置き換わる）
print(変数名)
```

#### 変数の値は更新できる！
```python
n = 100
print(n)

n = 200
print(n)

n = "Hello Python"
print(n)
```

---

### データの型

```md
データの型の基本4つ

1. int型：数値,数字（1, 2, 3,...）
2. str型：文字列型（"文字"）
3. float型：小数点（3.14）
4. bool型：真偽値（True, False）
```
#### サンプル
```python
a = 30
b = 50
c = "100"
d = "100"
c_1 = int(c) # strからintへ
d_1 = int(d) # strからintへ

print(a + b) # 80と出る
print(a, c)  # 30100とでる
print(a + c) # エラー
print(c + d) # 100100
print(C_1 + d_1)
```

---

### 演算記号
1. +： 足し算（int型）,連結・結合（str型）

2. -： 引き算（int型）

3. *： 掛け算（int型）※アスタリスク

4. **： べき乗 (2 ** 3)

5. /： わり算（float型）

6. //： わり算（int型）

7. %：割ったときの余り

8. ==： イコール（等しい）

9. !=： イコールでない（等しくない）

10. A > B： AがBより大きい

11. A < B： AがBより小さい

12. A >= B： AがB以上(A=Bも成り立つ)

13. A <= B： AがB以下(A=Bも成り立つ)

14. A and B：AとB, AかつB

15. A or B：AまたはB, どちらか片方

#### サンプル
```python
# 足す
a = 100 # int
b = 200 # int
c = a + b

print(c)       # 300
print(type(c)) # int

# 引き算
print(b - a) # 100

# 掛け算
print(a * b) # 200000

# わり算
print(b / a) # 2.0
print(b // a) # 2
```

---

### 配列（リスト）
- 配列：複数のデータをまとめて管理
- リスト(list)の使い方

```md
配列名 = [値1, 値2, 値3, ・・・]
score = [80, 100, 75]
player = ["マリオ", 100]
```

#### 参照する
```md
# 配列名[添え字]

要素→ 80,  100,  75
添字→ [0]  [1]   [2]

score[1] = 100
```

#### リストの便利なメソッド
**関数**：処理をまとめたもの
```md
組込み関数
print()
input()
：

リストの中で使える組込み関数
append()
clear()
：

辞書で使える組込み関数
get()
clear()
：
```

- append(値)：追加
　score.append(85)

- insert(添え字, 値)：挿入
　score.insert(2, 90)

- remove(値)：削除
　score.remove(75)

- clear()：全削除
　score.clear()

#### サンプル
```python
pokemon = ["ピカチュウ", "ホゲータ", "クワッス", "ニャオハ"]

print(pokemon[2]) # クワッスと出力
print(pokemon[:3]) #[0], [1], [2]の要素が出力

pokemon.append("パチリス")
print(pokemon) # パチリスが追加される

pokemon.insert(1, "ゲンガー")
print(pokemon) # ゲンガーが[1]番目に追加される

pokemon.remove("ゲンガー")
print(pokemon)

pokemon.clear()
print(pokemon) # 全削除
```

---

### 分岐

**if文**
```md
if 条件式 :
    処理1
else :
    処理2
```
- インデント（字下げ）の範囲を実行
- どちらかの処理しか実行されない
- else節は省略できる

```md
if 条件式 :
    処理1
elif 条件式 :
    処理2
else:
    処理3
```
- else if~ の省略形elif ~ にする
- どちらかの処理しか実行されない
- 上から条件判定が行われる


#### フローチャート : 信号機の分岐
![](/img/分岐.png)

```python
color = input("信号の色を入力してください：")

if color == "青":
    print("気を付けて渡りましょう")
elif color == "黄":
    print("危険です！渡るのをやめて止まりましょう")
else:
    print("危険！危険！子どもが見てます。止まりましょう！")
```

---

### while文 (くり返し)

**変数を用意！**
```md
# くり返しの条件で使用する変数
（例）i

# 変数を用意
i = 10

# 条件式を満たす分だけくり返し
while 条件式(iを使用) :

# くり返したい処理をインデント付きで書く
    処理1

# 変数の更新をインデント付きで書く
    処理2
```
#### 繰り返しフローチャート
![](/img/繰り返し.png)

#### サンプルプログラム
```python
i = 10 # 条件で使用する変数

while i > 0 : # 条件式を満たす分だけくり返し
    print(i)  # 処理1
    i = i - 1 # 処理2
```

---

### for文（繰り返しオブジェクト）
```python
# 構文
for 変数名 in range(終了値):
    処理

または

for 変数名 in 繰り返しオブジェクト:
    処理
```
#### rangeの3パターン
```md
# ➀range(終了値)
→0から(終了値-1)回繰り返す
```
```python
for i in range(5):
    print(i)
```
```md
0
1
2
3
4
```
```md
# ➁range(開始値, 終了値)
→開始値から(終了値-1)回繰り返す
```
```python
for i in range(1, 10):
    print(i)
```
```md
1
2
3
4
5
6
7
8
9
```
```md
# ➂range(開始値, 終了値, ステップ数)
→開始値から(終了値-1)までステップ数間隔で繰り返す
```
```python
for i in range(1, 10, 2):
    print(i)
```
```md
1
3
5
7
9
```
---
```md
# 繰り返しオブジェクト（イテラブル）
➀配列（リスト）：複数のデータを順番に持つ
例：　list1 = [1, 2, 3, 4, 5]
~~
for i in [1, 2, 3, 4, 5]:

~~

➁タプル：リストに似るが、変更できない
例： turple1 = (1, 2, 3, 4, 5)
~~
for i in (1, 2, 3, 4, 5):

~~

➂文字列：文字を1つずつ取り出す
例：　greeting = "Hello"
~~
for i in "Hello":

~~

➃辞書：keyとvalueを取り出せる
例：shop = {"apple": 3, "lemon": 5}
~~
for i, j in {"apple":3, "lemon":5}:

~~

➄集合：順番は無いが1つずつ取り出せる
例： set1 = {1, 2, 3, 4, 5}
~~
for i in {1, 2, 3, 4, 5}:

~~

➅enumerate()：インデックスと要素を取り出せる
~~
for x, y in enumerate([1, 2, 3, 4, 5]):

x：インデックス。野球の打順のようなもの。
y：要素。野球のバッターのようなもの。

~~
```
```md
👀フォーマット済み文字列リテラル
f-Strings

a = 10
b = 50

# エラーが出る場合
print(a + "個のリンゴと" + b + "個のレモン")
→int と strが混ざっているのでエラー

# f-stringsを使うと解消できます！
print(f"{a}個のリンゴと{b}個のレモン")
```
---

### break文：ループの強制終了
```python
for i in range(10): # 0~9まで増える
    if i == 5:      # iが5と等しいならば
        break       # ループの強制終了

    print(i)
```

### continue文：飛ばして継続
```python
for i in range(10):  # 0~9まで
    if i == 5:       # iが5と等しいならばTrue
        continue     # 飛ばして継続

    print(i)
```


#### サンプルプログラム
Q. 1から100までの値を出力するプログラムを書きなさい。
ただし、3の倍数の時は"Fizz"を、5の倍数の時は"buzz"を、3と5の倍数の時は"FizzBuzz"と出力するようにしなさい。
```python
for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        print("FizzBuzz")
    elif i % 3 == 0:
        print("Fizz")
    elif i % 5 == 0:
        print("Buzz")
    else:
        print(i)
```
Q. かけ算九九のプログラムを書きなさい。
```python
for i in range(1, 10):
    for j in range(1, 10):
        if j == 9:
            print(i * j)
        else:
            print(i * j, end=",")
```
### RPGマップ

### サンプルプログラム
```python
# 10 × 10 のRPGマップを考える
# アイテム：@, 壁：#, 建て物：$
# if文の条件を使うか、または自分の置きたい場所に置くにはどうすればよいか？

for i in range(1, 11):
    for j in range(1, 11):
        # --- 壁で周りを囲む ---
        if i == 1 or i == 10 or j == 1 or j == 10:
            print("#", end=" ")

        # --- 建物を中央に配置する ---
        elif 4 < i <= 6 and 4 < j <= 6:
            print("$", end=" ")
        
        # --- アイテムを(8,8)に置く ---
        elif i == 8 and j == 8:
            print("@", end=" ")

        else:
            print(".", end=" ")

    print()
```

### 完成イメージ
![](img/RPG.png)

---

### 関数：いくつかの処理のまとまり

```md
# 組込み関数
print(), input(), int(), str() etc...

# ユーザー定義関数
# 書き方と呼び出し方
def 関数名():
    処理

関数名()
```
```python
def greet():
    print("こんにちは")

greet()
```
👀関数のよいところ
- 何度でも呼び出せる
- 処理をまとめることができる
- 処理結果を他でも使用できる

#### 引き数：関数の中で使える「材料」

ポイント
- 関数の受け皿の順番通りに渡される
- 渡された引き数は関数の処理の中で必ず使用しなければならない（1回は登場させよ！）
- 使わない材料は渡してはいけない
- 関数の受け皿の数だけ渡すことができる
- 関数の受け皿よりも少ない数渡すことはできない

```python
def add(a, b):
    c = a + b
    print(c)

add(10, 20)  # 10がaに渡され、20がbに渡される
```

#### 戻り値：関数の処理結果として外に出る値

ポイント
- 外に出た後の行き先を整えてあげる必要がある
- 行き先が無い状態で外に出すことができない

```python
def add(a, b):
    c = a + b
    return c

result = add(10, 20)
```



