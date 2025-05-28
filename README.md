# EXP 5 Ammo Collection and Bullet Spawn System in Unreal Engine


## NAME:RAMPRASATH
## REG NO:212223220086
## Aim
To implement a gameplay feature where the player collects ammo pickups in the game world. Upon collecting ammo, the player's ammo count increases, enabling more bullet spawns (shots).

## Procedure
1. Setup Player Character
Open your PlayerCharacter Blueprint.s
Add a new Integer variable named AmmoCount.
Set an initial default value (e.g., AmmoCount = 10).
Ensure you have a shooting mechanism in place that uses AmmoCount to determine if a bullet can be fired.
2. Create Ammo Pickup Blueprint
Go to the Content Browser → Right-click → Blueprint Class → Select Actor → Name it BP_AmmoPickup.
Add components:
Static Mesh: Representing the ammo (e.g., a bullet or crate).
Sphere Collision: To detect overlap with the player.
In the Event Graph of BP_AmmoPickup:
Use OnComponentBeginOverlap on the Sphere Collision.
Cast to PlayerCharacter.
Increase the player’s AmmoCount (e.g., AmmoCount += 5).
Optionally, play a pickup sound or effect.
Destroy the ammo pickup actor.
3. Update Shooting Logic (Optional)
In your player’s shooting logic:
Before spawning a bullet, check if AmmoCount > 0.
If true:
Spawn bullet.
Decrease AmmoCount by 1.
4. Place Ammo in the World
Drag instances of BP_AmmoPickup into your level from the Content Browser.
Adjust position, mesh, and pickup range as needed.
## Output

![image](https://github.com/user-attachments/assets/d17571e1-4aea-4f10-9f28-606411ec22d1)
![image](https://github.com/user-attachments/assets/2fac8c29-a64b-43f5-b178-59234e4c8c52)
![image](https://github.com/user-attachments/assets/d0046f12-4ac4-4b5c-a930-03a0eb1f3eca)

![image](https://github.com/user-attachments/assets/b31c3760-326d-4dd8-803d-e413f0488624)



## Result
The player starts with a limited number of bullets.
When the player overlaps with an ammo pickup:
The ammo is collected.
The player's AmmoCount increases.
The player can now fire additional bullets based on the updated ammo count.
