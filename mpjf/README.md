# Minecraft Multiplayer Mob Jitter Fix

In beta versions of Minecraft, mobs would jitter around on servers because the client still applies velocity to them. This jitter is inconsistent as different mobs have varying amounts of gravity being applied to them. Every zip in this repository contains only one class file each. The only modification is this line of code that is inserted at the beginning of Entity.moveEntity: `if(this.worldObj.multiplayerWorld && this instanceof EntityLiving && !(this instanceof EntityPlayerSP)) return;`. It was that simple, Mojang!

## Installation
First, pick a zip for your respective version. Then drag the class file inside the zip into the version jar and delete META-INF if you haven't already. If you are using MultiMC or PrismLauncher, you can use "Add to Minecraft.jar". It's as simple as that!

## Before
https://github.com/BlueStaggo/MCMPJitterFix/assets/71090710/3354e707-f49c-45f5-b51e-516ab40915ec

## After
https://github.com/BlueStaggo/MCMPJitterFix/assets/71090710/fb784805-ac97-4be9-a4a5-5ef86dea4baf
