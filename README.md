# VR-movement
🧱 1. Create your player object
In Unity: Hierarchy → Right click → 3D Object → Capsule
Rename it to Player
⚙️ 2. Add required components

Click your Player, then in the Inspector:

✅ Add CharacterController
✅ Add the PlayerMovement script (drag it on)
🧩 3. Set up Ground Check (important)

This script needs a point to check if you're on the ground.

Right-click Player → Create Empty
Rename it to GroundCheck
Move it slightly down (like at the player’s feet, e.g. Y = -0.9)

Then:

Drag GroundCheck into the script’s groundCheck slot
🌍 4. Set up the ground layer

This is what tells the script what counts as “floor”

Click your floor object
At the top → Layer dropdown → Add Layer
Create a new layer called Ground
Assign your floor to that layer

Now go back to Player:

In the script → set groundMask to Ground
🎮 5. Controls (what to press)
W / A / S / D → Move
Space → Jump
▶️ 6. Hit Play

You should now be able to:

Walk around
Jump
Fall with gravity
⚠️ Common problems (quick fixes)

❌ Can’t move

Make sure the script is attached
Check there’s a CharacterController

❌ Jump doesn’t work

GroundCheck might be too high → move it lower
Ground layer not set correctly

❌ Falling through floor

Floor needs a Collider (like BoxCollider)
