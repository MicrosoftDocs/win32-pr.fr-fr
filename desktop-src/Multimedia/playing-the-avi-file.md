---
title: Lit le fichier AVI
description: Lit le fichier AVI
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31754bd5f66b455abc76d363c5ff3e5e286e8040
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314700"
---
# <a name="playing-the-avi-file"></a><span data-ttu-id="2162d-104">Lit le fichier AVI</span><span class="sxs-lookup"><span data-stu-id="2162d-104">Playing the AVI File</span></span>

<span data-ttu-id="2162d-105">Avant d’utiliser la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour envoyer la commande de [**\_ lecture MCI**](mci-play.md) , votre application alloue la mémoire pour la structure, initialise les membres qu’elle utilisera et définit les indicateurs correspondant aux membres utilisés dans la structure.</span><span class="sxs-lookup"><span data-stu-id="2162d-105">Before using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_PLAY**](mci-play.md) command, your application allocates the memory for the structure, initializes the members it will use, and sets the flags corresponding to the members used in the structure.</span></span> <span data-ttu-id="2162d-106">(Si votre application ne définit pas d’indicateur pour un membre de structure, les pilotes MCI ignorent le membre.) Par exemple, l’exemple suivant lit un film à partir de la position de départ spécifiée par **dwFrom** à la position de fin spécifiée par **dwTo**.</span><span class="sxs-lookup"><span data-stu-id="2162d-106">(If your application does not set a flag for a structure member, MCI drivers ignore the member.) For example, the following example plays a movie from the starting position specified by **dwFrom** to the ending position specified by **dwTo**.</span></span> <span data-ttu-id="2162d-107">(Si l’une ou l’autre position est égale à zéro, l’exemple est écrit de sorte que la position n’est pas utilisée.)</span><span class="sxs-lookup"><span data-stu-id="2162d-107">(If either position is zero, the example is written so that the position is not used.)</span></span>


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



 

 