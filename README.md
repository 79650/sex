
<p align="center">
  <img src="https://cdn3.emoji.gg/emojis/602959-boobs.gif" alt="arobsite" height="200">
</p>

<div align="center">
<h1>
Fast-Flags Guide
</h1>
</div>

# What are Fast-Flags?

**FastFlags (often shortened as FFlags) are internal toggleable options that control whether certain parts of Roblox’s source code should be executed or not.**

**In Roblox, the Engine Settings make use of this FastFlag system. It allows Roblox engineers to dynamically modify the game engine without releasing a full update, typically for [A/B testing](https://en.wikipedia.org/wiki/A/B_testing) or controlled feature rollouts. All FastFlags and their behaviors are defined by Roblox engineers, and a large list of them is loaded online when the client starts up.**

**Realistically, FastFlags are only intended for Roblox engineers during local testing. That said, they can sometimes offer useful functionality for example, exposing advanced graphics options where Roblox’s defaults fall short.**
> [!CAUTION]
> **Using FastFlags should be treated as operating in a kind of “superuser mode.” Superusers have the ability to break things: if you enable the wrong flag, you might cause Roblox Studio or the client to malfunction. In such cases, it wouldn’t usually count as a valid bug report unless you are certain that it’s connected to an upcoming feature and Roblox is unaware of the issue.**

# Will using this get me banned?
**Short answer: No, it won’t. We are 100% sure of it, and even [Roblox Staff have confirmed that fact.](https://devforum.roblox.com/t/welcoming-byfron-to-roblox/2018233/693?u=xtremeguy2256 ) Bootstrappers are not exploit software and have nothing to do with exploiting.**
> **But if you are still using abusive FFlags (such as Noclip, JumpBoost, or Visual Glitches), people can detect this and report you, which may result in a ban.**

# What sites/bot are available for finding Fast-Flags?</h2>
**[FVariables](https://raw.githubusercontent.com/MaximumADHD/Roblox-Client-Tracker/roblox/FVariables.txt) ~ A sorted list of fast variables, which are used by Roblox to toggle changes to the engine remotely on multiple platforms without having to redeploy the client**

**[Flemish FastFlags](https://discord.gg/UHfwyxjeya) ~ This bot brings together all the features in one place. Instead of using separate tools like FVariables, you can access and use every FastFlag-related function through simple commands**

---
<h2>Roblox Client Debug Menu Keybinds</h2>

| **Action**             | **Windows**              | **Mac**                   | **Mobile**                                    |
|------------------------|--------------------------|---------------------------|-----------------------------------------------|
| *Game stats*           | `Shift + F1`             | `Fn + Shift + F1`         | None                                          |
| *Graphics stats*       | `Shift + F2`             | `Fn + Shift + F2`         | None                                          |
| *Network stats*        | `Shift + F3`             | `Fn + Shift + F3`         | None                                          |
| *Network diagnostics*  | `Ctrl + Shift + F3`      | `⌘ + Fn + Shift + F3`     | Double-tap *"Joining game"* while loading    |
| *Network debugging*    | `Shift + F3`, then `Shift + 1` | `Fn + Shift + F3`, then `Shift + 1` | None |
| *Physics stats*        | `Shift + F4`             | `Fn + Shift + F4`         | None                                          |
| *Summary stats*        | `Shift + F5`             | `Fn + Shift + F5`         | None                                          |

<details>
<summary><h2> FastFlags Documentation</h2></summary>

<h2>1. What are Fast-Flags?</h2>

**FastFlags (often shortened as FFlags) are internal toggleable options that control whether certain parts of Roblox’s source code should be executed or not.**
**In Roblox, the Engine Settings make use of this FastFlag system. It allows Roblox engineers to dynamically modify the game engine without releasing a full update, typically for [A/B testing](https://en.wikipedia.org/wiki/A/B_testing) or controlled feature rollouts. All FastFlags and their behaviors are defined by Roblox engineers, and a large list of them is loaded online when the client starts up.**
> **Using FastFlags should be treated as operating in a kind of “superuser mode.” Superusers have the ability to break things: if you enable the wrong flag, you might cause Roblox Studio or the client to malfunction. In such cases, it wouldn’t usually count as a valid bug report unless you are certain that it’s connected to an upcoming feature and Roblox is unaware of the issue.**

<h2>2. Will using this get me banned?</h2>

**Short answer: No, it won’t. We are 100% sure of it, and even [Roblox Staff have confirmed that fact.](https://devforum.roblox.com/t/welcoming-byfron-to-roblox/2018233/693?u=xtremeguy2256 ) Bootstrappers are not exploit software and have nothing to do with exploiting.**
> **But if you are still using abusive FFlags (such as Noclip, JumpBoost, or Visual Glitches), people can detect this and report you, which may result in a ban.**

<h2>3. What sites/bot are available for finding Fast-Flags?</h2>

**[FVariables](https://raw.githubusercontent.com/MaximumADHD/Roblox-Client-Tracker/roblox/FVariables.txt) ~ A sorted list of fast variables, which are used by Roblox to toggle changes to the engine remotely on multiple platforms without having to redeploy the client**

**[Flemish FastFlags](https://discord.gg/UHfwyxjeya) ~ This bot brings together all the features in one place. Instead of using separate tools like FVariables, you can access and use every FastFlag-related function through simple commands**

<details>
<summary><h2>Fast-Flags Tips-Explanations</h2></summary>

> 1. Roblox is mainly a CPU based game.
> 2. You can find fastflags in the Roblox Dev Console Memory.
> 3. FLogDebugShowFlagState is 90% correct; it only turns 100% correct when you join a game.
> 4. Having overlays can actually harm FPS, so yes. `FFlagDebugDisplayFPS` can actually reduce FPS.
> 5. Disabling **all** `telemetry`, will not do anything in terms of performance. It will also cause visual and other bugs.
---
