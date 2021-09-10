---
title: Vérification du périphérique de sortie
description: Vérification du périphérique de sortie
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- Commande MCI_ STATUs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1774eb3df2a45f98558862a15349007cd299d142
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368351"
---
# <a name="verifying-the-output-device"></a>Vérification du périphérique de sortie

Après avoir ouvert Sequencer, vous devez vérifier si le Mappeur MIDI est disponible et sélectionné comme périphérique de sortie. L’exemple suivant utilise la commande [**MCI \_ Status**](mci-status.md) pour vérifier que le Mappeur midi est le périphérique de sortie du séquenceur MCI.


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



 

 




