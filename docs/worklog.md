# Worklog

## #24

Was going to work on the HUD message, but it won't work out the exact way that I
want. So instead I just started filling the sample mall to get a quick prototype
working of the gametype. I setup all 8 stores and now I have to setup the spawn
system and a trigger to start searching for the hacker sooner rather than later.

## #23

Spent time working on the win condition system. Hackers get 10 points per store
hacked, when a score of 50 is reached, they win. Guards will get 50 (currently
it is 500 cuz it is bugged) points when they kill the hacker, this will also end
the game. Now I have to work on a messaging system so hackers know they are the
hacker.

## #20, #21, #22

Continued work on the hacker assignment system. I had to duplicate everything
and create a configuration that would be easy to edit as I duplicated it for
each store. And I had to split up the class selector into 4 pieces so that way
it would not overload a single channel with too many receivers since the limit
is 60 receivers per channel. But now I have an infinite loop to deal with, and
I'll figure that out next session. But the mechanics of Clue are close to being
done. Then I have to make a win condition and actually build the full map.

## #19

We started work on the Hacker decider system using an RNG re-roll machine. And
after setting that up, we started work on the hacker assigner system, which will
turn the designated killer into the killer when they activate a store. We tested
it with the first store, and now it just needs to be duplicated for the other
stores. But it all seems to work well.

## #17, #18

Went back to working on Clue. Started with building out the store security
system. When a guard tries to activate the store security, it will lock down the
store for X seconds. When a hacker tries to activate the store, it will disable
store security. Next system that needs to be created is the hacker selection and
hacker assigner systems.

## #16

Gave up on the sneaky snowman exploration for a bit. Tried to test my theory for
round based changing of teams and that didn't work either. So instead I started
to explore what will be needed to make Clue work. Now that we have attribute
triggers, I have the ability to check whether an activator of the button is a
killer or a guard. This makes a huge difference. And also having 25 more
channels makes a big difference as well. I should have enough tools to create
Clue. So now the trick will be building the system to make Clue work and test
it. I might actually work on that today on stream. So we shall see how things
go. If not I'll finish Inception. I have multiple options to attempt to get
done.

## #15

So yesterday, after I put in my worklog entry. I realized there was something
wrong with my team switching system. Apparently it didn't switch for that
game... it actually switched for the next game. Which is really weird. But it
makes me think. Maybe I can make it work on a per round basis. Perhaps the team
traits are tacked on at the beginning of the round. If so, then I might be able
to do what I want. Until then. I had an idea this morning for a prop hunt type
gametype inspired by my hoarders gametype. I started working on playing around
with what the mechanics will be like. Lots of snowmen, in the dark, low
exposure, change into one, sneak around, find another snowman, kill them for
their loot, and gather as much loot as possible before the end. Right now just
screwing around, but I think I might have something. Just gotta keep
experimenting.

## #14

Spent this session designing a system where you can change a player's team
mid-game this will be crucial in systems where players can be forced to go to
certain teams for any particular reason. Apparently team settings plates
re-apply settings on respawn, so having multiple team settings plates, then
leaving one left then respawning the player, they will take on that remaining
plate's traits. Then for team switching you have that plate dictate "go to team
after last life". Easy setup... the problem is whether or not I have enough
channels to pull it off.

## #13

Moved the Inception sign to an appropriate spot on the wall. Started exploring
an aesthetically pleasing approach to showing off all of the weapons. I'm
currently thinking of mini gazebos to house the weapons. There needs to be a
place to put a label above the weapons as well as not blocking the sign. Luckily
we have some room to move the sign a bit upwards if necessary. Next session I'll
be screwing around with weapon housing styles until I have at least a decent
one. Of course these stations can be updated later with something better when I
get an artist to take a look.

## #11, #12

Took time to setup my worklog for my design portfolio to post directly to Github
whenever I finish and push up an entry. This will serve to be a direct location
for viewers to see what is happening with my design portfolio and keep up with
map releases and updates.

## #10

We finished the adjustment of the size of the sign to half of what it was. This
shrunk the room to a much more manageable size, which allowed us to pull in all
the walls and shrink the entire room so that way it makes better use of the
space and will ultimately waste less of players time walking around. Next thing
to do is to add the spawns and move the sign closer to the wall and to the side.
And we should be close to done. Should be good by the end of the stream.

## #9

Adjusted the positioning of all the weapons into groups. I started to explore
labeling the groups and didn't like the obvious solution, so the first thing I'm
going to do is reduce the size of the sign in the back to reduce the size of the
room. A smaller room should lend itself to a better setup for the weapons.

## #8

Spent time organizing the weapons into types, then started cleaning up excess
pieces outside of the spawn room. Cleaned up the corners so they look better and
fit all 16 spawns, and added pillars for a cleaner more polished look.

## #6, #7

Setup the full shape of the spawn room, including the quick access spawn point
to get back into the game quicker. I've also fully ported over the signage from
the old Inception. So now the spawn room looks good. Next we have to organize
the weapons and add some labeling to make things a little more self explanatory.
I also need to setup two classes, one for playing the game, and one for being in
the spawn room. Should only take a few more sessions, might finish tomorrow
fully.

## #5

Started by bringing over the old Inception sign that I made when Creative first
came out. We will use that to decorate the spawn room. In addition we started
redesigning the spawn room, setting it up so that way people can get back into
the action faster, but still have the option to change their loadout between
spawns if they so choose.

## #4

Closed up the map with walls and also removed any excess walls to reduce all
possible chances for too much memory. Everything seems to perform way better
now. So the next thing I want to start doing is clean up the spawn room.

## #3

We explored the power of teleporters and setup a teleporter at the bottom of
each of the main outer ramps. This will serve as the new entrance into the map
and you will now respawn in the spawn room, which gives you the opportunity to
change your loadout midgame. Or when someone joins midgame they can select their
loadout. Next thing to do is to finish walling off the map and then test it.
Then we probably want to work on making the spawn room look awesome.

## #2

Continued to remove another 2 tiles from each side of Inception. Tested the
unloading of the map and it seems to actually unload now, which is exactly the
progress we needed. So I just need to seal it up and it should be playable at
this point. The next thing I want to work on is to add teleporters and allow
people to spawn in the spawn room and take the teleporter whenever they are
ready. This will allow players to change weapons every spawn, and also allow new
players to still grab weapons and stuff.

## #1

We are focused on getting Inception featured on Fortnite Creative right now. So
the first thing we need to do is make sure it loads and unloads efficiently
rather than lag up the entire session and require a restart of Creative. So I
started with remove 2 tiles on each side, but it seems to not be working well
enough yet. So next session we'll remove 2 more tiles on each side.

## #10

We finished the adjustment of the size of the sign to half of what it was. This
shrunk the room to a much more manageable size, which allowed us to pull in all
the walls and shrink the entire room so that way it makes better use of the
space and will ultimately waste less of players time walking around. Next thing
to do is to add the spawns and move the sign closer to the wall and to the side.
And we should be close to done. Should be good by the end of the stream.

## #9

Adjusted the positioning of all the weapons into groups. I started to explore
labeling the groups and didn't like the obvious solution, so the first thing I'm
going to do is reduce the size of the sign in the back to reduce the size of the
room. A smaller room should lend itself to a better setup for the weapons.

## #8

Spent time organizing the weapons into types, then started cleaning up excess
pieces outside of the spawn room. Cleaned up the corners so they look better and
fit all 16 spawns, and added pillars for a cleaner more polished look.

## #6, #7

Setup the full shape of the spawn room, including the quick access spawn point
to get back into the game quicker. I've also fully ported over the signage from
the old Inception. So now the spawn room looks good. Next we have to organize
the weapons and add some labeling to make things a little more self explanatory.
I also need to setup two classes, one for playing the game, and one for being in
the spawn room. Should only take a few more sessions, might finish tomorrow
fully.

## #5

Started by bringing over the old Inception sign that I made when Creative first
came out. We will use that to decorate the spawn room. In addition we started
redesigning the spawn room, setting it up so that way people can get back into
the action faster, but still have the option to change their loadout between
spawns if they so choose.

## #4

Closed up the map with walls and also removed any excess walls to reduce all
possible chances for too much memory. Everything seems to perform way better
now. So the next thing I want to start doing is clean up the spawn room.

## #3

We explored the power of teleporters and setup a teleporter at the bottom of
each of the main outer ramps. This will serve as the new entrance into the map
and you will now respawn in the spawn room, which gives you the opportunity to
change your loadout midgame. Or when someone joins midgame they can select their
loadout. Next thing to do is to finish walling off the map and then test it.
Then we probably want to work on making the spawn room look awesome.

## #2

Continued to remove another 2 tiles from each side of Inception. Tested the
unloading of the map and it seems to actually unload now, which is exactly the
progress we needed. So I just need to seal it up and it should be playable at
this point. The next thing I want to work on is to add teleporters and allow
people to spawn in the spawn room and take the teleporter whenever they are
ready. This will allow players to change weapons every spawn, and also allow new
players to still grab weapons and stuff.

## #1

We are focused on getting Inception featured on Fortnite Creative right now. So
the first thing we need to do is make sure it loads and unloads efficiently
rather than lag up the entire session and require a restart of Creative. So I
started with remove 2 tiles on each side, but it seems to not be working well
enough yet. So next session we'll remove 2 more tiles on each side.
