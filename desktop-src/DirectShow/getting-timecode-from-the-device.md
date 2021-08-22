---
description: Obtention du code temporel de l’appareil
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Obtention du code temporel de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265769300c0134ec9f3b3635ada3e595205e8452ced262d4062f9fb6cdaaadc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564729"
---
# <a name="getting-timecode-from-the-device"></a>Obtention du code temporel de l’appareil

Pendant la durée de la diffusion d’une bande DV ou en mode pause-enregistrement, vous pouvez récupérer le code temporel SMPTE ou le numéro de piste absolue. Pour ce faire, appelez la méthode [**IAMTimecodeReader :: GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) . Cette méthode prend un pointeur vers une structure d' [**\_ exemple de code temporel**](/windows/win32/api/strmif/ns-strmif-timecode_sample) , qui décrit le code temporel. Avant d’appeler la méthode, initialisez le membre **dwFlags** de la structure. Utilisez la valeur ED \_ DEVCAP \_ code temporel \_ Read pour extraire le code temporel ou la valeur Ed \_ DEVCAP \_ ATN \_ Read pour récupérer le numéro de piste absolue.

Le membre du **code temporel** de la structure de l' **\_ exemple de code temporel** est une structure de code temporel. Lorsque la méthode est retournée, le membre **dwFrames** de la structure du code temporel contient le code temporel ou le numéro de piste. Pour le code temporel, les heures, les minutes, les secondes et les trames sont compressés dans une valeur DWORD sous forme de valeurs décimales codées binaires (BCD), avec le format *hhmmssff*. Utilisez des masques de retentes pour extraire les valeurs individuelles.

L’exemple suivant récupère le code temporel et le numéro de piste.


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
