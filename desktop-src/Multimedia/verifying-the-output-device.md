---
title: Vérification du périphérique de sortie
description: Vérification du périphérique de sortie
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- Commande MCI_ STATUs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b02c014b374f83b3de5df90fd7de1952f65acd99b13f5075a59bc95d40e6380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781652"
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



 

 




