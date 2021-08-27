---
title: Lit le fichier AVI
description: Lit le fichier AVI
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e0c490a61bbd53dd62a8223a3ded1aa047ce071d1d2544a2b26d1a9152450b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038014"
---
# <a name="playing-the-avi-file"></a>Lit le fichier AVI

Avant d’utiliser la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour envoyer la commande de [**\_ lecture MCI**](mci-play.md) , votre application alloue la mémoire pour la structure, initialise les membres qu’elle utilisera et définit les indicateurs correspondant aux membres utilisés dans la structure. (Si votre application ne définit pas d’indicateur pour un membre de structure, les pilotes MCI ignorent le membre.) Par exemple, l’exemple suivant lit un film à partir de la position de départ spécifiée par **dwFrom** à la position de fin spécifiée par **dwTo**. (Si l’une ou l’autre position est égale à zéro, l’exemple est écrit de sorte que la position n’est pas utilisée.)


```C++
DWORD PlayMovie(WORD wDevID, DWORD dwFrom, DWORD dwTo) 
{ 
    MCI_DGV_PLAY_PARMS mciPlay;    // play parameters 
    DWORD dwFlags = 0; 
 
    // Check dwFrom. If it is != 0 then set parameters and flags. 
    if (dwFrom){ 
        mciPlay.dwFrom = dwFrom; // set parameter 
        dwFlags |= MCI_FROM;     // set flag to validate member 
    } 
 
    // Check dwTo. If it is != 0 then set parameters and flags. 
    if (dwTo){ 
        mciPlay.dwTo = dwTo;    // set parameter 
        dwFlags |= MCI_TO;      // set flag to validate member 
    } 
 
    // Send the MCI_PLAY command and return the result. 
    return mciSendCommand(wDevID, MCI_PLAY, dwFlags, 
       (DWORD)(LPVOID)&mciPlay); 
} 
```



 

 