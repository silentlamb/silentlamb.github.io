Title: LD33: Ghosty Game post mortem
Date: 2015-09-19
Category: gamedev
Status: published
Tags: post-mortem, ludum-dare

Results of Ludum Dare 33 got already published so it's time for postmortem.

My main goal — making the game in time for the *Compo* — has not been acomplished.
I was far from having anything ready to be send and the deadline has been reached.
After getting some sleep, rest and spending time with family I decided not to
give up completely and try to drive the game to the finish line called *Jam*.

<!-- PELICAN_END_SUMMARY -->

For these readers who have no clue what's the difference between LD Compo and Jam, 
in short:

- Time to post entry to the compo is 48h, while for Jam it's 72h
- You are only allowed to work solo in the Compo, but for Jam you might work in a 
  team made of programmers, gfx artists, musicans, etc.
- For Compo you must create all in–game assets (graphics, audio) by yourself and 
  all of these need to be made during the 48h of the Compo. For Jam you are
  allowed to use already existing assets.
- Compo is very strict and limiting, while Jam is more careless

### Results

    :::text

      	​ 
 	​ 

      .---------------.-----------------.-----------------.
      |               |      LD 30      |       LD 33     |
      |  Category     |                 |                 |
      |               |  Score |  Place |  Score |  Place |
      +---------------+------- +--------+--------+--------+
      | Overall       |  2.79  |   950  |  3.00  |   716  |
      | Audio         |  2.19  |   816  |  2.41  |   623  |      Good job, minion!
      | Fun           |  2.85  |   730  |  3.11  |   485  |
      | Graphics      |  2.85  |   727  |  2.94  |   734  |           ,
      | Humor         |  2.67  |   354  |  ----  |   ---  |           |
      | Innovation    |  2.44  |  1022  |  2.53  |   873  |        ]  |.-._
      | Mood          |  2.75  |   766  |  ----  |   ---  |         \|"(0)"| _]
      | Theme         |  2.33  |  1056  |  2.31  |  1049  |         `|=\#/=|\/
      `---------------'--------'--------'--------'--------'          :  _  :
                                                                      \/_\/
                                                                       |=|
                                                                       `-' fsc

     	​ 
     	​ 

      

The results are generally better. Keep also in mind that in LD Jam you compete
against teams of people, not the lone designers; it's much harder to get better
score due to this single fact. I was really suprised that my overall score is
that high as the game was far from being finished.

In the other hand, I've been slowly working on enhancing my graphics and audio
skills and it seems like some progress has been made.



### Timelapse

<iframe width="560" height="315" src="https://www.youtube.com/embed/8HihdhlJQYA" frameborder="0" allowfullscreen></iframe>

### What went right

The goals were described in the [introduction article][3]. 

#### Visuals

I'm really happy that my pixel–art skills got improved. I was able to create
some animations and (for a beginner) decent looking characters. However, there is
still much more room for improvements. My next goal is to have enough skills
to produce content of similar quality to the [Ultimate Fantasy tileset][1].

![Working on the assets]({filename}/images/0007-pyxel.jpg){.img-thumbnail .center-block}
*Working on the assets*{: .center-block .text-center}

#### Audio

Music. I've finally made it! The tool of use was Bosca Ceoil. I was using it for
the first time. Bosca Ceoil is an awesome tool to create simple tunes using tons 
of different samples. I think it's good idea to stick to this program for a now
and focus on something else. 

![Bosca Ceoil music editor]({filename}/images/0006-music.jpg){.img-thumbnail .center-block}
*Bosca Ceoil music editor*{: .center-block .text-center}


#### Entity Component System

Before the LD I was working on my custom engine, based on ECS architecture.
I had no actual game to test if it works properly, so LD was a first test.
There were nasty bugs that took some time from my developement, mostly related
to initialization as I was reusing preallocated memory for component data,
but overall I'm really happy with the architecture. If you start thinking
with components and not game objects, everything magically starts working.
If you got your rendering, physics and audio systems already prepared you 
might focus on actual gameplay because attaching proper components will 
make everything magically work! This is the reason why people use engines
like Unity. Few hours later you got working prototype.

### What went wrong

#### Deadline missed

I was unable to deliver in time an entry for compo. I've lost over 6 hours of 
development due to a basic indexing issue which shouldn't happen to any 
software engineer. I didn't have any physic system ready to be used so I had
to make one by myself. This combined with not tested ECS–engine resulted
in too much time spent in a debugger trying to figure out what's going on.
Lesson (I hope) learnt and (I hope) next time I'll focus more on actual
gameplay.

#### Lack of actual gameplay

This is a big loss. As I've lost too much time fighting windmills, 
only single planned gameplay feature has been implemented. My plan was to
create a stealth evasion game with static obstacles, moving enemies with 
their cone of view, sound alarm system, bullet hell and simple logic 
puzzles (push this button to activate that). To me this game is far from
being playable. No idea where the 3.0 overall rating came from, but it's
kind of intresting.

#### Lesson to learn

Just one lesson but the most important one: **be focused on all the 
little things** in a software development process…

… such as table indices or early function exits, as they may screw your
mind when you try to debug complex logics. If you name variables, even
for side projects such as LD entries, use good naming convention.
I've spend over 6h because I couldn't find the mistake in 2d → 1d array 
index conversion; I've used wrong variable to determine size of the 
row (tile's width in pixels instead of number of tiles in
a row). It could have been avoided if I hadn't had variables named `TW`
(Tile Width) and `WW` (World Width). When participating in LD, you 
should have proffesional mindset too. 

![Index bug when setting up VertexArray]({filename}/images/0008-indexbug.jpg){.img-thumbnail .center-block}
*Debugging index bug described above*{: .center-block .text-center}


The second bug, that cost me some time, was a removal of early function
exit when calculating a direction from velocity vector. Due to 
refactoring I removed early exit on a vector length check. It resulted
in division by 0, which for floats results in NaN, which resulted in 
wrong position of the player's character, which resulted in a camera 
moved to strange position, which resulted in a whole game state layer not
being drawn and since I was using state-stack design, the MainMenu state got drawn,
which resulted in lost hours in a debugger trying to figure out what
the heck just happened. 

The other lesson from this bug is: **use asserts whenever you can**.
For release mode they will be removed. Which leads to the third bug:
putting logic in a preprocessor macro which happen to be removed (changed
to `do {} while(0)`) in the release mode. My only explanation is a tiredness.

#### Plans for the future

Next Ludum Dare in 3 months so there's plenty of time for
self–development and engine improvements. Right now I'm trying to
make my new game project to get off the ground. As for the programming 
tasks, I've made the list of things to be done:

- Add more features to the [mve-engine][2]
    - Cinematics
    - Animators
    - Shaders and processing effects (optional)
    - Input rebinding (optional)
    - Dynamic audio system (optional)
- Prepare level parser to be used
    - Parse image (png) based maps
    - Parse PyxelEdit txt format
    - Parse Tiled map format (optional)
- Implement algorithm to reduce unnecessary number of rigid bodies when loading a map
- Prepare for LD34 (12-14 Dec, 2015)
- Continue improving on pixel arts


[1]: http://oryxdesignlab.com/ultimatefantasy
[2]: https://github.com/silentlamb/mve-engine
[3]: {filename}/articles/imported/04_LD33_part1.md

*[ECS]: Entity Component System
*[LD]: Ludum Dare

