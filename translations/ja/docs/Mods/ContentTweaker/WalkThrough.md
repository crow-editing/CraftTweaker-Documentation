# ウォークスルー

## インストール後

First things first, before starting to create Blocks and such, it is suggested you run Minecraft at least once with ContentTweaker installed. これにより、ContentTweakerは必要なリソースフォルダを作成できます。

## 重要なフォルダ

ContentTweakerはMinecraftディレクトリに追加のフォルダ「リソース」を作成する必要があります。 The resources folder will be where all models, textures, and language files will be found. このフォルダの詳細は後で説明します。 The "scripts" folder added by CraftTweaker is where you should put all ContentTweaker scripts, however ContentTweaker scripts should begin with ```#loader contenttweaker``` ファイルの上部にあります。

## 最初のブロック

So for the best example of how ContentTweaker's content works, I'll be showing you one of the basic content pieces you will be creating, a block. There is other content that can be created, but I won't be including them in this walk-through. まず最初に、例として使うブロックのスクリプトを見てみましょう。 Explanation of these methods can be found at the Blocks Page.

```zenscript
#loader contenttweaker

import mods.contenttweaker.VanillaFactory;
import mods.contenttweaker.Block;

var antiIceBlock = VanillaFactory.createBlock("anti_ice", <blockmaterial:ice>);
antiIceBlock.setLightOpacity(3);
antiIceBlock.setLightValue(0);
antiIceBlock.setBlockHardness(5.0);
antiIceBlock.setBlockResistance(5.0);
antiIceBlock.setToolClass("pickaxe");
antiIceBlock.setToolLevel(0);
antiIceBlock.setBlockSoundType(<soundtype:snow>);
antiIceBlock.setSlipperiness(0.3);
antiIceBlock.register();
```

これにより Minecraft の Ice Block と少し似たような動作をするブロックが作成されます。 You will want to put this script in the 'scripts' folder, following the same rules as in CraftTweaker's scripts.

## リソース

You will also need to take a .png file and put it into 'resources/contenttweaker/textures/blocks' (This folder should be created for you, if you have run ContentTweaker already) The name of the file should match the name you put into createBlock, which in this case is 'anti_ice'. If you are planning on using a default cube shape with the block, ContentTweaker will generate the model jsons needed for it to function correctly.

これの他の部分は言語ファイルになります。 ContentTweaker will have already generated the en_us.lang file you will need to a line that will look like `tile.contenttweaker.<block_name>.name=Block name` or in our case with the AntiIce it will be `tile.contenttweaker.anti_ice.name=Anti Ice`. With both lang and texture filed in, you should be able to load up the game and see your block which will have a model, texture, and name.