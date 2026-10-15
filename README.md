# OFFRECORD-VR
VR Mod for OFFRECORD



OFFRECORD VR  -  VR mod for "OFFRECORD" (Unity 6000.0.70, URP, Mono x64)
=========================================================================

Version 0.1.2 (test build on Quest 3 VDXR).

CHANGES
* 0.1.2 - "Use" (B / E) works on what your RIGHT CONTROLLER points at (a short green beam shows when it points
        at something usable). [Input] InteractWith = Head for the old way (also in the VR menu).
        The game's own arms / hands are your VR hands ([Hands] HandModel = Game, now the default): the right
        hand (with forearm) is taken from the pistol's first-person arms in its grip pose, the left hand is
        its mirror image. Until you pick up the gun the built-in hands show. Hand only: [Hands]
        GameHandLength = Hand. Both are in the VR menu under "Controls / hands".
* 0.1.1 - VR settings menu: hold Y + left stick click for 1.7 s (right stick up/down = choose,
        left/right = change, A = toggle / select, B = close). Shows the frame rate at the top.
        Dizzy / doubled look when moving your head: the game's motion blur, depth of field, lens
        distortion, colour fringes and film grain are now switched off in the headset (menu: "Picture").
        Ambient occlusion can be switched off in the menu (faster).
        Keyboard keys asked for by name (GetKey("e")) now get the VR buttons too.
* 0.1.0 - First version.

WHAT IT DOES
------------
* Stereo VR through OpenXR (SteamVR, Meta/Oculus Link, Virtual Desktop, WMR...).
* 6DOF: your headset is the player's head. The player's body turns with your head, so walking,
  "use" (E) and the flashlight follow where you look. Left stick walks, right stick left/right snap-turns.
* The pistol sits in your right controller and shoots where it points. Hold the right grip for a laser.
* The ammo counter floats to the right of your right controller.
* The flashlight is in your left hand (shines where the left controller points).
* Cutscenes / death camera: you sit where the game's camera is.
* Menus, subtitles and the HUD are on a screen floating in front of you. In menus, point with the
  right controller and pull the right trigger to click.
* The game's full-screen "found footage" filter (CRT curve, VHS jitter, low resolution) is switched
  off in the headset - it is uncomfortable in VR. [Camera] GameScreenEffects = true brings it back.

INSTALL
-------
1. BepInEx 5 (5.4.23) is already in the game folder - you have it.
2. Copy the BepInEx folder from this zip into the game folder (merge / overwrite).
3. Start your VR runtime (SteamVR, Quest Link / Air Link, Virtual Desktop) first, then the game.

CONTROLS
--------
<img width="1024" height="683" alt="OFFRECORD" src="https://github.com/user-attachments/assets/81feab1d-a190-4196-a576-dd2e75c8c0c6" />


Right trigger (RT) ...... left mouse   (fire)

Left trigger (LT) ....... right mouse  (aim - tighter shots, the gun stays in your hand)

A ....................... Space (Next\Skip)

B ....................... E            (use / interact - point the right controller at it)

X ....................... Esc          (pause menu)

Y ....................... R            (reload)

Left grip ............... Left Shift   (sprint)

Left stick click (L3) ... Left Shift   (sprint)

Right stick click (R3) .. F            (flashlight - sent when you let go of the click)

Right stick up / down ... mouse wheel up / down (put away / take out the gun)

Right stick left / right  snap turn (smooth turn: [General] SnapTurn = false)

Right grip (hold) ....... laser sight

Left stick .............. walk

Both stick clicks together ............ recentre the view

Both stick clicks held 1.7 s (gun out) . move the gun in your hand: hold the left grip to grab it,
                                         B = back to default, A = save
                                         
Y + left stick click held 1.7 s ...... VR settings menu

Y + right stick click held 1.5 s ...... move / size your VR hands (right grip grabs the left hand,
                                         left grip the right hand, sticks up/down = size, A = save)
                                         

Crouch (Left Ctrl) has no button by default - give it one, e.g. [Bindings.Gameplay] OffTrigger = key:LeftControl
(that takes the aim off LT) or crouch for real.

SETTINGS
--------
BepInEx\config\offrecord.vr.cfg (made on the first start; saved changes apply while the game runs).
  [Bindings.Gameplay] / [Bindings.Menus]  every VR button: key:<KeyCode>, mouse:0/1/2, scroll:up/down,
                                          comma separated; :tap = only when let go quickly


