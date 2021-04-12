---
title: Modèles de conformité des périphériques audio
description: Modèles de conformité des périphériques audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media Format SDK, modèles de conformité des appareils
- ASF (Advanced Systems Format), modèles de conformité des appareils
- ASF (format des systèmes avancés), modèles de conformité des appareils
- Windows Media Format SDK, modèles de conformité des périphériques audio
- ASF (Advanced Systems Format), modèles de conformité des périphériques audio
- ASF (format de systèmes avancés), modèles de conformité de périphérique audio
- Codec Windows Media Audio 9, modèles de conformité de périphérique audio
- codecs, codec Windows Media Audio 9
- modèles de conformité des appareils, vidéo
- modèles de conformité des périphériques audio
- modèles, modèles de conformité de périphérique audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309989"
---
# <a name="audio-device-conformance-templates"></a><span data-ttu-id="f7684-114">Modèles de conformité des périphériques audio</span><span class="sxs-lookup"><span data-stu-id="f7684-114">Audio Device Conformance Templates</span></span>

<span data-ttu-id="f7684-115">Le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le codec Windows Media Audio 9, ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f7684-115">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 codec, or later.</span></span>



| <span data-ttu-id="f7684-116">Chaîne de modèle</span><span class="sxs-lookup"><span data-stu-id="f7684-116">Template string</span></span> | <span data-ttu-id="f7684-117">Plage de vitesses de transmission</span><span class="sxs-lookup"><span data-stu-id="f7684-117">Bit rate range</span></span>     | <span data-ttu-id="f7684-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f7684-118">Notes</span></span>                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7684-119">Ko</span><span class="sxs-lookup"><span data-stu-id="f7684-119">"L1"</span></span>            | <span data-ttu-id="f7684-120">64 Kbits/s 160 kbps</span><span class="sxs-lookup"><span data-stu-id="f7684-120">64 Kbps   160 Kbps</span></span> | <span data-ttu-id="f7684-121">Ce modèle est destiné aux appareils audio uniquement limités.</span><span class="sxs-lookup"><span data-stu-id="f7684-121">This template is intended for constrained audio-only devices.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="f7684-122">NIV</span><span class="sxs-lookup"><span data-stu-id="f7684-122">"L2"</span></span>            | <span data-ttu-id="f7684-123"><= 160 Kbits/s</span><span class="sxs-lookup"><span data-stu-id="f7684-123"><= 160 Kbps</span></span>     | <span data-ttu-id="f7684-124">Ce modèle correspond à la classe 4 dans le kit de portage des Windows Media Audio, qui prend en charge l’intégralité de l’implémentation du décodeur Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="f7684-124">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.</span></span>                                                                                   |
| <span data-ttu-id="f7684-125">Mémoire</span><span class="sxs-lookup"><span data-stu-id="f7684-125">"L3"</span></span>            | <span data-ttu-id="f7684-126"><= 384 Kbits/s</span><span class="sxs-lookup"><span data-stu-id="f7684-126"><= 384 Kbps</span></span>     | <span data-ttu-id="f7684-127">Ce modèle correspond à la classe 4 dans le kit de portage des Windows Media Audio, qui prend en charge l’intégralité de l’implémentation du décodeur Windows Media Audio. La plage de vitesses de transmission est la seule différence entre ce modèle et le niveau 2.</span><span class="sxs-lookup"><span data-stu-id="f7684-127">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.The bit rate range is the only difference between this template and L2.</span></span><br/> |
| <span data-ttu-id="f7684-128">Budget</span><span class="sxs-lookup"><span data-stu-id="f7684-128">"L"</span></span>             | <span data-ttu-id="f7684-129">Toutes les vitesses de transmission</span><span class="sxs-lookup"><span data-stu-id="f7684-129">All bit rates</span></span>      | <span data-ttu-id="f7684-130">Ce modèle est destiné uniquement aux ordinateurs personnels, et est généralement utilisé pour présenter les fonctionnalités complètes du codec.</span><span class="sxs-lookup"><span data-stu-id="f7684-130">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.</span></span>                                                                                                           |



 

<span data-ttu-id="f7684-131">Le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le codec vocal Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="f7684-131">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Voice codec.</span></span>



| <span data-ttu-id="f7684-132">Chaîne de modèle</span><span class="sxs-lookup"><span data-stu-id="f7684-132">Template string</span></span> | <span data-ttu-id="f7684-133">Plage de vitesses de transmission</span><span class="sxs-lookup"><span data-stu-id="f7684-133">Bit rate range</span></span> | <span data-ttu-id="f7684-134">Notes</span><span class="sxs-lookup"><span data-stu-id="f7684-134">Notes</span></span>                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7684-135">V1</span><span class="sxs-lookup"><span data-stu-id="f7684-135">"S1"</span></span>            | <span data-ttu-id="f7684-136"><= 20 Kbits/s</span><span class="sxs-lookup"><span data-stu-id="f7684-136"><= 20 Kbps</span></span>  | <span data-ttu-id="f7684-137">Ce modèle est destiné uniquement aux appareils très peu complexes. Ce modèle est uniquement vocal.</span><span class="sxs-lookup"><span data-stu-id="f7684-137">This template is intended for very low-complexity devices only.This template is speech only.</span></span><br/>                    |
| <span data-ttu-id="f7684-138">S2</span><span class="sxs-lookup"><span data-stu-id="f7684-138">"S2"</span></span>            | <span data-ttu-id="f7684-139"><= 20 Kbits/s</span><span class="sxs-lookup"><span data-stu-id="f7684-139"><= 20 Kbps</span></span>  | <span data-ttu-id="f7684-140">Il s’agit du modèle recommandé pour la plupart des applications. Ce modèle prend en charge les combinaisons de voix et de musique.</span><span class="sxs-lookup"><span data-stu-id="f7684-140">This is the recommended template for most applications.This template supports combinations of speech and music.</span></span><br/> |



 

<span data-ttu-id="f7684-141">Le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le codec Windows Media Audio 9 Professional, ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f7684-141">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Professional codec, or later.</span></span>



| <span data-ttu-id="f7684-142">Chaîne de modèle</span><span class="sxs-lookup"><span data-stu-id="f7684-142">Template string</span></span> | <span data-ttu-id="f7684-143">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f7684-143">Properties</span></span>                                                                                   | <span data-ttu-id="f7684-144">Notes</span><span class="sxs-lookup"><span data-stu-id="f7684-144">Notes</span></span>                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7684-145">M1</span><span class="sxs-lookup"><span data-stu-id="f7684-145">"M1"</span></span>            | <span data-ttu-id="f7684-146">Vitesse de transmission <= 384 KbpsSampling <= 48 kHz</span><span class="sxs-lookup"><span data-stu-id="f7684-146">Bit rate <= 384 KbpsSampling rate <= 48 kHz</span></span><br/> <span data-ttu-id="f7684-147">Canaux <= 5,1</span><span class="sxs-lookup"><span data-stu-id="f7684-147">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="f7684-148">Ce modèle est recommandé pour les films standard avec un son surround.</span><span class="sxs-lookup"><span data-stu-id="f7684-148">This template is recommended for standard movies with surround sound.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="f7684-149">Carré</span><span class="sxs-lookup"><span data-stu-id="f7684-149">"M2"</span></span>            | <span data-ttu-id="f7684-150">Vitesse de transmission <= 768 KbpsSampling <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="f7684-150">Bit rate <= 768 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="f7684-151">Canaux <= 5,1</span><span class="sxs-lookup"><span data-stu-id="f7684-151">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="f7684-152">Ce modèle est recommandé pour les films haute définition avec un son surround.</span><span class="sxs-lookup"><span data-stu-id="f7684-152">This template is recommended for high-definition movies with surround sound.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="f7684-153">M3</span><span class="sxs-lookup"><span data-stu-id="f7684-153">"M3"</span></span>            | <span data-ttu-id="f7684-154">Vitesse de transmission <= 1 500 KbpsSampling <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="f7684-154">Bit rate <= 1,500 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="f7684-155">Canaux <= 7,1</span><span class="sxs-lookup"><span data-stu-id="f7684-155">Channels <= 7.1</span></span><br/> | <span data-ttu-id="f7684-156">Ce modèle est recommandé pour les films haute définition avec un son surround à 8 canaux, tel que le contenu encodé pour la présentation dans des théâtres.</span><span class="sxs-lookup"><span data-stu-id="f7684-156">This template is recommended for high-definition movies with 8-channel surround sound, such as content encoded for presentation in theaters.</span></span>                                                                                                    |
| <span data-ttu-id="f7684-157">"M"</span><span class="sxs-lookup"><span data-stu-id="f7684-157">"M"</span></span>             | <span data-ttu-id="f7684-158">Taux d’échantillonnage de tous les bits ratesAll</span><span class="sxs-lookup"><span data-stu-id="f7684-158">All bit ratesAll sampling rates</span></span><br/> <span data-ttu-id="f7684-159">Tous les canaux</span><span class="sxs-lookup"><span data-stu-id="f7684-159">All channels</span></span><br/>                           | <span data-ttu-id="f7684-160">Ce modèle est destiné uniquement aux ordinateurs personnels, et est généralement utilisé pour présenter les fonctionnalités complètes du codec. Il s’agit également de la désignation du modèle pour toutes les données audio encodées avec le codec Windows Media Audio 9 Lossless.</span><span class="sxs-lookup"><span data-stu-id="f7684-160">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.This is also the template designation for all audio encoded with the Windows Media Audio 9 Lossless codec.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f7684-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7684-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7684-162">**Paramètres du modèle de conformité des appareils**</span><span class="sxs-lookup"><span data-stu-id="f7684-162">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> <dt>

[<span data-ttu-id="f7684-163">**Combinaisons recommandées de modèles de conformité des appareils**</span><span class="sxs-lookup"><span data-stu-id="f7684-163">**Recommended Device Conformance Template Combinations**</span></span>](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[<span data-ttu-id="f7684-164">**Modèles de conformité des périphériques vidéo**</span><span class="sxs-lookup"><span data-stu-id="f7684-164">**Video Device Conformance Templates**</span></span>](video-device-conformance-templates.md)
</dt> </dl>

 

 





