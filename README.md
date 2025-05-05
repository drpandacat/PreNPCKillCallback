basically its called before an entity is killed through dealt damage. useful as it gives all entity_tage_dmg arguments including the source of the damage, and you can also return true or false to cancel the damage or leave it at minimum hp. useful for custom entity death effects, or player-specific on kill effects

use it like any vanilla callback, callback id is PRE_NPC_KILL.ID
