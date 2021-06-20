---
title: Vue d’ensemble des manipulations avancées
description: Lisez une présentation graphique des manipulations avancées pour les applications. En savoir plus sur l’expansion, la rotation et la traduction.
ms.assetid: a0c3fecb-d3c7-4f12-90be-5f77f4f5883e
keywords:
- Tactile Windows, manipulations
- Tactile Windows, manipulations avancées
- Tactile Windows, manipulations complexes
- Tactile Windows, expansion
- Windows Touch, développement avancé
- Tactile Windows, rotation
- Tactile Windows, rotation avancée
- Tactile Windows, traduction
- Tactile Windows, traduction avancée
- manipulations, avancées
- manipulations, complexes
- manipulations, expansion
- manipulations, expansion avancée
- manipulations, rotation
- manipulations, rotation avancée
- manipulations, traduction
- manipulations, traduction avancée
- expansion, avancé
- rotation, avancé
- traduction, avancé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04dea220c213de75820075c9375a04e1800a880d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406332"
---
# <a name="advanced-manipulations-overview"></a><span data-ttu-id="0b355-124">Vue d’ensemble des manipulations avancées</span><span class="sxs-lookup"><span data-stu-id="0b355-124">Advanced Manipulations Overview</span></span>

<span data-ttu-id="0b355-125">Cette section décrit les manipulations avancées pour les applications.</span><span class="sxs-lookup"><span data-stu-id="0b355-125">This section explains advanced manipulations for applications.</span></span>

<span data-ttu-id="0b355-126">À des fins de convivialité, vous souhaiterez peut-être ajouter des manipulations complexes à votre application afin que les objets puissent être manipulés avec un degré de granularité précis.</span><span class="sxs-lookup"><span data-stu-id="0b355-126">For usability purposes, you may want to add complex manipulations to your application so that objects can be manipulated with a fine degree of granularity.</span></span> <span data-ttu-id="0b355-127">Les sections suivantes décrivent les manipulations avancées.</span><span class="sxs-lookup"><span data-stu-id="0b355-127">The following sections describe advanced manipulations.</span></span>

### <a name="advanced-expansion"></a><span data-ttu-id="0b355-128">Expansion avancée</span><span class="sxs-lookup"><span data-stu-id="0b355-128">Advanced Expansion</span></span>

<span data-ttu-id="0b355-129">L’illustration suivante montre deux interprétations de l’expansion.</span><span class="sxs-lookup"><span data-stu-id="0b355-129">The following illustration shows two interpretations of expansion.</span></span>

![Illustration montrant une expansion simple autour du point central d’un objet et une expansion avancée autour du point central de la manipulation](images/expansion.png)

<span data-ttu-id="0b355-131">Dans l’exemple A, l’exemple d’expansion simple, l’objet est développé autour de son point central.</span><span class="sxs-lookup"><span data-stu-id="0b355-131">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="0b355-132">Dans l’exemple B, l’objet est développé autour du point central de la manipulation.</span><span class="sxs-lookup"><span data-stu-id="0b355-132">In example B, the object is expanded around the center point of the manipulation.</span></span>

### <a name="advanced-rotation"></a><span data-ttu-id="0b355-133">Rotation avancée</span><span class="sxs-lookup"><span data-stu-id="0b355-133">Advanced Rotation</span></span>

<span data-ttu-id="0b355-134">L’illustration suivante montre deux interprétations de la rotation.</span><span class="sxs-lookup"><span data-stu-id="0b355-134">The following illustration shows two interpretations of rotation.</span></span>

![Illustration montrant deux types de rotation à un seul doigt : autour du centre ou autour du bord, avec la périphérie qui implique à la fois la rotation et la translation](images/rotation.png)

<span data-ttu-id="0b355-136">Dans l’exemple A, l’exemple de rotation simple, l’objet pivote autour de son point central.</span><span class="sxs-lookup"><span data-stu-id="0b355-136">In example A, the simple rotation example, the object is rotated around its center point.</span></span> <span data-ttu-id="0b355-137">Dans l’exemple B, l’objet pivote autour du point central de la manipulation.</span><span class="sxs-lookup"><span data-stu-id="0b355-137">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="0b355-138">Pour plus d’informations sur la rotation complexe, consultez la section [rotation avancée](advanced-rotation.md) .</span><span class="sxs-lookup"><span data-stu-id="0b355-138">For more information on complex rotation, see the [Advanced Rotation](advanced-rotation.md) section.</span></span>

## <a name="advanced-translation"></a><span data-ttu-id="0b355-139">Traduction avancée</span><span class="sxs-lookup"><span data-stu-id="0b355-139">Advanced Translation</span></span>

<span data-ttu-id="0b355-140">L’illustration suivante montre deux interprétations de la traduction.</span><span class="sxs-lookup"><span data-stu-id="0b355-140">The following illustration shows two interpretations of translation.</span></span>

![Illustration montrant une translation simple, dans laquelle un objet est déplacé sans rotation, et une traduction avancée, qui implique un déplacement et une rotation](images/translation.png)

<span data-ttu-id="0b355-142">Dans l’exemple A, l’exemple de traduction simple, l’objet est déplacé sans rotation.</span><span class="sxs-lookup"><span data-stu-id="0b355-142">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="0b355-143">Dans l’exemple B, l’objet est pivoté pendant la traduction selon l’emplacement du point de contact de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0b355-143">In example B, the object is rotated during the translation depending on where the object contact point is.</span></span> <span data-ttu-id="0b355-144">Si vous activez la rotation à un seul doigt comme décrit dans [rotation à un seul doigt](single-finger-rotation.md), vous pouvez activer la traduction complexe.</span><span class="sxs-lookup"><span data-stu-id="0b355-144">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b355-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b355-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b355-146">Manipulations</span><span class="sxs-lookup"><span data-stu-id="0b355-146">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




