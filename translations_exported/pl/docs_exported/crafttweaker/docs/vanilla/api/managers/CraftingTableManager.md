# CraftingTableManager



Ta klasa została dodana przez moda z mod-id `crafttweaker`. Więc musisz zainstalować tę modyfikację, jeśli chcesz używać tej funkcji.

## Importowanie klasy
Może być wymagane zaimportowanie pakietu, jeśli napotkasz jakiekolwiek problemy (np. rzucanie tablicy), tak aby były bezpieczne niż przepraszamy i dodaj import.
```zenscript
crafttweaker.api.CraftingTableManager
```

## Zaimplementowane interfejsy
CraftingTableManager implementuje następujące interfejsy. Oznacza to, że każda dostępna dla nich metoda może być również stosowana w tej klasie.
- [crafttweaker.api.brackets.CommandStringDisplayable](/vanilla/api/brackets/CommandStringDisplayable)
- [crafttweaker.api.registries.IRecipeManager](/vanilla/api/managers/IRecipeManager)

## Metody
### addJSONRecipe

Dodaje przepis na podstawie podanego IDaty. Dostarczone IData powinny reprezentować JSON pakietu DataPack, co pozwala na rejestrowanie przepisów dla każdego pakietu DataPack wspierającego systemy IRecipeType.

```zenscript
craftingTable.addJSONRecipe(nazwa jako String, data as crafttweaker.api.data.IData);
craftingTable.addJSONRecipe("recipe_name", {składnik:{item:<item:minecraft:gold_ore>.registryName},result:<item:minecraft:cooked_porkchop>.registryName,Doświadczenie:0.35 jako pływak, czasu gotowania:100});
```

| Parametr | Typ                                                    | Opis                          |
| -------- | ------------------------------------------------------ | ----------------------------- |
| Nazwa    | Ciąg znaków                                            | nazwa przepisu                |
| dane     | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | dane reprezentujące plik json |


### dodany

Dodaje kształt przepisu do stołu rzemieślniczego

```zenscript
craftingTable.addShaped(recipeName as String, output as crafttweaker.api.item.IItemStack, składniki jak crafttweaker.api.item.IIngredient[][], recipeFunction as crafttweaker.api.recipe.RecipeFunctionMatrix);
craftingTable.addShaped("recipe_name", <item:minecraft:dirt>, [[<item:minecraft:diamond>], [<tag:minecraft:wool>]);
craftingTable, ddShaped("recipe_name", <item:minecraft:dirt>, [[<item:minecraft:diamond>], [<tag:minecraft:wool>]], (zwykle jako IItemStack, wejścia jako IItemStack[][]) => {if(wejścia[0][0]. isplayName == "całkowicie prawdziwy blok diamentowy" ){return usualOut;}return <item:minecraft:clay>.setDisplayName("Diamond");});
```

| Parametr        | Typ                                                                                      | Opis                                                                                                                                     | Opcjonalnie | Wartość domyślna |
| --------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ----------- | ---------------- |
| nazwa receptury | Ciąg znaków                                                                              | nazwa przepisu do dodania.                                                                                                               | fałszywy    | `null`           |
| wyjście         | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)                        | output [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)                                                                 | fałszywy    | `null`           |
| składniki       | [crafttweaker.api.item.ISkładnik](/vanilla/api/items/IIngredient)[][]                    | tablica tablicy [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) dla wejść                                            | fałszywy    | `null`           |
| funkcja formuły | [crafttweaker.api.recipe.RecipeFunctionMatrix](/vanilla/api/recipe/RecipeFunctionMatrix) | opcjonalne [crafttweaker.api.recipe.RecipeFunctionMatrix](/vanilla/api/recipe/RecipeFunctionMatrix) dla bardziej zaawansowanych warunków | prawda      | `null`           |


### dodaj ShapedMirrored

Dodaje lustrzany przepis w kształcie litery do stołu rzemieślniczego

```zenscript
craftingTable.addShapedMirrored(recipeName as String, output as crafttweaker.api.item.IItemStack, składniki jak crafttweaker.api.item.IIngredient[][], recipeFunction as crafttweaker.api.recipe.RecipeFunctionMatrix);
craftingTable.addShapedMirrored("recipe_name", <item:minecraft:dirt>, [[<item:minecraft:diamond>], [<tag:minecraft:wool>]]);
tworzenie. ddShapedMirrored("recipe_name", <item:minecraft:dirt>, [[<item:minecraft:diamond>], [<tag:minecraft:wool>]], (zwykle jako IItemStack, wejścia jako IItemStack[][]) => {if(wejścia[0][0]. isplayName == "całkowicie prawdziwy blok diamentowy" ){return usualOut;}return <item:minecraft:clay>.setDisplayName("Diamond");});
```

| Parametr        | Typ                                                                                      | Opis                                                                                                                                     | Opcjonalnie | Wartość domyślna |
| --------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ----------- | ---------------- |
| nazwa receptury | Ciąg znaków                                                                              | nazwa przepisu do dodania.                                                                                                               | fałszywy    | `null`           |
| wyjście         | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)                        | output [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)                                                                 | fałszywy    | `null`           |
| składniki       | [crafttweaker.api.item.ISkładnik](/vanilla/api/items/IIngredient)[][]                    | tablica tablicy [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) dla wejść                                            | fałszywy    | `null`           |
| funkcja formuły | [crafttweaker.api.recipe.RecipeFunctionMatrix](/vanilla/api/recipe/RecipeFunctionMatrix) | opcjonalne [crafttweaker.api.recipe.RecipeFunctionMatrix](/vanilla/api/recipe/RecipeFunctionMatrix) dla bardziej zaawansowanych warunków | prawda      | `null`           |


### addShapeless

Dodaje bezkształtny przepis do stołu rzemieślniczego

```zenscript
craftingTable.addShapeless(recipeName as String, output as crafttweaker.api.item.IItemStack, składniki jak crafttweaker.api.item.IIngredient[], recipeFunction as crafttweaker.api.recipe.RecipeFunctionArray);
craftingTable.addShapeless("recipe_name", <item:minecraft:dirt>, [<item:minecraft:diamond>, <tag:minecraft:wool>]);
craftingTable, ddShapeless("recipe_name", <item:minecraft:dirt>, [<item:minecraft:diamond>, <tag:minecraft:wool>], (zwykle jako IItemStack, wejścia jako IItemStack[]) => {if(wejścia[0]. isplayName == "całkowicie prawdziwy blok diamentowy" ){return usualOut;}return <item:minecraft:clay>.setDisplayName("Diamond");});
```

| Parametr        | Typ                                                                                    | Opis                                                                                                                                   | Opcjonalnie | Wartość domyślna |
| --------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | ----------- | ---------------- |
| nazwa receptury | Ciąg znaków                                                                            | nazwa przepisu do dodania.                                                                                                             | fałszywy    | `null`           |
| wyjście         | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)                      | output [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)                                                               | fałszywy    | `null`           |
| składniki       | [crafttweaker.api.item.ISkładnik](/vanilla/api/items/IIngredient)[]                    | tablica [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) dla wejść                                                  | fałszywy    | `null`           |
| funkcja formuły | [crafttweaker.api.recipe.RecipeFunctionArray](/vanilla/api/recipe/RecipeFunctionArray) | opcjonalne [crafttweaker.api.recipe.RecipeFunctionArray](/vanilla/api/recipe/RecipeFunctionArray) dla bardziej zaawansowanych warunków | prawda      | `null`           |


### getRecipeByName

Typ zwrotu: [crafttweaker.api.recipes.WrapperRecipe](/crafttweaker/api/recipes/WrapperRecipe)

```zenscript
craftingTable.getRecipeByName(nazwa jako String);
```

| Parametr | Typ         | Opis             |
| -------- | ----------- | ---------------- |
| Nazwa    | Ciąg znaków | Nie podano opisu |


### getRecipesByOutput

Typ zwracania: Lista&lt;[crafttweaker.api.recipes.WrapperRecipe](/crafttweaker/api/recipes/WrapperRecipe)&gt;

```zenscript
craftingTable.getRecipesByOutput(output as crafttweaker.api.item.IIngredient);
```

| Parametr | Typ                                                              | Opis             |
| -------- | ---------------------------------------------------------------- | ---------------- |
| wyjście  | [crafttweaker.api.item.Składnik](/vanilla/api/items/IIngredient) | Nie podano opisu |


### usuń wszystko

Usuń wszystkie przepisy z tego rejestru

```zenscript
craftingTable.removeAll();
```

### usuń ByModid

Usuń przepis na podstawie modyfikacji nazwy rejestru

```zenscript
craftingTable.removeByModid(modid jako String);
craftingTable.removeByModid("minecraft");
```

| Parametr | Typ         | Opis                         |
| -------- | ----------- | ---------------------------- |
| modid    | Ciąg znaków | modid przepisów do usunięcia |



Usuń przepis na podstawie modida nazwy rejestru z dodanym sprawdzianem wykluczenia, dzięki czemu możesz usunąć cały mod poza kilkoma określonymi.

```zenscript
craftingTable.removeByModid(modid jako String, wyklucz jako crafttweaker.api.recipe.RecipeFilter);
craftingTable.removeByModid("minecraft", (nazwa jako string) => {return name == "orange_wool";});
```

| Parametr | Typ                                                                | Opis                             |
| -------- | ------------------------------------------------------------------ | -------------------------------- |
| modid    | Ciąg znaków                                                        | modid przepisów do usunięcia     |
| wyklucz  | [crafttweaker.api.recipe.Filter](/vanilla/api/recipe/RecipeFilter) | receptury na wyjście z usuwania. |


### removeByName

Usuń przepis na podstawie nazwy rejestru

```zenscript
craftingTable.removeByName(nazwa jako String);
craftingTable.removeByName("minecraft:furnace");
```

| Parametr | Typ         | Opis                                 |
| -------- | ----------- | ------------------------------------ |
| Nazwa    | Ciąg znaków | nazwa rejestru przepisu do usunięcia |


### removeByRegex

Usuń przepis na podstawie regex

```zenscript
craftingTable.removeByRegex(regex as String);
craftingTable.removeByRegex("\\d_\\d");
```

| Parametr | Typ         | Opis                           |
| -------- | ----------- | ------------------------------ |
| regex    | Ciąg znaków | regex do dopasowania przeciwko |


### usuń Przepis

Usuń przepis na podstawie jego wyjścia.

```zenscript
craftingTable.removeRecipe(wyjście jako crafttweaker.api.item.IItemStack);
craftingTable.removeRecipe(<item:minecraft:glass>);
```

| Parametr | Typ                                                               | Opis             |
| -------- | ----------------------------------------------------------------- | ---------------- |
| wyjście  | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | wyjście przepisu |



## Właściwości

| Nazwisko  | Typ         | Posiada Getter | Ma ustawienie |
| --------- | ----------- | -------------- | ------------- |
| polecenie | Ciąg znaków | prawda         | fałszywy      |

