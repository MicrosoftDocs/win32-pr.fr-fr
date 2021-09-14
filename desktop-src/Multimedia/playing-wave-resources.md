---
title: Jeux de ressources WAVE
description: Jeux de ressources WAVE
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- sons Waveform, ressources WAVE de jeu
- audio auxiliaire, lecture des ressources WAVE
- Jeux de ressources WAVE
- PlaySound, fonction, jeux de ressources WAVE
- sndPlaySound fonction)
- Fonction PlaySound, comparée à la fonction sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119534"
---
# <a name="playing-wave-resources"></a>Jeux de ressources WAVE

Vous pouvez utiliser la fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) pour lire un son stocké en tant que ressource. Bien que cela soit également possible à l’aide de la fonction [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) , **sndPlaySound** requiert que vous trouviez, chargez, verrouillez, déverrouillez et libérez la ressource. **PlaySound** réalise tout cela avec une seule ligne de code.

## <a name="playsound-example"></a>Exemple PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Exemple sndPlaySound

L' \_ indicateur de mémoire SND indique que le paramètre *lpszSoundName* est un pointeur vers une image en mémoire du fichier wave. Pour inclure un fichier WAVE en tant que ressource dans une application, ajoutez l’entrée suivante au script de ressources de l’application (. RC).


```C++
soundName WAVE c:\sounds\bells.wav 
```



Le nom *soundName* est un espace réservé pour un nom que vous fournissez pour faire référence à cette ressource Wave. les ressources WAVE sont chargées et accessibles comme d’autres ressources de Windows définies par l’application. La fonction PlayResource de l’exemple suivant lit une ressource WAVE spécifiée.


```C++
BOOL PlayResource(LPSTR lpName) 
{ 
    BOOL bRtn; 
    LPSTR lpRes; 
    HANDLE hResInfo, hRes; 
 
    // Find the WAVE resource. 
 
    hResInfo = FindResource(hInst, lpName, "WAVE"); 
    if (hResInfo == NULL) 
        return FALSE; 
 
    // Load the WAVE resource. 
 
    hRes = LoadResource(hInst, hResInfo); 
    if (hRes == NULL) 
        return FALSE; 
 
    // Lock the WAVE resource and play it. 
 
    lpRes = LockResource(hRes); 
    if (lpRes != NULL) { 
        bRtn = sndPlaySound(lpRes, SND_MEMORY | SND_SYNC | 
            SND_NODEFAULT); 
        UnlockResource(hRes); 
    } 
    else 
        bRtn = 0; 
 
    // Free the WAVE resource and return success or failure. 
 
    FreeResource(hRes); 
    return bRtn; 
} 
```



Pour lire une ressource WAVE à l’aide de cette fonction, transmettez à la fonction un pointeur vers une chaîne contenant le nom de la ressource, comme indiqué dans l’exemple suivant.


```C++
PlayResource("soundName"); 
```



 

 