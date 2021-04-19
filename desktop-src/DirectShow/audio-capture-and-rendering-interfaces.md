---
description: Interfaces de capture audio et de rendu
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfaces de capture audio et de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514915"
---
# <a name="audio-capture-and-rendering-interfaces"></a><span data-ttu-id="9dcb5-103">Interfaces de capture audio et de rendu</span><span class="sxs-lookup"><span data-stu-id="9dcb5-103">Audio Capture and Rendering Interfaces</span></span>

<span data-ttu-id="9dcb5-104">Ces interfaces prennent en charge la capture et le rendu audio dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="9dcb5-104">These interfaces support audio capture and rendering in DirectShow</span></span>



| <span data-ttu-id="9dcb5-105">Interface</span><span class="sxs-lookup"><span data-stu-id="9dcb5-105">Interface</span></span>                                              | <span data-ttu-id="9dcb5-106">Description</span><span class="sxs-lookup"><span data-stu-id="9dcb5-106">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dcb5-107">**IAMAudioInputMixer**</span><span class="sxs-lookup"><span data-stu-id="9dcb5-107">**IAMAudioInputMixer**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | <span data-ttu-id="9dcb5-108">Accédez aux entrées analogiques de la carte son du système et ajustez les caractéristiques, telles que mono ou stéréo, le niveau de mélange, le niveau de panoramique, le bruit, les aigus et les basses.</span><span class="sxs-lookup"><span data-stu-id="9dcb5-108">Access the analog inputs on the system's sound card and adjust characteristics, such as mono or stereo, mix level, pan level, loudness, treble, and bass.</span></span> |
| [<span data-ttu-id="9dcb5-109">**IAMAudioRendererStats**</span><span class="sxs-lookup"><span data-stu-id="9dcb5-109">**IAMAudioRendererStats**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | <span data-ttu-id="9dcb5-110">Obtenir des informations statistiques sur les performances des renderering audio.</span><span class="sxs-lookup"><span data-stu-id="9dcb5-110">Get statistical performance information about audio renderering.</span></span>                                                                                          |
| [<span data-ttu-id="9dcb5-111">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="9dcb5-111">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | <span data-ttu-id="9dcb5-112">Contrôler la façon dont le filtre de capture audio alloue des tampons.</span><span class="sxs-lookup"><span data-stu-id="9dcb5-112">Control how the audio capture filter allocates buffers.</span></span>                                                                                                   |
| [<span data-ttu-id="9dcb5-113">**IAMClockSlave**</span><span class="sxs-lookup"><span data-stu-id="9dcb5-113">**IAMClockSlave**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | <span data-ttu-id="9dcb5-114">Contrôler la tolérance d’un convertisseur audio lorsqu’il correspond à des vitesses avec une autre horloge.</span><span class="sxs-lookup"><span data-stu-id="9dcb5-114">Control the tolerance of an audio renderer when it matches rates with another clock.</span></span>                                                                      |
| [<span data-ttu-id="9dcb5-115">**IAMDirectSound**</span><span class="sxs-lookup"><span data-stu-id="9dcb5-115">**IAMDirectSound**</span></span>](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | <span data-ttu-id="9dcb5-116">Permet à une application de spécifier la fenêtre qui a le focus pour contrôler la lecture audio DirectSound.</span><span class="sxs-lookup"><span data-stu-id="9dcb5-116">Enables an application to specify which window has focus for controlling DirectSound audio playback.</span></span>                                                      |
| [<span data-ttu-id="9dcb5-117">**IAMResourceControl**</span><span class="sxs-lookup"><span data-stu-id="9dcb5-117">**IAMResourceControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | <span data-ttu-id="9dcb5-118">Maintenez une ressource de périphérique audio avant qu’elle ne soit nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9dcb5-118">Hold an audio device resource before it is needed.</span></span>                                                                                                        |
| [<span data-ttu-id="9dcb5-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="9dcb5-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | <span data-ttu-id="9dcb5-120">Interrogez et définissez le format de sortie du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="9dcb5-120">Query and set the capture filter's output format.</span></span>                                                                                                         |
| [<span data-ttu-id="9dcb5-121">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="9dcb5-121">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | <span data-ttu-id="9dcb5-122">Définissez le volume et le solde de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="9dcb5-122">Set audio output volume and balance.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="9dcb5-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9dcb5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dcb5-124">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9dcb5-124">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



