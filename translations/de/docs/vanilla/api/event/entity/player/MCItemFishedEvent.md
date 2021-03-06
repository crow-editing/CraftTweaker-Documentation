# MCItemFishedEvent

Diese Klasse wurde von einer Mod mit mod-id `crafttweaker` hinzugefügt. Wenn Sie diese Funktion nutzen möchten, müssen Sie diese Mod installiert haben.

## Diese Klasse importieren
Es kann erforderlich sein, dass Sie das Paket importieren, wenn Sie irgendwelche Probleme haben (wie zum Beispiel ein Array zu bearbeiten), also besser sicher sein als bedauern und fügen Sie den Import.
```zenscript
crafttweaker.api.event.entity.player.MCItemFishedEvent
```

## Konstrukteure
```zenscript
neue crafttweaker.api.event.entity.player.MCItemFishedEvent(Handler als Funktion.Verbraucher<crafttweaker.api.event.entity.player.MCItemFishedEvent>);
```
| Parameter | Type                                                                                                                            | Beschreibung                 |
| --------- | ------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| handler   | function.Consumer<[crafttweaker.api.event.entity.player.MCItemFishedEvent](/vanilla/api/event/entity/player/MCItemFishedEvent)> | Keine Beschreibung angegeben |



## Methoden
### beschädigter RodBy

```zenscript
myMCItemFishedEvent.damageRodBy(arg0 als int);
```

| Parameter | Type | Beschreibung                 |
| --------- | ---- | ---------------------------- |
| arg0      | int  | Keine Beschreibung angegeben |


### getEntityPlayer

Gibt [craftweaker.api.entity.player.MCPlayerEntity](/vanilla/api/entity/player/MCPlayerEntity) zurück

```zenscript
myMCItemFishedEvent.getEntityPlayer();
```

### getPlayer

Rückgaben: `Spieler`

Gibt [craftweaker.api.entity.player.MCPlayerEntity](/vanilla/api/entity/player/MCPlayerEntity) zurück

```zenscript
myMCItemFishedEvent.getPlayer();
```

### getRodschaden

Erhalte den Schaden, den die Stäbe erleidet. Gibt zurück: `Der Schaden, den die Stange erleidet,`

Retouren Int

```zenscript
myMCItemFishedEvent.getRodDamage();
```

### hasergebnis

Legt fest, ob dieses Ereignis einen signifikanten Ergebniswert erwartet. Hinweis: Ereignisse mit der HasResult-Anmerkung werden diese Methode automatisch hinzugefügt, um wahr zurückzugeben.

Rückgabewert boolesch

```zenscript
myMCItemFishedEvent.hasResult();
```

### isabbrechbar

Legen Sie fest, ob diese Funktion überhaupt abgebrochen werden kann. Gibt zurück: `Wenn der Zugriff auf setCanceled erlaubt sein sollte
 Hinweis:
 Ereignisse mit der abbrechbaren Anmerkung werden diese Methode automatisch hinzugefügt, um true zurückzugeben.`

Rückgabewert boolesch

```zenscript
myMCItemFishedEvent.isCancelable();
```

### ist abgebrochen

Legen Sie fest, ob dieses Ereignis abgebrochen wird und nicht mehr ausgeführt werden soll. Rückgabe: `Der aktuell abgebrochene Status`

Rückgabewert boolesch

```zenscript
myMCItemFishedEvent.isCanceled();
```

### abgebrochen

```zenscript
myMCItemFishedEvent.setCanceled(abbrechen als boolean);
```

| Parameter | Type    | Beschreibung                 |
| --------- | ------- | ---------------------------- |
| abbrechen | boolean | Keine Beschreibung angegeben |



