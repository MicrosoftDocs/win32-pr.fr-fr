---
title: Vérification du périphérique de sortie
description: Vérification du périphérique de sortie
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- Commande MCI_ STATUs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1774eb3df2a45f98558862a15349007cd299d142
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940080"
---
# <a name="verifying-the-output-device"></a><span data-ttu-id="3ae63-104">Vérification du périphérique de sortie</span><span class="sxs-lookup"><span data-stu-id="3ae63-104">Verifying the Output Device</span></span>

<span data-ttu-id="3ae63-105">Après avoir ouvert Sequencer, vous devez vérifier si le Mappeur MIDI est disponible et sélectionné comme périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="3ae63-105">After opening the sequencer, you should check whether the MIDI mapper was available and selected as the output device.</span></span> <span data-ttu-id="3ae63-106">L’exemple suivant utilise la commande [**MCI \_ Status**](mci-status.md) pour vérifier que le Mappeur midi est le périphérique de sortie du séquenceur MCI.</span><span class="sxs-lookup"><span data-stu-id="3ae63-106">The following example uses the [**MCI\_ STATUS**](mci-status.md) command to verify that the MIDI mapper is the output device for the MCI sequencer.</span></span>


```C++
UINT wDeviceID;      // valid MCI sequencer ID
DWORD dwReturn;
MCI_STATUS_PARMS mciStatusParms;

// Make sure the opened device is the MIDI mapper.

mciStatusParms.dwItem = MCI_SEQ_STATUS_PORT;

if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM,
    (DWORD)(LPVOID) &mciStatusParms))
{
    
    // Error sending MCI_STATUS command. 
    
    return;
}
if (LOWORD(mciStatusParms.dwReturn) == MIDI_MAPPER)
{
    
    // The MIDI mapper is the output device. 
    
}
Else
{
    
    // The MIDI mapper is not the output device. 
    
} 
```



 

 




