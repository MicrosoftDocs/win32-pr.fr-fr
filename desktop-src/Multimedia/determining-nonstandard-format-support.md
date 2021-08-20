---
title: Détermination de la prise en charge des formats non standard
description: Détermination de la prise en charge des formats non standard
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- audio Wave, prise en charge des formats non standard
- audio auxiliaire, prise en charge du format non standard
- audio Wave, prise en charge du format standard
- audio auxiliaire, prise en charge du format standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a90d38f7419b6fbdb3de951c0aa2205ccd3dd9ff5366eb1e69eab945220db1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497279"
---
# <a name="determining-nonstandard-format-support"></a>Détermination de la prise en charge des formats non standard

Pour déterminer si un appareil prend en charge un format particulier (standard ou non standard), vous pouvez appeler la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) avec \_ l' \_ indicateur de requête format Wave. L’exemple suivant utilise cette technique pour déterminer si un périphérique Wave-audio prend en charge un format spécifié.


```C++
// Determines whether the specified waveform-audio output device 
// supports a specified waveform-audio format. Returns 
// MMSYSERR_NOERROR if the format is supported, WAVEERR_BADFORMAT if 
// the format is not supported, and one of the other MMSYSERR_ error 
// codes if there are other errors encountered in opening the 
// specified waveform-audio device. 
 
MMRESULT IsFormatSupported(LPWAVEFORMATEX pwfx, UINT uDeviceID) 
{ 
    return (waveOutOpen( 
        NULL,                 // ptr can be NULL for query 
        uDeviceID,            // the device identifier 
        pwfx,                 // defines requested format 
        NULL,                 // no callback 
        NULL,                 // no instance data 
        WAVE_FORMAT_QUERY));  // query only, do not open device 
} 
```



Cette technique pour déterminer la prise en charge des formats non standard s’applique également aux périphériques d’entrée Waveform-Audio. La seule différence est que la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) est utilisée à la place de [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) pour interroger la prise en charge du format.

Pour déterminer si un format de données Waveform-Audio particulier est pris en charge par l’un des périphériques audio Wave dans un système, utilisez la technique illustrée dans l’exemple précédent, mais spécifiez la \_ constante du mappeur Wave pour le paramètre *uDeviceID* .

 

 