---
title: Empaquetage du plug-in DSP
description: Empaquetage du plug-in DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Plug-ins du lecteur Windows Media, pipeline Media Foundation
- plug-ins, pipeline Media Foundation
- plug-ins de traitement de signal numérique, pipeline Media Foundation
- Plug-ins DSP, pipeline Media Foundation
- Pipeline Media Foundation
- Plug-ins du lecteur Windows Media, pipeline DirectShow
- plug-ins, pipeline DirectShow
- plug-ins de traitement de signal numérique, pipeline DirectShow
- Plug-ins DSP, pipeline DirectShow
- Pipeline DirectShow
- plug-ins de traitement de signal numérique, de base
- Plug-ins DSP, de base
- Plug-ins du lecteur Windows Media, DSP de base
- plug-ins, DSP de base
- plug-ins de base DSP
- Plug-ins du lecteur Windows Media, DSP en deux modes
- plug-ins, DSP en deux modes
- plug-ins de traitement de signal numérique, double mode
- Plug-ins DSP, double mode
- plug-ins DSP à double mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513530"
---
# <a name="dsp-plug-in-packaging"></a><span data-ttu-id="aafca-123">Empaquetage du plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="aafca-123">DSP Plug-in Packaging</span></span>

<span data-ttu-id="aafca-124">Le lecteur Windows Media effectue le rendu des données audio et vidéo à l’aide de l’un des pipelines suivants.</span><span class="sxs-lookup"><span data-stu-id="aafca-124">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="aafca-125">DirectShow</span><span class="sxs-lookup"><span data-stu-id="aafca-125">DirectShow</span></span>
-   <span data-ttu-id="aafca-126">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aafca-126">Media Foundation</span></span>

<span data-ttu-id="aafca-127">Dans Microsoft Windows XP et les versions antérieures, le lecteur utilise DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aafca-127">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="aafca-128">Dans Windows Vista, le lecteur utilise parfois DirectShow et utilise parfois Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="aafca-128">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="aafca-129">Un plug-in DSP conçu pour s’exécuter dans le pipeline DirectShow est appelé un *plug-in DSP de base*.</span><span class="sxs-lookup"><span data-stu-id="aafca-129">A DSP plug-in that is designed to run in the DirectShow pipeline is called a *basic DSP plug-in*.</span></span> <span data-ttu-id="aafca-130">Un plug-in DSP de base agit comme un objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="aafca-130">A basic DSP plug-ins acts as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="aafca-131">Un plug-in DSP de base peut s’exécuter en mode natif dans le pipeline DirectShow et peut également s’exécuter dans le pipeline Media Foundation à l’intérieur d’un wrapper fourni par Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="aafca-131">A basic DSP plug-in can run natively in the DirectShow pipeline and can also run in the Media Foundation pipeline inside a wrapper provided by Media Foundation.</span></span>

<span data-ttu-id="aafca-132">Un plug-in DSP conçu pour s’exécuter en mode natif (aucun Wrapper requis) à la fois dans les pipelines DirectShow et Media Foundation est appelé un *plug-in DSP à double mode*.</span><span class="sxs-lookup"><span data-stu-id="aafca-132">A DSP plug-in that is designed to run natively (no wrapper required) in both the DirectShow and Media Foundation pipelines is called a *dual-mode DSP plug-in*.</span></span> <span data-ttu-id="aafca-133">Un plug-in DSP à deux modes peut agir comme DMO ou comme une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="aafca-133">A dual-mode DSP plug-in can act as a DMO or as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="aafca-134">Un plug-in DSP est un objet COM qui est empaqueté en tant que fichier. dll à inscription automatique.</span><span class="sxs-lookup"><span data-stu-id="aafca-134">A DSP plug-in is a COM object that is packaged as a self-registering .dll file.</span></span> <span data-ttu-id="aafca-135">Les interfaces implémentées par le plug-in varient selon que le plug-in est conçu comme un plug-in DSP de base ou en tant que plug-in DSP à double mode.</span><span class="sxs-lookup"><span data-stu-id="aafca-135">The interfaces that the plug-in implements depend on whether the plug-in is designed as a basic DSP plug-in or as a dual-mode DSP plug-in.</span></span> <span data-ttu-id="aafca-136">Pour obtenir des informations détaillées sur les interfaces que les plug-ins DSP doivent implémenter, consultez [interfaces requises](required-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="aafca-136">For detailed information about the interfaces that DSP plug-ins must implement, see [Required Interfaces](required-interfaces.md).</span></span>

<span data-ttu-id="aafca-137">Un plug-in DSP qui s’exécute dans le pipeline Media Foundation (soit en mode natif, soit encapsulé) doit inscrire son modèle de thread comme « both ».</span><span class="sxs-lookup"><span data-stu-id="aafca-137">A DSP plug-in that runs in the Media Foundation pipeline (either natively or wrapped) must register its threading model as "Both".</span></span> <span data-ttu-id="aafca-138">Pour plus d’informations sur les sous-clés et les entrées de Registre associées aux plug-ins DSP, consultez [inscription des plug-ins DSP](registering-dsp-plug-ins.md).</span><span class="sxs-lookup"><span data-stu-id="aafca-138">For detailed information about registry subkeys and entries associated with DSP plug-ins, see [Registering DSP Plug-ins](registering-dsp-plug-ins.md).</span></span>

<span data-ttu-id="aafca-139">Un plug-in DSP qui implémente des interfaces personnalisées et s’exécute dans le pipeline Media Foundation (en mode natif ou encapsulé) doit être associé à un fichier. dll proxy-stub qui peut marshaler les interfaces personnalisées au-delà des limites du processus.</span><span class="sxs-lookup"><span data-stu-id="aafca-139">A DSP plug-in that implements custom interfaces and runs in the Media Foundation pipeline (either natively or wrapped) must be paired with a proxy-stub .dll file that can marshal the custom interfaces across process boundaries.</span></span> <span data-ttu-id="aafca-140">Pour plus d’informations sur le composant proxy-stub, consultez [mise à jour des plug-ins DSP existants](updating-existing-dsp-plug-ins.md) et [mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="aafca-140">For information about the proxy-stub component, see [Updating Existing DSP Plug-ins](updating-existing-dsp-plug-ins.md) and [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span>

<span data-ttu-id="aafca-141">Les objets de plug-in DSP ne doivent pas être créés en tant que singletons.</span><span class="sxs-lookup"><span data-stu-id="aafca-141">DSP plug-in objects must not be created as singletons.</span></span> <span data-ttu-id="aafca-142">Le lecteur Windows Media doit être en mesure de créer plusieurs instances distinctes d’un plug-in DSP particulier.</span><span class="sxs-lookup"><span data-stu-id="aafca-142">Windows Media Player must be able to create multiple separate instances of a particular DSP plug-in.</span></span>

<span data-ttu-id="aafca-143">Les plug-ins DSP qui s’exécutent dans le chemin d’accès de support protégé de Windows Vista (PMP) doivent être signés.</span><span class="sxs-lookup"><span data-stu-id="aafca-143">DSP plug-ins that run in the Windows Vista Protected Media Path (PMP) must be signed.</span></span> <span data-ttu-id="aafca-144">Pour plus d’informations, consultez [signature du code pour les composants multimédias protégés dans Windows Vista](/windows-hardware/test/hlk/).</span><span class="sxs-lookup"><span data-stu-id="aafca-144">For more information, see [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aafca-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aafca-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aafca-146">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="aafca-146">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 