---
title: Ouverture d’un périphérique simple en utilisant le nom de l’appareil
description: Ouverture d’un périphérique simple en utilisant le nom de l’appareil
ms.assetid: 9e116499-2094-40e1-b2bc-3e3b8281a472
keywords:
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d186451717a056188d6fc990188c7e73fcf34cf1339b0787f7cec6e7573557
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802325"
---
# <a name="opening-a-simple-device-by-using-the-device-name"></a>Ouverture d’un périphérique simple en utilisant le nom de l’appareil

L’exemple suivant ouvre un périphérique CD audio en spécifiant le nom de l’appareil à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a CD audio device by specifying the device name.

mciOpenParms.lpstrDeviceType = "cdaudio";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN, MCI_OPEN_TYPE,
    (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 