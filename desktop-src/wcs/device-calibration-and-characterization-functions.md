---
title: Fonctions d’étalonnage et de caractérisation des appareils
description: Les fonctions suivantes sont utiles pour écrire les outils d’étalonnage et de caractérisation des appareils nécessaires à l’installation et à l’étalonnage des appareils d’affichage de couleur tels que les moniteurs et les imprimantes.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Color System (WCS), fonctions
- WCS (système de couleurs Windows), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
- Windows Color System (WCS), étalonnage de l’appareil
- WCS (Windows Color System), étalonnage de l’appareil
- gestion des couleurs des images, étalonnage des appareils
- gestion des couleurs, étalonnage des appareils
- couleurs, étalonnage de l’appareil
- Référence WCS, étalonnage de l’appareil
- référence pour WCS, étalonnage de l’appareil
- Système de couleurs Windows (WCS), caractérisation
- WCS (système de couleurs Windows), caractérisation
- gestion des couleurs des images, caractérisation
- gestion des couleurs, caractérisation
- couleurs, caractérisation
- Référence WCS, caractérisation
- référence pour WCS, caractérisation
- étalonnage de l’appareil
- Auto
- caractérisation
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106531307"
---
# <a name="device-calibration-and-characterization-functions"></a><span data-ttu-id="1502f-127">Fonctions d’étalonnage et de caractérisation des appareils</span><span class="sxs-lookup"><span data-stu-id="1502f-127">Device Calibration and Characterization Functions</span></span>

<span data-ttu-id="1502f-128">Les fonctions suivantes sont utiles pour écrire les outils d’étalonnage et de caractérisation des appareils nécessaires à l’installation et à l’étalonnage des appareils d’affichage de couleur tels que les moniteurs et les imprimantes.</span><span class="sxs-lookup"><span data-stu-id="1502f-128">The following functions are useful for writing device calibration and characterization tools needed for installing and calibrating color display devices such as monitors and printers.</span></span>



| <span data-ttu-id="1502f-129">Fonction</span><span class="sxs-lookup"><span data-stu-id="1502f-129">Function</span></span> | <span data-ttu-id="1502f-130">Description</span><span class="sxs-lookup"><span data-stu-id="1502f-130">Description</span></span> |
|-|-|
| [<span data-ttu-id="1502f-131">**CloseColorProfile**</span><span class="sxs-lookup"><span data-stu-id="1502f-131">**CloseColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-closecolorprofile) | <span data-ttu-id="1502f-132">Ferme un handle de profil ouvert.</span><span class="sxs-lookup"><span data-stu-id="1502f-132">Closes an open profile handle.</span></span> |
| [<span data-ttu-id="1502f-133">**CreateDeviceLinkProfile**</span><span class="sxs-lookup"><span data-stu-id="1502f-133">**CreateDeviceLinkProfile**</span></span>](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | <span data-ttu-id="1502f-134">Crée un *profil de lien d’appareil* ICC (International Color Consortium) à partir d’un ensemble de profils de couleurs, à l’aide des intentions spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1502f-134">Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.</span></span> |
| [<span data-ttu-id="1502f-135">**GetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="1502f-135">**GetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | <span data-ttu-id="1502f-136">Copie les données d’un élément de profil balisé spécifié d’un profil de couleurs spécifié dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1502f-136">Copies data from a specified tagged profile element of a specified color profile into a buffer.</span></span> |
| [<span data-ttu-id="1502f-137">**GetColorProfileElementTag**</span><span class="sxs-lookup"><span data-stu-id="1502f-137">**GetColorProfileElementTag**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | <span data-ttu-id="1502f-138">Récupère le nom de balise spécifié par *dwIndex* dans la table des balises d’un profil de couleurs ICC (International Color Consortium) donné, où *dwIndex* est un index de base 1 dans cette table.</span><span class="sxs-lookup"><span data-stu-id="1502f-138">Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.</span></span> |
| [<span data-ttu-id="1502f-139">**GetColorProfileFromHandle**</span><span class="sxs-lookup"><span data-stu-id="1502f-139">**GetColorProfileFromHandle**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| <span data-ttu-id="1502f-140">Récupère le contenu du profil de couleurs en fonction d’un handle d’un profil de couleurs ouvert.</span><span class="sxs-lookup"><span data-stu-id="1502f-140">Retrieves the color profile contents given a handle to an open color profile.</span></span>     |
| [<span data-ttu-id="1502f-141">**GetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="1502f-141">**GetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | <span data-ttu-id="1502f-142">Récupère ou dérive une structure d’en-tête ICC à partir du profil de couleurs ICC ou du profil XML WCS.</span><span class="sxs-lookup"><span data-stu-id="1502f-142">Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile.</span></span> <span data-ttu-id="1502f-143">Les pilotes et les applications doivent supposer que retourne la **valeur true** indique qu’un en-tête correctement structuré est retourné.</span><span class="sxs-lookup"><span data-stu-id="1502f-143">Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned.</span></span> <span data-ttu-id="1502f-144">Chaque balise doit toujours être validée indépendamment à l’aide de l’API ICM2 héritée ou des API de schéma XML.</span><span class="sxs-lookup"><span data-stu-id="1502f-144">Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.</span></span> |
| [<span data-ttu-id="1502f-145">**GetCountColorProfileElements**</span><span class="sxs-lookup"><span data-stu-id="1502f-145">**GetCountColorProfileElements**</span></span>](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | <span data-ttu-id="1502f-146">Récupère le nombre d’éléments avec balises dans un profil de couleurs donné.</span><span class="sxs-lookup"><span data-stu-id="1502f-146">Retrieves the number of tagged elements in a given color profile.</span></span> |
| [<span data-ttu-id="1502f-147">**GetPS2ColorRenderingDictionary**</span><span class="sxs-lookup"><span data-stu-id="1502f-147">**GetPS2ColorRenderingDictionary**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | <span data-ttu-id="1502f-148">Récupère le dictionnaire de rendu de couleur PostScript de niveau 2 à partir du profil de couleurs ICC spécifié.</span><span class="sxs-lookup"><span data-stu-id="1502f-148">Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.</span></span> |
| [<span data-ttu-id="1502f-149">**GetPS2ColorRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="1502f-149">**GetPS2ColorRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | <span data-ttu-id="1502f-150">Récupère l' [intention de rendu](r.md) de couleur PostScript de niveau 2 d’un profil de couleurs ICC.</span><span class="sxs-lookup"><span data-stu-id="1502f-150">Retrieves the PostScript Level 2 color [rendering intent](r.md) from an ICC color profile.</span></span> |
| [<span data-ttu-id="1502f-151">**GetPS2ColorSpaceArray**</span><span class="sxs-lookup"><span data-stu-id="1502f-151">**GetPS2ColorSpaceArray**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | <span data-ttu-id="1502f-152">Récupère le tableau d' [espace colorimétrique](c.md) PostScript de niveau 2 à partir d’un profil de couleurs ICC.</span><span class="sxs-lookup"><span data-stu-id="1502f-152">Retrieves the PostScript Level 2 [color space](c.md) array from an ICC color profile.</span></span> |
| [<span data-ttu-id="1502f-153">**IsColorProfileTagPresent**</span><span class="sxs-lookup"><span data-stu-id="1502f-153">**IsColorProfileTagPresent**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | <span data-ttu-id="1502f-154">Signale si une balise ICC (International Color Consortium) spécifiée est présente dans le profil de couleurs spécifié.</span><span class="sxs-lookup"><span data-stu-id="1502f-154">Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.</span></span> |
| [<span data-ttu-id="1502f-155">**IsColorProfileValid**</span><span class="sxs-lookup"><span data-stu-id="1502f-155">**IsColorProfileValid**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | <span data-ttu-id="1502f-156">Permet de déterminer si le profil spécifié est un profil ICC (International Color Consortium) valide ou un handle de profil WCS (Windows Color System) valide qui peut être utilisé pour la gestion des couleurs.</span><span class="sxs-lookup"><span data-stu-id="1502f-156">Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management.</span></span> |
| [<span data-ttu-id="1502f-157">**OpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="1502f-157">**OpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-opencolorprofilew) | <span data-ttu-id="1502f-158">Crée un handle vers un profil de couleurs spécifié.</span><span class="sxs-lookup"><span data-stu-id="1502f-158">Creates a handle to a specified color profile.</span></span> <span data-ttu-id="1502f-159">Le descripteur peut ensuite être utilisé dans d’autres fonctions de gestion des profils.</span><span class="sxs-lookup"><span data-stu-id="1502f-159">The handle can then be used in other profile management functions.</span></span> |
| [<span data-ttu-id="1502f-160">**SetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="1502f-160">**SetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | <span data-ttu-id="1502f-161">Définit les données d’élément pour un élément de profil balisé dans un profil de couleurs ICC.</span><span class="sxs-lookup"><span data-stu-id="1502f-161">Sets the element data for a tagged profile element in an ICC color profile.</span></span> |
| [<span data-ttu-id="1502f-162">**SetColorProfileElementReference**</span><span class="sxs-lookup"><span data-stu-id="1502f-162">**SetColorProfileElementReference**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | <span data-ttu-id="1502f-163">Crée dans un profil de couleurs ICC spécifié une nouvelle balise qui référence les mêmes données qu’une balise existante.</span><span class="sxs-lookup"><span data-stu-id="1502f-163">Creates in a specified ICC color profile a new tag that references the same data as an existing tag.</span></span> |
| [<span data-ttu-id="1502f-164">**SetColorProfileElementSize**</span><span class="sxs-lookup"><span data-stu-id="1502f-164">**SetColorProfileElementSize**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | <span data-ttu-id="1502f-165">Définit la taille d’un élément balisé dans un profil de couleurs ICC.</span><span class="sxs-lookup"><span data-stu-id="1502f-165">Sets the size of a tagged element in an ICC color profile.</span></span> |
| [<span data-ttu-id="1502f-166">**SetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="1502f-166">**SetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | <span data-ttu-id="1502f-167">Définit les données d’en-tête dans un profil de couleurs ICC spécifié.</span><span class="sxs-lookup"><span data-stu-id="1502f-167">Sets the header data in a specified ICC color profile.</span></span> |
| [<span data-ttu-id="1502f-168">**WcsGetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="1502f-168">**WcsGetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | <span data-ttu-id="1502f-169">Détermine si la gestion du système de l’état d’étalonnage de l’affichage est activée.</span><span class="sxs-lookup"><span data-stu-id="1502f-169">Determines whether system management of the display calibration state is enabled.</span></span> |
| [<span data-ttu-id="1502f-170">**WcsSetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="1502f-170">**WcsSetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | <span data-ttu-id="1502f-171">Détermine si la gestion du système de l’état d’étalonnage de l’affichage est activée.</span><span class="sxs-lookup"><span data-stu-id="1502f-171">Determines whether system management of the display calibration state is enabled.</span></span> |



 

 

 




