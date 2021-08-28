---
description: Utilisation de demux avec la Flux PSI
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Utilisation de demux avec la Flux PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3935e188b6e06d1037f08d4ca7bab98918f87d2c652b8506650a6cf3a280dc04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633139"
---
# <a name="using-the-demux-with-psi-streams"></a>Utilisation de demux avec la Flux PSI

Pour récupérer les informations PSI à partir d’un flux de transport MPEG-2 à l’aide du filtre demux MPEG-2, créez une broche de sortie sur le demux avec le type de média suivant :

-   Type majeur : KSDATAFORMAT, \_ type, \_ \_ sections MPEG2
-   Sous-type : MEDIASUBTYPE \_ None
-   Type de format : GUID \_ null

Appelez ensuite la méthode [**IMPEG2PIDMap :: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) de la broche de sortie avec le PID souhaité et l’indicateur Media \_ MPEG2 \_ psi.


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



Chaque section PSI complète est fournie dans un seul échantillon de support. Pour récupérer le numéro PID associé à une section de table, appelez [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) sur l’exemple de support. Le PID est fourni dans les 13 bits de poids faible de l’indicateur **dwTypeSpecificFlags** dans la structure des **\_ \_ Propriétés am SAMPLE2** . Cela est utile si vous mappez plusieurs PID PSI à la même broche de sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



