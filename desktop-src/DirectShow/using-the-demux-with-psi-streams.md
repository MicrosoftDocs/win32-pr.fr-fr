---
description: Utilisation de demux avec des flux PSI
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Utilisation de demux avec des flux PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528210"
---
# <a name="using-the-demux-with-psi-streams"></a><span data-ttu-id="ea7e0-103">Utilisation de demux avec des flux PSI</span><span class="sxs-lookup"><span data-stu-id="ea7e0-103">Using the Demux with PSI Streams</span></span>

<span data-ttu-id="ea7e0-104">Pour récupérer les informations PSI à partir d’un flux de transport MPEG-2 à l’aide du filtre demux MPEG-2, créez une broche de sortie sur le demux avec le type de média suivant :</span><span class="sxs-lookup"><span data-stu-id="ea7e0-104">To get PSI information from an MPEG-2 transport stream using the MPEG-2 demux filter, create an output pin on the demux with the following media type:</span></span>

-   <span data-ttu-id="ea7e0-105">Type majeur : KSDATAFORMAT, \_ type, \_ \_ sections MPEG2</span><span class="sxs-lookup"><span data-stu-id="ea7e0-105">Major type: KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>
-   <span data-ttu-id="ea7e0-106">Sous-type : MEDIASUBTYPE \_ None</span><span class="sxs-lookup"><span data-stu-id="ea7e0-106">Subtype: MEDIASUBTYPE\_None</span></span>
-   <span data-ttu-id="ea7e0-107">Type de format : GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="ea7e0-107">Format type: GUID\_NULL</span></span>

<span data-ttu-id="ea7e0-108">Appelez ensuite la méthode [**IMPEG2PIDMap :: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) de la broche de sortie avec le PID souhaité et l’indicateur Media \_ MPEG2 \_ psi.</span><span class="sxs-lookup"><span data-stu-id="ea7e0-108">Then call the output pin's [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) method with the desired PID and the flag MEDIA\_MPEG2\_PSI.</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



<span data-ttu-id="ea7e0-109">Chaque section PSI complète est fournie dans un seul échantillon de support.</span><span class="sxs-lookup"><span data-stu-id="ea7e0-109">Each complete PSI section is delivered in one media sample.</span></span> <span data-ttu-id="ea7e0-110">Pour récupérer le numéro PID associé à une section de table, appelez [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) sur l’exemple de support.</span><span class="sxs-lookup"><span data-stu-id="ea7e0-110">To retrieve the PID number associated with a table section, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the media sample.</span></span> <span data-ttu-id="ea7e0-111">Le PID est fourni dans les 13 bits de poids faible de l’indicateur **dwTypeSpecificFlags** dans la structure des **\_ \_ Propriétés am SAMPLE2** .</span><span class="sxs-lookup"><span data-stu-id="ea7e0-111">The PID is given in the low 13 bits of the **dwTypeSpecificFlags** flag in the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="ea7e0-112">Cela est utile si vous mappez plusieurs PID PSI à la même broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="ea7e0-112">This is useful if you map multiple PSI PIDs to the same output pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea7e0-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea7e0-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea7e0-114">Utilisation du démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ea7e0-114">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



