# ページ遷移について

flutter上でページ遷移を実装するためには`Navigation`と`Router`という2つの選択肢がある。
選択基準として[複雑なDeepLinkがあるかどうかで判断するとよいとされている。](https://docs.flutter.dev/ui/navigation)

|複雑なDeepLink|Navigation|Router|
|---|---|---|
|なし|✅||
|あり|✅|✅|

## Deep linkとは
「アプリを開く」だけでなく「特定の場所のUIを開く」リンクのこと。

## 実装

ナビゲーションの実装をするときは以下のような形で実装することができる。

```dart
// ページ遷移
Navigator.push(
    context,
    MaterialPageRoute(builder: (context) => const SecondRoute()),
)

// ページ戻り
Navigator.pop(
   context 
)
```