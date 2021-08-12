# sm_cbomb
WiLdTuRkEy's Clusterbomb Plugin

see https://forums.alliedmods.net/showthread.php?p=1789358
 
This is pretty much what the title says. It allows you to toss a clusterbomb that can be customized via cvars. It can also set up as admin-only or for all
players. I built this with HL2 in mind, but it should work for any mod as long as you set the model and sound cvars to something that exists in that mod.

How it works...

You fire the command.
A canister is thrown in the direction/pitch you are aiming. The model is models/props_junk/PropaneCanister001a.mdl,
but you can change it to anything. 2.5 seconds later (default time), the canister expels 10 (default) grenades into
the air. The expulsion pattern depends on the vertvel, spreadvel, and variation cvars. By default, they just get
thrown up a little and spread a little. Grenade models are models/Weapons/w_grenade.mdl, but can be whatever you
want. NOTE! Some models tend to get stuck inside of each other and they all just freeze together. You just need to
try some and find good ones that don't. ;)
Each grenade explodes at a random time between 0.5 and 1.0 seconds after being expelled.

Note... You can also knock someone out if you hit them with the canister itself.

Commands

    sm_cb | sm_cbomb | sm_clusterbomb - Toss a clusterbomb in the direction you are aiming!

ConVars

    sm_cbomb_enabled - Is the clusterbomb feature enabled? (0|1)
    sm_cbomb_enabled_plr - Can non-admins use clusterbombs? (0|1)
    sm_cbomb_wait_time_plr - How many seconds non-admins must wait between clusterbombs. (1 - 600)
    sm_cbomb_wait_time_admin - How many seconds admins must wait between clusterbombs. (1 - 600)
    sm_cbomb_throwspeed - How fast you throw the clusterbombs away from you. (0.0 - 2000.0)
    sm_cbomb_detonation_delay - Clusterbomb will detonate this many seconds after throwing it. (1.0 - 5.0)
    sm_cbomb_bomblet_count - How many bomblets does each clusterbomb contain? (2 - 30)
    sm_cbomb_bomblet_vertvel - How fast bomblets are thrown in the air when spawned. (20.0 - 500.0)
    sm_cbomb_bomblet_spreadvel - How fast bomblets spread out after they are spawned. (20.0 - 500.0)
    sm_cbomb_bomblet_variation - Vertical and spread speeds will be varied between 1X and this value. (1.0 - 5.0)
    sm_cbomb_bomblet_magnitude - Damage magnitude of each bomblet. 100 is about like a normal grenade. (0 - 500)
    sm_cbomb_canister_model - The model that holds all of the bomblets in it.
    sm_cbomb_bomblet_model - The model that represents the individual bomblets.
    sm_cbomb_detonation_sound - The sound made when the clusters are spawned.
    sm_cbomb_version - duh...

A cfg file will automatically be created with some default values here -> gamemod/cfg/sourcemod/sm_cbomb.cfg. Note that you can also change things on-the-fly
in-game (including models and sounds).
