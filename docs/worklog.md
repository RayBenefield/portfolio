# Worklog

## #131, #132, #133

Alright so the spawning system seems to be fully working properly. I discovered
that I used the wrong channels so I'm going to have to fix that to make it
playable. The next thing I have to figure out is how to fix the bug of a player
dying while their contract is being negotiated. I was going to make them
invincible but realized I can't do that or anybody without a contract is
invincible and if I do that then people could get a contract for someone that
was invincible and would be stuck on that contract. So I was going to try to
make them invincible while they were searching for a contract, but I don't have
an extra class. So I have to come up with a different way to solve this problem.

## #130

Started the spawning room system and realized that the wanted posters will be
easier to see see with lights on during the warm up phase. So I setup lights
around each wanted poster that I could find. Looks like I missed one, but now I
can get back to the spawn room system.

## #128, #129

So I've spent almost all morning yesterday trying to figure out a good spawning
solution to use portals as "spawns". The problem with most solutions is they
won't catch a player on respawn at all which is terrible. It would only work at
game start. But I finally found a solution that will catch you consistently on
respawn. So I have a couple needs. I need to not use many channels, I need all
players to spawn at different locations at the beginning of the game, I need
respawns to also be random.

My solution will be the following, there will be a box of 16 player spawns, each
spawn has a teleporter tied to a different group. These teleporters will handle
the initial spawn into the game at guaranteed different locations. In addition
there will be a capture plate that takes gold coins and teleports on gold coin
consumption. This will handle respawns. In order to make respawns random I need
to have another box of 16 teleporters that react to the single channel for
teleporting for all the capture plates, but it randomly chooses one of those 16
teleporters and drops you into one of the 16 grouped teleporters. This ensures
that I won't need a channel per teleporter. This whole system only costs 2
channels. In addition to the teleport channel, there is a toggle disable/enable
channel on a timer 1 sec loop. This enable/disable system is what guarantees
trigger on respawn. The reason we need a gold coin is because just "capturing"
doesn't trigger on enable/disable toggle when a player spawns directly in it.
HOWEVER, an item filter and consumption WILL trigger, I'm assuming because there
is a secondary event that checks for capture regularly that will trigger on a
stationary respawned player. This also means I need a team settings plate that
grants a gold coin on respawn. And that should be all the pieces needed... a
very complex system, but something that should achieve my goals.

## #124, #125, #126, #127

So I tried to setup spawns, at first I tried to do them with teleporters so I
could control the angle a player is facing, but that turned out not to work
well for various reasons. I fiddled with it quite a bit and it looks like I'm
just going to have to go with regular spawns. Then I realized that when a player
dies while negotiating a contract the system doesn't get the chance to reset
because when the player dies the instigator of the event gets removed so it
can't trigger the attribute channels that reset the ability to get contracts. So
I need to get creative and figure out how to circumvent that problem. My theory
is only make players vulnerable when they have a contract and they can't deal
damage to a player when they don't have a contract also. I'll have to explore
options.

## #119, #120, #121, #122, #123

Alright so I did a ton of work on getting the prototype for Gunrunners playable.
I started out these 5 sessions with setting up the wanted posters to acquire
contracts... I found locations for them and placed them everywhere. Then
realized that you could activate buttons through walls and had to resize them
and perfectly position them then replace them everywhere. I then realized that
an increased movement speed allowed for more parkour options because you had a
farther jump, so I played with that for a bit. Then this last session I started
working on a spawn system.

So with the spawn system I found that I wanted to use teleporters to control
direction and specific location for spawns. Then realized players weren't facing
the proper direction when I did that. It was the fact that teleporting happens
too fast. So I setup an intermediate teleporter in a black box so players drop
into a second teleporter... this allowed me to enforce direction properly as
needed. Now that I have a system I just have to polish it up a bit and place all
the teleporters... I'm going to take a quick break though.

## #118

Setup the stores on the map and setup the initial team settings with a blue
tactical shottie and tons of shottie ammo. I've also decided to turn on names to
allow bigger games to not get frustrating so you have a goal of checking each
player. It also gets rid of the frustration of people with the same skins. Next
steps are going to be setting up spawns and bulletin boards. First bulletin
boards... they should work out well hopefully, just gotta find enough spots on
the map that it makes sense.

## #117

Thanks to Tubby and PTO I was able to rebuild the system to account for having a
bulletin board now. I've also updated the scoring system to negative points
whenever you kill anyone and lots of positive points for a successful contract,
that should reduce the amount of people just killing for fun.

## #116

Copied the one corner I had created all over the rest of the map and now I have
a fully developed map. The next thing I need to do is make it actually playable
by setting up the vendors and the spawns and the bulletin boards. Gotta figure
out where to start... I think I need to start by first creating the new bulletin
board system before actually populating the map.

## #112, #113, #114, #115

Filled in the rest of a single corner of the basic layout built with just wood.
I'm at the point where I can just copy the corner into the other 3 corners and
get it ready to playtest. I also setup where all 16 vendors are going to be on
the map. I was able to also design a cool looking bulletin board to be used when
people do not have a contract. Instead of having players automatically get a
contract when they turn in the a contract, they will have to go to a bulletin
board whenever a contract is available (nobody is being assigned a contract).

## #109, #110, #111

Now that I've confirmed that Gunrunners is actually playable I'm at the part
where I am designing the layout for the actual map. I'm pumped and this is a ton
of fun. I'm excited to encourage the hiding aspect of weapons as well as
encouraging a constant up and down traversal of the map. I started working on
figuring out where the vendors should go and properly spacing them out and then
filling the in with buildings based on the pueblo prefabs. I'll divide the map
similar to the block fort map from Mario Kart... a color per corner. I also have
to consider the order in which teams are filled in. There is tons to consider,
but this map will probably be my most complex at this point.

The system I'm using to make Gunrunners work is made up of 49 triggers, 48
attribute triggers, 16 quest trackers, 16 elimination managers, 16 class
selectors, 16 conditional buttons, 2 score managers, and a partridge in a pear
tree (an RNG). So it is fairly complex. But it works. :D I'm sooo excited to get
this working.

## #106, #107, #108

Move is all done and I found some time this morning to get some work done.
Despite a bunch of bugs in the controls, I was able to get something working
this morning. This most recent update added a quest/challenge tracker which was
actually able to solve my problem with telling people which contract they had
for Gunrunners. So now I think I have a solid playable game system for
Gunrunners that just needs to be tested with a larger group. I now assign a
quest to a person to match the contract that they have been given and remove the
quest when they turn in the contract. The only thing I have to verify is whether
or not a quest is removed from multiple people when the same contract is
fulfilled. I don't think this will happen, but I just need to ensure it doesn't.

The next thing I want to do is actually go play with Clue and make it assign the
quest to the hacker when they become the hacker, rather than telling a person
that they are the hacker before they actually become the hacker (securing a gate
after they have been chosen to be a hacker). When I'm done with that I want to
play with the aesthetics of the Gunrunner mechanism and make it easily testable.
I also need to give Stormbreaker a win condition.

## #104, #105

Started working on a new linear matchmaking algorithm. It looks like it clears
up some scripting channels that I can use for other things like immediate lobby
creation when no open lobbies exist. And the matchmaking is much faster.
However, the big problem I am running into is that sequencers do not pass the
instigating player and hence I can't portal players using this new matchmaking
system. Which sucks cuz it could be amazing for the system. I'm going to file a
bug on Reddit tonight and hope that it gets tracked and fixed.

## #102, #103

Earlier today I created a quick prototype based on a reddit user's request. It
allows teams to capture a zone to gain control of a weapon and when they respawn
they also get all weapons based on what they control when they respawn. Took an
hour.

## #101

Finally finished what seems like most of the bugs for Forever Fights... there is
still one bug that happens randomly, but it looks like it is recoverable for
now. I'm excited for making it all pretty and working now. YAY!!!

## #97, #98, #99, #100

Worked on various bugs that were causing problems. One bug involved having
multiple open lobbies available that could be chosen. I need to add another set
of channels to setup a gate for checking open lobbies, so if one open lobby is
joined, the others can't be joined until search reset. The next bug I just
discovered requires the lobby be open separately from the room being open.
Because when a player gets eliminated we need to send on a separate channel so
it doesn't assume all rooms are unavailable.

## #96

Made the final modifications for making the box fight mechanics work for the
most part, just need to lock down the leave lobby buttons and the join
matchmaking button until the searches are done.

## #95

Finished up the class system for box fights to assign weapons accordingly. You
are invulnerable and get c4 to clear out the builds from the previous fight. The
weapons are a purple pump, blue ar, 1 slurp fish, and 3 minis with 500 wood. I
have to adjust the class selector system to not overlap into the spectator zone,
but other than that it looks like it is mostly working and just needs some final
tweaks.

## #94

Setup the blocker systems for box fight mechanics. There is an invisble blocker
that is always there by default to allow players to see through it and clear out
the builds of the previous fights and you should be invulnerable during that.
There is an opaque barrier that spawns when a challenger arrives and then it
disappears with the invisible blocker 5 seconds after the challenger to start
the fight. When the winner is decided, they get teleported to the host side and
the invisible blocker respawns and you are given a class with C4 only.

## #91, #92, #93

We finished up all of the box fight arenas with proper sizing, a box, and home
and away portal spawns. We made sure the leave lobby button worked as well as
double checked our scripting systems to make sure everything was in order. Also
setup the elimination manager system that detects when someone wins their box
fight. The next thing to do is to setup barriers to run the box fight
accordingly. A barrier to prevent people from seeing where the other person
starts, and another barrier that is transparent and allows the winner to clear
out the builds of the room. Hopefully one day we'll get explosives that can
clear the builds automatically.

## #89, #90

Created the lobbies to be joined when a lobby is both opened as a new room as
well as when a player joins an open lobby. The test seems to be successful. I
need to shut off the matchmaking button until both searches are done, but I also
need to actually make each of the box fight rooms as well as add the elimination
manager that will trigger when someone gets a kill in that lobby. We will use
classes to designate who is in what lobby to know when the elimination manager
should fire.

## #88

So I've setup the room search to trigger after the challenge search. When a room
is selected it disables all other rooms from being opened, and also opens the
challenge for that room in the challenge search. Next thing to do is to prevent
a room search if a challenge is found, now that we can open challenges. I've
also designed a system where a player can leave a room when there is no
challenger. This will make the room available and remove the challenge
associated with the room. So if nobody is available to start a challenge, they
can go back to spectating and wait for another player to be available for a
challenge.

Winners stay in the room they win and get ported back to the starting
point to wait for a new challenger. Thinking about it, I won't have an easy
system to reset the builds in the room, that will probably be the main problem.
I can probably create a system where players are responsible for clearing out
their rooms, but I'll worry about that later.

## #86, #87

I just came up with the craziest idea and as a result created a super powerful
device that I need for future things. I want to design a Box Fight gametype
where you are able to continuously participate in box fights. When someone tries
to challenge someone else, if there are no available challengers it will create
a new room and put that person in that room making that person available for a
challenge. However if there is an available challenger it will put that person
in that available room and then make it no longer available then start the
fight. To do this I needed to create a search engine that will scan for
available challenges to join. Then if it fails to find one, it will trigger a
new search for an available room, create it and then make it available for
challenging so the next challenge search will find it. This is a SUPER complex
system, but could be very valuable to the competitive Fortnite community.

I just spent 2 sessions and created the search engine system. Now I need to use
that to create the "Forever Fights" game mode. I'm very happy with my progress
and super pumped for this.

## #85

Fixed the entire side that was off by one and added blockers all over the place
so they work properly and keep players in the map. The only thing the map needs
now is a win condition system so when the entire side of the map is destroyed it
should trigger the win for the other team.

## #82, #83, #84

Started the prototype for stormbreaker. It seems to work alright, but I setup
one side off the grid by one. So I have to redo that whole area as well as
figure out a way to end the game when an entire side is destroyed.

## #80, #81

Finished up the last of the polishing. The trees on the edge were rotated
randomly to add some variety, then duplicated to thicken the edges of the
minimap. I also added a HUD message to teach people to crouch below the bushes
to turn off the spotlights. One gameplay change I made was reducing a player's
inventory to only 3 slots. This should improve gameplay for much larger groups
of players to ensure more weapons are available for pickup. Covet is now
officially published. :D https://www.epicgames.com/fn/9730-1332-8075

## #78, #79

Finished up the last of the bush cornering that needed to happen around the
spawn areas. Then recreated the entire grass floor with less pieces than it
originally had because object sizing is now to x5 instead of x3. Also restarted
the surrounding tree cover. I still need to finish filling it in, but I think it
is pretty much good to go. The map feels like it's pretty much done and ready
for publishing.

## #77

Finished up all of the convex and concave corners that were missing pieces. I
just have one more batch which are the bushes around the spawn areas. Once that
is done I have to cover the floor with grass once again. When that is done then
I need to remove all of the gallery stuff outside of the map. After that I'm not
sure what is left. Perhaps a nebula skybox or something will make it feel
better.

## #73, #74, #75, #76

Started working on the corner bushes, but ran into a lot of problems with pieces
being deleted as I was working on things. So I had to remove the entire grass
floor so I could start from a good point. Now I've got into a good groove where
I'm "painting" corner bushes on the convex corners. Once I'm finished with
those, I have to work on the concave corners. The reason for these bushes is to
prevent people getting spotlights on them even when they are crouched and
traversing the map. They should only be revealed with spotlights if they are
uncrouched.

## #71, #72

Duplicated the Covet map so I could create a gallery of pieces for Covet so I
can make new Covet maps in the future with the same mechanics. Spent these two
sessions just deleting the main portion of the map to leave the reusable pieces.
Next focus is to fill in the corner bushes all over the map.

## #69, #70

We setup the stores and the gun dropping systems for each of the teams. In
addition we avoided the potential bug of mutliple teams turning in a contract
while another team is waiting for a new contract. The gametype will not work
until we have a way to give HUD messages to specific players or classes. When we
can do that then we can tell players what their contract is. Until then... this
will wait to be played.

## #67, #68

Setup a new system to avoid teams getting a contract for themselves. Instead of
counting players entering the game, we just guarantee that a store/contract is
available when that team exists in a game. The team number will dictate the gun
they are running, and a gated system exists that makes sure that the class
number for a new contract, does not match the team number for the team that
needs a contract. This avoids teams getting contracts for themselves. Now to
work on the actual dropping of weapons and the stores.

## #66

This morning fixed up all the perception triggers on Covet to ensure that they
actually look at players and highlight them. This is necessary for the new
Covet. Next thing that really need to work on is the corner bushes so you aren't
revealed as you crouch around the map. I also need to adjust the weapon balance
for the map.

## #63, #64, #65

Started exploring a kill contract gametype I'm dubbing Gunrunners. Right now I
worked on the system for changing your contract when you turn in the gun that
you have. I need to adjust the system to never choose the class that you are.

## #61, #62

Realized I never put in my last couple sessions from the stream two days ago. My
last couple sessions were spent setting up the perception triggers on the new
map. I moved them higher than they were and removed all the bonus settings. Only
to discover that a channel needs to be set for the animated portion of the
perception trigger. So now I have to go through and turn the channel on for
every single perception trigger to make it playable in a good way. One of the
things I want to tackle today is adjusting the weapons a bit, perhaps finding a
better way to grant ammo/weapons. I also want to add gas/smoke grenades to be
able to improve a person's ability to get weapons or make it easier to traverse
certain areas of the map. I want to move the scars a little bit as well as
change out the sniper to something a little more reliable. Later I also want to
create a gallery map for building more Covet maps in the future.

## #57, #58, #59, #60

Spent 4 full sessions just removing the bushes of the old height and putting new
bushes of the lowered height. It took the full hour and a half. Next is to
verify the visible vs invisible system to make it work better. Once it works
properly then it should be testable.

## #56

Fixed up the Risk issues. I needed to setup the objective to end at 20 captures,
in order to do that I needed to add 2 more objectives, one for each team. So I
added a new starting one that will unlock the first three. We'll see how things
progress, so I can figure out how to improve the gameplay a bit and make it more
interesting.

## #53, #54, #55

Finished up ALL the switching systems to make Risk work. Including the
territories opening other territories, and visual blockers being removed so it
is clear where you can go next.

## #51, #52

Started work on the full switch system for Risk. Setup the first couple
territories that unlock when you capture any adjacent one. Still have lots to
go.

## #50

Started working on the prototype for my Risk boardgame gametype. Just setup the
basic map and aesthetics and next thing to work on is the switch system that
will unlock territories.

## #49

Created the post for both Reddit and Twitter... what is left is submitting it to
Epic Games for featuring as well as writing my portfolio post for Inception into
this repository. Going to be playing this in playground fill to spread the word.

## #47, #48

Spent a couple sessions just throwing together the trailer. Not the greatest,
but I'll be more informed and less rushed in the future. This is my first go
around with my new routine. Next is the post.

## #45, #46

Started off by collecting some clips from the gameplay yesterday. I don't need
much since it is only just a teaser trailer to show off the map.

## #44

Some minor updates to Inception. I realized the light shining into the spawn
room was being blocked by the barriers and weapon free zone lines. So I
increased their sizes to prevent it from messing up the lighting on the sign. I
also adjusted the screenshot for the map. I also explored what the next set of
optimizations will be as I move forward to improve the map performance. Setting
tiles to props will be the next optimization which will essentially be a full
rebuild of the bulk of the map, rebuilding the columns and the ramps. However
this optimization may get rid of the stutter when unloading the map. Now I need
to start working on the publishing materials to publish Inception tomorrow and
play it on stream.

## #42, #43

Started exploring some of the new devices available and new options available in
Creative. Kill confirm is sort of possible. Risk is definitely a creatable
gametype now that I need to create. I can use build materials as well.

## #40, #41

Did some quick playtesting for Inception. Had to adjust the teleporters to not
be in the teleporter group as well as adjust the spawn system to more reliably
spawn players in the quick spawn lane. Also had to adjust lighting a bit so you
could see the sign in the spawn room better.

## #38, #39

New patch came out this morning and I am honestly PSYCHED to get to work on some
new gametypes. I think my Risk gametype is possible now as well as a Contract
based killing system. I'm super excited. But for now I spent two sessions doing
some more cleaning up of Inception. Changed to the new barrier setup with a
hollow box which fixed a problem on the roof where you could see the tops of all
the objects. Sadly we don't have the right width or depth to work with for the
full boundaries, but I left the side ones until they add more size options. I
also had to re-create the item spawners so they work properly after the patch. I
added oversized glacier walls that block out the sunlight properly since
lighting doesn't include the barriers. They were worth the performance cost to
create a better lighting experience. I swapped the Six Shooter with the purple
pistol as well. Everything should be mostly ready. I can do more performance
optimizations in the future now that we can convert any build piece to a prop. I
have lots more options. But it is good for now. I think I just need playtesting
right now and perhaps a default loadout.

## #35, #36, #37

Finished up removing the rest of the floors and walls and replaced them with
barriers to save more memory. Seems like everything is working. There were a few
sacrifices like lighting is a tad weird near the tops and sides because barriers
don't block the map's natural light sources. But it's worth the performance
optimizations. The map now loads over 3 times faster than it did. Now in less
than a minute when it was over 2 mins before... closer to 3. There's probably
one or two more sessions before this is done. I think I may need to setup a
default loadout so people can immediately jump into the game without swapping
things out. We shall see how testing goes tomorrow. For now... I'm done. Did a
LOT of work today. 10 total sessions in one day is quite a bit.

## #31, #32, #33, #34

So I realized that I have some REALLY good options for optimizations for
performance sake. First of all, I have stretchable prop blocks that I can use as
walls. In addition to that I can use the barrier device to create a pure black
wall... which I can use for the roof of the spawn room, but also use as the
walls for the actual map and the roof as well. So I have removed a LOT of pieces
as a result. It has made a huge difference in terms of loading time. Hopefully I
remove the unloading stutters that it normally causes. I still have more sides
to remove to optimize, but ultimately things are moving very very quickly for
how much performance I'm squeezing out.

## #30

Setup the spawn system and the new class system that will give you max speed
while in the spawn room. All that's really left is the weapon-free zone and
optimizing the sign on the wall and probably a minimap cover for the spawn room.
Though that actually isn't that important, so I won't do it due to performance
reasons. It was important for the main map to remove focus on the minimap during
the game. We should be just about ready for a full release. One more quick
session, then a few playtests and filming for a trailer, then writing up the
post.

## #28, #29

Finally found a decent style for the weapon organization. Had to shift the sign
upwards and make the rift more obvious, but ultimately the room looks really
nice. You can see the signs for each weapon station and you can see the portal
even when you spawn. When you respawn you can see the loadout room on the right.
The entire area looks solid. All I'm missing is a spawn room class, a weapon
free zone, and an in-game class. I then need to script players to switch classes
when they enter the map. Finally, I'll need to clean up the mini-map for the
spawn room.

## #26, #27

Spent a lot of time on performance optimizations for Inception. Removed two full
tiles off the top as well as the whole additional stuff on top of the map for
the minimap. It was worth removing it for the bit of extra performance.
Sometimes the unloading was nearly twice as fast. So hopefully as more
performance updates come to Creative it should get a much smoother unloading
experience.

## #25

Setup the spawn areas and the lighting and blockers in order to make the
gametype playtestable. And everything seems to be working great. Now it just
needs a full custom map built for it.

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
