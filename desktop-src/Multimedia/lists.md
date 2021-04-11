---
title: Listes
description: Listes
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- mixages audio, contrôles
- mixages audio, listes
- mélangeurs, contrôles
- mélangeurs, listes
- contrôles de liste
- Structure MIXERCONTROLDETAILS_BOOLEAN
- Structure MIXERCONTROLDETAILS_LISTTEXT
- contrôle à sélection unique
- contrôle à sélection multiple
- contrôle mixer
- multiplexeur (multiplexeur)
- MUX (multiplexeur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314778"
---
# <a name="lists"></a><span data-ttu-id="62a19-115">Listes</span><span class="sxs-lookup"><span data-stu-id="62a19-115">Lists</span></span>

<span data-ttu-id="62a19-116">Les contrôles de liste fournissent des États à sélection unique ou à sélection multiple pour les lignes audio complexes.</span><span class="sxs-lookup"><span data-stu-id="62a19-116">The list controls provide single-select or multiple-select states for complex audio lines.</span></span> <span data-ttu-id="62a19-117">Ces contrôles utilisent la [**structure \_ booléenne MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) pour récupérer et définir des propriétés de contrôle.</span><span class="sxs-lookup"><span data-stu-id="62a19-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="62a19-118">La structure [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) est également utilisée pour récupérer toutes les descriptions textuelles d’un contrôle à plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="62a19-118">The [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure is also used to retrieve all text descriptions of a multiple-item control.</span></span> <span data-ttu-id="62a19-119">Le tableau suivant décrit les types de contrôles de liste.</span><span class="sxs-lookup"><span data-stu-id="62a19-119">The following table describes the types of list controls.</span></span>



| <span data-ttu-id="62a19-120">Contrôler</span><span class="sxs-lookup"><span data-stu-id="62a19-120">Control</span></span>           | <span data-ttu-id="62a19-121">Description</span><span class="sxs-lookup"><span data-stu-id="62a19-121">Description</span></span>                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a19-122">Sélection simple</span><span class="sxs-lookup"><span data-stu-id="62a19-122">Single-select</span></span>     | <span data-ttu-id="62a19-123">Limite la sélection de contrôle à un élément à la fois.</span><span class="sxs-lookup"><span data-stu-id="62a19-123">Restricts the control selection to one item at a time.</span></span> <span data-ttu-id="62a19-124">Contrairement au contrôle multiplexeur, ce contrôle peut être utilisé pour contrôler plus que les lignes de la source audio.</span><span class="sxs-lookup"><span data-stu-id="62a19-124">Unlike the multiplexer control, this control can be used to control more than audio source lines.</span></span> <span data-ttu-id="62a19-125">Par exemple, vous pouvez utiliser ce contrôle pour sélectionner un filtre à passage faible dans une liste de filtres pris en charge par un appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="62a19-125">For example, you could use this control to select a low-pass filter from a list of filters supported by a mixer device.</span></span> |
| <span data-ttu-id="62a19-126">Multiplexeur (multiplexeur)</span><span class="sxs-lookup"><span data-stu-id="62a19-126">Multiplexer (MUX)</span></span> | <span data-ttu-id="62a19-127">Limite la sélection de ligne à une ligne source à la fois.</span><span class="sxs-lookup"><span data-stu-id="62a19-127">Restricts the line selection to one source line at a time.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="62a19-128">Sélection multiple</span><span class="sxs-lookup"><span data-stu-id="62a19-128">Multiple-select</span></span>   | <span data-ttu-id="62a19-129">Permet à l’utilisateur de sélectionner simultanément plusieurs éléments dans une liste.</span><span class="sxs-lookup"><span data-stu-id="62a19-129">Allows the user to select multiple items from a list simultaneously.</span></span> <span data-ttu-id="62a19-130">Contrairement au contrôle mixer, le contrôle à sélection multiple peut être utilisé pour contrôler plus que les lignes de la source audio.</span><span class="sxs-lookup"><span data-stu-id="62a19-130">Unlike the mixer control, the multiple-select control can be used to control more than audio source lines.</span></span>                                                                                                  |
| <span data-ttu-id="62a19-131">Mixer</span><span class="sxs-lookup"><span data-stu-id="62a19-131">Mixer</span></span>             | <span data-ttu-id="62a19-132">Permet à l’utilisateur de sélectionner des lignes sources dans une liste simultanément.</span><span class="sxs-lookup"><span data-stu-id="62a19-132">Allows the user to select source lines from a list simultaneously.</span></span>                                                                                                                                                                                                               |



 

 

 