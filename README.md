# Aperture-PS5
This is a bullet hell dungeon crawler developed using the Abertay in-house engine, made for the PS5 Dev Kit, with local coop support and procedural levels, with rebindable controls! It was a challenge, but much was learnt from the project, such as better time management, how to better divvy up tasks in a team, and generally getting used to ECS and the PS5 ecosystem.
[The gameplay part of the video is downloadable](_Dominykas_Jucys-ApertureScience_PS5_Game.mp4) as the rest of it is the team discussing their contributions, though since embeds are not as easy on GitHub, GIFs have been provided.
![Game](media/gifs/Gameplay-Start.gif)

## My Contributions
- **2D to 3D** - I singlehandedly ported over the game from Box2D to Jolt. After a couple of days, I understood how Jolt works, and had to implement some helper functions to make sure my teammates could make use of it properly, and without the hassle of having to delve into the documentation themselves.
- **ENTT (ECS) Support** - Having had experience with ENTT, I had to outline to my teammates how to best make use of the ECS system, to not compromise on performance.
- **Optimizations** - There were plenty of places to improve performance on, however, I managed to rework the intent component and system to make it 7x more efficient by utilising singular bits, so more components could fit into the cache of a CPU, and therefore increase performance.
- **Team Debugger** - On account of having been programming for a while, and having looked through almost every part of the in-house engine, my teammates constantly turned to me for questions, and to help debug their code, as well as fix their merge conflicts, which usually ate away at my time, stopping me from as much some days
- **Project Planning** - I would host weekly meetups, to make sure we all know what to do, and when, as well as to catch everyone up on work, and explain any C++ or ENTT specific problems.

## Where is the game?
At the current moment, I am unsure how much I am able to release, due to the NDA put on the PS5 Dev Kit, and how much of the in-house engine can be shown around. For the time being, I have the video we had to make displaying the gameplay.
Please contact me for more information.
