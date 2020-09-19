# IPotionBrewEvent

Событие продлевается всеми событиями, связанными с винтовой стендой, хотя и не на основе игрока, можно извлечь предметы из пивоварняной стенды.

## Импорт класса
Возможно, потребуется [импортировать](/AdvancedFunctions/Import/) класс, чтобы избежать ошибок.  
`импортировать crafttweaker.event.IPotionBrewEvent;`

## Что можно сделать с ними?

| ZenGetter | ZenSetter | type |
| --------- | --------- | ---- |
| `длина`   |           | int  |

## Методы

- [IItemStack](/Vanilla/Items/IItemStack/) `getItem()`

Возвращает IItemStack, содержащийся в списке элементов в указанном массиве. Возвращает пустой IItemStack, если указанный индекс превышает `длину`.

- `setItem(int,` [`IItemStack`](/Vanilla/Items/IItemStack/) `)`

Заменяет элемент в указанном индексе на указанный элемент. Если индекс больше длины массива предметов, ничего не произойдет.