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
ms.openlocfilehash: 9d0933a82ca8da53c89e1cb8b7d32b40dc89ae0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031152"
---
# <a name="determining-nonstandard-format-support"></a><span data-ttu-id="713fc-107">Détermination de la prise en charge des formats non standard</span><span class="sxs-lookup"><span data-stu-id="713fc-107">Determining Nonstandard Format Support</span></span>

<span data-ttu-id="713fc-108">Pour déterminer si un appareil prend en charge un format particulier (standard ou non standard), vous pouvez appeler la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) avec \_ l' \_ indicateur de requête format Wave.</span><span class="sxs-lookup"><span data-stu-id="713fc-108">To see whether a device supports a particular format (standard or nonstandard), you can call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function with the WAVE\_FORMAT\_QUERY flag.</span></span> <span data-ttu-id="713fc-109">L’exemple suivant utilise cette technique pour déterminer si un périphérique Wave-audio prend en charge un format spécifié.</span><span class="sxs-lookup"><span data-stu-id="713fc-109">The following example uses this technique to determine whether a waveform-audio device supports a specified format.</span></span>


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



<span data-ttu-id="713fc-110">Cette technique pour déterminer la prise en charge des formats non standard s’applique également aux périphériques d’entrée Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="713fc-110">This technique for determining nonstandard format support also applies to waveform-audio input devices.</span></span> <span data-ttu-id="713fc-111">La seule différence est que la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) est utilisée à la place de [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) pour interroger la prise en charge du format.</span><span class="sxs-lookup"><span data-stu-id="713fc-111">The only difference is that the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function is used in place of [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) to query for format support.</span></span>

<span data-ttu-id="713fc-112">Pour déterminer si un format de données Waveform-Audio particulier est pris en charge par l’un des périphériques audio Wave dans un système, utilisez la technique illustrée dans l’exemple précédent, mais spécifiez la \_ constante du mappeur Wave pour le paramètre *uDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="713fc-112">To determine whether a particular waveform-audio data format is supported by any of the waveform-audio devices in a system, use the technique illustrated in the previous example, but specify the WAVE\_MAPPER constant for the *uDeviceID* parameter.</span></span>

 

 