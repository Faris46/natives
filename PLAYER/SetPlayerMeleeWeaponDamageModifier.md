---
ns: PLAYER
---
## SET_PLAYER_MELEE_WEAPON_DAMAGE_MODIFIER

```c
// 0x4A3DC7ECCC321032 0x362E69AD
void SET_PLAYER_MELEE_WEAPON_DAMAGE_MODIFIER(Player player, float modifier);
```

```
NativeDB Added Parameter 3: BOOL p2
```

## Parameters
* **player**: 
* **modifier**: 
local MeeleWeapons = {
    ["WEAPON_NIGHTSTICK"] = 0.1,
    ["WEAPON_BAT"] = 0.000001
}

Citizen.CreateThread(function()
    while true do
        Citizen.Wait(5)

		for weapon, modifier in pairs(MeeleWeapons) do
			if GetSelectedPedWeapon(PlayerPedId()) == GetHashKey(weapon) then
				SetPlayerMeleeWeaponDamageModifier(PlayerId(), v)
			end
		end
    end
end)
