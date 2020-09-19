# Получение `последовательности`с

## Обзор
Получение `Последовательности` представляет собой двухэтапный процесс: сначала необходимо получить ссылку на последовательного конструктора правильного типа, затем вызовы конструктора, передавая либо список элементов данного типа, либо готовый массив данного типа завершит процесс строительства.

Некоторые интеграции CraftTweaker также могут обеспечить способ получения `последовательности` либо напрямую, либо методом. В этом случае нет необходимости делать вызовы конструкторов. С другой стороны, общий тип не будет явно указан , требуя от пользователя написать ментальную заметку о возвращаемом типе.

## Шаг 1: Конструктор
Конструктор `Последовательность` выполняется специальным обработчиком скобок, который имеет следующий синтаксис:

```zenscript
<sequence:CLASSNAME>
```

В вышеприведенном сниппете, `КЛАССИМЯ` представляет либо короткое, либо полное имя класса, для которого эта последовательность будет обобщена. В простых словах это будет определять, какой тип элементов последовательность сможет хранить при вызове конструктора.

Рассмотрим следующие два примера:

```zenscript
<sequence:IItemStack> # 1
<sequence:crafttweaker.item.IIngredient> # 2
```

Выражение последовательности, отмеченное `# 1` возвращает ссылку конструктору для последовательности, которая сможет держать экземпляры `IItemStack`. Обратите внимание, что для работы этого класса требуется импортировать его в текущий скрипт.

Выражение последовательности, отмеченное `# 2` , возвращает ссылку конструктору для последовательности, которая сможет держать любой тип `IIngredient`, означая, что он будет принимать `IItemStack`с, а также `IOreDictEntr`ies или любые другие пользовательские `IIngredient` реализация.

**ВАЖНО:** Этот начальный тип будет влиять только на текущий тип последовательности. Всегда возможно изменить тип сохраненный в этой последовательности позже через любой `последовательность`-type-converting вызовов, такие как `карта`. Более подробная информация доступна в [документации класса](/Mods/Boson/Sequences/Docs/).

## Шаг 2: Вовлечение конструктора
Поскольку обработчики скобок не вызывают конструктора, а просто ссылаются на него, теперь необходимо напрямую вызвать конструктор . Это можно сделать с помощью обычного синтаксиса вызова метода, за исключением того, что это делается через брекет-обработчик и не имя метода.

Конструктор последовательности является переменной, что означает, что он может принять любое количество аргументов, до тех пор, пока они все общего типа , указанного в ссылках конструктора. Например, обработчик скобков `<sequence:IItemStack>` не сможет принять `<ore:ingotCopper>` в своем конструкторе, поскольку `IOreDictEntry` не является `IItemStack`.

Конструктор не может давать никаких аргументов, в этом случае последовательность будет пустой.

Кроме того, можно сами представить массив или ссылку на массив либо в виде метода либо переменной. В этом случае массив будет принят, только если тип соответствует `CLASSNAME[]`, где `CLASSNAME` - это имя типа объектов в последовательности. Обратите внимание, что это поведение **может потребовать включить** экспериментальный флаг. Обратитесь к к [экспериментальному процессору флагов](/Mods/Boson/Preprocessor/Exp/) для получения дополнительной информации.

Ниже приведен сниппет кода, который показывает, как вышеуказанное применяется в коде.

```zenscript
val emptySequence = <sequence:string>();
val sequenceWithStacks = <sequence:IItemStack>(<minecraft:iron_ingot>, <minecraft:gold_nugget>, <minecraft:apple>);
val sequenceOfRecipes = <sequence:ICraftingRecipe>(рецепты. ll); # требуется указать -Esao
```

## Что дальше?
Now that the `Sequence` has been buily, refer to [the class documentation](/Mods/Boson/Sequences/Docs/) for a list of supported methods.