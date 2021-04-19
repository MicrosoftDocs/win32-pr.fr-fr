---
description: Capture d’audio TV
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Capture d’audio TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138ce631aedf12ddfb52be92d08ffb47da0cbdec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514503"
---
# <a name="capturing-tv-audio"></a><span data-ttu-id="9a030-103">Capture d’audio TV</span><span class="sxs-lookup"><span data-stu-id="9a030-103">Capturing TV Audio</span></span>

<span data-ttu-id="9a030-104">Pour capturer l’audio d’un téléviseur analogique dans un fichier, utilisez le [filtre de capture audio](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="9a030-104">To capture audio from analog television to a file, use the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="9a030-105">Utilisez l’énumérateur de périphérique système pour créer le filtre de capture audio.</span><span class="sxs-lookup"><span data-stu-id="9a030-105">Use the System Device Enumerator to create the Audio Capture Filter.</span></span> <span data-ttu-id="9a030-106">Il peut y avoir plusieurs périphériques de capture audio sur le système de l’utilisateur ; l’utilisateur doit sélectionner l’appareil qui représente la carte son.</span><span class="sxs-lookup"><span data-stu-id="9a030-106">There may be several audio capture devices on the user's system; the user must select the device that represents the sound card.</span></span>

<span data-ttu-id="9a030-107">Connectez la broche de sortie de capture audio au filtre Mux :</span><span class="sxs-lookup"><span data-stu-id="9a030-107">Connect the audio capture output pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



<span data-ttu-id="9a030-108">Il n’est pas nécessaire que les broches d’entrée soient connectées à quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="9a030-108">The input pins do not have to be connected to anything.</span></span> <span data-ttu-id="9a030-109">Chaque broche d’entrée représente une entrée physique sur le périphérique de capture audio.</span><span class="sxs-lookup"><span data-stu-id="9a030-109">Each input pin represents a physical input on the audio capture device.</span></span> <span data-ttu-id="9a030-110">Utilisez l’interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) pour activer l’entrée qui reçoit le flux audio du tuner.</span><span class="sxs-lookup"><span data-stu-id="9a030-110">Use the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface to enable the input that receives the audio stream from the tuner.</span></span> <span data-ttu-id="9a030-111">Les broches d’entrée sont identifiées par leur nom, par exemple « ligne in » ou « CD audio ».</span><span class="sxs-lookup"><span data-stu-id="9a030-111">The input pins are identified by name, such as "Line In" or "CD Audio."</span></span> <span data-ttu-id="9a030-112">Malheureusement, les noms peuvent passer d’un appareil à l’autre.</span><span class="sxs-lookup"><span data-stu-id="9a030-112">Unfortunately, the names can change from one device to the next.</span></span> <span data-ttu-id="9a030-113">En outre, différentes cartes tuner TV utilisent des entrées différentes de la carte son.</span><span class="sxs-lookup"><span data-stu-id="9a030-113">Also, different TV tuner cards use different inputs to the sound card.</span></span> <span data-ttu-id="9a030-114">Par conséquent, il revient à l’utilisateur d’identifier l’entrée à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9a030-114">Therefore, it is up to the user to identify which input to use.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9a030-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a030-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a030-116">Télévision analogique audio</span><span class="sxs-lookup"><span data-stu-id="9a030-116">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="9a030-117">Capture audio</span><span class="sxs-lookup"><span data-stu-id="9a030-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



