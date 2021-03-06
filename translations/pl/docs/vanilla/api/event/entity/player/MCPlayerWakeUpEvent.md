# MCPlayerWakeUpEvent

Ta klasa została dodana przez moda z mod-id `crafttweaker`. Więc musisz zainstalować tę modyfikację, jeśli chcesz używać tej funkcji.

## Importowanie klasy
Może być wymagane zaimportowanie pakietu, jeśli napotkasz jakiekolwiek problemy (np. rzucanie tablicy), tak aby były bezpieczne niż przepraszamy i dodaj import.
```zenscript
Zdarzenie crafttweaker.api.event.entity.player.MCPlayerWakeUps
```

## Konstruktorzy
```zenscript
nowe crafttweaker.api.event.entity.player.MCPlayerWakeUpEvent(handler jako funkcja.Consumer<crafttweaker.api.event.entity.player.MCPlayerWakeUpEvent>);
```
| Parametr | Typ                                                                                                                                  | Opis             |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------ | ---------------- |
| handler  | Funkcja Konsumenta<[crafttweaker.api.event.entity.player.MCPlayerWakeUpEvent](/vanilla/api/event/entity/player/MCPlayerWakeUpEvent)> | Nie podano opisu |



## Metody
### getEntityPlayer

Zwraca [crafttweaker.api.entity.player.MCPlayerEntity](/vanilla/api/entity/player/MCPlayerEntity)

```zenscript
myMCPlayerWakeUpEvent.getEntityPlayer();
```

### getPlayer

Zwroty: `Gracz`

Zwraca [crafttweaker.api.entity.player.MCPlayerEntity](/vanilla/api/entity/player/MCPlayerEntity)

```zenscript
myMCPlayerWakeUpEvent.getPlayer();
```

### wynik

Określa, czy to zdarzenie oczekuje znaczącej wartości wyniku. Uwaga: Zdarzenia z adnotacją HasResult będą automatycznie dodane, aby zwrócić true.

Zwraca wartość logiczną

```zenscript
myMCPlayerWakeUpEvent.hasResult();
```

### anulowalne

Określ czy ta funkcja jest w ogóle anulowalna. Zwroty: `Jeśli dostęp do setCanceled powinien być dozwolony
 Uwaga:
 Zdarzenia z anulowaną adnotacją będą automatycznie dodawane do tej metody, aby zwrócić true.`

Zwraca wartość logiczną

```zenscript
myMCPlayerWakeUpEvent.isCancelable();
```

### Anulowane

Określ czy to wydarzenie jest anulowane i powinno przestać wykonywać. Zwroty: `Aktualnie anulowany stan`

Zwraca wartość logiczną

```zenscript
myMCPlayerWakeUpEvent.isCanceled();
```

### Anulowane

```zenscript
myMCPlayerWakeUpEvent.setCanceled(anuluj jako boolean);
```

| Parametr | Typ     | Opis             |
| -------- | ------- | ---------------- |
| anuluj   | boolean | Nie podano opisu |


### [PLACEHOLDER] shouldSetSpawn

Wskazuje, czy uśpienie gracza zostało uznane za udane. W wanilii jest to używane do określenia, czy fragment spawnu ma być ustawiony na pozycję łóżka.

Zwraca wartość logiczną

```zenscript
myMCPlayerWakeUpEvent.shouldSetSpawn();
```

### aktualizuj Świat

Wskazuje, czy serwer powinien być powiadamiany o zmianach trybu uśpienia. Będzie to fałszywe tylko wtedy, gdy serwer zostanie już uznany za 'aktualny', ponieważ na przykład zainicjował połączenie.

Zwraca wartość logiczną

```zenscript
myMCPlayerWakeUpEvent.updateWorld();
```

### Wybudzanie natychmiast

Używane do animacji obudzania. Jest to fałszywe, jeśli gracz jest uważany za "śpiący", a nakładka powinna powoli zanikać.

Zwraca wartość logiczną

```zenscript
myMCPlayerWakeUpEvent.wakeNatychmiastowo();
```


