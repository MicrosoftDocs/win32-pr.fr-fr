---
title: Fonctions de base à utiliser dans un contexte d’appareil
description: Les fonctions WCS suivantes offrent des fonctionnalités de mappage de couleurs de base dans les contextes de périphérique. Elles sont utiles pour toutes les applications qui doivent implémenter la gestion des couleurs avec une faible surcharge et une intervention minimale de l’utilisateur.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Color System (WCS), fonctions
- WCS (système de couleurs Windows), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
- Système de couleurs Windows (WCS), contextes de périphérique
- WCS (système de couleurs Windows), contextes de périphérique
- gestion des couleurs des images, contextes de périphérique
- gestion des couleurs, contextes de périphérique
- couleurs, contextes de périphérique
- Référence WCS, contextes de périphérique
- référence pour WCS, contextes de périphérique
- contextes de périphérique
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "106538033"
---
# <a name="basic-functions-for-use-within-a-device-context"></a><span data-ttu-id="7c7a6-119">Fonctions de base à utiliser dans un contexte d’appareil</span><span class="sxs-lookup"><span data-stu-id="7c7a6-119">Basic Functions for Use Within a Device Context</span></span>

<span data-ttu-id="7c7a6-120">Les fonctions WCS suivantes offrent des fonctionnalités de [mappage de couleurs](c.md) de base dans les contextes de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-120">The following WCS functions deliver basic [color mapping](c.md) capabilities within device contexts.</span></span> <span data-ttu-id="7c7a6-121">Elles sont utiles pour toutes les applications qui doivent implémenter la gestion des couleurs avec une faible surcharge et une intervention minimale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-121">They are useful to all applications that need to implement color management with low overhead and minimal user intervention.</span></span>



| <span data-ttu-id="7c7a6-122">Fonction</span><span class="sxs-lookup"><span data-stu-id="7c7a6-122">Function</span></span>                                                           | <span data-ttu-id="7c7a6-123">Description</span><span class="sxs-lookup"><span data-stu-id="7c7a6-123">Description</span></span>                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c7a6-124">**CheckColorsInGamut**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-124">**CheckColorsInGamut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | <span data-ttu-id="7c7a6-125">Vérifie si les couleurs spécifiées se trouvent dans la gamme d’appareils.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-125">Checks if given colors are in a device's gamut.</span></span>                                                                                                     |
| [<span data-ttu-id="7c7a6-126">**ColorCorrectPalette**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-126">**ColorCorrectPalette**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | <span data-ttu-id="7c7a6-127">Corrige les entrées dans une palette pour un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-127">Corrects the entries in a palette for a device context.</span></span>                                                                                             |
| [<span data-ttu-id="7c7a6-128">**ColorMatchToTarget**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-128">**ColorMatchToTarget**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | <span data-ttu-id="7c7a6-129">Effectue un mappage des couleurs à des fins de préversion.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-129">Performs color mapping for preview purposes.</span></span>                                                                                                        |
| [<span data-ttu-id="7c7a6-130">**CreateColorSpace**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-130">**CreateColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | <span data-ttu-id="7c7a6-131">Crée un espace de couleurs.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-131">Creates a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="7c7a6-132">**DeleteColorSpace**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-132">**DeleteColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | <span data-ttu-id="7c7a6-133">Supprime un espace de couleurs.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-133">Deletes a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="7c7a6-134">**EnumICMProfiles**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-134">**EnumICMProfiles**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | <span data-ttu-id="7c7a6-135">Énumère les profils de couleur de sortie disponibles pour un contexte de périphérique donné.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-135">Enumerates output color profiles available for a given device context.</span></span>                                                                              |
| [<span data-ttu-id="7c7a6-136">**EnumICMProfilesProcCallback**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-136">**EnumICMProfilesProcCallback**</span></span>](/windows/desktop/api/Wingdi/) | <span data-ttu-id="7c7a6-137">Fonction de rappel définie par l’application pour [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span><span class="sxs-lookup"><span data-stu-id="7c7a6-137">Application-defined callback function for [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span></span> <span data-ttu-id="7c7a6-138">Le nom de cette fonction est également défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-138">The name of this function is also defined by the application.</span></span> |
| [<span data-ttu-id="7c7a6-139">**GetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-139">**GetColorSpace**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | <span data-ttu-id="7c7a6-140">Obtient l’espace colorimétrique d’entrée actuel dans un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-140">Gets the current input color space in a device context.</span></span> |
| [<span data-ttu-id="7c7a6-141">**GetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-141">**GetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | <span data-ttu-id="7c7a6-142">Obtient le profil de couleur de sortie actuel d’un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-142">Gets the current output color profile of a device context.</span></span>                                                                                          |
| [<span data-ttu-id="7c7a6-143">**GetLogColorSpace**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-143">**GetLogColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | <span data-ttu-id="7c7a6-144">Obtient la structure [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) d’un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-144">Gets the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure of a device context.</span></span>                                                                      |
| [<span data-ttu-id="7c7a6-145">**SetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-145">**SetColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | <span data-ttu-id="7c7a6-146">Définit l’espace colorimétrique d’entrée d’un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-146">Sets a device context's input color space.</span></span>                                                                                                          |
| [<span data-ttu-id="7c7a6-147">**SetICMMode**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-147">**SetICMMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | <span data-ttu-id="7c7a6-148">Active ou désactive la gestion des couleurs dans un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-148">Turns color management on or off in a device context.</span></span>                                                                                               |
| [<span data-ttu-id="7c7a6-149">**SetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-149">**SetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | <span data-ttu-id="7c7a6-150">Définit le profil de couleur de sortie pour un contexte de périphérique donné.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-150">Sets the output color profile for a given device context.</span></span>                                                                                           |
| [<span data-ttu-id="7c7a6-151">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="7c7a6-151">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | <span data-ttu-id="7c7a6-152">Énumère tous les profils de couleurs qui répondent aux critères d’énumération dans la portée de gestion des profils spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-152">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                      |



 

 

 




