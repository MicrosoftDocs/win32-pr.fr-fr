---
title: Types de données d’entrée Waveform-Audio
description: Types de données d’entrée Waveform-Audio
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- audio Waveform, types de données d’entrée
- Waveform-interface audio, types de données d’entrée
- enregistrement de l’audio de forme d’onde, types de données d’entrée
- Handle HWAVEIN
- WAVEFORMATEX, structure
- WAVEHDR, structure
- WAVEINCAPS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031171"
---
# <a name="waveform-audio-input-data-types"></a><span data-ttu-id="c3f2b-110">Types de données d’entrée Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="c3f2b-110">Waveform-Audio Input Data Types</span></span>

<span data-ttu-id="c3f2b-111">Les types de données suivants sont définis pour les fonctions d’entrée Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="c3f2b-111">The following data types are defined for waveform-audio input functions.</span></span>



| <span data-ttu-id="c3f2b-112">Type</span><span class="sxs-lookup"><span data-stu-id="c3f2b-112">Type</span></span>                                 | <span data-ttu-id="c3f2b-113">Description</span><span class="sxs-lookup"><span data-stu-id="c3f2b-113">Description</span></span>                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f2b-114">**HWAVEIN**</span><span class="sxs-lookup"><span data-stu-id="c3f2b-114">**HWAVEIN**</span></span>                          | <span data-ttu-id="c3f2b-115">Handle d’un périphérique d’entrée Waveform-Audio ouvert.</span><span class="sxs-lookup"><span data-stu-id="c3f2b-115">Handle of an open waveform-audio input device.</span></span>                                                                                                                  |
| [<span data-ttu-id="c3f2b-116">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="c3f2b-116">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | <span data-ttu-id="c3f2b-117">Structure qui spécifie les formats de données pris en charge par un périphérique d’entrée Waveform-Audio particulier.</span><span class="sxs-lookup"><span data-stu-id="c3f2b-117">Structure that specifies the data formats supported by a particular waveform-audio input device.</span></span> <span data-ttu-id="c3f2b-118">Cette structure est également utilisée pour les périphériques de sortie Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="c3f2b-118">This structure is also used for waveform-audio output devices.</span></span> |
| [<span data-ttu-id="c3f2b-119">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="c3f2b-119">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | <span data-ttu-id="c3f2b-120">Structure utilisée comme en-tête d’un bloc de données d’entrée Waveform Audio.</span><span class="sxs-lookup"><span data-stu-id="c3f2b-120">Structure used as a header for a block of waveform-audio input data.</span></span> <span data-ttu-id="c3f2b-121">Cette structure est également utilisée pour les périphériques de sortie Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="c3f2b-121">This structure is also used for waveform-audio output devices.</span></span>                             |
| [<span data-ttu-id="c3f2b-122">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="c3f2b-122">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | <span data-ttu-id="c3f2b-123">Structure utilisée pour se renseigner sur les fonctionnalités d’un périphérique d’entrée Waveform-Audio particulier.</span><span class="sxs-lookup"><span data-stu-id="c3f2b-123">Structure used to inquire about the capabilities of a particular waveform-audio input device.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="c3f2b-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3f2b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3f2b-125">Enregistrement de la forme d’onde</span><span class="sxs-lookup"><span data-stu-id="c3f2b-125">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 