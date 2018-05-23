# RPG dice analyzer

The aim of this project is creating an iOS app, that analyzes the dice outcome for a RPG game.  
It will be written in Swift 4 using xcode 9.  
  
I'm pretty new to swift still. And i am therefore having some difficulties programming this. 
The biggest problem is actually the math behind calculating the dice.  

**The game**
The game has heroes and enemies (as everything so often have).  
You can buy different weapons that uses different attack dice and you can use two different type of block-dice.   
The amount of each type of die can vary.  
  
**Attacking**  
The attack dice has two different type of values on them:  
    Damage (dam):  gives one damage per point  
    Ability points (AP): which an be used on different things, for example extra damge.
    
There are four different type of attack dice. Each has 6 sides. The different sides of the dices are shown underneath:
Red:        [1dam], [2dam], [2dam], [2dam, 1AP], [3dam], [3dam]  
Blue:       [1AP], [1dam], [2dam], [1dam, 1AP], [2dam], [1dam]  
Green:     [1AP], [1dam, 1AP], [2dam], [1dam, 1AP], [2dam], [2dam]  
Yellow:     [1AP], [2AP, 1dam], [2dam], [1AP, 1 dam], [1AP], [1dam]  

**Blocking**
Then there is two different types block-dices. They have the values:  
    Block (Bl): Blocks one point of damage  
    Evade (Ev): removes one ability point (AP)  
    Dodge (Dod): Removes all possible damage both from directly dam and from ability points.  
  
The sides of the two different block-dice. Each has 6 sides. They are shown underneath:  
Black:      [1Bl], [1Bl], [2Bl], [2Bl], [3Bl], [1Ev]  
White:      [Nothing], [1Bl], [1Ev], [1Bl, 1Ev], [1Bl, 1Ev], [1Dod]   
  
   
**Probability**
Let us say im attacking with a weapon that uses one red die and one blue die. 
The chance of giving at least 1 dam is 100% (36/36)  
Chance of giving at least 2 dam ≈ 97% (35/36)  
Chance of giving at least 3 dam ≈ 89% (32/36)  
Chance of giving at least 4 dam ≈ 44% (16/36)  
Chance of giving at least 5 dam ≈ 11%  (4/36)  
  
This is however without calculating the AP and the blocking dice.  
  
If the defender is using 1 black die the chances of blocking damage are:  
Chance of blocking at least 1 dam ≈  83% (5/6)  
Chance of blocking at least 2 dam ≈ 50% (3/6)  
Chance of blocking at least 3 dam ≈ 17% (1/6)  
Chance of blocking 0 dam ≈ 17% (1/6)  
  
If the defender is using 1 white die the chances of blocking damage are:  
Chance of blocking at least 1 dam ≈ 67% (4/6)  
Chance of blocking at least 2 dam ≈ 17% (1/6)  
Chance of blocking at least 3 dam and up ≈ 17% (1/6)  
Chance of blocking at 0 dam ≈ 34% (1/6)  
  
Again, this is without calculating evade and ability points.  
  
In the app you choose what dice the attaker is using, if he has any abilities that can add damage by using ability points, and the dice of the defender is chosen.  
Somehow this should be calculated to give the possibilities of giving at least 1 dam, 2 dam and so on calculating the different dice that the attacker and defender is using.  
This shall be shown as a graph.  
  
To view the website this idea is based on go to: [http://mattyellen.github.io/imperial-assault-calculator/]  
To view the different dice go to: [http://imperial-assault.wikia.com/wiki/Dice]





    
