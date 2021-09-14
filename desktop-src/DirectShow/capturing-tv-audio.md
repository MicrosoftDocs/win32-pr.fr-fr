---
description: Capture d’audio TV
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Capture d’audio TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138ce631aedf12ddfb52be92d08ffb47da0cbdec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094865"
---
# <a name="capturing-tv-audio"></a>Capture d’audio TV

Pour capturer l’audio d’un téléviseur analogique dans un fichier, utilisez le [filtre de capture audio](audio-capture-filter.md). Utilisez l’énumérateur de périphérique système pour créer le filtre de capture audio. Il peut y avoir plusieurs périphériques de capture audio sur le système de l’utilisateur ; l’utilisateur doit sélectionner l’appareil qui représente la carte son.

Connecter la broche de sortie de capture audio au filtre mux :


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



Il n’est pas nécessaire que les broches d’entrée soient connectées à quoi que ce soit. Chaque broche d’entrée représente une entrée physique sur le périphérique de capture audio. Utilisez l’interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) pour activer l’entrée qui reçoit le flux audio du tuner. Les broches d’entrée sont identifiées par leur nom, par exemple « ligne in » ou « CD audio ». Malheureusement, les noms peuvent passer d’un appareil à l’autre. En outre, différentes cartes tuner TV utilisent des entrées différentes de la carte son. Par conséquent, il revient à l’utilisateur d’identifier l’entrée à utiliser.


```C++
IEnumPins *pEnum = NULL;
hr = pAudioCap->EnumPins(&pEnum);
if (SUCCEEDED(hr))
{
    IPin *pPin = NULL;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        IAMAudioInputMixer *pMix;
        hr = pPin->QueryInterface(IID_IAMAudioInputMixer, (void**)&pMix);
        if (SUCCEEDED(hr))
        {
            // Use IPin::QueryPinInfo to get the pin name.
            pPin->Release();
            if (...) // If the user selects this pin:
            {
                pMix->put_Enable(TRUE);
                pMix->put_MixLevel(1.0);
                pMix->Release();
                break;
            }
            pMix->Release();
        }
    }
}
pEnum->Release();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Télévision analogique audio](analog-television-audio.md)
</dt> <dt>

[Capture audio](audio-capture.md)
</dt> </dl>

 

 



