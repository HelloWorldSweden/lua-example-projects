# Jumping
## Et ofärdigt flappybird liknande sidescroller
### Utveckla klart spelet!
#### Lite ledtrådar

Factory
 - `factory.script`
    - Skriv koden för att periodvist skapa hinder
    [Ledtråd: API](https://defold.com/ref/timer/#timer.delay:delay-repeat-callback)
- Gör att hindrena skapas med en större spridning i höjden.

Obstacle
- `obstacle.script`
    - Hindren som skapas (efter du fixat factory grejerna), kolliderar inte korrekt med spelaren. Fixa detta. 
Player
- `player.script`
    - Fixa så att man kan få poäng genom att kommunicera med GUI.