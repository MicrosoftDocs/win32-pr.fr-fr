---
title: Utilisation du processus de mappage des couleurs avec WCS
description: Le mappage des couleurs WCS est basé sur les profils d’appareil.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Color System (WCS), mappage des couleurs
- WCS (système de couleurs Windows), mappage des couleurs
- gestion des couleurs des images, mappage des couleurs
- gestion des couleurs, mappage des couleurs
- couleurs, mappage des couleurs
- mappage des couleurs
- Windows Color System (WCS), profils d’appareil
- WCS (système de couleurs Windows), profils d’appareil
- gestion des couleurs des images, profils d’appareil
- gestion des couleurs, profils d’appareil
- couleurs, profils d’appareil
- Système de couleurs Windows (WCS), profils
- WCS (système de couleurs Windows), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- profils d’appareil
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106522862"
---
# <a name="using-the-color-mapping-process-with-wcs"></a><span data-ttu-id="54984-120">Utilisation du processus de mappage des couleurs avec WCS</span><span class="sxs-lookup"><span data-stu-id="54984-120">Using The Color Mapping Process with WCS</span></span>

<span data-ttu-id="54984-121">Le mappage des couleurs WCS est basé sur les [profils d’appareil](d.md).</span><span class="sxs-lookup"><span data-stu-id="54984-121">WCS color mapping is based on [device profiles](d.md).</span></span> <span data-ttu-id="54984-122">Ils sont fournis par les fournisseurs de périphériques matériels en couleurs et installés lors de l’installation d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="54984-122">These are supplied by vendors of color hardware devices and installed when a device is installed.</span></span> <span data-ttu-id="54984-123">Lorsque le mappage des couleurs est utilisé par un programme d’application, WCS accède au profil d’appareil de l’image pour récupérer les informations nécessaires à la conversion de l’image en PC.</span><span class="sxs-lookup"><span data-stu-id="54984-123">When color mapping is used by an application program, WCS accesses the device profile of the image to get the information needed to convert the image to the PCS.</span></span> <span data-ttu-id="54984-124">La conversion est effectuée par le CMM.</span><span class="sxs-lookup"><span data-stu-id="54984-124">The conversion is done by the CMM.</span></span>

<span data-ttu-id="54984-125">Un profil d’appareil peut être incorporé dans l’image elle-même.</span><span class="sxs-lookup"><span data-stu-id="54984-125">A device profile can be embedded into the image itself.</span></span> <span data-ttu-id="54984-126">Le profil d’appareil est donc parcouru avec l’image, même sur Internet.</span><span class="sxs-lookup"><span data-stu-id="54984-126">So the device profile travels with the image, even across the Internet.</span></span> <span data-ttu-id="54984-127">Un utilisateur n’a pas besoin de l’appareil source pour obtenir un mappage de couleurs précis.</span><span class="sxs-lookup"><span data-stu-id="54984-127">A user does not need the source device to get an accurate color mapping.</span></span> <span data-ttu-id="54984-128">Si une image n’a pas de profil d’appareil, l’espace sRVB est utilisé comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="54984-128">If an image does not have a device profile, the sRGB space is used as a default.</span></span> <span data-ttu-id="54984-129">Pour plus d’informations, consultez [utilisation de la gestion des couleurs sur Internet](using-color-management-on-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="54984-129">For more details, see [Using Color Management on the Internet](using-color-management-on-the-internet.md).</span></span>

<span data-ttu-id="54984-130">Notez que les applications qui utilisent WCS ne doivent jamais incorporer le profil sRVB dans une image.</span><span class="sxs-lookup"><span data-stu-id="54984-130">Note that applications which use WCS should never embed the sRGB profile into an image.</span></span> <span data-ttu-id="54984-131">L’espace colorimétrique sRVB fournit un espace de couleurs standardisé qui est portable sur tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="54984-131">The sRGB color space provides a standardized color space that is portable across all devices.</span></span> <span data-ttu-id="54984-132">Elle est automatiquement disponible pour les utilisateurs de Windows 98 et versions ultérieures, ainsi que Windows 2000 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="54984-132">It is automatically available to users of Windows 98 and later as well as Windows 2000 and later.</span></span> <span data-ttu-id="54984-133">Par conséquent, il n’est pas nécessaire de voyager avec l’image.</span><span class="sxs-lookup"><span data-stu-id="54984-133">Therefore, it does not need to travel with the image.</span></span>

<span data-ttu-id="54984-134">Une fois que les couleurs de l’image se trouvent dans les [PC](p.md), WCS accède au profil d’appareil de l’appareil de destination.</span><span class="sxs-lookup"><span data-stu-id="54984-134">After the image colors are in the [PCS](p.md), WCS accesses the device profile of the destination device.</span></span> <span data-ttu-id="54984-135">Il obtient le CMM pour convertir les couleurs d’image des PC en gamme de l’appareil de destination.</span><span class="sxs-lookup"><span data-stu-id="54984-135">It gets the CMM to convert the image colors from PCS to the gamut of the destination device.</span></span>

<span data-ttu-id="54984-136">Un mappage de couleurs plus complexe peut également être effectué à l’aide du WCS.</span><span class="sxs-lookup"><span data-stu-id="54984-136">More complex color mapping can also be done with WCS.</span></span> <span data-ttu-id="54984-137">Par exemple, il peut être utilisé pour obtenir une idée de ce à quoi ressemble une image créée sur un écran vidéo lorsqu’elle est imprimée sur une imprimante laser haute résolution.</span><span class="sxs-lookup"><span data-stu-id="54984-137">For example, it can be used to get an idea of what an image created on a video display would look like when printed on a high resolution laser printer.</span></span> <span data-ttu-id="54984-138">L’exemple devient plus complexe s’il n’existe qu’une imprimante à jet d’encre standard sur laquelle le prévisualiser.</span><span class="sxs-lookup"><span data-stu-id="54984-138">The example gets more complex if there is only a standard inkjet printer on which to preview it.</span></span> <span data-ttu-id="54984-139">L’image peut être convertie à partir de la gamme de l’affichage, dans la gamme de l’imprimante à jet d’encre.</span><span class="sxs-lookup"><span data-stu-id="54984-139">The image can be converted from the gamut of the display, into the gamut of the inkjet printer.</span></span> <span data-ttu-id="54984-140">À partir de là, il peut être converti en gamme de l’imprimante laser.</span><span class="sxs-lookup"><span data-stu-id="54984-140">From there it can converted into the gamut of the laser printer.</span></span> <span data-ttu-id="54984-141">L’image résultante peut être imprimée sur l’imprimante à jet d’encre.</span><span class="sxs-lookup"><span data-stu-id="54984-141">The resulting image can be printed on the inkjet printer.</span></span> <span data-ttu-id="54984-142">Bien sûr, l’image serait à une résolution plus élevée lorsqu’elle est imprimée sur l’imprimante laser couleur.</span><span class="sxs-lookup"><span data-stu-id="54984-142">Of course the image would be at a higher resolution when printed on the color laser printer.</span></span> <span data-ttu-id="54984-143">Toutefois, les couleurs de l’image de vérification imprimée sur l’imprimante à jet d’encre sont une correspondance proche des couleurs que l’imprimante laser peut imprimer.</span><span class="sxs-lookup"><span data-stu-id="54984-143">However, the colors of the proofing image printed on the inkjet printer would be a close match to the colors that the laser printer would print.</span></span>

<span data-ttu-id="54984-144">La façon dont les conversions dans l’exemple sont effectuées consiste à convertir les couleurs de l’image de la gamme de l’affichage en PC.</span><span class="sxs-lookup"><span data-stu-id="54984-144">The way the conversions in the example are accomplished is to convert the image colors from the display's gamut into the PCS.</span></span> <span data-ttu-id="54984-145">Une fois les couleurs d’image converties en PC, le profil d’appareil de l’imprimante à jet d’encre est utilisé pour les transformer en couleurs de l’imprimante à jet d’encre.</span><span class="sxs-lookup"><span data-stu-id="54984-145">After the image colors are converted into the PCS, the device profile of the inkjet printer would be used to transform them into the gamut of the inkjet printer.</span></span> <span data-ttu-id="54984-146">Ensuite, la transformation gamme à PC est utilisée pour ramener les couleurs aux PC.</span><span class="sxs-lookup"><span data-stu-id="54984-146">Next, the gamut to PCS transform would be used to move the colors back to the PCS.</span></span> <span data-ttu-id="54984-147">À partir de là, le profil d’appareil de l’imprimante laser est utilisé pour convertir les couleurs des PC dans la gamme de l’imprimante laser.</span><span class="sxs-lookup"><span data-stu-id="54984-147">From there, the laser printer's device profile is used to convert the colors from PCS into the gamut of the laser printer.</span></span>

<span data-ttu-id="54984-148">La possibilité de transformer facilement les couleurs d’une gamme d’appareils en ordinateurs, puis de nouveau, permet de vérifier les couleurs d’image destinées à un appareil de sortie en couleur sur pratiquement tous les autres.</span><span class="sxs-lookup"><span data-stu-id="54984-148">The ability to easily transform colors from a device gamut to the PCS and back again enables image colors intended for one color output device to be proofed on almost any other.</span></span>

<span data-ttu-id="54984-149">Dans l’exemple précédent, la description est légèrement différente de la procédure réelle pour plus de clarté.</span><span class="sxs-lookup"><span data-stu-id="54984-149">In the preceding example, the description varies from the actual procedure somewhat for clarity.</span></span> <span data-ttu-id="54984-150">En réalité, toutes les transformations mentionnées dans le paragraphe précédent sont concaténées en une seule transformation.</span><span class="sxs-lookup"><span data-stu-id="54984-150">In reality, all of the transformations mentioned in the preceding paragraph would be concatenated into a single transformation.</span></span>

 

 




