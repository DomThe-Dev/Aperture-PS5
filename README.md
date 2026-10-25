# Aperture-PS5
This is a bullet hell dungeon crawler developed using the Abertay in-house engine, made for the PS5 Dev Kit, with local coop support and procedural levels, with rebindable controls! It was a challenge, but much was learnt from the project, such as better time management, how to better divvy up tasks in a team, and generally getting used to ECS and the PS5 ecosystem.

A video showing most of the gameplay [is downloadable](_Dominykas_Jucys-ApertureScience_PS5_Game.mp4), as the rest of that video is the team discussing how the project went, though since embeds are not as easy on GitHub, GIFs have been provided.
![Game](media/gifs/Gameplay-Start.gif)

## My Contributions
- **2D to 3D** - I had to migrate us from Box2D to Jolt, which took a couple days of reading the documentation, experimenting, implementing it into our ENTT systems, and adding helper functions as well as an entire wiki page to make using the physics as easy as possible for my teammates.
<img width="1241" height="875" alt="image" src="https://github.com/user-attachments/assets/e0d3928b-1a7f-49da-8241-e03f5dc64620" />

- **ENTT (ECS) Support** - Having had experience with ENTT, I had to outline to my teammates how to best make use of the ECS system, to not compromise on performance.
- **Optimizations** - The game had plenty of places where performance could be improved, though due to the small scale, it was usually better not to mess with the it. I did reowrk the intent component and system to make it **~600%** more efficient, making use of every bit in a byte to dictate what that entity wants to do, rather than a lot of bools, so that more of these components could fit into the CPU cache at once. It was something similar to this:
```
enum CharacterFlag : uint8_t
{
	Interact = 1 << 0, // First bit, not shifted
	Attack = 1 << 1, // Second bit, because 1 was shifted by 1
	Run = 1 << 2, // Third bit, because 1 was shifted by 2
	Dodge = 1 << 3 // Fourth bit because 1 was shifted by 3
};
```
With getters, setters, etc, to properly make use of the component. It was reusable for the player and the enemy AI.

![Game](media/gifs/Shooting-Enemy.gif)
- **Team Debugger** - Most of my time, especially near the end, was fixing the bugs of other people, explaining why certain parts of code weren't working, and fixing merge conflicts, especially within the last 3 hours, where I had to merge everyone's work together, fix any issues, and then finally implement my final features to the project. 
- **Project Planning** - I would host weekly meetups, to make sure we all know what to do, and when, as well as to catch everyone up on work, and explain any C++ or ENTT specific problems.

![Game](media/gifs/Smooth-Menu.gif)

There are other contributions too, however, this repository is still being developed for my portfolio, so if there are questions or anything, contact me, my information is [on my portfolio](https://domthe-dev.github.io/devportfolio/).

## Where is the game?
At the current moment, I am unsure how much I am able to release, due to the NDA put on the PS5 Dev Kit, and how much of the in-house engine can be shown around. For the time being, I have the video we had to make displaying the gameplay.
Please contact me for more information.
