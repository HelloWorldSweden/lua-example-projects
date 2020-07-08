# Football
## Ett ofärdigt 2-spelarspel
### Utveckla klart spelet!

#### Lite ledtrådar på var man ska leta fel
- Player 1:
    - `player1.script` -> `on_input()`
        - Vi måste skriva in kod för att göra att player1 kan röra på sig.
    - `player1.go`
        - Vi behöver koppla ett skrip som styr spelobjektet player1.go (go - gameobject)
- Player 2:
    - `player2.script` -> `on_input()`
        - Spelare 2 kan bara röra sig upp och till vänster
        - Ta en titt i */input/game.input_binding*
- Goal 1
    - `goal1.script` 
        - Vad borde hända när bollen rör målet?
    - `goal1.go` 
        - Vi måste se till att målets två kollisionsobjekt är korrekt konfigurerade.
- Goal 2
    - `goal2.script`
        - Vad borde hända när bollen rör målet?
        - Vi måste se till att målets två kollisionobjekt är rätt konfigurerade
- Ball
    - `ball.script`
        - När någon gjort mål så bör bollen läggas tillbaka på mittpunkten. Fixa detta.
- GUI
    - `gui.gui_script`
        - Det saknas en en funktion som sätter poängtexten för spelare 2

    

