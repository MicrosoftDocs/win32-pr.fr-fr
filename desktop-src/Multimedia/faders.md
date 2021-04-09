---
title: Faders
description: Faders
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- mixages audio, contrôles
- mixages audio, faders
- mélangeurs, contrôles
- mélangeurs, faders
- faders
- Structure MIXERCONTROLDETAILS_UNSIGNED
- contrôle de l’atténuation du volume
- contrôle de fondu du volume de basses
- contrôle de fondu du volume des aigus
- contrôle d’égaliseur graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940887"
---
# <a name="faders"></a><span data-ttu-id="0acdb-113">Faders</span><span class="sxs-lookup"><span data-stu-id="0acdb-113">Faders</span></span>

<span data-ttu-id="0acdb-114">Les contrôles d’atténuation sont généralement des contrôles verticaux qui peuvent être ajustés ou réduits.</span><span class="sxs-lookup"><span data-stu-id="0acdb-114">The fader controls are typically vertical controls that can be adjusted up or down.</span></span> <span data-ttu-id="0acdb-115">Ces contrôles ont une échelle linéaire et utilisent la [**structure \_ non signée MIXERCONTROLDETAILS**](/previous-versions//dd757298(v=vs.85)) pour récupérer et définir les détails du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0acdb-115">These controls have a linear scale and use the [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structure to retrieve and set control details.</span></span> <span data-ttu-id="0acdb-116">Le tableau suivant décrit les types de faders.</span><span class="sxs-lookup"><span data-stu-id="0acdb-116">The following table describes the types of faders.</span></span>



| <span data-ttu-id="0acdb-117">Contrôler</span><span class="sxs-lookup"><span data-stu-id="0acdb-117">Control</span></span>   | <span data-ttu-id="0acdb-118">Description</span><span class="sxs-lookup"><span data-stu-id="0acdb-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0acdb-119">Émission</span><span class="sxs-lookup"><span data-stu-id="0acdb-119">Fader</span></span>     | <span data-ttu-id="0acdb-120">Contrôle d’atténuation général.</span><span class="sxs-lookup"><span data-stu-id="0acdb-120">General fade control.</span></span> <span data-ttu-id="0acdb-121">La plage de valeurs acceptables est comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="0acdb-121">The range of acceptable values is 0 through 65,535.</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0acdb-122">Volume</span><span class="sxs-lookup"><span data-stu-id="0acdb-122">Volume</span></span>    | <span data-ttu-id="0acdb-123">Contrôle général de l’atténuation du volume.</span><span class="sxs-lookup"><span data-stu-id="0acdb-123">General volume fade control.</span></span> <span data-ttu-id="0acdb-124">La plage de valeurs acceptables est comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="0acdb-124">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="0acdb-125">Pour plus d’informations sur la modification de cette plage, consultez la documentation de votre appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="0acdb-125">For information about changing this range, see the documentation for your mixer device.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="0acdb-126">Graves</span><span class="sxs-lookup"><span data-stu-id="0acdb-126">Bass</span></span>      | <span data-ttu-id="0acdb-127">Contrôle de fondu du volume de basses.</span><span class="sxs-lookup"><span data-stu-id="0acdb-127">Bass volume fade control.</span></span> <span data-ttu-id="0acdb-128">La plage de valeurs acceptables est comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="0acdb-128">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="0acdb-129">Les limites de la bande de fréquence des basses sont spécifiques au matériel.</span><span class="sxs-lookup"><span data-stu-id="0acdb-129">The limits of the bass frequency band are hardware specific.</span></span> <span data-ttu-id="0acdb-130">Pour plus d’informations sur les limites de bande, consultez la documentation de votre appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="0acdb-130">For information about band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="0acdb-131">Les aigus</span><span class="sxs-lookup"><span data-stu-id="0acdb-131">Treble</span></span>    | <span data-ttu-id="0acdb-132">Contrôle de fondu des volumes aigus.</span><span class="sxs-lookup"><span data-stu-id="0acdb-132">Treble volume fade control.</span></span> <span data-ttu-id="0acdb-133">La plage de valeurs acceptables est comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="0acdb-133">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="0acdb-134">Les limites de la bande de fréquence des aigus sont spécifiques au matériel.</span><span class="sxs-lookup"><span data-stu-id="0acdb-134">The limits of the treble frequency band are hardware specific.</span></span> <span data-ttu-id="0acdb-135">Pour plus d’informations sur les limites de bande, consultez la documentation de votre appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="0acdb-135">For information about the band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="0acdb-136">Equalizer</span><span class="sxs-lookup"><span data-stu-id="0acdb-136">Equalizer</span></span> | <span data-ttu-id="0acdb-137">Contrôle d’égaliseur graphique.</span><span class="sxs-lookup"><span data-stu-id="0acdb-137">Graphic equalizer control.</span></span> <span data-ttu-id="0acdb-138">La plage de valeurs acceptables pour une bande de l’égaliseur est comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="0acdb-138">The range of acceptable values for one band of the equalizer is 0 through 65,535.</span></span> <span data-ttu-id="0acdb-139">Le nombre de bandes d’égaliseur et leurs limites sont spécifiques au matériel.</span><span class="sxs-lookup"><span data-stu-id="0acdb-139">The number of equalizer bands and their limits are hardware specific.</span></span> <span data-ttu-id="0acdb-140">Pour plus d’informations sur l’égaliseur, consultez la documentation de votre appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="0acdb-140">For information about the equalizer, see the documentation for your mixer device.</span></span> <span data-ttu-id="0acdb-141">Vous pouvez utiliser la structure [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) pour récupérer des étiquettes de texte pour l’égaliseur.</span><span class="sxs-lookup"><span data-stu-id="0acdb-141">You can use the [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure to retrieve text labels for the equalizer.</span></span> |



 

 

 