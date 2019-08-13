# INSTRUKTIONER

## Krossa godisarna

Välkommen till spelet Crush Candy! Här ska vi krossa så många godisar vi kan genom att klicka på dem. Testa spelet genom att klicka på en godis. Om du vill starta om spelet klickar du på **restart** upp till vänster.

När du har testat klart är det dags att se om kan göra spelet roligare genom att ändra i koden som styr det. Lycka till!

----------------------------------------------------------------------------

## Hur skapas godisarna?

Om vi vill att datorn ska hoppa över en kod-rad kan vi göra om den till en kommentar. Det gör vi genom att skriva två bindestreck `--` i början av raden.

### Uppgift 1

- Testa att göra rad 4 i `candy_factory.script` till en kommentar.
- Starta om spelet genom att trycka på **restart**.
- Vad händer?


### Uppgift 2

- Ta bort bindestrecken på rad 4 i `candy_factory.script`.
- Testa att göra rad 9 i `candy_factory.script` till en kommentar. Kom ihåg att klicka på **restart** för att starta om spelet.
- Vad händer nu?

----------------------------------------------------------------------------

## Var skapas godisarna?

Just nu skapas godisar på samma ställe hela tiden. I `candy_factory.script` kan du se att godisens **x-position är 0** och **y-positionen är 0** när den skapas. Om x-positionen är **högre än 0** kommer godisen att placeras längre åt **höger**. Om x-positionen är **mindre än 0** kommer godisen att placeras längre åt **vänster**. Godisens y-position styr hur högt eller lågt godisen placeras.

![Bild på koordinatsystem](https://i.gyazo.com/0688fba747933d69b66205e460a4f1e5.png "Koordinatsystem")

I bilden ovan ser vi ett koordinatsystem som visar två punkter och deras x- och y-position. Den en punkten har x-positionen 3 och y-positionen 1 medan den andra punkten har x-positionen 1 och y-positionen 3. Kan du se vilken som är vilken?

### Uppgift 3

- Testa att ändra värdet på godisens x-position och y-position (i `candy_factory.script`) så att den skapas på någon annan plats. Varje gång du ändrat värdet så klickar du på **restart** för att köra den nya koden.
- Kan du skriva in ett värde så att godisen placeras utanför bilden?

Vi vill nu att godisarna ska hamna på olika ställen varje gång. Då behöver vi lära oss att använda `math.random()` för att få fram slumptal.

### Uppgift 4

- Testa att ändra så att x-positionen slumpas fram med hjälp av `math.random()`. Du kan göra det genom att använda koden nedan:

    ```
    position.x = math.random(0, 500)
    ```

    X-positionen kommer då att bli ett slumpat tal mellan **0** och **500**.

- Gör likadant för y-positionen.
- Testa att ändra på värdena **0** och **500** så att godisarna inte hamnar utanför kanten.

----------------------------------------------------------------------------

## Få en miljon poäng

När vi startar spelet så har du 0 poäng. Hur många poäng du startar med bestäms i skriptet som heter `points.gui_script`. Du kan öppna det genom att klicka på fliken precis över kodfönstret där det står `points.gui_script`

### Uppgift 5

- Testa att ändra rad 1 i `points.gui_script` så att du startar med mer än 0 poäng.
- Är det möjligt att starta med mindre än 0 poäng?

Varje gång du krossar en godis så får du ett poäng. Nu vill vi ändra så att du kan få olika många poäng.

### Uppgift 6

- Testa att ändra rad 9 i `points.gui_script` så att du får två poäng för varje godis du krossar.
- Ändra så att du förlorar ett poäng varje gång du krossar en godis (använd `-` för att subtrahera)
- Ändra så att du får dubbelt så många poäng varje gång du krossar en godis (använd `*` för att göra multiplikation).
- Ändra så att slumpen bestämmer hur många poäng du får. Använd `math.random()` på samma sätt som när vi placerade ut godisarna.

----------------------------------------------------------------------------

## Ändra texten

På rad 9 i `points.gui_script` uppdateras alltså hur många poäng du har. På rad 15 i `points.gui_script` ändras texten som syns i spelet. Texten som syns är en sammanslagning av strängen `"Points: "` och variabeln `points` som håller koll på hur många poäng vi har.

<details>
<summary>
<b>Läs mer om strängar</b>
</summary>
För datorn är det skillnad på texter och tal. Som vi sett är det inget konstigt när vi ska använda tal utan det går bra att skriva exempelvis

```
x = 5
y = 3958
```

Texter är lite speciella. För att datorn ska veta var som är texter måste vi använda citationstecken **""** runt texten, exempelvis

```
text = "Hej på dig"
name = "Nicolina"
```

I programmering brukar texter kallas för **strängar**.<br><br>
Om vi vill lägga ihop två strängar så använder vi två punkter `..`. Exempelvis

```
text = "My name is " .. "Jeff"
```

Då lägger datorn ihop strängarna så att de blir en sträng. Två punkter kan vi också använda för att lägga ihop en sträng och en siffra. Som exempelvis

```
text = "Poäng: " .. 193
```

eller

```
local points = 193
text = "Poäng: " .. points
```

</details>

### Uppgift 7

- Testa att ändra texten på rad 15 i `points.gui_script` så att det blir en annan text på skärmen.
- Testa att sätta citationstecken runt `points` så att det blir

    ```
    text = "Points: " .. "points"
    ```

- Vad händer och varför?


----------------------------------------------------------------------------

## Flygande godisar

Nu rör sig inte godisarna men vi skulle vilja göra så att de åtminstone börjar åka fram och tillbaka. Detta ska vi göra genom att ändra i koden i `candy_movement.script` som du hittar i fliken längst till höger ovanför kodfönstret. I skriptet finns det redan kod för att skapa en animation för godisarna men vi behöver aktivera den.

### Uppgift 8

- Aktiver animationen genom att göra så att rad 11 inte är en kommentar.


En animation innehåller flera inställningar och vi ska testa att ändra några av dem. Hastigheten på animationen bestäms av variabeln med namnet `animation_length`. `animation_length = 2` innebär att det ska ta två sekunder för animationen att köra ett varv.

### Uppgift 9

- Testa att ändra hastigheten på animationen så att den både går jättesnabbt och jättelångsamt.


En annan inställning som vi kan ändra på är hur långt godisen ska åka fram och tillbaka. Det styr vi genom att ändra värdet på `destination.x`. På rad 8 hämtar vi positionen som godisen har när den skapas och sparar den i en variabel med namn `destination`. På rad 9 ändrar vi slutpositionen för godisen så att x-värdet är till 100 pixlar åt höger genom att skriva `destination.x = destination.x + 100`.

### Uppgift 10

- Testa att ändra hur långt godisen åker fram och tillbaka.

Nu åker godisarna fram och tillbaka åt höger och vänster. Det är eftersom det bara är positionens x-värde som vi ändrar på. Om vi vill att godisen ska åka uppåt eller neråt istället så behöver vi ändra positionens y-värde.

### Uppgift 11

- Ändra så att godisen åker uppåt och neråt istället för åt höger och vänster. Gör det genom att byta ut **x** mot **y** på rad 9.



- Gör så att godisen både ändrar x-positionen och y-positionen. Då behöver du lägga till en rad som liknar rad 9 väldigt mycket men där vi bestämmer slutpositionens x-värde istället..


Alla godisar har nu samma animation och åker likadant. För att göra så att godisarna åker olika kan vi göra så att slutpositionen slumpas istället för att ha ett bestämt värde.

### Uppgift 12

- Gör så att godisens x-position och y-position slumpas genom att använda `math.random()`.



- Testa olika inställningar tills du är nöjd med animationerna. Du kan exempelvis också göra så att hastigheten för animationen slumpas.

----------------------------------------------------------------------------

## Skapa många godisar

Just nu skapas bara en godis i taget och varje gång du krossar en godis så skapas en ny. Som vi märkte tidigare så är det rad 4 i `candy_factory.script` som skapar den första godisen och rad 9 som skapar en godis när du krossat en annan. Nu ska vi skapa flera godisar samtidigt.

### Uppgift 13

- Gör så att två godisar skapas när spelet startas. För att skapa flera godisar kan vi kopiera den kod som skapar en godis: `create_candy()` och lägga den på en ny rad under rad 4. Då skulle en del av koden se ut så här:

    ```
    create_candy()
    create_candy()
    ```

- Gör så att två eller flera nya godisar skapas varje gång man krossar en godis.


Om vi vill skapa fem godisar när spelet startar skulle vi kunna upprepa `create_candy()` fem gånger och skriva:

```
function init(self)
  math.randomseed(os.time())
  math.random()
  create_candy()
  create_candy()
  create_candy()
  create_candy()
  create_candy()
end
```

Istället för att upprepa samma rad många gånger så kan vi använda en **for-loop**. Om vi vill skapa fem godisar när spelet startar skulle vi då kunna skriva:

```
function init(self)
  math.randomseed(os.time())
  math.random()
  for i=1,5 do
    create_candy()
  end
end
```

Det är talet **5** som bestämmer hur många gånger `create_candy()` ska upprepas och det talet kan du ändra till hur många godisar du vill ska skapas när spelet startar.

![Bild på for-loop](https://i.gyazo.com/fcd1a59e4edfbb4e1bf73deb0240b72c.png "For-loop")

### Uppgift 14

- Använd en **for-loop** så att **10** godisar skapas när spelet startar.

----------------------------------------------------------------------------

## Extrauppgifter

Bra jobbat! Nu har du lärt dig hur du själv kan programmera om ett spel så att fungerar mer som du vill.

Här finns några extrauppgifter som du kan göra om du har tid över. Vissa är lite kluriga så ha tålamod!

### Extrauppgift 1

- Gör så att texten på skärmen som visar hur många poäng du har inte uppdateras även fast du krossar en godis.

  <details>
    <summary>
    <b>Tips</b>
    </summary>
    Du kan få datorn att hoppa över en rad genom att göra om den till en kommentar. Läs mer om det i avsnittet som heter **Hur skapas godisarna?**.

  </details>

### Extrauppgift 2

- Gör så att texten på skärmen som beskriver hur många poäng du har säger **You have 0 points** när spelet startas. Siffran **0** ska uppdateras som vanligt när du krossar en godis.

  <details>
    <summary>
    <b>Tips</b>
    </summary>
    Använd `..` för att lägga ihop texter och tal eller texter och variabler. Läs mer om det i avsnittet som heter **Ändra texten**.

  </details>

### Extrauppgift 3

- Testa att ändra till andra typer av animationer genom att ändra **go.PLAYBACK\_LOOP\_PINGPONG** och **go.EASING_INOUTSINE**. Läs mer på:
* <a href="https://www.defold.com/manuals/animation/#_playback_modes" target="_blank">Dokumentation för playback modes</a>
* <a href="https://www.defold.com/manuals/animation/#_easing" target="_blank">Dokumentation för easing</a>

### Extrauppgift 4

- Gör så att godisen försvinner när animationen är klar.

  <details>
    <summary>
    <b>Tips</b>
    </summary>
    Läs mer om hur `go.animation()` fungerar i <a href="https://www.defold.com/ref/go/#go.animate:url-property-playback-to-easing-duration--delay---complete_function-" target="_blank">dokumentation för animationer</a>. Titta speciellt på **complete_function**. Du kan använda dig av funktionen `delete_candy` som finns i `candy_movement.script`.

  </details>

<!-- ### Extrauppgift X

Gör så att det läggs till fler godisar varje gång en godis genom att antingen:
- Skapa en **funktion** som heter `create_candies(ammount)` där **ammount** är antalet godisar som skapas.

  <details>
    <summary>
    <b>Tips</b>
    </summary>
    Kolla hur de andra funktionerna i scripen ser ut. Använd sedan en **for-loop** för att skapa flera godisar. Använd `ammount`i for-loopen på ett liknande sätt som `points` används i funktionen `set_text(points)` i filen `points.gui_script`. 
  </details> -->
