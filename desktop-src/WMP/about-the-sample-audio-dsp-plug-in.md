---
title: À propos de l’exemple de plug-in audio DSP
description: À propos de l’exemple de plug-in audio DSP
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Plug-ins du lecteur Windows Media, exemples
- plug-ins, exemples
- plug-ins de traitement de signal numérique, exemples
- Plug-ins DSP, exemples
- Plug-ins du lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, exemples audio
- Plug-ins DSP, exemples audio
- exemples, plug-ins DSP
- plug-ins DSP audio, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310097"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="10614-113">À propos de l’exemple de plug-in audio DSP</span><span class="sxs-lookup"><span data-stu-id="10614-113">About the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="10614-114">L’exemple de plug-in audio DSP fournit une implémentation de traitement simple qui met à l’échelle l’amplitude du son en fonction d’un facteur fourni par l’utilisateur dans la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="10614-114">The sample audio DSP plug-in provides a simple processing implementation that scales the amplitude of the audio by a factor provided by the user in the property page.</span></span> <span data-ttu-id="10614-115">Le plug-in accepte des valeurs comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="10614-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="10614-116">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="10614-116">The default value is 1.</span></span> <span data-ttu-id="10614-117">La valeur 1 n’a aucun effet sur le son ; d’autres facteurs de mise à l’échelle sont des multiplicateurs pour les échantillons audio.</span><span class="sxs-lookup"><span data-stu-id="10614-117">A value of 1 has no effect upon the sound; other scale factors are multipliers for the audio samples.</span></span> <span data-ttu-id="10614-118">Par exemple, une valeur de 0,5 entraînerait une baisse de 6 décibels du volume.</span><span class="sxs-lookup"><span data-stu-id="10614-118">For instance, a value of .5 would result in a 6 decibel decrease in volume.</span></span> <span data-ttu-id="10614-119">La valeur zéro produit un silence.</span><span class="sxs-lookup"><span data-stu-id="10614-119">A value of zero results in silence.</span></span>

<span data-ttu-id="10614-120">L’exemple de plug-in audio DSP fonctionne avec le son stéréo ou mono PCM.</span><span class="sxs-lookup"><span data-stu-id="10614-120">The sample audio DSP plug-in works with stereo or mono PCM audio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10614-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10614-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10614-122">**Génération d’un plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="10614-122">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




