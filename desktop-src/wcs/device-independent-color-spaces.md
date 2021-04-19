---
title: Espaces de couleurs indépendants de l’appareil
description: Reconnaissant la nécessité de mesures de couleur standard, indépendantes des appareils, la Commission internationale de l’Eclairage (Commission internationale sur l’éclairage) ou CIE, a créé un espace de couleurs basé sur \ 0034 ; imaginaire-0034 ; couleurs principales.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Système de couleurs Windows (WCS), espaces de couleurs indépendants du périphérique
- WCS (système de couleurs Windows), espaces de couleurs indépendants du périphérique
- gestion des couleurs des images, espaces de couleurs indépendants du périphérique
- gestion des couleurs, espaces de couleurs indépendants du périphérique
- couleurs, espaces de couleurs indépendants du périphérique
- espaces de couleurs, indépendants du périphérique
- espaces de couleurs indépendants du périphérique
- Commission internationale de l’Eclairage (CIE)
- International Commission on illumination (CIE)
- CIE (Commission international de l’Eclairage)
- CIE (Commission internationale sur l’éclairage)
- Espace de couleurs CIEXYZ
- Espace de couleurs XYZ
- espace colorimétrique sRVB
- espaces de couleurs, CIEXYZ
- espaces de couleurs, sRVB
- espaces de couleurs, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106539363"
---
# <a name="device-independent-color-spaces"></a><span data-ttu-id="36e3c-120">Espaces de couleurs indépendants de l’appareil</span><span class="sxs-lookup"><span data-stu-id="36e3c-120">Device-Independent Color Spaces</span></span>

<span data-ttu-id="36e3c-121">Reconnaissant la nécessité de mesures de couleur standard, indépendantes des appareils, la Commission internationale de l’Eclairage (Commission internationale sur l’éclairage) ou CIE, a créé un [espace de couleurs](c.md) basé sur les [couleurs primaires](p.md)« imaginaires ».</span><span class="sxs-lookup"><span data-stu-id="36e3c-121">Recognizing the need for standard, device-independent color measurements, the Commission International de l'Eclairage (International Commission on Illumination), or CIE, created a [color space](c.md) based on "imaginary" [primary colors](p.md).</span></span> <span data-ttu-id="36e3c-122">Aucun appareil réel ne devrait produire des couleurs dans cet espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="36e3c-122">No actual device is expected to produce colors in this color space.</span></span> <span data-ttu-id="36e3c-123">Il est utilisé comme moyen de convertir les couleurs d’un espace de couleurs à un autre.</span><span class="sxs-lookup"><span data-stu-id="36e3c-123">It is used as a means of converting colors from one color space to another.</span></span> <span data-ttu-id="36e3c-124">Les couleurs primaires de cet espace colorimétrique sont les couleurs abstraites X, Y et Z.</span><span class="sxs-lookup"><span data-stu-id="36e3c-124">The primary colors in this color space are the abstract colors X, Y, and Z.</span></span>

<span data-ttu-id="36e3c-125">L’espace de couleurs 1931 CIEXYZ est largement utilisé comme base pour la conversion de l’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="36e3c-125">The 1931 CIEXYZ color space is widely used as the basis for color space conversion.</span></span> <span data-ttu-id="36e3c-126">Avec l’avènement d’Internet, toutefois, les considérations relatives à la bande passante ont rendu l’espace de couleurs XYZ plus complexe.</span><span class="sxs-lookup"><span data-stu-id="36e3c-126">With the rise of the Internet, however, bandwidth considerations have made the XYZ color space unwieldy.</span></span> <span data-ttu-id="36e3c-127">L’échange d’images sur la bande passante limitée d’Internet nécessite un modèle de [couleurs](c.md)plus compact.</span><span class="sxs-lookup"><span data-stu-id="36e3c-127">The exchange of images over the limited bandwidth of the Internet necessitates a more compact [color model](c.md).</span></span>

<span data-ttu-id="36e3c-128">Par conséquent, Hewlett-Packard et Microsoft ont proposé l’adoption d’un espace de couleurs RVB prédéfini standard, connu sous le nom d’sRGB, afin de permettre une gestion des couleurs précise avec très peu de surcharge de données.</span><span class="sxs-lookup"><span data-stu-id="36e3c-128">As a result, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined RGB color space known as sRGB, so as to allow accurate color management with very little data overhead.</span></span> <span data-ttu-id="36e3c-129">Cette norme a été approuvée comme norme internationale officielle par le Commission Électrotechnique Internationale (IEC) en tant que IEC 61966-2-1 : systèmes multimédias et mesure EquipmentColour et ManagementPart 2-1 : Color ManagementDefault RGB Color Space.</span><span class="sxs-lookup"><span data-stu-id="36e3c-129">This standard has been approved as a formal international standard by the International Electrotechnical Commission (IEC) as IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Colour ManagementDefault RGB Colour Space.</span></span> <span data-ttu-id="36e3c-130">Elle est disponible directement à partir du service IEC à l’adresse <https://www.iec.ch/> .</span><span class="sxs-lookup"><span data-stu-id="36e3c-130">It is available directly from the IEC at <https://www.iec.ch/>.</span></span> <span data-ttu-id="36e3c-131">Les informations qui décrivent les problèmes techniques inhérents à sRVB sont disponibles sur Internet à l’adresse suivante :</span><span class="sxs-lookup"><span data-stu-id="36e3c-131">Information discussing the technical issues involved in sRGB is available on the Internet at:</span></span>

[<span data-ttu-id="36e3c-132">Un espace de couleurs par défaut standard pour Internet-sRGB</span><span class="sxs-lookup"><span data-stu-id="36e3c-132">A Standard Default Color Space for the Internet - sRGB</span></span>](https://www.w3.org/Graphics/Color/sRGB.html)

<span data-ttu-id="36e3c-133">Une version de fichier d’aide d’un livre blanc traitant des problèmes techniques liés à sRVB, sRVB. HLP, est disponible dans le \\ dossier d’aide du Guide de référence du programmeur WCS 1,0 dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="36e3c-133">A help-file version of a white paper discussing the technical issues involved in sRGB, sRGB.HLP, is available in the \\Help folder of the WCS 1.0 Programmer's Reference in the Platform SDK.</span></span>

<span data-ttu-id="36e3c-134">Différents formats de fichiers peuvent utiliser ou ajouter un indicateur pour spécifier que l’image se trouve dans l’espace de couleurs sRVB.</span><span class="sxs-lookup"><span data-stu-id="36e3c-134">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="36e3c-135">Dans le format DIB (Device-Independent Bitmap) Windows, la définition du membre **bV5CSType** de la structure [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) sur LCS \_ sRVB spécifie que les couleurs DIB se trouvent dans l’espace de couleurs sRVB.</span><span class="sxs-lookup"><span data-stu-id="36e3c-135">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) structure to LCS\_sRGB specifies that the DIB colors are in the sRGB color space.</span></span>

 

 




