---
title: Espace de couleurs standard sRVB
description: À la suite de considérations relatives à la bande passante Internet, Hewlett-Packard et Microsoft ont proposé l’adoption d’un espace de couleurs prédéfini standard, connu sous le nom d’sRGB (IEC 61966-2-1), afin de permettre un mappage précis des couleurs avec très peu de surcharge de données.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS), espace de couleurs sRVB
- WCS (système de couleurs Windows), espace de couleurs sRVB
- gestion des couleurs de l’image, espace de couleurs sRVB
- gestion des couleurs, espace colorimétrique sRVB
- couleurs, espace colorimétrique sRVB
- espace colorimétrique sRVB
- espaces de couleurs, sRVB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2021
ms.locfileid: "106529513"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="20d8c-110">sRGB : espace de couleurs standard</span><span class="sxs-lookup"><span data-stu-id="20d8c-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="20d8c-111">À la suite de considérations relatives à la bande passante Internet, Hewlett-Packard et Microsoft ont proposé l’adoption d’un [espace de couleurs](c.md) prédéfini standard, connu sous le nom d' *sRGB* (IEC 61966-2-1), afin de permettre un mappage précis des [couleurs](c.md) avec très peu de surcharge de données.</span><span class="sxs-lookup"><span data-stu-id="20d8c-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="20d8c-112">Une version de fichier d’aide d’un livre blanc traitant des détails techniques de sRVB, sRVB. hlp, est disponible dans le \\ dossier d’aide du Guide de référence du programmeur WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="20d8c-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="20d8c-113">Différents formats de fichiers peuvent utiliser ou ajouter un indicateur pour spécifier que l’image se trouve dans l’espace de couleurs sRVB.</span><span class="sxs-lookup"><span data-stu-id="20d8c-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="20d8c-114">Dans le format DIB (Device-Independent Bitmap) Windows, la définition du membre **bV5CSType** de la structure [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) sur **LCS \_ sRVB** spécifie que les couleurs DIB se trouvent dans l’espace de couleurs sRVB.</span><span class="sxs-lookup"><span data-stu-id="20d8c-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="20d8c-115">WCS 1,0 fournit la prise en charge native de sRVB.</span><span class="sxs-lookup"><span data-stu-id="20d8c-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="20d8c-116">Il existe deux façons d’utiliser WCS 1,0 pour le rendu d’une image définie dans l’espace de couleurs sRVB :</span><span class="sxs-lookup"><span data-stu-id="20d8c-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="20d8c-117">**Pour afficher une image dans le contexte de périphérique**</span><span class="sxs-lookup"><span data-stu-id="20d8c-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="20d8c-118">Créez un contexte de périphérique (DC) sur le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20d8c-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="20d8c-119">Définissez la gestion des couleurs à l’aide de la fonction [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) .</span><span class="sxs-lookup"><span data-stu-id="20d8c-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="20d8c-120">Utilisez la fonction [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) pour transférer le DIB dans le DC.</span><span class="sxs-lookup"><span data-stu-id="20d8c-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="20d8c-121">Tant que le membre **bV5CSMType** de la structure [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) DIB est défini sur **LCS \_ sRVB**, le système effectue la gestion des couleurs appropriée.</span><span class="sxs-lookup"><span data-stu-id="20d8c-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="20d8c-122">**Pour afficher une image en dehors du contexte de périphérique**</span><span class="sxs-lookup"><span data-stu-id="20d8c-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="20d8c-123">Créez une transformation à l’aide de [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span><span class="sxs-lookup"><span data-stu-id="20d8c-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="20d8c-124">Le membre **lcsCSType** de la structure [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) vers laquelle pointe le paramètre *PLogColorSpace* doit être défini sur **LCS \_ sRVB**.</span><span class="sxs-lookup"><span data-stu-id="20d8c-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="20d8c-125">Le paramètre *hDestProfile* indique l’espace colorimétrique du périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20d8c-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="20d8c-126">Utilisez la transformation de couleur créée pour mettre en correspondance l’image avant de l’afficher sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20d8c-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="20d8c-127">Paramètres par défaut WCS 1,0 pour l’espace colorimétrique d’entrée et le profil de sortie</span><span class="sxs-lookup"><span data-stu-id="20d8c-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="20d8c-128">Si aucun espace colorimétrique d’entrée n’est spécifié, par défaut, WCS 1,0 utilise l’espace de couleurs sRVB comme espace colorimétrique d’entrée pour le [mappage des couleurs](c.md).</span><span class="sxs-lookup"><span data-stu-id="20d8c-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="20d8c-129">Quand aucun profil de sortie n’est spécifié, mais qu’un appareil par défaut est spécifié, WCS 1,0 sélectionne un profil de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="20d8c-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="20d8c-130">Si le périphérique par défaut n’est associé à aucun profil, WCS 1,0 utilise l’espace de couleurs sRVB comme profil de sortie.</span><span class="sxs-lookup"><span data-stu-id="20d8c-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="20d8c-131">Le tableau suivant présente les transformations de couleur résultantes lorsqu’un appareil par défaut n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="20d8c-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|                                 | <span data-ttu-id="20d8c-132">Profil de sortie spécifié</span><span class="sxs-lookup"><span data-stu-id="20d8c-132">Output Profile Specified</span></span>                              | <span data-ttu-id="20d8c-133">Profil de sortie non spécifié</span><span class="sxs-lookup"><span data-stu-id="20d8c-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="20d8c-134">Espace colorimétrique d’entrée spécifié</span><span class="sxs-lookup"><span data-stu-id="20d8c-134">Input Color Space Specified</span></span>     | <span data-ttu-id="20d8c-135">La transformation utilise les profils spécifiés.</span><span class="sxs-lookup"><span data-stu-id="20d8c-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="20d8c-136">La transformation convertit l’espace de couleurs d’entrée connu en sRVB.</span><span class="sxs-lookup"><span data-stu-id="20d8c-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="20d8c-137">Espace colorimétrique d’entrée non spécifié</span><span class="sxs-lookup"><span data-stu-id="20d8c-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="20d8c-138">Transformation convertit de l’sRGB en profil de sortie connu.</span><span class="sxs-lookup"><span data-stu-id="20d8c-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="20d8c-139">La transformation de sRVB en sRVB est supposée ; aucune action n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="20d8c-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="20d8c-140">Profils sRVB et incorporés</span><span class="sxs-lookup"><span data-stu-id="20d8c-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="20d8c-141">À partir de la version ICM 2,0, les applications qui utilisent WCS peuvent incorporer des profils dans les images.</span><span class="sxs-lookup"><span data-stu-id="20d8c-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="20d8c-142">Les profils incorporés assistent les applications des utilisateurs dans le maintien d’une apparence de couleur homogène même si les images sont transmises sur Internet.</span><span class="sxs-lookup"><span data-stu-id="20d8c-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="20d8c-143">Les images qui utilisent l’espace de couleurs sRVB n’ont pas besoin d’un profil de couleurs incorporé.</span><span class="sxs-lookup"><span data-stu-id="20d8c-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="20d8c-144">Étant donné qu’ils n’ont pas de profil incorporé, les images sRVB sont plus petites et plus faciles à transférer entre les canaux de données avec une bande passante limitée.</span><span class="sxs-lookup"><span data-stu-id="20d8c-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="20d8c-145">Les applications doivent définir l’indicateur de groupe de réinitialisation **LCS \_** dans l’en-tête bitmap de l’image pour indiquer que l’image utilise l’espace de couleurs sRVB.</span><span class="sxs-lookup"><span data-stu-id="20d8c-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="20d8c-146">Pour plus d’informations, consultez [structures d’en-tête de bitmap Windows](using-structures-in-wcs-1-0.md) et [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span><span class="sxs-lookup"><span data-stu-id="20d8c-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 