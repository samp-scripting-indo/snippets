# snippets
List snippet yang dibuat oleh member [SAMP-INDO] Lean Scripting/Mapping

## List Snippet

### IsValidRoleplay(playerid) - [Live Script](https://fiddle.sa-mp.dev/FoldableCivilisatoryAfricanpiedkingfisher)

Script dari: Bintang
```
#define isupper(%0) (%0 >= 65 && %0 <= 90)

IsRoleplayName(playerid) {
    new 
        playerName[MAX_PLAYER_NAME + 1],
        count = 0,
        found = -1;
    
   GetPlayerName(playerid, playerName, sizeof(playerName));

    for (new i; i < strlen(playerName); i ++) {
        if (isupper(playerName[i])) count++;
    }

    if ((found = strfind(playerName, "_", true, 2)) == -1) return 0;
    if (!isupper(playerName[0])) return 0;
    if (!isupper(playerName[found + 1])) return 0;
    if (count > 2) return 0;

    return 1;
}
```
