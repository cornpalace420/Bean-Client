
# 🫘 Bean Client

## Browser Compatibility

The JavaScript runtime of EaglercraftX 1.8 is currently known to work on browsers as old as Chrome 38 on Windows XP, the game supports both WebGL 1.0 and WebGL 2.0 however features such as dynamic lighting and PBR shaders require WebGL 2.0. The game also supports mobile browsers that don't have a keyboard or mouse, the game will enter touch screen mode automatically when touch input is detected. The game also includes an embedded OGG codec (JOrbis) for loading audio files on iOS where the browsers don't support loading OGG files in an AudioContext.

## WebAssembly GC Support

EaglercraftX 1.8 also has an experimental WebAssembly GC (WASM-GC) runtime, almost all of the features supported on the JavaScript runtime are also supported on the WebAssembly GC runtime, however it is still incompatible with several major browsers (especially Safari) and will not run in Chrome unless you can access the `chrome://flags` menu or request an origin trial token from Google for your website. Its based on experimental technology and may still crash sometimes, mostly due to browser bugs. Hopefully in the coming months the required feature (JSPI, WebAssembly JavaScript Promise Integration) will become enabled by default on the Chrome browser. It performs significantly better than the JavaScript client, around 50% more FPS and TPS in some cases, and will hopefully replace it someday. Just make sure you enable VSync when you play it, otherwise the game will run "too fast" and choke the browser's event loop, causing input lag.

## Singleplayer

EaglercraftX 1.8 fully supports singleplayer mode through an integrated server. Worlds are saved to your browser's local storage and are available even if your device does not have an internet connection. You can also import and export worlds in EaglercraftX as EPK files to copy them between devices and send them to your friends.

You can also import and export your existing vanilla Minecraft 1.8 worlds into EaglercraftX using ZIP files if you want to try playing all your old 1.8 maps in a modern browser. Beware that the inventories of LAN world players are not saved when the world is converted to vanilla, and pets (dogs, cats, horses, etc) might sometimes forget their owners due to the UUID changes.

## LAN Worlds

If you would like to invite other players to join your singleplayer world and play the game together, use the "Invite" button in the pause menu. You can configure gamemode and cheats for the other players joining your world, you can also decide if you would like to hide your world from other people on your wifi network or advertise your world to them. If hidden is "off" then other people on your same wifi network will see your world listed on their game's "Multiplayer" screen with all of their servers.

Once you press "Start Shared World", EaglercraftX 1.8 will give you a "join code" (usually 5 letters) to share with your friends. On a different device, go the "Multiplayer" screen and press "Direct Connect" and press "Join Shared World", enter the join code given to you when you started the shared world and press "Join World". Given a few seconds, the client should successfully be able to join your shared world from any other device on the internet that also has unrestricted internet access. If it does not work, check the "Network Settings" screen and make sure you and your friends all have the same set of shared world relay URLs configured or your clients will not be able to find each other.

## PBR Shaders

EaglercraftX 1.8 includes a deferred physically-based renderer modeled after the GTA V rendering engine with many new improvements and a novel raytracing technique for fast realistic reflections. It can be enabled in the "Shaders" menu in the game's options screen. Shader packs in EaglercraftX are just a component of resource packs, so any custom shaders you install will be in the form of a resource pack. EaglercraftX also comes with a very well optimized built-in PBR shader pack and also a built-in PBR material texture pack to give all blocks and items in the game realistic lighting and materials that looks better than most vanilla Minecraft shader packs. The default shader and texture packs were created from scratch by lax1dude, shaders packs made for vanilla Minecraft will not work in EaglercraftX and no shaders in EaglercraftX were taken from vanilla Minecraft shader packs. The shaders are not available in WebGL 1.0 mode or if floating point HDR render targets are not fully supported.

## Voice Chat

EaglercraftX 1.8 includes an integrated voice-chat service that can be used in shared worlds and also on multiplayer servers when it is enabled by the server owner. This feature also uses WebRTC like shared worlds, so be careful that you don't leak your IP address accidentally by using it on a public server.

## Resource Packs

EaglercraftX 1.8 allows you to use any vanilla Minecraft 1.8 resource pack in your browser by importing it as a zip file, resource packs are saved to your browser's local storage and are saved between page refreshes. This can be used to add the original C418 soundtrack back into the game, download and import [this pack](https://bafybeiayojww5jfyzvlmtuk7l5ufkt7nlfto7mhwmzf2vs4bvsjd5ouiuq.ipfs.nftstorage.link/?filename=Music_For_Eaglercraft.zip) to add music back to Eaglercraft. A known bug with the debug desktop runtime is that sound files in resource packs do not play, this may be fixed in the future but is not a high priority issue.
