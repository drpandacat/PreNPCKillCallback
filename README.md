Uses
- Called before an NPC is killed by damage
- Passes info on the damage that would kill an entity, including the damage source
- Return true to prevent kill, false to prevent incoming damage that would kill. Useful for custom enemy death sequences, provides`frozen` argument passed to dictate whether or not enemy death effects should take place.

Why this over a simple damage amount and `HitPoints` check?
- `HitPoints` is only updated the frame after damage is taken, meaning that this check will fail if the sum of multiple instances of damage taken in a single frame is greather than or equal to the entity's `HitPoints` while none of the parts alone are. Commonly seen with multishot items.

Parameters:
- npc `EntityNPC`
- source `EntityRef`
- frozen `boolean`
- amt `number`
- flags `DamageFlag`
- cooldown `integer`

Optional argument `EntityType`

```lua
mod:AddCallback(PRE_NPC_KILL.ID, function (_, npc, source, frozen, amt, flags, cooldown)
    print("Hi")
end)
```
