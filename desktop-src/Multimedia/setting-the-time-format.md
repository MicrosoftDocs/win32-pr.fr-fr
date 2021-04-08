---
title: Définition du format d’heure
description: Définition du format d’heure
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842186"
---
# <a name="setting-the-time-format"></a>Définition du format d’heure

Utilisez le message de commande [**\_ Set MCI**](mci-set.md) avec la [**structure \_ Set \_ PARMS de MCI**](mci-set-parms.md) pour définir le format d’heure d’un appareil ouvert. Définissez le membre **dwTimeFormat** sur l’une des constantes suivantes.



| Constante                   | Format de l’heure                                          |
|----------------------------|------------------------------------------------------|
| \_octets au format MCI \_         | Octets (dans les fichiers de format PCM modulé en code Pulse \[ \] ) |
| FORMAT MCI en \_ \_ millisecondes  | Millisecondes                                         |
| FORMAT MCI ( \_ \_ MSF)           | Minute/seconde/image                                  |
| \_exemples de format MCI \_       | Exemples                                              |
| \_Format MCI \_ SMPTE \_ 24     | SMPTE, 24 Frame                                      |
| \_Format MCI \_ SMPTE \_ 25     | SMPTE, 25 frame                                      |
| FORMAT MCI, \_ \_ SMPTE \_ 30     | SMPTE, 30 Frame                                      |
| \_Format MCI \_ \_ 30DROP SMPTE | SMPTE, 30 images                                 |
| \_format MCI \_ TMSF          | Suivi/minute/seconde/image                            |
| MCI \_ Seq \_ format \_ SONGPTR  | Pointeur de chanson MIDI                                    |



 

L’exemple suivant définit le format d’heure sur millisecondes sur l’appareil spécifié par la variable wDeviceID à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 