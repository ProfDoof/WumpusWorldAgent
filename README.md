# WumpusWorldAgent
Creating a logical agent that will attempt to find the gold in a grid and then get out all while surviving pits and a Wumpus.

> # Inputs
> My agent can perceive 5 things
> * Wumpus Stench
> * Pit Breeze
> * Gold Glitter
> * Wall Bump
> * Wumpus Scream

> # Rules for Wumpus World
> * You can only move in four directions: North, South, East, or West
> * You can only take one action each turn
> * You can take five actions
> > * Turn Left
> > * Turn Right
> > * Move Forward
> > * Shoot Arrow
> > * Stand Still ????
> * You will receive one arrow
> * If you shoot the arrow it will be lost
> * If the arrow hits the Wumpus the Wumpus dies and the Wumpus will scream
> * If you smell the Wumpus Stench then the Wumpus is in a square adjacent to you.
> * If you feel a Pit Breeze then there is a pit in a square adjacent to you.
> * If you see Gold Glitter then the gold is in the square you are currently occupying
> * If you run into the wall you will feel a Wall Bump
> * If the Wumpus dies then you will hear the Wumpus Scream from anywhere in the cave
> * There will only ever exist one Wumpus
> * The Wumpus, Gold, and Pit objects can all share one space.
> * If you walk into a Pit, or the Wumpus you die.

> # Planning the Agent
> 1. Create a knowledge base with changeable goals.
> 2. Add all information discovered to knowledge base
> > 1. Ask if the four options around are safe based on the KB.
> > 2. If you can't determine if any of them are safe choose randomly.
> > 3. Repeat
> >
> > Notes: Generally speaking it is wiser to simply avoid the Wumpus while mapping out the surroundings. Once you find the gold or determine that the gold must be in a pit return to exit.
