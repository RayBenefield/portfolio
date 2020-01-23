# Worklog

## #313, #314

Trying to figure out the best way to handle assigning classes since so much is
going on at the same time. I needed a "busy" class that prevents players from
queueing while they are creating a lobby, or creating a lobby when they are next
in line. But they should be able to create a lobby while in a queue and not next
in line. There was a problem where a "busy" class was being given to a player
that joined the lobby and I need to avoid that from happening. I also need to
consider removing classes when a player dies or leaves a lobby. When they die,
they need to respawn and clear their class, however I need a gate to make sure
that the player entering the zone doesn't have a busy class because they
shouldn't be able to clear that busy class by respawning or anything. Lots of
little timing details I have to figure out.

## #310, #311, #312

I got sucked into make pretty things and got lost in the time... I haven't eaten
yet, but hey I might have a cool spawn room that I like. Now to actually take a
break.

## #308, #309

Spent time exploring what an aesthetic for people in the queue will be like. I
was hoping to use customizable lights, but the receivers don't respect the team
filter.

## #307

Created a queue for each of the 16 players and re-organized things to prepare
for a huge group of Pickaxe fighting tests. Hopefully this goes smoothly when I
do test. Still quite a bit to do.

## #304, #305, #306

Custom designed a nice little housing for my matchmaking system. I still need to
design a custom queue system, but for now this works perfect and gives me some
motivation moving forward. Next thing I need to do is make sure the queue system
works for a bunch of people.

## #302, #303

Just had a MASSIVE win. I redesigned my queue based system to only use a single
channel per player rather than two channels per player. Which opens up my system
to have 16 more channels than before. This will allow me to have a full 8
lobbies as I originally wanted rather than 5... this means all 16 players can
play at the same time now. LET'S GO!!!

## #299, #300, #301

The latest Creative Lesson took FOREVER compared to the others. It really only
should take me two sessions, but Quantity over Quality was a very big topic to
cover. Next week I'll probably cover Discipline over Motivation.

## #297, #298

Just a tad closer... had to explore combinations of joining while searching for
a lobby or dying at the same time and just lots of weird combinations to test. I
have one more minor detail to setup which is if you are in queue then you get a
red coloring and when you join then you lose that coloring. I also need to add a
HUD message for when you are next in line. And I need to start planning the
start match and what not. I also want to allow players to create a lobby while
in matchmaking, but it should also stop your queue search so you don't join a
lobby while in another lobby.

## #294, #295, #296

Got most of the system in place now. I even made the device kind of pretty. But
the create lobby system seems to be working alright and I think there is a
couple bugs with the join lobby system. I really need to just sit down and
verify a few things and test it over and over again and also drag some people in
to test it with me.

## #292, #293

Finished the spawning and the classes for BotA. Includes spawning in the sky on
their base... also took the time to setup new mutator zones to stop building all
the way to the walls, which should prevent a couple exploits.

## #289, #290, #291

Changed the Jewel system for BotA, setup a whole capture area system in the
middle. Also updated the spawn system to dynamically look at the Jewels when it
is time for the Setup phase. And I still need a spawn system that will allow
people to drop out of the sky whenever they respawn. Should be awesome when it
is ready. Oh and I put it in the middle of a large gulch.

## #281, #282, #283, #284, #285, #286, #287, #288

Spent many many sessions, too much, trying to get the dynamic quest system
working with trackers for Battle of the Architects. Ultimately I learned that
players that do not share your quest cannot affect your quest. So a team cannot
increment the target of the enemy team. SO instead I'm going to have to
compensate with a different and much simpler system honestly.

Since I didn't talk about the system in the last entry, this is the game mode
I'm making:

Phase 1️⃣ - Build a permanent Fortress for your team

Phase 2️⃣ - Hide Jewels throughout your Fortress

Phase 3️⃣ - Protect your jewels, infiltrate the enemy Fortress, take ALL of their Jewels or more than they take from you

## #279, #280

Had to test a bunch of mechanics and devices and settings and stuff for my new
idea Battle of the Architects. Should be a good one. I'll explain later.

## #276, #277, #278

Finally taking time to paint over the Gunrunners map... I started with the white
corner. So each corner feels like it will take 2-3 sessions. So this whole
painting could take about 5 hours at most. Just need to push through and get it
done.

## #274, #275

Two sessions to spit out a full lesson for the Creative Lessons. It all went
really well actually. Next thing to do is work on the publishing on Reddit for
others to enjoy. Gotta worry about links to the past article.

## #270, #271, #272, #273

Spent 4 sessions getting the video together for Creative Lesson 1 that was put
out last week. The first video took a while as I worked on setting up a nice
template to do this more in the future. Next time should take less than an hour,
which will be really nice.

## #263, #264, #265, #266, #267, #268, #269

Setup the initial prototype and all the switching required for a new Fashion
Show gametype where the streamer has control over who security guards are and
judging whether or not people move on to the next round.

## #262

Updated the inventory for Risk to include 3 chug splashes instead of minis. This
will encourage more team gameplay moving forward. I've also updated the
inventory system to use a perception trigger and an item granter to give people
their inventory more reliably.

## #261

Finished writing my first article on Innovation and did a single read out review
of it. I'm going to take a quick break and then do one more read out loud review
and then work on publishing it to the appropriate outlets.

## #260

Started out the writing for my very first Creative Lesson on Innovation. Got off
to a good start, feeling like it is a little bloated. I'm ok with that since
this is my return to the venture of writing. I'll actually take time to edit it
better this time around. Gonna take a short break so my mind can simmer.

## #259

I'm starting a whole new design series similar to my old Halo Forge ones. This
time focused on the Fortnite Creative community. I just spent a session
reacquainting myself with my old articles. I'm hoping these will serve to be
helpful for the community.

## #257, #258

Updated Forever Fights and Melee with the necessary updates I've been wanting. A
glow while you matchmake, no glider redeploy, scoring, increased cleanup time,
leave button after cleanup, and additional create/join lobby and matchmaking
buttons. Both are now re-published and I think it is a good time to start
exploring my old Forge Lessons and planning for my Creative Lessons.

## #254, #255, #256

Went through and figured out a good distance for perception triggers so I could
replace the current ones with an optimal spacing to reduce the trigger count. It
is down from 100 to 64. Now it should be much better. I also got a better
screenshot for it.

## #253

Spent some time cleaning up Stormbreaker. Fixed the darn broken barrier that
keeps eluding me. Also adjusted the pro jump to only glide through 2 sections
instead of 3. And removed a bunch of build to prop pieces.

## #252

Spent a session exploring potential ideas with 2 slotted inventories and it
looks like it won't be too bad. If someone has a grappler with their Jewel and
they go home, it will remove the grappler from their inventory. Since a common
technique is the reverse pyramid, the counter to that is to give people access
to a Grappler at 500 gold. Which is about what it takes to build a decent
inverse pyramid. Easy counter. This will force home owners to build confusing
houses instead to get their Jewels. I'm also going to be removing damaging traps
as they are not symmetrical functionally to thieves and estate owners.

Next thing I have to counter is people being able to block off the exits. To
counter that I actually have to build the entire map in the sky and not allow
building around the exits. You can still chain a wall over there, but in the
future I will have access to working no build zones. Disallowing building around
the statue will also prevent people from blocking themselves off from the statue
early on easily. In addition I'm going to create a charity vending machine where
every activiation is 1 metal so you have to sit their for a while to collect
enough building resources to get back into your base if you make it hard to get
into. All good ideas, but I think I need to take a break from this project for
now and let it simmer. I've been at it for a week so now I want to focus on
publishing other things and polishing already published stuff. And working on
another idea... probably Voltron.

## #250, #251

Worked on the flag spawners and realized that the flag spawners decided not to
work, the problem being that flags do not drop out of capture item spawners,
which sucks, but I get it. I also technically found a solution to my bugged
jewel system where if you pick it up with a boombow it breaks your inventory. I
setup an item granter that is delayed by 1 second, but gives you a single
shotgun shell. This refrehes the inventory and reveals the jewel. But after last
night's sub games, I've decided to just expand the inventory to 2 slots to
counter some common strategies that exist.

## #249

Worked to remove an entire set of 16 channels based around Flag dropping. This
should open up possibilities for more features. Next is convert all jewels into
flag spawners and update the capture points.

## #246, #247, #248

Explored some bug fixing opportunities. I figured out how HUD messages work for
the most part so I setup the HOME message to show up every time the offering
starts. I also setup team tracking to use a damage zone, this will save on
having to have everyone go back to hub every single time. I also discovered that
Flags do not have the same pickup bug for a single slot as Jewels do, so to
avoid that bug I can replace all jewels with a flag, which will take quite a
while to do. I also spent some time thinking about UX and how to teach the game,
I think I'm close to a sweet spot that will work better. I delayed the first
offering for a minute so people can experience the inability to pickup Jewels at
their house and also spend time building. If I use damage zone properly, I may
be able to remove the need for some channels. I'll have to think on things.

## #245

Updated things for balance. Removed the broken mutator zone for no weapon usage
in the hub. Updated the teleporter system so you leave by the portal of the
estate you left. And added a few experimental things to buy.

## #241, #242, #243, #244

Finished up all the last details which included setting up the vending machines,
verifying that the spawns were working and so on and so forth.

## #238, #239, #240

Just spent three sessions finishing up the last of the team based stuff. Had to
setup the attribute triggers, the team settings devices with names and colors,
as well as making sure the portals only spawn when the team is in the game. Next
thing to do is work on scoring and teaching.

## #235, #236, #237

Did some quick changes so the building system is only dependent on classes
instead of mutator zones. Everything should be working proplery from that
perspective. Then I spent 2 sessions setting up a decent looking hub to work
with for the future. It is rounded, and I'm going to use it to create a
marketplace for the thieves. Next I have to create the spawnpads to make players
spawn in the game as well as HUD messages to explain the game.

## #233, #234

Was able to work on copying the final mechanisms to make Covet work all the way
through. It took 2 sessions on stream, but things should technically work if
nothing was bugged. Problem here is that the mutator zones are buggy as all hell
right now, so I'm going to replace them with just doing class changes. The last
work that needs to be done is detecting when a team spawns into the game and
enabling their teleporter and creating the entire marketplace.

## #231, #232

So I finally figured out all the things that need to happen to make Covet work
fully with item pickup vs no item pickup and building vs not building. All the
pieces are in place on Diamond... now I just have to replicate it onto the other
15 estates... which will take too much time before the stream. Guess I won't be
able to finish it yet.

## #230

Currently playing around with resources, guns, and what not to make sure you
don't have items at the wrong time and can't exploit the system. Like having a
gun while you are a thief, or losing resources when you become a thief.

## #229

Finished up fixing the places that were all broken on each estate. Now exploring
the building vs pickup stuff that is needed for the actual game.

## #227, #228

Just replaced all of the jewel spawners as well as went through to test all of
the estates... turns out there are 3 that need minor fixes, then I'll work on
the offering class switching for picking up items and what not.

## #226

Alright with some adjustments I think that the new jewel placement should be
great moving forward. Next few sessions I'll work on duplicating it to every
plot, which will be kind of difficult since they are all on different channels
for disabling. Should be its own kind of fun. I also had an idea to have gold
spawners that drop stacks of say 30 gold or so on every property so in down time
you can go to various islands and farm gold that respawn after every offering.

## #225

Finally fixed all of the floors properly. You can now build a floor on every
square as expected. You also can't build underneath the cliffs any more. Next
thing to tackle is to reduce the number of jewel spawn locations. We are going
to drop it from 20 to 16. This is going to take quite a bit of work, probably
around 2 hours by itself. A session just to find the new locations, and then 2-3
just to replace all of them properly. Once those spawns are gone, then I'll have
8 free scripting channels to be able to handle class changing for offerings
which will allow home owners to pickup items on their land.

## #223, #224

Alright going to stop to take a breath every couple sessions to be more
efficient with my brain. I finally found the problem with the flooring. The
grass tile I was using was counting as a tile rather than a prop, no matter what
size or placement. So it was blocking floor building. I replaced it with a
different grass tile and it should work out better. I also lined the edges with
the original tile to actually block building on those tiles. I just deleted all
the flooring for every single estate, now to actually place the replacement
florring.

## #215, #216, #217, #218, #219, #220, #221, #222

I drained myself on getting these last details together for 8 straight sessions.
I need more breaks in between. I spent the time getting the teleporters working,
the blockers for the minimap, the classes, the new actual income, etc. Sooo much
was done, yet I still have so much to do.

## #211, #212, #213, #214

Spent 4 sessions just screwing around with the look of the plots of land for
Covet. I still have a lot to do to get it working, but I think it is quite close
really. I need to create the hub and the portals and the ability to exit as well
as name all the plots of land. Lots of little details need to be set up to get
it working, but I have the bare bones in place so far.

## #209, #210

Fixed a bug that would not re-roll the jewel placement and just generally tested
and verified that everything was working properly.

## #207, #208

Copy and pasted all of the Jewel spawners to all 16 player lots and made sure
that we didn't go over any receiver limitations (60 receivers per channel).

## #202, #203, #204, #205, #206

Worked fully on the scripting system that manages the Jewel spawning throughout
the game. And have it fully prepared for copying to each plot now. It required
20 Jewel locations in order to get a nice spread of locations on a plot. And
that equated to 4 different income levels. Now I need to place all of the jewel
spawners on every plot of land and create the portals and team counter and
timers properly. But I could be done in a couple of sessions.

## #199, #200, #201

Explored a few things like full size of the plot of land as well as how to cover
the whole plot and how to handle the offering statue. I think just leaving it
open in the center is best and hope that players don't screw up their path to
the offering statue. I also figured out what size the cornfields need to be to
cover a whole square while also getting broken appropriately (a wall breaks both
touching squares every time). Based on basic calculations just the cornfields
alone will result in 35K memory. Luckily this map isn't too memory intensive in
and of itself. Didn't get to much scripting, but all this exploration was
helpful for the future.

## #197, #198

Spent a whole hour just planning out the potential drop locations of all of the
jewels on the map. It looks like the end house is expected to be around 19x19 at
minimum to cover all the jewels, but this is like LONG game material. So who
knows how often it would reach a 19x19 square.

## #196

Spent one session yesterday cleaning up Boombox a bit for publishing. It was
already playable, just needed to get cleaned up a bit mechanics wise. Like
removing the speed boosts and what not. I got rid of the outside aesthetics for
now. Perhaps I'll rebuild and polish it in the future. But on to new projects...
like the new Covet. :D

## #195

Found the combination of settings needed to fix the no build bug for Forever
Fights. Also updated the blockers on Stormbreaker to not block weapon fire. I
also fixed the matchmaking bug in Forever Melee.

## #192, #193, #194

Spent three sessions just cleaning up the showcase area for Forever Fights. Also
attempted to fix the no build bug by adding new mutator zones for joining
players. Hopefully it is enough to get things working well. Otherwise I will
just cry over and over again.

## #190, #191

Started to setup the initial scripting systems needed for the new take on Covet.
Had to play with quest trackers and item granters to create the income system
for it.

## #187, #188, #189

Spent three sessions making Forever Fights pretty and polished. It is now fully
published and ready to see the public.

## #185, #186

So I just came up with an insane idea... an idea I had YEARS ago for a game,
that I just realized I can actually build in Fortnite. This could be a crazy
crazy game. A very long game of planning and deception and sneakyness... it
could create the most insanely fun and surprising gameplay while also being
tactical and deliberate. It's also a long duration game where you have to invest
a lot of time into it. And it uses mechanics not really used in any other games
that I've seen. Makes shadow bombs a staple item. Perhaps could make use of a
prop gun as well. I'm kind of excited and it requires very little aesthetics on
my part as well. This could be an awesome game.

## #179, #180, #181, #182, #183, #184

Repurposed Forever Melee into Forever Fights which is a box fight version with
matchmaking. I've enclosed the entire map, setup a layout, created all the
arenas, updated the barriers, mutator zones, and timers, and also added a buffer
barrier on the outside. I also utilized the last 5 channels in order to create a
cleanup phase after a box fight so C4 can be used to cleanup before making the
arena available again. So now it is ready for testing, the aesthetics for
publishing.

## #175, #176, #177, #178

Fully decked out the aesthetics for the Forever Melee map and got it completely
published. This includes walls, and encompassing the matchmaking system and
decorating the outside of the boxes.

## #169, #170, #171, #172, #173, #174

Spent all morning upgrading the Forever Melee system to support 5 lobbies. I've
think I've fully done it, plus added some nice visual systems to show when a
lobby is open or closed from the outside and how to join or create a lobby. I'm
excited about the little features and it should be a lot of fun to test today.
Then I can start working on Forever Fights.

## #166, #167, #168

Took some time, but with some great help from GEB, Tubby, Cookie, and Royal I
was able to get the Forever MM system working with a simple Pickaxe proof of
concept. The elimination managers weren't working, but I figured out why
(something I ran into before). And now it works like a charm... it breaks every
once in a while, but otherwise it is SUPER consistent and I'm excited to use
this system for future 1v1 gametypes.

## #165

Finished up the bases and the roof and the vines and the bushes for the new
style for Risk. Should be close to done, just need HUD messages and what nots.

## #162, #163, #164

Found some bugs in the room search system, patched those up and I think I have
everything working. I just need to setup the class and timer and mutator system
to verify the box fights are actually fully fleshed out, then I need to actually
build everything according to 5 different rooms.

## #159, #160, #161

I think I fully re-setup the matchmaking system with 3 available rooms while
also creating the ability to join and create a lobby on the fly at each
individual lobby. This should speed things up as not everyone needs to join
matchmaking right away, they can all run and start lobbies and this also allows
people spectating to challenge said person. Could result in great moments of
matching against the person that keeps winning while you spectate. And leaving
is now disabled during a match so that will be good as well. Next things to do
is to build in the blocker/timer start match and elimination system. If that all
works well then I can build the whole system with - what looks like - 5 rooms
total. Meaning optimal size of games is 10, but it can hold 16, they just have
to wait for a lobby to open up. I want to build an infinite matchmaking system
that will keep searching until a room or lobby becomes available. So that way
people that can queue up and wait for the next available.

## #157, #158

Started working on a revamped system for Forever Fights. I am setting up lobbies
to be explicitly joinable from the front of the lobby. Also I want people to be
able to manually create lobbies when they walk up to an available room. This
will result in more channels used, so less available rooms overall. So less
rooms means not everyone can fit in when there are 16 people. So I would like to
implement an infinite matchmaking search that will keep scrolling until a lobby
becomes available. Right now I'm just making the system with 3 lobbies to see
how many channels it is going to take per lobby.

## #151, #152, #153, #154, #155, #156

Started a whole new aesthetic for Risk so we can get Risk published, the
gameplay is actually solid and I just need it to look good now. I'm going with
an aztec style indoor stadium with vines and pillars in the middle. I think this
should work out really well moving forward. The 6 sessions I pulled off resulted
in quite an awesome looking place.

## #149, #150

Spent a couple sessions just creating new overlays for every single gametype
idea I've had that needs to be published. Right now I'm at 15 ideas... which is
absolutely insane. And I'm not even close to done yet. So pumped to get all of
these published. It's awesome that every single one is unique in its own way.
There is no duplicate gameplay in the slightest. Just gotta keep building and
pushing out as fast as I can while coming up with new ideas.

## #148

Finished up the last bits for Stormbreaker. Moved the checkpoints and added
decals accordingly, just needs a final test to verify. Also added a HUD message
for players to know how to play.

## #146, #147

Setup the blockers to allow for weapon fire and we created a switch system using
sequencers to trigger a win condition when one team defeats the other and breaks
their structures. The next thing to do is extend the locations of the
checkpoints so the decision to hit a checkpoint is a deliberate one and slows
you down towards the middle.

## #142, #143, #144, #145

Spent many sessions trying to redesign the stream overlay that holds the
information on the current map so it looks more detailed and cleaner. I think I
have something I can work on later, but I need to move on to creating logos for
all of the gametypes I have before anything so I at least have those setup and
ready to go for the stream.

## #135, #136, #137, #138, #139, #140, #141

So I actually spent a ton of time creating logos and a basic stream overlay to
show the name of the map we are playing on as well as the code. Super simple
right now. I'm actually quite happy cuz I found something that feels good.

## #134

I believe I have a fix for the dying while negotiating a contract bug that uses
a sequencer to reset the wanted posters. If it doesn't get a re-roll trigger
after X amount of time it will enable the wanted posters again to allow for a
new contract. This either happens when a contract is given or when a person dies
before getting their contract. I am working on the alternate spawn system right
now, trying to build a reliable teleport system out of dropping people into a
teleporter. Hopefully it works well.

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
