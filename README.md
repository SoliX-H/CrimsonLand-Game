# CrimsonLand

A 2D zombie-survival game built with **C++** and **SFML**.

CrimsonLand brings together survival-focused gameplay, multiple game
modes, a menu-driven interface, score tracking, and a custom
asset-delivery pipeline. This release provides a ready-to-run Windows
build, with game resources packaged and encrypted for distribution.

            “THE MYTH SAYS THAT CRIMSONLAND IS CURSED, BUT IF YOU REACH THE END, YOU'LL READ THAT ITS MEN ARE VICTORIOUS.”

`CRIMSONLAND HAS WITHSTOOD CENTURIES OF DISASTERS AND WARS. MOST RECENTLY, AFTER A BRUTAL WAR WHERE IT TRIUMPHED AGAINST THE COLONIZERS, THE ENEMY RETALIATED THROUGH A HORRIFYING PLAN: A VIRAL EPIDEMIC. THIS OUTBREAK HAS DEVASTATED THE ISLAND, TURNING ITS PEOPLE INTO ZOMBIES.`

`YOU PLAY AS A WAR-TORN SOLDIER — A SURVIVOR OF THE FINAL BATTLE — NOW FORCED TO FLEE FROM ONE SAFE ZONE TO ANOTHER. ALONG YOUR JOURNEY, YOU'LL FACE ENDLESS DANGERS, ENCOUNTER ALLIES, AND PIECE TOGETHER THE ISLAND’S TRAGIC PAST. EVENTUALLY, YOU'LL REUNITE WITH FELLOW SURVIVORS TO CARRY OUT HIGH-RISK MISSIONS AND RECLAIM YOUR HOMELAND FROM THE ZOMBIE MENACE.`

              You Always Have Two Choices: Give up and Let CrimsonLand Fall... Or Survive and Preserve its Great Heritage.


## What's Built

-   **Two game modes**
    -   **Story Mode** --- progress through the game's story-driven
        experience.
    -   **Rush Mode** --- take on an arcade-style survival challenge.
-   **Game interface** --- menus and in-game screens for navigating the
    experience.
-   **Score tracking** --- records and loads high scores.
-   **Custom game assets** --- visual and audio resources used
    throughout the game.
-   **Integrated asset pipeline** --- game resources are collected and
    prepared into a distributable package, keeping the release organized
    and self-contained.

## Asset Packaging & Encryption

CrimsonLand uses a custom asset-packaging workflow instead of shipping
the game's resources as a loose collection of files.

-   Game assets are gathered from the game's asset directory and bundled
    into `assets.pak`.
-   The packaging workflow supports encryption of the packaged data
    using a key supplied to the packaging process.
-   The corresponding runtime asset-loading path reads from the package
    so the game can access its resources without requiring the original
    loose asset directory.
-   This keeps the distributed build compact and tidy, while making the
    original asset files less directly accessible to someone browsing
    the release folder.

The packaging and encryption are intended as an asset-protection and
distribution measure; they should not be considered a guarantee that
assets cannot be extracted by a determined reverse engineer.

## What's Included in This Release

The `CrimsonLand.zip` archive contains the Windows release build:

  File                Purpose
  ------------------- -------------------------------------------------------
  `CrimsonLand.exe`   Main game executable
  `assets.pak`        Packaged game assets used by the runtime asset loader
  `openal32.dll`      Audio runtime library required by the build

Keep these files together in the same directory. The game expects the
asset package and runtime library to remain alongside the executable.

## Running the Game

1.  Download `CrimsonLand.zip` from the GitHub Release.
2.  Extract the archive to a folder on your Windows PC.
3.  Open the extracted folder.
4.  Run `CrimsonLand.exe`.

**Important:** Do not move, rename, or remove `assets.pak` or
`openal32.dll`. The game may fail to start or load resources if either
file is missing.

## Build & Technology

-   **Language:** C++
-   **Graphics / multimedia framework:** SFML
-   **Build configuration:** 64-bit Release
-   **Build environment:** Microsoft Visual C++ / Visual Studio
-   **Asset delivery:** Custom asset packaging and encrypted resource
    workflow

## Release Notes

This is a packaged executable release intended for playing the game on
Windows. The archive contains the runtime files needed by this
distribution; it is not a source-code development package.

If you encounter an issue, please include: - Your Windows version. - The
steps that led to the issue. - Any error message displayed by the game.

------------------------------------------------------------------------

**CrimsonLand** --- survive, play, and see how long you can last.
