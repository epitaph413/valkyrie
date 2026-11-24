# Changelog

What changed in each version of Valkyrie, newest first. Dates are Brisbane time.

## 0.19.0 (2026-11-24): nothing is known until it is carried

- **Information travels like cargo.** Every relay station, star carrier, picket, courier, trader and captain keeps
  its own intelligence database. A record is what one observer saw at one moment: who held a system and how firmly,
  a battle and its result, a fleet massing, a holding fleet's size, a relay up or down, an enemy carrier or picket
  sighted. Records move only when two holders meet, newest wins (a doubtful report counts as ten minutes older), and
  nothing is ever broadcast. Each record keeps when it was first seen, when last confirmed, who saw it, how many hands
  it has passed through, whether it has been passed on, and how far to trust it.
- **27 relay stations**, one in every system the two powers hold, each a real station you can fly to (and shoot):
  - **Local** (11): connects its own system; sync only at the relay itself.
  - **Regional** (6): Ilkmere, Hearthfall, Descant; Graelhold, Cinderhome, Ascendancy. Each runs a regional star
    carrier round the local relays near it.
  - **Strategic** (4): Lattice Throne, Choir's Veil; Vorrak Prime, Vashkar March. High command, linked by long-haul
    star carriers; pickets are built here.
  - **Military** (6): Radiance, Spindrift, Lanternrest; Rampart, Veyr, Slagreach. Pickets report here first, a courier
    rides anything urgent to high command, and they can order reinforcements.
  - The free ports (Tarsis, Brasshold, Driftmark, Meridian) trade public news only, carried by two Orrin traders.
- **Ships of the networks**, each a real ship that moves system to system on its own: 8 long-haul and 6 regional star
  carriers, 6 couriers, 9 pickets. They avoid enemy space and battles where they can, can be intercepted on the way,
  and turn up in front of you. A destroyed one loses everything it carried; strip its wreck and you get its data core.
  Lost ships are rebuilt at their home relay after 10 to 20 minutes.
- **Pickets** sit in the other side's border systems, watching. When they see something urgent (above all a fleet
  massing for an attack) they run for the nearest military relay at once.
- **It changes the war.** Attacks now mass for four minutes in a neighbouring system first. A defender brings a
  second capital group at the start only if its command already heard about the massing fleet; otherwise the second
  group comes only when a battle report reaches one of its strategic or military relays, and then has to fly there.
  Attackers choose targets by what their own command believes each system's hold to be. A side whose network is in
  pieces wins fewer of the battles fought while you are away. A captured relay hands its whole database to the side
  that took it.
- **Your own picture.** Your map and the War tab show what you know, never the truth: who holds each system as last
  reported, with how old that is and who said so; battles as reported (BATTLE or WRECKS, with their age); relays by
  type; network ships seen. Old news is drawn dashed and faded. Comms only announces a battle or a change of hands
  when you see it yourself or a report reaches you.
- **The War tab** adds an Intelligence table of every record you hold, marked **Observed**, **Recent**,
  **Outdated**, **Historical** or **Unconfirmed**, with age, source, hands and trust; and the relay networks as far as
  you know them. Old records are kept, never deleted.
- **Syncing is automatic.** Fly into range of a relay of a power that trusts you (standing 0 or better) and you swap
  reports; they pay in standing for news of the other side (up to +150 a visit). Docking at Tarsis swaps public news.
- In a hosted game each captain has their own picture, kept by the host and sent to them alone.
- Network protocol 9: everyone needs 0.19.0 to play together.

## 0.18.0 (2026-11-24): a galaxy at war

- **32 systems instead of five.** Every race has its own territory: two to four systems each, one of them a
  capital that never falls. There are neutral systems too: Tarsis, the Free Companies at Brasshold, the Outer
  Collective at Driftmark and independent Meridian. The Elysian Gate's dead star is in the north, held by no one.
  All 32 can be reached from Tarsis on the Magpie's starting 6.5 ly drive, a few hops at a time.
- **The front moves.** Flash points now burn wherever Concord space meets Dominion space, not at four fixed
  places. Every system has a hold. A battle the defenders win shores it up; one they lose knocks it down, and at
  zero the system changes hands, to the race whose space the attack came from, with a new holding fleet. A side
  that has lost ground brings its second capital ship more often.
- **You can push it.** Fight with a side at a flash point, or wreck a system's holding fleet: each holding ship
  lost costs that system 12% of its hold. Holding fleets rebuild eight minutes after the last one goes.
- **The war goes on while you are away**: another battle somewhere on the front for every twenty minutes, up to
  ten. When you launch, comms tells you what changed hands.
- **The three great fronts** from the lore are on the map: the Ashen Frontier, where the Dominion is winning; the
  Elysian Front round the Gate, where flash points wake the Remnants more often; and the Celestial Reach, where
  the Seraphine keep their best ships.
- **A new galaxy map**: each race's space tinted in its colour, the front line burning between the two powers,
  capitals marked. Drag to pan, scroll or use the buttons to zoom. Pick a system to see who holds it, its hold,
  what it borders and its holding fleet.
- **A War tab at the station**: the same map, how many systems each race holds (and how that has changed), and
  news from the front. The station board tells you when systems have changed hands since you last looked.
- In a hosted game everyone sees the host's war. Network protocol 8: everyone needs 0.18.0 to play together.

## 0.17.0 (2026-11-23): a clearer first flight, dropped links, better reports

- **The first sortie brings the cockpit in a few windows at a time.** Finding her shows only the scanner,
  contacts, comms and the speed and sensor orders. The Target window and gunnery orders arrive when you go after
  her, your own systems when she starts shooting back, and the rest after that. Each new window is outlined for a
  moment, and the tutorial card says in a line what it is for. Ending or finishing the tutorial shows everything;
  free flight and multiplayer are unchanged.
- **Seen: how old your picture of a ship is**, now up front. The Target window leads with it in big type, with how
  far she has moved at her last speed since that light left her. The box around her in the view carries it, and
  Contacts has a new **Seen** column. Blue is fresh, yellow is 3 s or older, red is 10 s or older or a lost track.
- **Dropped connections.** If a friend's link drops mid-sortie, the host holds their ship for 90 seconds and the
  friend's game reconnects by itself (it tries every few seconds), back in the same ship with the same orders.
  If they don't return in time their ship goes home. Friends waiting at the station see the host come back after
  the host closes and reopens the game. Tested: drop and rejoin, orders after rejoining, the grace running out,
  the host leaving and returning.
- **Problem reports.**
  - The game keeps the end of its log in the browser's storage, so a report made after a crash includes the session that crashed.
  - A start-up that never draws its first frame is noticed next time: the station says so and offers a report.
  - After two failed start-ups in a row, the game starts with safe graphics (smaller planet maps and the older planets) until a start-up works.
  - In the app, reports also include the app's own log of crashes it saw from outside the game page (graphics process, game page, freezes).
  - The report dialog now says plainly what a report contains, what it never contains and where it goes, and has a box to leave captain names out.
- **The app** moved from Electron 33 to Electron 45 (a current Chromium, with the security fixes since). Its build
  tools were updated too: `npm audit` reports no known vulnerabilities. The app also turns off Electron features
  it does not use (running as plain Node, Node options, the debugger port) and only loads its own packed files.
- **What's new** at the station shows this list once after an update; **CHANGELOG.md** has every version.
- **Packaging:** SHA-256 fingerprints of the downloads (SHA256SUMS.txt), the code-signing warning and how to get
  past it explained in Start here and Read me, copyright and description in the exe's properties, and a fix for
  the Read me repeating its last line.
- Network protocol 7: everyone needs 0.17.0 to play together.

## 0.16.2 (2026-11-23): set your own Follow distance

Next to Follow in the Target window there is a box: type any
distance in km (0.4, 3, 250...) and press Enter. Follow then holds you that far off her. Leave it blank for automatic
(just inside gun range, as before). It is kept with your career, and works for friends in a hosted game too.

## 0.16.1 (2026-11-23): Windows black-screen fix

- on Windows the app went black on Host or Solo: the planet painter's shader took the graphics
  driver over 45 seconds to compile. Its noise now comes from a small 3D texture, and each planet type has its own
  shader; on an RTX 3080 Ti each compiles in under 0.2 s.

## 0.16.0 (2026-11-23): new skies

- **Planets are painted on the graphics card** when you arrive, at 2048 by 1024, and drawn with their own lighting:
  a soft day/night line, relief you can see in the low sun, sun glint on oceans, clouds that drift and throw shadows,
  city lights on the night side of Tarsis II, glowing cracks and seas on the lava worlds, red-brown cracks on the ice
  worlds, crater fields on the rocky ones, storms and shearing bands on the gas giants, and a thin atmosphere at the
  rim. Rings have gaps, are shadowed by their planet and shadow it in turn. The maps are freed when you leave a system.
- **The star** has a streaming corona and lens streaks, and faint lens ghosts when it is on screen (hidden when a
  planet or a rock is in the way).
- **The galaxy:** a warm core, red and teal glowing gas along the band, dark dust lanes and filaments, distant
  galaxies as small smudges, and many more faint stars.
- **Asteroids from Blender:** a new set of 14 rocks (eight big, six small) with craters, rims and baked regolith
  replaces the old noise rocks. Each field keeps its tint. The model is `models\Asteroids\static_rocks.glb`; the
  scene is `static_rocks.blend` next to it, and the script is `source\blender\tarsis\asteroids.py`.
- Multiplayer protocol 6, unchanged. Everyone should still update to 0.16.2 so you all see the same skies.

## 0.15.1 (2026-11-23): the new Tarsis Ring

- Tarsis Ring rebuilt in Blender as a fortified free port (bastions, gun turrets, a turning habitat ring,
  21 lights): `models\Tarsis Ring`.

## 0.15.0 (2026-11-23): the shard rings, and infamy

- **A Gate shard aboard rings on every jump**, fitted or in the hold, and the apex powers hear it. Resonance (shown
  in the Ship window) climbs about 22% a jump and slowly with time in space; docking at the Ring halves it, and a shard
  left in your stores does not ring. After each jump, the louder it is, the likelier someone follows (about 20 to 45
  seconds later):
  - **Seraphine Wardens** hail first, with a 30-second answer box on screen: **Hand it over** (Concord standing
    +2,500, they leave, and a worn Myrr loaner jump drive goes in its socket so you are not stranded) or **Refuse**
    (they attack). Firing on them is also an answer.
  - **A Vorrakai hunt** does not hail. If they wreck you while they are still in the fight, they cut the shard out of
    the wreck before the tug arrives.
  - The party grows with the resonance, from a picket and a frigate up to a destroyer with escorts. The shard
    ignores 65% of their damping, so jumping clear is usually possible.
- **Three buyers at the Ring** (top of the Missions tab while you own a shard): the Seraphine Envoy (¢60,000 and
  +3,000 Concord standing), a Vorrakai broker (¢120,000, +3,000 Dominion, −1,500 Concord) and a Myrr guild factor
  (¢180,000, no standing either way: nobody will know).
- **Infamy** (top of the station): kills and captures add to it, more for bigger and higher-tier ships; a Remnant
  brought down adds 30 and a beaten hunt 10 to 12. Ranks: Nobody, Noticed (15), Notorious (50), Feared (120),
  Dreaded (250), Legend (500).
- **Ships talk on COMMS** when they engage you, when they are losing and when they strike. Each race has its own
  voice: Vorrakai arrogant, Grael by-the-book, Vashkar engineers, Krell miners, Dustborn bitter salvagers, Seraphine
  serene and condescending, Myrr precise, Ilk transactional, Tessari practical, Pell young and nervous. Whether they
  sneer or beg depends on their class, their tier against your guns, their race's temper and your infamy. Until you
  are Notorious they call you "salvager" or "scrap-picker"; after that they know your ship's name.
- **Fear changes fights:** a ship that is scared of you starts with less nerve and strikes sooner.
- Multiplayer protocol 6: everyone needs 0.15.0.

## 0.14.0 (2026-11-22): the Remnants

- **Some flash points now have a Remnant lying between the fleets**: a First Architect machine from the lore, a dark
  octahedral lattice with four lance blades, an eye, a damping ring and two great rings turning around it. About half of
  all flash points have one.
- **It is dormant, and it drinks.** Every shot fired near it and every ship that dies feeds it, and it charges slowly
  on its own while the war is there (the same way the war is waking the Elysian Gate). Its charge shows in the Target
  window and the contacts list; sensors warn at about 35%, 70% and 90%. Shooting it while it sleeps feeds it too: on the
  Disable rules the gunner holds fire on it.
- **Filled, it wakes.** Its plates open and the light comes through, its damping field comes up (no one jumps out near
  it) and its four lance nodes burn whatever is loudest within 280 km: Concord, Dominion or you. A lance burns through
  up to three systems. Run silent and slow and it may pass you over; you get a warning, and a couple of seconds, when it
  turns on you.
- **Both fleets turn on it.** Masers do not trip Architect work. Its Heart and the Gate shard are warded while its lance
  nodes stand, and damaged nodes re-knit unless destroyed outright: bring all four down and it collapses. Sometimes the
  fleets win; sometimes it burns them and goes quiet again, and is still there.
- **The prize: the Gate shard**, cut from the wreck: a jump drive with 40% more range that **ignores 65% of any damping
  field**. The wreck also gives Architect lances (masers that trip and burn 30% harder), an Architect eye (sensors),
  the Stillness ring (damping projector) and lattice plate (armour). On the Magpie they hang as the actual pieces.
  An ordinary part of the same type and tier can mend an Architect one; an Architect part is never used up mending an
  ordinary one.
- Unwatched, a Remnant still wakes in the background, and ops reports the gravimetric spike from wherever you are.
- Multiplayer protocol 5: everyone needs 0.14.0.

## 0.13.0 (2026-11-22): every ship redesigned, and the bridge decides your hull

- **All 55 ship models are new**, built to the ship style guide (in the project: "Ship style guide") and the setting
  lore. The old models were the game's box-and-cylinder shapes with detail painted on; these are designed hulls:
  - Dominion: the Vashkar build its hardware, so the Grael (slab-armoured bastions, a troop carrier with drop pods),
    Krell (mining rigs, an excavator, an ore hauler) and Dustborn (patched and stripped cast-offs, a broken white ring
    painted over Dominion marks) all fly Vashkar-pattern hulls. The Vorrakai are black armour with red light leaking
    from the seams: blades, talons and dreadnoughts.
  - Concord: every member builds its own way. Pell tank stacks and troop drums, Tessari work ships with torch-arms
    and farm drums, Ilk needles carrying other races' parts, Myrr crystal (the destroyer is a tuning fork), and the
    Seraphine: pearl daggers with gold feather wings, a halo carrier and a caged-core capital.
  - Every targetable system is a real part in the right place, so called shots hit what you see.
- **Bridges are a part now, and the bridge you fit decides your hull.** Strip a bridge from a picket, frigate,
  destroyer or carrier (a capital's only sells) and fit it: you fly that ship's hull at full size. Bigger hulls are
  tougher (destroyer +45% hull, carrier +60%) and hold more (+3 and +5 bays) but are slower, turn worse and are easier
  to spot; a picket hull is the reverse. A higher-tier bridge brings a sharper crew: 6% tighter gunnery and better
  tracking per tier. The human bridge keeps the Magpie-class cutter.
- **Fitted parts are the actual pieces cut from their makers' models**, on the classic cutter and on alien hulls
  alike; a slot fitted with a human part keeps that hull's own system.
- **Name your ship** at the top of the Fitting bay. "Magpie" is now the class.
- **Network protocol 4:** host and friends need 0.13.0.

## 0.12.2 (2026-11-22): first sortie, part comparison, bug reports

- **First sortie (tutorial).** Play solo and press **First sortie** at the station (new captains are offered it in
  the Captain's notes). Eight steps against a lone Dustborn deserter near the ring: undock, find her, go quiet and close
  in, call a shot on her power, make her strike, strip her, take it home, refit. Each step finishes when you do it, the
  buttons it means light up, and it can be skipped, ended or replayed. No standing changes; ¢500 when you finish.
- **Part comparison in the Fitting bay.** Every part in stores shows its numbers next to the fitted part's (damage,
  reload, range, sensor quality, jump range, tear risk and so on, from the same formulas the ship flies with), marked
  better or worse, plus who made it, exactly what it takes to restore it, and what it is worth.
- **Report a problem** (in Orders and at the station): say what went wrong and press Send. The report carries the
  game's own flight recorder (errors, network events, frame times), the version, the multiplayer state and the
  graphics card, and the player can read all of it first. If the game hits an error it offers a report by itself.
  Reports go through a Formspree form, so the address they arrive at is never in the game. Until the form is set up,
  Send is replaced by Save as a file and Copy.
- **Polish:** version and network protocol shown in Orders, at the station and on the report; `Start here.html` works
  offline (fonts built in), has a Hosting section (Tailscale or playit.gg) and proper table headers;
  `THIRD-PARTY-NOTICES.txt` lists the licences for three.js, Electron and the fonts; the gunner now says "She has
  struck. Holding fire" instead of "No target with a track" over a beaten ship.

## 0.12.1 (2026-11-20): strike craft fixed

- **Your gunner now fights strike craft on its own.** Before, it only shot the ship you had selected, so a carrier's
  craft could pick the Magpie apart (in testing: dead in about 70 seconds, no craft hit). Now the maser pulses at any
  hostile craft in reach, whatever you have selected, while the railgun stays on your target. Same test: alive after
  three minutes with every craft shot down.
- **Craft masers are light weapons now:** a hit trips the system it strikes for one second, instead of five, and no
  longer shuts down the power buses behind it (which kept both your guns dark).
- **A fitted point-defence turret reaches craft where they circle** (about 23 km, at reduced odds), not just missiles.

## 0.12.0 (2026-11-19): clearer controls and easier joining

- **The key guide is rewritten** in the game (How it works), in the friends' `Read me.txt` and in `Start here.html`:
  grouped by flying, chasing, sensors, gunnery, salvage and view, with what each key actually does (what Silent,
  Active and Ping change, what each gunnery rule lets your gunner do, when a micro-jump works, that 1 is Stop and also
  breaks off a chase).
- **Test connection** on the Join screen checks the host before joining and says exactly what's wrong: wrong name,
  no answer (asleep, wrong network or firewall), PC answered but nobody hosting, can't reach that network, not a
  Valkyrie server, different versions, game full, or host not in the game yet. Join runs the same check.
- **The host's station screen** shows the server status (running, captains aboard, accepting players, version), each
  address with a **Copy address** button, and **Copy join details**: the address, version and steps, ready to paste
  into a message.
- Hosts now answer a small status page (`/valk-status`) so the test can see the version, the host and the head count.

## 0.11.1 (2026-11-19): Follow toggle

The Target window has a **Follow** button under the track bar. Press it (or P) and
the helm closes on your target and holds at gun range; it lights up and shows the distance it is holding. Press it
again (or P) to break off at your current speed. It works for friends in multiplayer too.

## 0.11.0 (2026-11-19): Blender models

- **Every ship has a Blender model.** All ten races' pickets, frigates, destroyers, carriers and strike craft, both
  capitals, Tarsis Ring, the Vashkar fleet base and its PDS guns: 55 models. Same designs as before, now with
  chamfered edges, smooth organic hulls, baked shading and each race's own skin (lit window runs, circuits, rust and
  hazard paint, coral, hide, crystal, filigree, red veins). Systems are still separate parts that scorch and blow off.
- **Where they show.** In `Valkyrie Host.exe`, the friends' `Valkyrie.exe`, the browser version through the server,
  and the web version. Opening `play\Valkyrie Space Prototype.html` straight from the file can't load them (browsers
  block that), so it shows the built-in models. Each model loads the first time that ship appears; ships switch over
  as it arrives.
- **The files.** `models` holds each race's `.glb` (what the game loads) and `.blend` (open in Blender to edit; the
  procedural materials are kept inside). Comparison sheets are in `docs\models`, and `docs\shipyard\Valkyrie
  Shipyard.html` has a switch between the Blender and original models. See `models\About these models.txt`.
- **The Magpie** (your ship) keeps its built-in model, because it is put together from the parts you fit.

## 0.10.0 (2026-11-19): the cockpit

- **Elite Dangerous layout, EVE Online glass.** Amber holographic text on smoked glass with cut corners. Amber is the
  interface, cyan is you and your allies, red is hostile, violet is damping fields. Pictures are in `docs\cockpit`.
- **Windows.** Contacts and Navigation (tabs) and Comms on the left; Systems on the right; a console of Target,
  Scanner and Ship along the bottom, with Orders beneath. Drag any window by its title bar, collapse it with –,
  and it stays where you put it next time. **Reset layout** (in Orders) puts everything back. Side windows lean in
  like Elite's panels. On small screens the windows lock into a compact layout.
- **Overview.** Every contact in one table, nearest first: stance mark, name, type, range and state (charging,
  spooling, field, wreck, ally). Click a row to target.
- **Scanner.** Elite's ellipse, ship-relative with ahead at the top. Stalks show height; filled marks are above you,
  hollow ones below. Wheel or −/+ changes the range; click a mark to target it.
- **Holograms.** The target is drawn in light, as seen from your ship, with each system coloured by its state and
  destroyed ones gone. Your own ship shows in cyan with its systems as coloured points.
- **Throttle, navigation, station.** A throttle bar beside the scanner; a Navigation tab listing every place in the
  system (flash points included); the station as Elite-style services down the left; the map, launcher and the
  friends' Start here page in the same colours. Allies in the view are small cyan marks, named only up close.

## 0.9.0 (2026-11-19): capital ships and flash points

- **Two capital ships, one per apex species.** The Seraphine Lattice cathedral and the Vorrakai dreadnought, each
  12 km long, with four gun batteries (the aft pair on the aft bus), missiles, heavy point defence, a hangar of strike
  craft and a damping field about 240 km across. Their systems are armoured to match, so they take minutes to bring down.
- **Flash points.** Four border sites (Kessan Gap, Ilkmere Verge, March Frontier, Veil Breach) where the war flares
  up, one at a time. Each side brings one or two capitals, never more, and every capital brings an escort group of a
  destroyer, two frigates and a picket from its side's races. The comms announce it; the map marks it.
- **Fleets fight each other.** Concord and Dominion ships target, shoot, launch missiles and craft, and shoot down
  each other's missiles. Ships finish off or chase down the broken, and the beaten side runs for it.
- **Your side.** A side that trusts you at least as much as the other (and isn't negative) treats you as an ally:
  its ships are tagged green and leave you alone. The other side shoots at you as well as its real enemy. Fire on an
  ally and that side turns on you. Standing with the winner rises if you were there and on their side.
- **Wreck fields.** The beaten fleet's wrecks stay for salvage until the victors move on; then the war moves to
  another flash point. With nobody present, battles are fought in the background, a round at a time.
- `tests/space-v9-*.js` cover the battles, the background war, multiplayer and the station notice.

## 0.8.0 (2026-11-18): the shipyard

- **Every race rebuilt, every class distinct.** Each of the ten races now builds its own picket, frigate, destroyer,
  carrier and strike craft, with the same look as before in more detail. Pickets carry a long sensor spar; destroyers
  a prow ram, belt armour and heavier guns; carriers a lit recovery bay. Pictures of every race are in `docs\shipyard`.
- **Systems you can see and break.** Every system you can target (bridge, sensors, guns, missiles, point defence,
  reactor, jump drive, drive, damper, hangar, buses) is a separate part of the model, built where the hit model puts
  it. Below 40% it goes scorched black; destroyed, it blows off the hull; stripped, it is gone.
- **Stations too.** Tarsis Ring, the Vashkar base at the Anchorage and its PDS guns were rebuilt the same way.
- **Salvaged parts match.** An alien part fitted to the Magpie is now the same part its makers bolt on their own ships.

## 0.7.0 (2026-11-18)

- **Chase a ship.** Left-click her and the helm closes to gun range and holds there. Press 4 to swing round under
  her stern at flank, V to keep after her while jinking across incoming slugs, 1 to break off. P chases your current target.
- **Salvage runs.** Left-click a wreck: the Magpie flies over, slows and strips her. Shift + right-click more wrecks to
  queue them; the run ends when the queue is empty or the hold is full.
- **Stars and planets are places.** In the jump plot, pick "Fly close to" a star or a planet (or click it on the system map).
  You arrive at a close pass of the star or in low orbit, and the body fills the sky. Gravity wells damp wormholes like a
  projector: about 0.28 at a star's corona and 0.19 in low orbit, so leaving carries tear risk. The Ring's tugs keep its corridor calm.
- **A Frankenstein ship.** Every alien part you fit is drawn on the Magpie in its makers' style: Krell flesh, Seraphine gold
  crystal, Vorrakai black blades, and so on.
- **Shipwright commissions and transmog.** At Trusted rank each power offers a commission (the Flesh-Wright in Kessan b's
  well for the Concord, the Coral Wright above Ilkmere a for the Dominion). Complete one and the fitting bay lets you restyle
  any slot in that power's looks, or human ones, as long as you have salvaged that look for that slot before. Looks only.

## 0.6.0 (2026-11-17)

The oldest friends zip still on the drive. Its notes were not kept.
