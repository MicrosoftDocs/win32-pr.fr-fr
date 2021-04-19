---
description: ICE10 vérifie que l’état de publication des fonctionnalités enfants correspond à celui de sa fonctionnalité parente.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521810"
---
# <a name="ice10"></a><span data-ttu-id="fdd0e-103">ICE10</span><span class="sxs-lookup"><span data-stu-id="fdd0e-103">ICE10</span></span>

<span data-ttu-id="fdd0e-104">ICE10 vérifie que l’état de publication des fonctionnalités enfants correspond à celui de sa fonctionnalité parente.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-104">ICE10 validates that the advertise state of child features matches that of its parent feature.</span></span>

<span data-ttu-id="fdd0e-105">Une fonctionnalité enfant peut ne pas autoriser la publication pendant que sa fonctionnalité parente autorise la publication.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-105">A child feature may not disallow advertisement while its parent feature allows advertisement.</span></span> <span data-ttu-id="fdd0e-106">La combinaison suivante d’attributs parents et enfants n’est donc pas valide.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-106">The following combination of parent and child attributes is therefore invalid.</span></span>

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

<span data-ttu-id="fdd0e-107">Cette combinaison n’est pas valide, car elle désactive le parent chaque fois que le parent était supposé être publié.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-107">This combination is invalid because it would turn off the parent whenever the parent was supposed to be advertised.</span></span> <span data-ttu-id="fdd0e-108">Toutefois, l’inverse est autorisé.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-108">However, the reverse is allowed.</span></span> <span data-ttu-id="fdd0e-109">Un enfant peut être marqué pour favoriser la publication tandis que le parent est marqué pour interdire la publication.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-109">A child can be marked to favor advertisement while the parent is marked to disallow advertisement.</span></span>

<span data-ttu-id="fdd0e-110">L’action personnalisée ICE10 détermine l’état des fonctionnalités parent et enfant à partir de la colonne attributs du tableau des [fonctionnalités](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fdd0e-110">The ICE10 custom action determines the state of parent and child features from the Attributes column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="fdd0e-111">Notez qu’il est possible d’affecter la valeur 0 à l’état d’une fonctionnalité et de faire en sorte que son parent ou enfant soit configuré pour privilégier ou interdire la publication.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-111">Note that it is valid to set the state of a feature to 0 and have its parent or child set to favor or disallow advertisement.</span></span>

## <a name="result"></a><span data-ttu-id="fdd0e-112">Résultats</span><span class="sxs-lookup"><span data-stu-id="fdd0e-112">Result</span></span>

<span data-ttu-id="fdd0e-113">ICE10 publie une erreur si la colonne attributs du tableau des [fonctionnalités](feature-table.md) contient une incompatibilité dans l’état de publication.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-113">ICE10 posts an error if the Attributes column of the [Feature](feature-table.md) table contains a mismatch in the advertise state.</span></span>

## <a name="example"></a><span data-ttu-id="fdd0e-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="fdd0e-114">Example</span></span>

<span data-ttu-id="fdd0e-115">ICE10 publie le message d’erreur suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-115">ICE10 posts the following error message for the example shown.</span></span>

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

<span data-ttu-id="fdd0e-116">Remarque pour cet exemple, Microsoft Excel et Microsoft Word sont des fonctionnalités enfants de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-116">Note for this example that Microsoft Excel and Microsoft Word are child features of Microsoft Office.</span></span>

<span data-ttu-id="fdd0e-117">Table des [fonctionnalités](feature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="fdd0e-117">[Feature](feature-table.md) table (partial)</span></span>



| <span data-ttu-id="fdd0e-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="fdd0e-118">Feature</span></span> | <span data-ttu-id="fdd0e-119">Parent de la fonctionnalité \_</span><span class="sxs-lookup"><span data-stu-id="fdd0e-119">Feature\_Parent</span></span> | <span data-ttu-id="fdd0e-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="fdd0e-120">Attributes</span></span> |
|---------|-----------------|------------|
| <span data-ttu-id="fdd0e-121">Office</span><span class="sxs-lookup"><span data-stu-id="fdd0e-121">Office</span></span>  | <span data-ttu-id="fdd0e-122">Null</span><span class="sxs-lookup"><span data-stu-id="fdd0e-122">Null</span></span>            | <span data-ttu-id="fdd0e-123">4</span><span class="sxs-lookup"><span data-stu-id="fdd0e-123">4</span></span>          |
| <span data-ttu-id="fdd0e-124">Excel</span><span class="sxs-lookup"><span data-stu-id="fdd0e-124">Excel</span></span>   | <span data-ttu-id="fdd0e-125">Office</span><span class="sxs-lookup"><span data-stu-id="fdd0e-125">Office</span></span>          | <span data-ttu-id="fdd0e-126">4</span><span class="sxs-lookup"><span data-stu-id="fdd0e-126">4</span></span>          |
| <span data-ttu-id="fdd0e-127">Word</span><span class="sxs-lookup"><span data-stu-id="fdd0e-127">Word</span></span>    | <span data-ttu-id="fdd0e-128">Office</span><span class="sxs-lookup"><span data-stu-id="fdd0e-128">Office</span></span>          | <span data-ttu-id="fdd0e-129">8</span><span class="sxs-lookup"><span data-stu-id="fdd0e-129">8</span></span>          |



 

<span data-ttu-id="fdd0e-130">Dans l’exemple, Word est configuré pour ne pas autoriser la publication, ce qui est en conflit avec l’état d’autorisation de publication de son parent, Office.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-130">In the example, Word is set to disallow advertisement, which conflicts with the allow advertisement state of its parent, Office.</span></span>

<span data-ttu-id="fdd0e-131">Dans certains cas, ICE10 publie l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="fdd0e-131">In some cases ICE10 posts the following error:</span></span>

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

<span data-ttu-id="fdd0e-132">Cela fait référence à une référence de clé étrangère non valide.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-132">This refers to an invalid foreign key reference.</span></span> <span data-ttu-id="fdd0e-133">Le correctif consiste à avoir le point « enfant » sur sa fonctionnalité parente correcte, ou à ajouter une entrée pour la fonctionnalité parente « parent » à la table des [fonctionnalités](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fdd0e-133">The fix is to have 'Child' point to its correct parent feature, or add an entry for the parent feature 'Parent' to the [Feature](feature-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdd0e-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fdd0e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdd0e-135">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="fdd0e-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



