---
title: Élément EQUALIZERSETTINGS
description: Élément EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Apparences du lecteur Windows Media, élément EQUALIZERSETTINGS
- habillages, élément EQUALIZERSETTINGS
- Élément EQUALIZERSETTINGS
- informations de référence sur les habillages, élément EQUALIZERSETTINGS
- éléments, EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae20500dfba656450c3102ee80b4a06e089fe8ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507243"
---
# <a name="equalizersettings-element"></a><span data-ttu-id="a0b04-108">Élément EQUALIZERSETTINGS</span><span class="sxs-lookup"><span data-stu-id="a0b04-108">EQUALIZERSETTINGS Element</span></span>

<span data-ttu-id="a0b04-109">L’élément **EQUALIZERSETTINGS** fournit un moyen de manipuler l’égaliseur graphique et d’autres paramètres audio du lecteur Windows Media à l’aide des attributs et de la méthode répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="a0b04-109">The **EQUALIZERSETTINGS** element provides a way to manipulate the graphic equalizer and other audio settings of Windows Media Player using the attributes and method listed here.</span></span>

<span data-ttu-id="a0b04-110">L’élément **EQUALIZERSETTINGS** prend en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="a0b04-110">The **EQUALIZERSETTINGS** element supports the following attributes.</span></span>



| <span data-ttu-id="a0b04-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="a0b04-111">Attribute</span></span>                                                          | <span data-ttu-id="a0b04-112">Description</span><span class="sxs-lookup"><span data-stu-id="a0b04-112">Description</span></span>                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0b04-113">bandes</span><span class="sxs-lookup"><span data-stu-id="a0b04-113">bands</span></span>](equalizersettings-bands.md)                               | <span data-ttu-id="a0b04-114">Récupère le nombre de bandes de fréquence prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a0b04-114">Retrieves the number of frequency bands supported.</span></span>                                                      |
| [<span data-ttu-id="a0b04-115">omettre</span><span class="sxs-lookup"><span data-stu-id="a0b04-115">bypass</span></span>](equalizersettings-bypass.md)                             | <span data-ttu-id="a0b04-116">Spécifie ou récupère une valeur indiquant si le filtre d’égaliseur est contourné dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="a0b04-116">Specifies or retrieves a value indicating whether the equalizer filter is bypassed in the filter graph.</span></span> |
| [<span data-ttu-id="a0b04-117">Fondu enchaîné</span><span class="sxs-lookup"><span data-stu-id="a0b04-117">crossFade</span></span>](equalizersettings-crossfade.md)                       | <span data-ttu-id="a0b04-118">Spécifie ou récupère une valeur indiquant si le fondu croisé est activé.</span><span class="sxs-lookup"><span data-stu-id="a0b04-118">Specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>                                |
| [<span data-ttu-id="a0b04-119">crossFadeWindow</span><span class="sxs-lookup"><span data-stu-id="a0b04-119">crossFadeWindow</span></span>](equalizersettings-crossfadewindow.md)           | <span data-ttu-id="a0b04-120">Spécifie ou récupère la quantité de chevauchement de fondu croisé en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a0b04-120">Specifies or retrieves the amount of cross-fade overlap in milliseconds.</span></span>                                |
| [<span data-ttu-id="a0b04-121">currentPreset</span><span class="sxs-lookup"><span data-stu-id="a0b04-121">currentPreset</span></span>](equalizersettings-currentpreset.md)               | <span data-ttu-id="a0b04-122">Spécifie ou récupère l’index de la présélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="a0b04-122">Specifies or retrieves the index of the current preset.</span></span>                                                 |
| [<span data-ttu-id="a0b04-123">currentPresetTitle</span><span class="sxs-lookup"><span data-stu-id="a0b04-123">currentPresetTitle</span></span>](equalizersettings-currentpresettitle.md)     | <span data-ttu-id="a0b04-124">Récupère le titre de la présélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="a0b04-124">Retrieves the title of the current preset.</span></span>                                                              |
| [<span data-ttu-id="a0b04-125">currentSpeakerName</span><span class="sxs-lookup"><span data-stu-id="a0b04-125">currentSpeakerName</span></span>](equalizersettings-currentspeakername.md)     | <span data-ttu-id="a0b04-126">Récupère le nom du paramètre de haut-parleur actuel.</span><span class="sxs-lookup"><span data-stu-id="a0b04-126">Retrieves the name of the current speaker setting.</span></span>                                                      |
| [<span data-ttu-id="a0b04-127">enableSplineTension</span><span class="sxs-lookup"><span data-stu-id="a0b04-127">enableSplineTension</span></span>](equalizersettings-enablesplinetension.md)   | <span data-ttu-id="a0b04-128">Spécifie ou récupère une valeur indiquant si la tension de la spline est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="a0b04-128">Specifies or retrieves a value indicating whether spline tension is enabled or disabled.</span></span>                |
| [<span data-ttu-id="a0b04-129">enhancedAudio</span><span class="sxs-lookup"><span data-stu-id="a0b04-129">enhancedAudio</span></span>](equalizersettings-enhancedaudio.md)               | <span data-ttu-id="a0b04-130">Spécifie ou récupère une valeur indiquant si l’audio étendu est activé.</span><span class="sxs-lookup"><span data-stu-id="a0b04-130">Specifies or retrieves a value indicating whether enhanced audio is turned on.</span></span>                          |
| [<span data-ttu-id="a0b04-131">gainLevels</span><span class="sxs-lookup"><span data-stu-id="a0b04-131">gainLevels</span></span>](equalizersettings-gainlevels.md)                     | <span data-ttu-id="a0b04-132">Spécifie ou récupère le niveau de gain de la bande correspondant à l’index fourni.</span><span class="sxs-lookup"><span data-stu-id="a0b04-132">Specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>                  |
| [<span data-ttu-id="a0b04-133">gainLevel1</span><span class="sxs-lookup"><span data-stu-id="a0b04-133">gainLevel1</span></span>](equalizersettings-gainlevel1.md)                     | <span data-ttu-id="a0b04-134">Spécifie ou récupère le niveau de gain de la bande 1.</span><span class="sxs-lookup"><span data-stu-id="a0b04-134">Specifies or retrieves the gain level of band 1.</span></span>                                                        |
| [<span data-ttu-id="a0b04-135">gainLevel2</span><span class="sxs-lookup"><span data-stu-id="a0b04-135">gainLevel2</span></span>](equalizersettings-gainlevel2.md)                     | <span data-ttu-id="a0b04-136">Spécifie ou récupère le niveau de gain de la bande 2.</span><span class="sxs-lookup"><span data-stu-id="a0b04-136">Specifies or retrieves the gain level of band 2.</span></span>                                                        |
| [<span data-ttu-id="a0b04-137">gainLevel3</span><span class="sxs-lookup"><span data-stu-id="a0b04-137">gainLevel3</span></span>](equalizersettings-gainlevel3.md)                     | <span data-ttu-id="a0b04-138">Spécifie ou récupère le niveau de gain de la bande 3.</span><span class="sxs-lookup"><span data-stu-id="a0b04-138">Specifies or retrieves the gain level of band 3.</span></span>                                                        |
| [<span data-ttu-id="a0b04-139">gainLevel4</span><span class="sxs-lookup"><span data-stu-id="a0b04-139">gainLevel4</span></span>](equalizersettings-gainlevel4.md)                     | <span data-ttu-id="a0b04-140">Spécifie ou récupère le niveau de gain de la bande 4.</span><span class="sxs-lookup"><span data-stu-id="a0b04-140">Specifies or retrieves the gain level of band 4.</span></span>                                                        |
| [<span data-ttu-id="a0b04-141">gainLevel5</span><span class="sxs-lookup"><span data-stu-id="a0b04-141">gainLevel5</span></span>](equalizersettings-gainlevel5.md)                     | <span data-ttu-id="a0b04-142">Spécifie ou récupère le niveau de gain de la bande 5.</span><span class="sxs-lookup"><span data-stu-id="a0b04-142">Specifies or retrieves the gain level of band 5.</span></span>                                                        |
| [<span data-ttu-id="a0b04-143">gainLevel6</span><span class="sxs-lookup"><span data-stu-id="a0b04-143">gainLevel6</span></span>](equalizersettings-gainlevel6.md)                     | <span data-ttu-id="a0b04-144">Spécifie ou récupère le niveau de gain de la bande 6.</span><span class="sxs-lookup"><span data-stu-id="a0b04-144">Specifies or retrieves the gain level of band 6.</span></span>                                                        |
| [<span data-ttu-id="a0b04-145">gainLevel7</span><span class="sxs-lookup"><span data-stu-id="a0b04-145">gainLevel7</span></span>](equalizersettings-gainlevel7.md)                     | <span data-ttu-id="a0b04-146">Spécifie ou récupère le niveau de gain de la bande 7.</span><span class="sxs-lookup"><span data-stu-id="a0b04-146">Specifies or retrieves the gain level of band 7.</span></span>                                                        |
| [<span data-ttu-id="a0b04-147">gainLevel8</span><span class="sxs-lookup"><span data-stu-id="a0b04-147">gainLevel8</span></span>](equalizersettings-gainlevel8.md)                     | <span data-ttu-id="a0b04-148">Spécifie ou récupère le niveau de gain de la bande 8.</span><span class="sxs-lookup"><span data-stu-id="a0b04-148">Specifies or retrieves the gain level of band 8.</span></span>                                                        |
| [<span data-ttu-id="a0b04-149">gainLevel9</span><span class="sxs-lookup"><span data-stu-id="a0b04-149">gainLevel9</span></span>](equalizersettings-gainlevel9.md)                     | <span data-ttu-id="a0b04-150">Spécifie ou récupère le niveau de gain de la bande 9.</span><span class="sxs-lookup"><span data-stu-id="a0b04-150">Specifies or retrieves the gain level of band 9.</span></span>                                                        |
| [<span data-ttu-id="a0b04-151">gainLevel10</span><span class="sxs-lookup"><span data-stu-id="a0b04-151">gainLevel10</span></span>](equalizersettings-gainlevel10.md)                   | <span data-ttu-id="a0b04-152">Spécifie ou récupère le niveau de gain de la bande 10.</span><span class="sxs-lookup"><span data-stu-id="a0b04-152">Specifies or retrieves the gain level of band 10.</span></span>                                                       |
| [<span data-ttu-id="a0b04-153">normalisation</span><span class="sxs-lookup"><span data-stu-id="a0b04-153">normalization</span></span>](equalizersettings-normalization.md)               | <span data-ttu-id="a0b04-154">Spécifie ou récupère une valeur indiquant si la normalisation est activée.</span><span class="sxs-lookup"><span data-stu-id="a0b04-154">Specifies or retrieves a value indicating whether normalization is enabled.</span></span>                             |
| [<span data-ttu-id="a0b04-155">normalizationAverage</span><span class="sxs-lookup"><span data-stu-id="a0b04-155">normalizationAverage</span></span>](equalizersettings-normalizationaverage.md) | <span data-ttu-id="a0b04-156">Récupère la valeur de normalisation moyenne.</span><span class="sxs-lookup"><span data-stu-id="a0b04-156">Retrieves the average normalization value.</span></span>                                                              |
| [<span data-ttu-id="a0b04-157">normalizationPeak</span><span class="sxs-lookup"><span data-stu-id="a0b04-157">normalizationPeak</span></span>](equalizersettings-normalizationpeak.md)       | <span data-ttu-id="a0b04-158">Récupère la valeur de normalisation de pointe.</span><span class="sxs-lookup"><span data-stu-id="a0b04-158">Retrieves the peak normalization value.</span></span>                                                                 |
| [<span data-ttu-id="a0b04-159">presetCount</span><span class="sxs-lookup"><span data-stu-id="a0b04-159">presetCount</span></span>](equalizersettings-presetcount.md)                   | <span data-ttu-id="a0b04-160">Récupère le nombre de présélections disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0b04-160">Retrieves the number of presets available.</span></span>                                                              |
| [<span data-ttu-id="a0b04-161">Haut-parleur</span><span class="sxs-lookup"><span data-stu-id="a0b04-161">speakerSize</span></span>](equalizersettings-speakersize.md)                   | <span data-ttu-id="a0b04-162">Spécifie ou récupère l’index de la taille actuelle de l’orateur.</span><span class="sxs-lookup"><span data-stu-id="a0b04-162">Specifies or retrieves the index of the current speaker size.</span></span>                                           |
| [<span data-ttu-id="a0b04-163">splineTension</span><span class="sxs-lookup"><span data-stu-id="a0b04-163">splineTension</span></span>](equalizersettings-splinetension.md)               | <span data-ttu-id="a0b04-164">Spécifie ou récupère la tension de la spline pour le contrôle égaliseur.</span><span class="sxs-lookup"><span data-stu-id="a0b04-164">Specifies or retrieves the spline tension for the equalizer control.</span></span>                                    |
| [<span data-ttu-id="a0b04-165">truBassLevel</span><span class="sxs-lookup"><span data-stu-id="a0b04-165">truBassLevel</span></span>](equalizersettings-trubasslevel.md)                 | <span data-ttu-id="a0b04-166">Spécifie ou récupère le niveau de TruBass du SRS.</span><span class="sxs-lookup"><span data-stu-id="a0b04-166">Specifies or retrieves the SRS TruBass level.</span></span>                                                           |
| [<span data-ttu-id="a0b04-167">wowLevel</span><span class="sxs-lookup"><span data-stu-id="a0b04-167">wowLevel</span></span>](equalizersettings-wowlevel.md)                         | <span data-ttu-id="a0b04-168">Spécifie ou récupère le niveau de l’effet SRS WOW.</span><span class="sxs-lookup"><span data-stu-id="a0b04-168">Specifies or retrieves the SRS WOW Effect level.</span></span>                                                        |



 

<span data-ttu-id="a0b04-169">L’élément **EQUALIZERSETTINGS** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a0b04-169">The **EQUALIZERSETTINGS** element supports the following methods.</span></span>



| <span data-ttu-id="a0b04-170">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0b04-170">Method</span></span>                                                 | <span data-ttu-id="a0b04-171">Description</span><span class="sxs-lookup"><span data-stu-id="a0b04-171">Description</span></span>                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="a0b04-172">nextPreset</span><span class="sxs-lookup"><span data-stu-id="a0b04-172">nextPreset</span></span>](equalizersettings-nextpreset.md)         | <span data-ttu-id="a0b04-173">Applique la présélection d’égaliseur suivante.</span><span class="sxs-lookup"><span data-stu-id="a0b04-173">Applies the next equalizer preset.</span></span>                                   |
| [<span data-ttu-id="a0b04-174">presetTitle</span><span class="sxs-lookup"><span data-stu-id="a0b04-174">presetTitle</span></span>](equalizersettings-presettitle.md)       | <span data-ttu-id="a0b04-175">Récupère le nom de la présélection de l’égaliseur avec l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0b04-175">Retrieves the name of the equalizer preset with the specified index.</span></span> |
| [<span data-ttu-id="a0b04-176">previousPreset</span><span class="sxs-lookup"><span data-stu-id="a0b04-176">previousPreset</span></span>](equalizersettings-previouspreset.md) | <span data-ttu-id="a0b04-177">Applique la présélection précédente de l’égaliseur.</span><span class="sxs-lookup"><span data-stu-id="a0b04-177">Applies the previous equalizer preset.</span></span>                               |
| [<span data-ttu-id="a0b04-178">reset</span><span class="sxs-lookup"><span data-stu-id="a0b04-178">reset</span></span>](equalizersettings-reset.md)                   | <span data-ttu-id="a0b04-179">Rétablit les niveaux de gain de toutes les bandes à zéro décibels.</span><span class="sxs-lookup"><span data-stu-id="a0b04-179">Resets the gain levels of all bands to zero decibels.</span></span>                |



 

<span data-ttu-id="a0b04-180">L’élément **EQUALIZERSETTINGS** peut implémenter les gestionnaires d’événements [ \_ OnChange d’attribut](attribute-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b04-180">The **EQUALIZERSETTINGS** element can implement the [attribute\_onchange](attribute-onchange.md) event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0b04-181">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0b04-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0b04-182">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="a0b04-182">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




