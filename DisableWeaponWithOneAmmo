public OnPlayerWeaponShot(playerid, weaponid, hittype, hitid, Float:fX, Float:fY, Float:fZ)
{
    new weapon, ammo;

    #if defined _YSF_INCLUDED
        GetPlayerWeaponData(playerid, GetWeaponSlot(weaponid), weapon, ammo);
    #else
        for(new i = 0; i < 10; i++)
        {
            GetPlayerWeaponData(playerid, i, weapon, ammo);
            if(weapon == weaponid) break;
        }
    #endif
    if(ammo <= 1)
    {
        GivePlayerWeapon(playerid, weaponid, 1);
        SetPlayerArmedWeapon(playerid, 0);
        return 0;
    }

    #if defined HOOK_OnPlayerWeaponShot
        return HOOK_OnPlayerWeaponShot(playerid, weaponid, hittype, hitid, fX, fY, fZ);
    #else
        return 1;
    #endif
}

#if defined _ALS_OnPlayerWeaponShot
    #undef OnPlayerWeaponShot
#else
    #define _ALS_OnPlayerWeaponShot
#endif

#define OnPlayerWeaponShot HOOK_OnPlayerWeaponShot

#if defined HOOK_OnPlayerWeaponShot
    forward HOOK_OnPlayerWeaponShot(playerid, weaponid, hittype, hitid, Float:fX, Float:fY, Float:fZ); 
#endif
