# TGM:I "Mei Yan"
Earth is found and invited into a multiversal civilization along with several parallel Earths with each societies competing to be the first finish the tutorial and conquering their designated worlds.

The magician (user - you) is lucky to be selected to participate in the competition but has to go through the tutorial in one of the academies the civilation has created for humanity. The magician is taught magick, history, and other miscellanous skills.

The magician has a repertiore of magic abilities in which they can move their character, create, switch and stack magic spells, and plant magical herbs in an assigned garden.

Mei Yan is a proof of concept and a prototype of the game TGM:I. 

## Magic System
Tiers:
- Beginner
- Intermediate
- Advanced
- Expert
- Master
- Grand

Ranks 1-9 except Master and Grand

Aspirant Magicians are screened to map their stats (CON, QI and LUK). They are all hidden stat. There are also other stats such as cast speed, and physical and magical efficiency. LUK cannot be raised. CON can be raised through both efficiency stats and herbal medicine. Cast speed is raised through magical efficiency. CON raises total mana/qi which helps clear meridians (calculated every day) which raises QI stat. 

Advancing through tiers and ranks raises every stats' base value except for cast speed, approaching a logarithmic curve (limit increases for every advancement).

### Basic Stats
#### Constitution(CON)
CON is a measurement of the body's ability to take physical and magical stress. It is also used for damage calculation, total mana/qi calculation, defense, magical defense.
#### Qi Circulation(QI)
Qi Circulation is the measurement of qi circulation in the body respective of the magicians realm (tier and rank). It is used for total mana/qi calculation, physical and magical efficiency. Lowers with every realm advancement.

### Special Stats
#### Physical Efficiency
Body control. Raises attack, speed, cast speed. Raised through medicines and physical practice.

#### Magical Efficiency
Magical Control. Raises attack, magical attack, speed, cast speed. Raised through QI stat, medicines, and magical practice.

#### Cast Speed
Speeds up casting of spells(free-form and spell-form). Raised through physical and magical efficiency.

### Affinity
Ability to gather specific element particles causing less qi usage. Specific element awakening depends on environment's elemental properties e.g. fire room increases fire element awakening chance.

### Removed Stats
- Strength (STR) is a derivative property from the magician's constitution and physical efficiency. It might not be needed because damage calculation relies on constitution, QI, magical efficiency and other attack and resist values.
- Dexterity (DEX) is a measure of speed, dodge/hit chance, body control which could be a derivative property of physical efficiency in this game. So it will have to be removed in the meantime.

## Challenges
The user can create, and switch skills in limited slots while being able to move(using movement with magic abilities) during battle. Find out what design pattern(s) is needed to achieve this. The user can raise and harvest herbs in the game.

### Character Movement
The user can move and attack at the same time during battle. They can also use all limbs to either attack or move.
#### Problem 1
Figure out the strategy to achieve attacking and moving at the same time.
**Solution 1**
Use a dynamic heirarchical state machine to manage ability changes and movement. Both inherits from a base state which they can use to communicate between each other.

### Farming Aspect
#### Problem 1
The user can collect plant seeds in the game. Find out what is needed(the strategy?) for the entire plant ecology.

#### Problem 2
The user can raise and harvest plants in the game. Find out what design pattern is needed for the farming feature.

### Stat and Skills
#### Problem 1
Create the class diagram for stat attributes.
**Solution 1**
STR, DEX, CON, QI, and LUK inherit from BaseAttribute class with each stat...

#### Problem 2
Create the class diagram for physical and magical efficiency.
**Solution 1**
