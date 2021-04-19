---
title: Espaces de couleurs dépendants de l’appareil
description: La plupart des espaces de couleurs sont dépendants des appareils.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Color System (WCS), espaces de couleurs dépendants du périphérique
- WCS (système de couleurs Windows), espaces de couleurs dépendants du périphérique
- gestion des couleurs des images, espaces colorimétriques dépendants du périphérique
- gestion des couleurs, espaces colorimétriques dépendants du périphérique
- couleurs, espaces de couleurs dépendants du périphérique
- espaces de couleurs, dépendant du périphérique
- espaces de couleurs dépendants du périphérique
- point blanc
- colorants
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106523087"
---
# <a name="device-dependent-color-spaces"></a><span data-ttu-id="a689a-112">Espaces de couleurs dépendants de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a689a-112">Device-Dependent Color Spaces</span></span>

<span data-ttu-id="a689a-113">La plupart des [espaces de couleurs](c.md) sont dépendants des appareils.</span><span class="sxs-lookup"><span data-stu-id="a689a-113">Most [color spaces](c.md) are device dependent.</span></span> <span data-ttu-id="a689a-114">Même si un appareil particulier, tel qu’une imprimante, peut utiliser l’espace colorimétrique CMJN, les couleurs qu’il affiche pour des valeurs CMJN spécifiques sont souvent légèrement différentes de celles des autres types d’imprimantes.</span><span class="sxs-lookup"><span data-stu-id="a689a-114">Even though a particular device, such as a printer, may use the CMYK color space, the colors it renders for specific CMYK values are often slightly different than all other types of printers..</span></span> <span data-ttu-id="a689a-115">C’est précisément pour cette raison que le système de gestion des couleurs WCS 1,0 est si utile.</span><span class="sxs-lookup"><span data-stu-id="a689a-115">It is precisely for this reason that the WCS 1.0 color management system is so useful.</span></span>

<span data-ttu-id="a689a-116">Tous les espaces de couleurs ont un *point blanc*, qui est défini comme le blanc le plus blanc qui peut être produit dans cet espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="a689a-116">All color spaces have a *white point*, which is defined as the whitest white that can be produced in that color space.</span></span> <span data-ttu-id="a689a-117">Étant donné que les appareils peuvent différer les uns des autres, leurs points blancs peuvent également différer.</span><span class="sxs-lookup"><span data-stu-id="a689a-117">Since devices can differ from one another, their white points can also differ.</span></span> <span data-ttu-id="a689a-118">Toutes les couleurs qu’un appareil peut produire sont relatives à son point blanc.</span><span class="sxs-lookup"><span data-stu-id="a689a-118">All colors that a device can produce are relative to its white point.</span></span> <span data-ttu-id="a689a-119">Par conséquent, un système de gestion des couleurs doit être en mesure de mapper le point blanc d’un espace de couleurs à un autre et de conserver les emplacements relatifs de toutes les couleurs.</span><span class="sxs-lookup"><span data-stu-id="a689a-119">Therefore, a color management system must be able to map the white point of one color space into another and preserve the relative locations of all colors.</span></span> <span data-ttu-id="a689a-120">Il doit également être en mesure de mapper une couleur dans un espace de couleurs à sa correspondance la plus proche dans un autre espace colorimétrique, quelles que soient les différences entre les points blancs.</span><span class="sxs-lookup"><span data-stu-id="a689a-120">It must also be able to map a color in one color space to its closest match in another color space regardless of the differences in the white points.</span></span> <span data-ttu-id="a689a-121">WCS 1,0 peut effectuer ces deux tâches.</span><span class="sxs-lookup"><span data-stu-id="a689a-121">WCS 1.0 is able to accomplish both of these tasks.</span></span>

<span data-ttu-id="a689a-122">L’espace colorimétrique RVB est souvent utilisé sur les moniteurs d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a689a-122">The RGB color space is often used on computer monitors.</span></span> <span data-ttu-id="a689a-123">En tant que tel, il dépend de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a689a-123">As such, it is device dependent.</span></span> <span data-ttu-id="a689a-124">Les imprimantes utilisent généralement des [couleurs](c.md)CMJN.</span><span class="sxs-lookup"><span data-stu-id="a689a-124">Printers typically use CMYK [colorants](c.md).</span></span> <span data-ttu-id="a689a-125">Chaque imprimante implémente sa propre version de l’espace colorimétrique CMJN.</span><span class="sxs-lookup"><span data-stu-id="a689a-125">Each printer implements its own version of the CMYK color space.</span></span> <span data-ttu-id="a689a-126">Les images numériques ne stockent pas réellement les couleurs.</span><span class="sxs-lookup"><span data-stu-id="a689a-126">Digital images may not actually store colors in them.</span></span> <span data-ttu-id="a689a-127">Ils peuvent stocker des numéros d’index dans une palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="a689a-127">They may store index numbers into a palette of colors.</span></span> <span data-ttu-id="a689a-128">Le résultat est qu’il est très difficile pour les développeurs d’applications individuels d’utiliser ou de fournir une méthode standardisée pour déplacer des images de couleur d’un appareil vers un autre.</span><span class="sxs-lookup"><span data-stu-id="a689a-128">The result is that it is very hard for individual application developers to use or provide a standardized method of moving color images from one device to another.</span></span> <span data-ttu-id="a689a-129">Les professionnels de l’imagerie subissent généralement la frustration liée à la création d’une image graphique sur un écran d’ordinateur et à son fonctionnement très différent lors de son impression.</span><span class="sxs-lookup"><span data-stu-id="a689a-129">Imaging professionals commonly experience the frustration of creating a graphic image on a computer screen and having it turn out very differently when it is printed.</span></span> <span data-ttu-id="a689a-130">WCS 1,0 répond à ces besoins en imagerie.</span><span class="sxs-lookup"><span data-stu-id="a689a-130">WCS 1.0 addresses these imaging needs.</span></span>

 

 




