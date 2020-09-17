# InitialInventory

## 説明

このmodでは、初めてワールドに参加したプレイヤーにアイテムを提供できる機能を追加しています。他の一部のmodにおいて、プレイーが初めてワールドに参加したときに本などを与えるのと同じようなものです。

## パッケージ
`mods.initialinventory.InvHandler`

## 開始アイテムを追加中

これにより、プレイヤーがワールドに参加した際に、プレイヤーのインベントリにアイテムが追加されます。

パラメータは次のとおりです。


Param: `key`

Type: `String`

説明:

アイテムを与えるかどうかを決定する際に使用します。 キー(key)は任意の文字列に設定することができ、その取っ掛かりというのは、以前にそのプレイヤーにアイテムセットが与えられたかどうかの判定をすることです。

これは、別のキーを使用することで、開始時のアイテムを、後からさらに追加するようなmodpackにおいて役に立ちます。すでにpackをプレイし始めているプレイヤーも、引き続きそれらのアイテムを受け取ることが可能になります。 例は、以下のようなものになります:

開始時のアイテム, key"1"としてダイヤモンドを追加します。ワールドに参加したプレイヤーは、ダイヤモンドを受け取ることができます。

開始時のアイテム, key"2"としてリンゴを追加します。ワールドに参加すると、プレイヤーはリンゴを受け取ることができますが、ダイヤモンドをもう一度受け取ることはありません。

新たにワールドを作成した場合、プレイヤーはリンゴとダイヤモンドの両方を受け取ることができます。

param: `item`

Type `IItemStack`

説明:

プレイヤーが参加した際に、プレイヤーに与えられるアイテムです。

パラメータ: `index`

Type: `int`

説明:

オプションであるこの整数は、アイテムが与えられる場所を定義するものです。与えるアイテムを防具スロットのようなインベントリスロットに配置する場合などに使用できます。

省略した場合、デフォルトでは-1に設定されます。つまり、使用可能な最初のスロットに配置されるか、すでにインベントリにある別の同じアイテムと一緒にまとめられます。


## 例

```zenscript
//mods.initialinvHandler.addStartingItem(String key, IItemStack item, Optional int index);
mods.initialinvHandler.addStartingItem("apples", <item:minecraft:apple>);
mods.initialinvHandler.addStartingItem("apples", <item:minecraft:golden_apple>, 5);
```

