-Module:
Basic Trader Profiles Expansion

----------------------------------------------------------
-Compatibility:

Mods adding new items to traders should remain compatible, but authors may want to check the changes and new files to make use of them.

These mods are redundant with this mod and not needed:
	Barkeeper - Advanced Trader
	Beard - Artifact Hunter
	CZ75 Automatic for Military's trader
	Kalancha buys artefacts & mutant parts
	Sin trader fix
	Trader Trapper

Vanilla Trade Fix is supported, use the patch included. More info below.

No known conflicts are known with the following mods, and should be compatible:
	Actor-NPC trade QoL Pack [Mumuskeh]
	Faction Based Economy [HarukaSai]
	Spleen stock fix [KalakCZ]
	Trader Destockifier [TheMrDemonized]

Other trade overhauls may not be compatible. Trader Overhaul probably isn't. Do not ask me to patch for it.


----------------------------------------------------------
-Explanation:

This mod takes the fixes in Vanilla Trade Fix as a base, adding changes from other mods without extraneous items, and then some more tweaks. 

This is only a trader overhaul in the sense that it expands over what some traders do. I'm unaware of how compatible would it be with other trader overhauls (Trader Overhaul is right out though), but it can be used as a stepping stone for one, and by other mods just trying to add their items of course.

This mod includes new trader profiles to be used by different traders who previously only used a generic one in vanilla. The main idea is that some certain areas and/or factions are lacking in some merchant types. So we expand what some of the existing traders do to cover those needs.

Trade Overhaul does something similar, but with more traders and it always felt too complicated to even dare touching it. This should be much more simple. At least for now.

Do understand, mods need to actively use these new profiles to actually add their items to these traders.
Mods using the trader_autoinject method should be fine as long as you use the patched version of the script included in this mod. For example, WPO, OPO, Hideout Furniture, Powered Exos, or Toxic Air.
Mods that use their own method targeting for example the trader's logic file should also be fine. For example, Armor Modkits.

For those using the DLTX method, it requires patching. A simple DLTX patch included with the main files of a mod should be enough. If a user isn't using Basic Trader Profiles Expansion, such patch will simply fail to apply and the game will run as normal. However, ideally this requires the mod's author doing it.

This is the list of traders with new profiles, and the new files you'd have to DLTX patch for each:

-Ashot		->	trade_freedom_ashot.ltx		->	mod_trade_freedom_ashot_mymod.ltx
-Barkeep	->	trade_stalker_barkeep.ltx	->	mod_trade_stalker_barkeep_mymod.ltx
-Beard		->	trade_stalker_beard.ltx		->	mod_trade_stalker_beard_mymod.ltx
-Forester	->	trade_stalker_forester.ltx	->	mod_trade_stalker_forester_mymod.ltx
-Kalancha	->	trade_csky_kalancha.ltx		->	mod_trade_csky_kalancha_mymod.ltx
-Peregrine	->	trade_ecolog_peregrine.ltx	->	mod_trade_ecolog_peregrine_mymod.ltx
-Trapper	->	trade_stalker_trapper.ltx	->	mod_trade_stalker_trapper_mymod.ltx
-Tukarev	->	trade_ecolog_tukarev.ltx	->	mod_trade_ecolog_tukarev_mymod.ltx

Ashot shared a profile with Flint. Some mods already attempted to add items to Ashot's inventory as if he had his own profile, but no such thing existed. Now it does, and those mods can live in peace.

Barkeep remains a barman, but now sells bandages and medkits. As you grind your goodwill he will start to offer some equipment, weapons, and armor. Nothing cheap like a PM, but nothing heavy, explosive, or expensive either like PKMs, Exos, Veles detectors... also attempts to not repeat anything sold by Duty. Basically, if you're a non-Dutier with no gun or armor, he can fix you up with something until you return to your main faction trader for a true replacement, but that's all. After all, it's not good to have your kitchen full of weapon boxes.

Beard will remain a barman, but like scientists he'll also be in the artefact hunting business.

Forester remains a mechanic. But he'll now sell some basic food, cooking, and first aid supplies, in case the Red Forest, uh... You know. Red Forests your ass. No need of toolboxes.

Kalancha will remain a medic, but also buy artifacts and mutant parts at a high rate like scientists.

Peregrine and Tukarev remain as mechanics, but now will double as suppliers for ecologist players, independently from toolkits: ammo, knifes, outfits, non detector devices, PDAs, combat oriented purchasable attachments. All of that is also removed from Sakharov and Hermann who now only sell the SPP outfits, Screen helmet and detectors. Peregrine and Tukarev will only sell gear, not buy (so you don't abuse that 0.01 condition factor to buy all technicians have).
This bloats their inventory a bit, but I think it should be fine. And this way, a new ecologist player can start gearing up after some quick jobs, without need to travel to other areas with friendly factions, and free the scientists for science items only.
Something similar can be done to other technicians if there's any interest, but their seemed the only justified cases.
DO UNDERSTAND, this will cause inconsistent behavior with mods adding items to Sakharov and Herman. The patching is easy, the issue is doing it at the source.

Trapper now trades with hunting equipment and mutant parts. Basically the same items as Butcher, but minus the break action shotguns, which don't cut it anymore at the north, and plus additions like the missing knifes, Saiga and Vepr shotguns, and the Remington 700, which only Freedom sells in vanilla. Haven't touched the dialog rewards for the parts, hopefully those remain more profitable than selling them directly.

Additionally, all main weapon and outfit traders (ie: Dutchman for mercs, but not Vector in Zaton) get a sixth supply tier, [supplies_6], that checks for true faction membership, meaning players from different factions can't access them, no disguises.
They're empty for now. However, they can be used to space out inventory a bit more. And/or if you want to hide your modded items at very high goodwill requirements, as I do with Connelly's Unifying Nosorog Tweaks.

The goodwill progression with some traders now allows for other factions. Basically, they recognize you're not just anyone, that you may have some standing, that you may be useful, and more importantly, the money to spend.
Barkeep, Loris, Owl, and Sidorovich (and the flea market with Vanilla Trade Fix) will accept goodwill grinded with rest of the "respectable" factions: loner, Clear Sky, Duty, Ecologists, and Freedom. They're just making business, after all.
Some factions may also accept the goodwill gained with another:
-Army and Ecologists.
-Army and Duty.
-Bandits and Renegades.
-Ecologists and loners.
-ISG and Mercs.
-Monolith and Sin.
However, this only takes you as far as the third supply level (fourth with the loner traders). Beyond that, you'll need to grind their actual faction goodwill.
Redone Rank Progression does something similar, but only for Owl, and for Barkeep and Forester in its Trade Overhaul patch.

Also, for some reason the Sin and Renegade traders were checking for the Monolith and Bandit goodwills, so, uh, now they check for their real faction goodwill.
Of the three ISG traders, the starting one gets no food or meds. He does now.
Clear Sky was the only faction to sell the Ash-12, at the second goodwill tier. Too early and too scarce, I think. Similarly, the Mercs and ISG were the only factions to sell the CZ75, and other factions may not be too friendly with them.
I raised the Ash-12 one tier, and gave both weapons to Duty and the Army as well. Peregrine too, if you provide all toolboxes and high eco goodwill.

Other than that, traders will keep working as always for the most part.


I'm already patching several mods covered by Uncalled, or that I otherwise manage, to natively use the new features, and only have Hermann as the one of the two scientists selling guns.
If you want to ensure Sakharov and Hermann doen't get any new weapons or outfits from existing mods, I'm afraid that best that can be done by now is to make a filter search in MO2 for
mod_trade_ecolog_sakharov
mod_trade_ecolog_hermann
and right click hide any of them you're sure it doesn't add anything important.

----------------------------------------------------------
-Patches:

Vanilla Trade Fix
This patch integrates the tweaks into VTF's fixes. Let it overwrite its files.
A typo in VTF that broke the addition to traders of an explosive (it added "mine _new" when it should be "mine_new") has also been fixed.
However, Boomsticks and Sharpsticks may not be compatible with VTF, and hence with that patch.
Boomsticks and Sharpsticks Lite will be updated to account for all changes. The only requirement is that you disable the gamedata/scripts/bas_trade_inject.script file in the original BaS.

Nimble as a Clear Sky contact
Usually, most traders have five supply tiers as you progress acquiring goodwill with their faction. Nimble's profile though only have one. Now, if you're a true CS member (disguises won't help) even without goodwill gained, he'll start offering through all five usual tiers the faction outfits and some weapons.
At first I thought about Nimble not having those weapons if Owl already does, except when Spore offers them at a lower goodwill than Owl. But it is possible for CS players to not grind their loner goodwill, so Nimble will indeed have the same stock as Spore, even if it overlaps with Owl. Except for utilities and most ammo and basic equipment, so that you don't forget about grinding your loner goodwill.
This of course bloats his inventory (more than even Peregrine's case, hence optional), but it should make it easier for CS players to gear up if you're north, or even if you use some mod to start the game north instead of at the Swamp. It's not a proper CS northern outpost, but it's something. And if there ever comes one, you can discard this file (hence, being optional).
Can be used with and without the VTF patch above (technically they'd need different values for total consistency but the difference is trivial and fuuuuuuuuuck making even more files).

Ecologist technicians as armorers
In vanilla Anomaly, the ecologists don't sell guns or combat helmets. This will add a very limited selection to Peregrine and Tukarev, though you still want to check with other factions for real firepower:
Tier 1: PM, Fort, Kiparis, TOZ-194, grenades.
Tier 2: Beretta, Fort 500, PP2000, SKS, L85, silencers, scopes, ACH-7EX helmet.
Tier 3: Walther P99, AKMN, FAL, GP-10z gas mask.
Tier 4: GSh18, Saiga, SVD, Exohelm (to pair up with the eco exo in case you play with Separate Helmets).

trader_autoinject patch
Modified trader_autoinject.script so the new profiles are properly assigned an internal trader type.
This should help avoid issues where mods adding stuff through this script end up adding it to the wrong trader profiles. For example, Hideout Furniture adding full furniture to Peregrine, instead of only the technician selection.
Install it as a separate mod at the top of everything, after every other instance of trader_autoinject.script.
Includes a fix by RavenAscendant to avoid a busy hands bug, previously unidentified since the last update by Arti.

Boomsticks and Sharpsticks
Tweaks some of the script files in BaS for proper compatibility.
Do not use with BaS Lite, as it uses DLTX for distribution.

Hideout Furniture
This modifies one of HF's placeable_items_trade.script file to prevent it from adding furniture to the inventories of Nimble and Trapper.
Make sure it loads after HF. You can replace the original with this one, I'm not aware of other mods touching it.

ReDONE Rank Progression
Make sure this patch loads on top of the mod, as it overwrites some of its files.


----------------------------------------------------------
-To-dos:

For Beard, I'd like to recreate his artefact hunting jobs like in CoP, but that requires some work with dialog files. Another time, maybe.

Ideally, I would like to recreate the relationship between Beard and Owl as in CoP, where Beard doesn't trust Owl and Owl only cares about the information you sell him. Basically, Beard would sell some basic loner gear to make sure peeps are safe, and Owl only offers better supplies to those who sell him enough looted PDAs. Not sure how to get around the later yet to justify the former.

Spleen seems to have all toolboxes, meaning you can't unlock his trade tiers. Spleen stock fix gives him goodwill progression like traders. Ideally, his tooldbox progression would be restored.


----------------------------------------------------------
-Information for modders:

To use the new supplies_6 in main traders, you only need to treat it as any other supply level with a DLTX patch. For example:

![supplies_6]
wpn_very_rare_rifle

--------------------------
Nimble receives a "supplies_1_cs" that forks from his lone vanilla supplies_1, which has his special orders, then keep going with normal "supplies_x" sections from 2 to 5:
	[supplies_1_cs]:supplies_1 
	[supplies_2]:supplies_1_cs
	[supplies_3]:supplies_2
	etc

You can keep using his supplies_1 for the very rare weapons as normal.
If you're also adding stuff to Spore (for example, you're authoring a weapon pack), just duplicate it.
Remember, Nimble's supply level for *normal* stuff is supplies_1_cs, not supplies_1. Consider it a gating tier.
For example:

![supplies_1]
wpn_very_rare_rifle	= 1, 1
![supplies_1_cs]
wpn_cheap pistol	= 1, 0.88
![supplies_2]
wpn_normal_smg		= 1, 0.88
![supplies_3]
wpn_decent_rifle	= 1, 0.88

--------------------------
Peregrine and Tukarev's profiles can be patched just like the generic mechanic one if you're only changing that aspect. However, if you want to add gear to their supplies, things are a bit more complicated.

A set of sections gear_x are added from 1 to 5. Each one is the equivalent of a supplies_x in normal suppliers, and these are where you need to add your item.

Peregrine starts at:

[supplies_1_gear_1]:common_stock,gear_1

Meaning he'll offer both the basics of tech items and gear. If you provide the basic tools:

[supplies_2_gear_1]:supplies_1_gear_1,gear_1

He'll now offer the next stage of tech items, but still the same gear. If now we pass the first goodwill treshold:

[supplies_2_gear_2]:supplies_1_gear_1,gear_2

Now he provides the next batch of gear, up until reaching supplies_4_gear_5

Past that is supplies_6, which works like those added to other traders.

Hopefully, this retains compatibility with scripted methods of changing the inventory of technicians.

In short. For a DLTX patch, instead of the usual:

![supplies_1]
wpn_myweapon

use:

![gear_1]
wpn_myweapon

----------------------------------------------------------
-Known issues:

Mods using trader_autoinject don't seem to quite apply their items correctly even with the patched file?

Mods using DLTX for item distribution would have to use the new trade files for correct assignment. Not much I can do here, it's up to modders to make use of them.