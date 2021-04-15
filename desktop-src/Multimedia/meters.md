---
title: Mètres
description: Mètres
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- mixages audio, contrôles
- mixages audio, mètres
- mélangeurs, contrôles
- mélangeurs, mètres
- contrôles de compteur
- Structure MIXERCONTROLDETAILS_BOOLEAN
- Structure MIXERCONTROLDETAILS_SIGNED
- Structure MIXERCONTROLDETAILS_UNSIGNED
- Contrôle booléen
- contrôle de pointe
- contrôle signé
- contrôle non signé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463143"
---
# <a name="meters"></a><span data-ttu-id="3f229-115">Mètres</span><span class="sxs-lookup"><span data-stu-id="3f229-115">Meters</span></span>

<span data-ttu-id="3f229-116">Le compteur contrôle les données de mesure en passant par une ligne audio.</span><span class="sxs-lookup"><span data-stu-id="3f229-116">The meter controls measure data passing through an audio line.</span></span> <span data-ttu-id="3f229-117">Ces contrôles utilisent les structures [**MIXERCONTROLDETAILS \_ Boolean**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS \_ signed**](/previous-versions//dd757297(v=vs.85))et [**MIXERCONTROLDETAILS \_ non signées**](/previous-versions//dd757298(v=vs.85)) pour récupérer et définir des propriétés de contrôle.</span><span class="sxs-lookup"><span data-stu-id="3f229-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)), and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="3f229-118">Le tableau suivant décrit les types de compteurs.</span><span class="sxs-lookup"><span data-stu-id="3f229-118">The following table describes the types of meters.</span></span>



| <span data-ttu-id="3f229-119">Contrôler</span><span class="sxs-lookup"><span data-stu-id="3f229-119">Control</span></span>  | <span data-ttu-id="3f229-120">Description</span><span class="sxs-lookup"><span data-stu-id="3f229-120">Description</span></span>                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f229-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="3f229-121">Boolean</span></span>  | <span data-ttu-id="3f229-122">Mesure si une valeur entière est FALSe/OFF (zéro) ou TRUE/ON (valeur différente de zéro).</span><span class="sxs-lookup"><span data-stu-id="3f229-122">Measures whether an integer value is FALSE/OFF (zero) or TRUE/ON (nonzero).</span></span>                                                                            |
| <span data-ttu-id="3f229-123">Peak</span><span class="sxs-lookup"><span data-stu-id="3f229-123">Peak</span></span>     | <span data-ttu-id="3f229-124">Mesure la déviation de 0 dans les directions positive et négative.</span><span class="sxs-lookup"><span data-stu-id="3f229-124">Measures the deflection from 0 in both the positive and negative directions.</span></span> <span data-ttu-id="3f229-125">La plage de valeurs entières pour le compteur de pic est comprise entre – 32 768 et 32 767.</span><span class="sxs-lookup"><span data-stu-id="3f229-125">The range of integer values for the peak meter is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="3f229-126">Signé</span><span class="sxs-lookup"><span data-stu-id="3f229-126">Signed</span></span>   | <span data-ttu-id="3f229-127">Mesure les valeurs entières dans la plage comprise entre – 231 et (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="3f229-127">Measures integer values in the range of –231 through (231 – 1).</span></span> <span data-ttu-id="3f229-128">Le pilote de mixage définit les limites de ce compteur.</span><span class="sxs-lookup"><span data-stu-id="3f229-128">The mixer driver defines the limits of this meter.</span></span>                                     |
| <span data-ttu-id="3f229-129">Non signé</span><span class="sxs-lookup"><span data-stu-id="3f229-129">Unsigned</span></span> | <span data-ttu-id="3f229-130">Mesure les valeurs entières dans la plage comprise entre 0 et (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="3f229-130">Measures integer values in the range of 0 through (232 – 1).</span></span> <span data-ttu-id="3f229-131">Le pilote de mixage définit les limites de ce compteur.</span><span class="sxs-lookup"><span data-stu-id="3f229-131">The mixer driver defines the limits of this meter.</span></span>                                        |



 

 

 