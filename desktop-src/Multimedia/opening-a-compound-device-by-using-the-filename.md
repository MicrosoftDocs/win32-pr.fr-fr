---
title: Ouverture d’un appareil composé à l’aide du nom de fichier
description: Ouverture d’un appareil composé à l’aide du nom de fichier
ms.assetid: 5199bb68-44be-4fad-af5b-8fe89f27caee
keywords:
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20eb271658f77c5af4d35db96dd7bdbe6753af08
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368292"
---
# <a name="opening-a-compound-device-by-using-the-filename"></a>Ouverture d’un appareil composé à l’aide du nom de fichier

L’exemple suivant ouvre le périphérique Waveform-Audio en spécifiant un fichier Waveform-Audio nommé «TIMPANI. WAV» à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a waveform-audio device by specifying the device and 
// file name.

mciOpenParms.lpstrDeviceType = "waveaudio";
mciOpenParms.lpstrElementName = "timpani.wav";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_ELEMENT, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 