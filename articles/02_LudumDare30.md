Title: Ludum Dare 30 — Node 54
Date: 2014-08-23
Modified: 2016-10-19
Category: gamedev
Status: published
Tags: imported, ludum-dare
Thumbnail: thumb_02.png

This article is an imported set of post describing my participation in Ludum Dare 30.
First part is a summary of Day 1, the second one describes final thoughts.

<!-- PELICAN_END_SUMMARY -->

### Day 1: Let's meet Node54

*introduction not imported*

But I love game development. I read tons of stuff. I try to think about
various algorithms or design patterns that might be used to resolve some
problem that bugs me. The problem is, I haven't finish anything yet. All
of my game development stops on the engine.

So one day, looking at the calendar I saw that my wife with son are
going out and they won't be at home for the whole weekend. And the great
thing about it is that the same weekend belongs to LD30! So I thought to
myself: why not try to sign in? And here I am.

![Main screen of Node54]({filename}/images/0002-title.png){.img-thumbnail .center-block}

So after 10h of design and development (Inkscape, GIMP, PyxelEdit, VS
C++ & SFML lib) I've achieved the following state:

- Simple rendering engine using stack states is done
- Resources management (textures, fonts) is finished
- Level loader that uses .png files as its input is finished
- Level mechanics
- Simple assets are finished: menu background, game background and

Still to be done:

- Collision detection, this is main mechanics
- Player movement based on gravity
- Audio effects & Music (there's gonna be no music probably as I don't 
  know much about this topic)
- Sprite polishing
- Better input handling: Joystick support + rebindable keys
- Maybe (big maybe) PCG-ed levels


### Day 2: Final thoughts

In this part of an article I'd like to talk about conclusions that came to my 
mind after finishing LD30 entry and receiving feedback from various people.

#### My goals

- Finish a game. This could be the single goal because this is the main reason 
  I've joined LD
- The game should be simple enough so it might be done by someone having no 
  experience in gamedev. This means I wanted to use existing idea because
  having no experience in gamedev means I won't be able to finish the game if I
  tried to do something too original.
- The game should not have "raw" visuals
- The game should have some kind of audio: sounds of sfxer + a simple music in
  the background
- The game should be fast-paced and the goal for player is to finish it as fast
  as he/she can
- The game should be looking polished; it should have bindable keys, and
  reasonable amount of juicyness
- The game should have possibility to be improved when LD30 is finished

![Node54 with an example level]({filename}/images/0003-level.png){.img-thumbnail .center-block}

#### What went right

##### I've finished playable game

I wasn't sure I was good enough to actually finish a game. I've tried thousands
of times but every time it stopped being a game engine instead of actual game.
Node54 is real and I'm very happy and proud of myself.

##### The game doesn't crash

When it works, it works. It doesn't look to have much bugs expect the collision
issues and sticking to walls.

##### Visuals

The game is not a kind of beauty, but it also doesn't look bad. My goal of
having not ugly visuals has been fulfilled. Friends told me that the game
background with irregular squares looks really nice when compared to ideal
squares of walls. The best thing is that I've made it for about 4-5 minutes.
Gimp -> pick blue color -> create clouds from filters -> motion blur -> create
mosaic from filters. That's all!

##### Experience

I still want to improve it, I got plenty of ideas so further development will
be continued for sure. Now that I have already a playable it's gonna be much
easier.

I've learned a lot. I've improved some technical skills as well as mental ones.
Finishing this game gave me enormous amount of confidence and motivation. I've
learned the importance of having 10-30 minutes long breaks from a work. Proper
amount of sleep is also substantial. The best thing about our brain is that
when we sleep it doesn't fully shutdown. It's resting in a standby mode in
which it dumps a lot of garbage thoughts. When you wake up (after morning
coffee of course) it contains with thousands of ideas what to do next and how
to do it. If I wasn't sleeping for at least 6 hours every day, me rate of work
would be significantly slower. I also wanted to to let it go on the second day.
My code was so much of garbage that I couldn't implement anything I wanted. So
i thought to myself: time for a shower and some hot beverage. It helped. I
refactored few critical "god" classes and everything started to work as I
wanted it to.

##### Linux port

Linux port which I haven't planned. The good thing about using a wrapper lib
like SFML is that porting is very simple. The code is almost not touched
(almost), and the only thing you need to resolve is compilation and linking to
be finished successfully.

#### What went wrong

##### Time management

I wasn't quite aware of how little time I was given. My first idea for the
development of Node54 was to implement physics (movement + collisions) by
myself. By the end of day one I was having movement of poor quality and no
collision at all. When I was thinking on the collision module design I realized
that it's going be very, very thought to finish. So many edge cases, so many
debugging. And then I read in some social media post that this guy has
something playable thanks to Box2D. I heard about this library but that's all.
So I've decided to give it a try. Manual was kind of well-written, so I've
managed to finish collision system. What went wrong? I was learning Box2D from
scratch and due to no experience I wasn't aware of several issues. First of
all, visual debugging. If I could prepare it before LD it would be much easier
to resolve issues related to pixels->meters conversions and not updating
Box2D/SFML positions. Next thing are issues with friction. Walls in Node54 are
simple rectangles. This means that friction attached to them is the same
horizontally and vertically. Because of that player sometimes stick to walls.
If I divided every block to 4 triangles I could set different friction to
different part of the wall block. Another thing is collision box of the player.
I've used simple rectangle because I wanted to replace this temporary drawn
blue guy with something better. The idea was to add a frame to look more like a
moving platform. I didn't have enough time to have it done.

##### Temporary visuals

There is a saying in software development, that temporary solutions are the
most persistent. I really wanted to make it more pixelarty, unfortunately my
pixel art skills requires quite a long piece of time which I could not afford.

##### Quality of audio
The only sounds I've added to the game were simple samples generated by sfxer.
Unfortunately I haven't read the documentation carefully, so instead setting
volume within the range of (0.f - 100.f) I used (0.f - 1.f).  This means that
sound cannot be heard. I wanted to create some chip tune music in Milky Tracker
but again: no time and no skills to make it fast. I definitely want to improve
that in the future.

##### Lack of feedback

No guide for a player what the game is about and how to play it. For me it was
obvious that I move using arrow keys and when you want to move up you need to
push yourself from the ground. It was also obvious that when player is given
too much of speed it's going to crash during contact with walls. Player don't
receive any feedback and is not given any guide of the rules. He doesn't know
that he has to pick cargo boxes of a color and deliver it to the flag of same
color. He doesn't know that to pick a cargo he needs to press spacebar key. He
doesn't know that when you pick a cargo it cannot be dropped until delivered. A
lot of little things so obvious to me.

##### Lack of juiciness
    
No juiciness in game. No animations. I've skipped animation part because I
thought that it's going to take too much development time from me. So
everything is static. In my engine I don't even have a class for animations. I
started to drawing some animations (explosion which is present in the assets
folder) but it only took some time and didn't make it to the final game. There
is no screen shake when player dies. There are no particles when the player
starts moving. This little things that make every game look polished.

![Tilesets from the game]({filename}/images/0004-atlas.png){.img-thumbnail .center-block}


[1]: {filename}/articles/02_LD30_part1.md
[2]: http://ludumdare.com/compo/ludum-dare-30/?action=preview&uid=40102

