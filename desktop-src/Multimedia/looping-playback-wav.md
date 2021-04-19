---
title: Lecture en boucle (Wave audio)
description: Lecture en boucle (Wave audio)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio Wave, sons en boucle
- Waveform-interface audio, bouclage des sons
- audio Wave, lecture en boucle
- Waveform-interface audio, lecture en boucle
- bouclage des sons Wave Audio
- bouclage-lecture audio
- waveOutWrite fonction)
- waveOutBreakLoop fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106531162"
---
# <a name="looping-playback"></a><span data-ttu-id="67f3b-111">Lecture en boucle</span><span class="sxs-lookup"><span data-stu-id="67f3b-111">Looping Playback</span></span>

<span data-ttu-id="67f3b-112">Le bouclage d’un son est contrôlé par les membres **dwLoops** et **dwFlags** dans les structures [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) passées à l’appareil avec la fonction [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="67f3b-112">Looping a sound is controlled by the **dwLoops** and **dwFlags** members in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structures passed to the device with the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> <span data-ttu-id="67f3b-113">Utilisez les indicateurs **WHDR \_ BEGINLOOP** et **WHDR \_ ENDLOOP** dans le membre **dwFlags** pour spécifier les blocs de données de début et de fin pour la boucle.</span><span class="sxs-lookup"><span data-stu-id="67f3b-113">Use the **WHDR\_BEGINLOOP** and **WHDR\_ENDLOOP** flags in the **dwFlags** member to specify the beginning and ending data blocks for looping.</span></span>

<span data-ttu-id="67f3b-114">Pour effectuer une boucle sur un bloc de données unique, spécifiez les deux indicateurs pour le même bloc.</span><span class="sxs-lookup"><span data-stu-id="67f3b-114">To loop a single data block, specify both flags for the same block.</span></span> <span data-ttu-id="67f3b-115">Pour spécifier le nombre de boucles, utilisez le membre **dwLoops** dans la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pour le premier bloc de la boucle.</span><span class="sxs-lookup"><span data-stu-id="67f3b-115">To specify the number of loops, use the **dwLoops** member in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure for the first block in the loop.</span></span>

<span data-ttu-id="67f3b-116">Vous pouvez appeler la fonction [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) pour arrêter un son en boucle.</span><span class="sxs-lookup"><span data-stu-id="67f3b-116">You can call the [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) function to stop a looping sound.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67f3b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67f3b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67f3b-118">Jeux de fichiers Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="67f3b-118">Playing Waveform-Audio Files</span></span>](playing-waveform-audio-files.md)
</dt> </dl>

 

 
