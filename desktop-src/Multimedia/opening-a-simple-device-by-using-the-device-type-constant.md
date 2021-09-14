---
title: Ouverture d’un appareil simple à l’aide de la constante Device-Type
description: Ouverture d’un appareil simple à l’aide de la constante Device-Type
ms.assetid: 6ed5fd4b-534a-4e03-8130-07f831403a8e
keywords:
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef65cf4546da2d7f7b6fdb5883232d0b1802f7b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416783"
---
# <a name="opening-a-simple-device-by-using-the-device-type-constant"></a>Ouverture d’un appareil simple à l’aide de la constante Device-Type

L’exemple suivant ouvre un périphérique CD audio en spécifiant une constante de type périphérique à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;

// Opens a CD audio device by specifying a device-type constant.

mciOpenParms.lpstrDeviceType = (LPCSTR) MCI_DEVTYPE_CD_AUDIO;

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_TYPE_ID, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 