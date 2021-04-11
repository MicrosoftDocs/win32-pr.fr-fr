---
title: Nombres (Windows Multimedia)
description: Nombres
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- mixages audio, contrôles
- mixages audio, chiffres
- mélangeurs, contrôles
- mélangeurs, nombres
- contrôles Number
- Structure MIXERCONTROLDETAILS_SIGNED
- Structure MIXERCONTROLDETAILS_UNSIGNED
- contrôle décibel
- contrôle de pourcentage
- contrôle signé
- contrôle non signé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102672"
---
# <a name="numbers-windows-multimedia"></a><span data-ttu-id="d108a-114">Nombres (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="d108a-114">Numbers (Windows Multimedia)</span></span>

<span data-ttu-id="d108a-115">Les contrôles Number permettent à l’utilisateur d’entrer des données numériques associées à une ligne.</span><span class="sxs-lookup"><span data-stu-id="d108a-115">The number controls allow the user to enter numerical data associated with a line.</span></span> <span data-ttu-id="d108a-116">Les données numériques sont exprimées en tant qu’entiers signés, entiers non signés ou valeurs de décibels entières.</span><span class="sxs-lookup"><span data-stu-id="d108a-116">The numerical data is expressed as signed integers, unsigned integers, or integer decibel values.</span></span> <span data-ttu-id="d108a-117">Ces contrôles utilisent les structures [**\_ non signées**](/previous-versions//dd757298(v=vs.85)) [**MIXERCONTROLDETAILS \_ signées**](/previous-versions//dd757297(v=vs.85)) et MIXERCONTROLDETAILS pour récupérer et définir des propriétés de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d108a-117">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="d108a-118">Le tableau suivant décrit les types de contrôles Number.</span><span class="sxs-lookup"><span data-stu-id="d108a-118">The following table describes the types of number controls.</span></span>



| <span data-ttu-id="d108a-119">Contrôler</span><span class="sxs-lookup"><span data-stu-id="d108a-119">Control</span></span>  | <span data-ttu-id="d108a-120">Description</span><span class="sxs-lookup"><span data-stu-id="d108a-120">Description</span></span>                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d108a-121">Signé</span><span class="sxs-lookup"><span data-stu-id="d108a-121">Signed</span></span>   | <span data-ttu-id="d108a-122">Autorise les valeurs entières entrées dans la plage comprise entre – 231 et (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="d108a-122">Allows integer values entered in the range of – 231 through (231 –1).</span></span>                                                               |
| <span data-ttu-id="d108a-123">Non signé</span><span class="sxs-lookup"><span data-stu-id="d108a-123">Unsigned</span></span> | <span data-ttu-id="d108a-124">Autorise les valeurs entières entrées dans la plage comprise entre 0 et (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="d108a-124">Allows integer values entered in the range of 0 through (232 –1).</span></span>                                                                   |
| <span data-ttu-id="d108a-125">Décibel</span><span class="sxs-lookup"><span data-stu-id="d108a-125">Decibel</span></span>  | <span data-ttu-id="d108a-126">Permet d’entrer des valeurs entières de décibels, en dixièmes de décibels.</span><span class="sxs-lookup"><span data-stu-id="d108a-126">Allows integer decibel values to be entered, in tenths of decibels.</span></span> <span data-ttu-id="d108a-127">La plage de valeurs pour ce contrôle est comprise entre – 32 768 et 32 767.</span><span class="sxs-lookup"><span data-stu-id="d108a-127">The range of values for this control is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="d108a-128">Pourcentage</span><span class="sxs-lookup"><span data-stu-id="d108a-128">Percent</span></span>  | <span data-ttu-id="d108a-129">Permet d’entrer des valeurs sous forme de pourcentages.</span><span class="sxs-lookup"><span data-stu-id="d108a-129">Allows values to be entered as percentages.</span></span>                                                                                         |



 

 

 
