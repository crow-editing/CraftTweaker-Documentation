# Constructor de objetos básico

El constructor básico para elementos, también llamado por [mods.contenttweaker.item.basic.ItemBuilderBasic#build](/mods/contenttweaker/API/item/basic/ItemBuilderBasic/#build). No tiene propiedades especiales, existe.

Esta clase fue añadida por un mod con mod-id `contenttweaker`. Necesitas tener este mod instalado si quieres usar esta caracteristica.

## Importar la clase
Puede ser requerido que importes el paquete si encuentras algun problema (como crear un Array).
```zenscript
mods.contenttweaker.item.basic.ItemBuilderBasic
```

## Interfaces implementadas
ItemBuilderBasic implementa las siguientes interfaces. Esto significa que cualquier método disponible también puede ser usado en esta clase.
- [mods.contenttweaker.api.IIsBuilder](/mods/contenttweaker/API/api/IIsBuilder)
- [mods.contenttweaker.item.ItemTypeBuilder](/mods/contenttweaker/API/item/ItemTypeBuilder)

## Métodos
### construir

Instruye CoT para construir lo que se supone que este constructor está construyendo.

```zenscript
new ItemBuilder().withType<ItemBuilderBasic>().build(resourceLocation as String);
new ItemBuilder().withType<ItemBuilderBasic>().build("my_awesome_block");
```

| Parámetro            | Tipo   | Descripción                              |
| -------------------- | ------ | ---------------------------------------- |
| ubicacin del recurso | Cadena | La ruta de recursos para dar este bloque |



