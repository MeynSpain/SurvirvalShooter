# SurvirvalShooter

Developed with Unreal Engine 4  
  
Link to the task board: https://app.weeek.net/ws/291518/project/3/board/4 

# Branches
## Branch: Master
Init Project.
## Branch: Develop
Add:  
* First person view
* Third Person view
* Switching between views
* Helth Stats Component
    * Helth
    * Hunger
    * Thirst 
    * Stamina
* Level Stats Component
    * Level
    * Experiens
    * Experience for next level
* Speeding on "Left Shift"
* Crouch on "Left Ctrl", but no animation
* Simple event Any Damage
* Event Death (enable Ragdall)
## Branch: Feature/Inventory  
### Commits
SS-04 #comment Add Storage Component and Storage Item  
  
![img.png](Images/img.png)  
![img_2.png](Images/img_2.png)
![img_1.png](Images/img_1.png)  

SS-05 #comment Inventory  

![img_3.png](Images/img_3.png)  
![img_4.png](Images/img_4.png)  

## Branch: Feature/Weapon  
Add:  
1. Enum: `E_DamageType`  
Stores the types of damage:  
* Simple Damage
* Point Damage
* Radial Damage (fallof)
2. BluePrint: `BP_Weapon_Base`  
Added functinons:
    * Deal Damage  
    Depends on the type of damage  
    * Deal Radial Damage  
    Called in Deal Damage if DamageType = Radial Damage
    * @Override Equip Item
    * @Override Un Equip Item
    * Use Weapon
3. BluePrint: `BPC_EqipComponent` 
Functions:  
    * Equip Item
    * Un Equip Item
    * Is Slot Equipped
    * Equip Weapon
    * Attach Weapon
4. Library with Weapons Assets  
5. BluePrint: `BP_RangeWeapon` - it's child of `BP_Weapon_Base`
6. BluePrint: `W_Rifle` - it's child of `BP_RangeWeapon` 

In `BP_EquipableItem` logic was changed in functions:  
 * Equip Item
 * Un Equip Item
 * @Override Dropped to World
