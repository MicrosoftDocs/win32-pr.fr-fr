---
description: Obtention du code temporel de l’appareil
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Obtention du code temporel de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519177"
---
# <a name="getting-timecode-from-the-device"></a><span data-ttu-id="5f7c7-103">Obtention du code temporel de l’appareil</span><span class="sxs-lookup"><span data-stu-id="5f7c7-103">Getting Timecode from the Device</span></span>

<span data-ttu-id="5f7c7-104">Pendant la durée de la diffusion d’une bande DV ou en mode pause-enregistrement, vous pouvez récupérer le code temporel SMPTE ou le numéro de piste absolue.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-104">While a DV tape is playing or is in record-pause mode, you can retrieve the SMPTE timecode or the absolute track number.</span></span> <span data-ttu-id="5f7c7-105">Pour ce faire, appelez la méthode [**IAMTimecodeReader :: GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) .</span><span class="sxs-lookup"><span data-stu-id="5f7c7-105">To do this, call the [**IAMTimecodeReader::GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) method.</span></span> <span data-ttu-id="5f7c7-106">Cette méthode prend un pointeur vers une structure d' [**\_ exemple de code temporel**](/windows/win32/api/strmif/ns-strmif-timecode_sample) , qui décrit le code temporel.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-106">This method takes a pointer to a [**TIMECODE\_SAMPLE**](/windows/win32/api/strmif/ns-strmif-timecode_sample) structure, which describes the timecode.</span></span> <span data-ttu-id="5f7c7-107">Avant d’appeler la méthode, initialisez le membre **dwFlags** de la structure.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-107">Before calling the method, initialize the **dwFlags** member of the structure.</span></span> <span data-ttu-id="5f7c7-108">Utilisez la valeur ED \_ DEVCAP \_ code temporel \_ Read pour extraire le code temporel ou la valeur Ed \_ DEVCAP \_ ATN \_ Read pour récupérer le numéro de piste absolue.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-108">Use the value ED\_DEVCAP\_TIMECODE\_READ to retrieve the timecode or the value ED\_DEVCAP\_ATN\_READ to retrieve the absolute track number.</span></span>

<span data-ttu-id="5f7c7-109">Le membre du **code temporel** de la structure de l' **\_ exemple de code temporel** est une structure de code temporel.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-109">The **timecode** member of the **TIMECODE\_SAMPLE** structure is a TIMECODE structure.</span></span> <span data-ttu-id="5f7c7-110">Lorsque la méthode est retournée, le membre **dwFrames** de la structure du code temporel contient le code temporel ou le numéro de piste.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-110">When the method returns, the **dwFrames** member of the TIMECODE structure contains the timecode or track number.</span></span> <span data-ttu-id="5f7c7-111">Pour le code temporel, les heures, les minutes, les secondes et les trames sont compressés dans une valeur DWORD sous forme de valeurs décimales codées binaires (BCD), avec le format *hhmmssff*.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-111">For timecode, the hours, minutes, seconds, and frames are packed into a DWORD as binary coded decimal (BCD) values, with the format *hhmmssff*.</span></span> <span data-ttu-id="5f7c7-112">Utilisez des masques de retentes pour extraire les valeurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-112">Use bitmasks to extract the individual values.</span></span>

<span data-ttu-id="5f7c7-113">L’exemple suivant récupère le code temporel et le numéro de piste.</span><span class="sxs-lookup"><span data-stu-id="5f7c7-113">The following example retrieves the timecode and track number.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5f7c7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f7c7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f7c7-115">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="5f7c7-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
