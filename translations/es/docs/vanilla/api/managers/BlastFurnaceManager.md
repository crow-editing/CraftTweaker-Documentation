# Gestor de horno explosivo



Esta clase fue añadida por un mod con la ID  `crafttweaker`. Necesitas tener este mod instalado si quieres usar esta caracteristica.

## Importar la clase
Puede ser requerido que importes el paquete si encuentras algun problema (como crear un Array).
```zenscript
crafttweaker.api.Gestor de BlastFurnace
```

## Interfaces implementadas
BlastFurnaceManager implementa las siguientes interfaces. Esto significa que cualquier método disponible también puede ser usado en esta clase.
- [crafttweaker.api.registries.ICookingRecipeManager](/vanilla/api/managers/ICookingRecipeManager)

## Métodos
### addReceta

Añade una receta basada en determinados parámetros.

```zenscript
blastFurnace.addRecipe(nombre como String, salida como crafttweaker.api.item.ItemStack, entrada como crafttweaker.api.item.IIngredient, xp as float, cookTime as int);
blastFurnace.addRecipe("wool2diamond", <item:diamond>, <tag:minecraft:wool>, 1.0, 0);
```

| Parámetro      | Tipo                                                                | Descripción                            |
| -------------- | ------------------------------------------------------------------- | -------------------------------------- |
| nombre         | Cadena                                                              | Nombre de la nueva receta              |
| salida         | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | Salida de la pila de ítem de la receta |
| input          | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | Entrada de IIngrediente de la receta   |
| xp             | flotante                                                            | cuánto xp obtiene el jugador           |
| hora de cocina | int                                                                 | cuánto tiempo se tarda en cocinar      |


### eliminar receta

Elimina una receta basada en su salida y entrada.

```zenscript
blastFurnace.removeRecipe(output as crafttweaker.api.item.IIItemStack, input as crafttweaker.api.item.IIngredient);
blastFurnace.removeRecipe(<item:minecraft:diamond>, <tag:minecraft:wool>);
```

| Parámetro | Tipo                                                                | Descripción                           |
| --------- | ------------------------------------------------------------------- | ------------------------------------- |
| salida    | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | Salida de ItemStack de la receta.     |
| input     | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | IIngrediente de la receta a eliminar. |



