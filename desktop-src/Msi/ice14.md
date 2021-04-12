---
description: ICE14 valide la table des fonctionnalités d’une base de données Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319506"
---
# <a name="ice14"></a><span data-ttu-id="8f499-103">ICE14</span><span class="sxs-lookup"><span data-stu-id="8f499-103">ICE14</span></span>

<span data-ttu-id="8f499-104">ICE14 valide les éléments suivants pour les fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="8f499-104">ICE14 validates the following for features:</span></span>

-   <span data-ttu-id="8f499-105">Pour les fonctionnalités parentes racine, le bit msidbFeatureAttributesFollowParent n’est pas défini dans la colonne attributs du [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f499-105">That root parent features do not have the msidbFeatureAttributesFollowParent bit set in the Attributes column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="8f499-106">Une fonctionnalité racine n’a pas de parent.</span><span class="sxs-lookup"><span data-stu-id="8f499-106">A root feature does not have a parent.</span></span>
-   <span data-ttu-id="8f499-107">Cette fonctionnalité n’a pas la même entrée dans les colonnes parentes Feature et Feature \_ de la [table Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f499-107">That no feature has the same entry in the Feature and Feature\_Parent columns of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="8f499-108">Aucune fonctionnalité ne peut être son propre parent.</span><span class="sxs-lookup"><span data-stu-id="8f499-108">No feature can be its own parent.</span></span>

## <a name="result"></a><span data-ttu-id="8f499-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="8f499-109">Result</span></span>

<span data-ttu-id="8f499-110">ICE14 publie un message d’erreur s’il trouve une fonctionnalité racine avec l’ensemble de bits msidbFeatureAttributesFollowParent ou une fonctionnalité avec des entrées identiques dans les \_ colonnes parentes de fonctionnalité et de fonctionnalité de la table des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="8f499-110">ICE14 posts an error message if it finds a root feature with the msidbFeatureAttributesFollowParent bit set or a feature with identical entries in the Feature and Feature\_Parent columns of the Feature table.</span></span>

## <a name="example"></a><span data-ttu-id="8f499-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f499-111">Example</span></span>

<span data-ttu-id="8f499-112">ICE14 retournerait les erreurs suivantes pour l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="8f499-112">ICE14 would return the following errors for the following example:</span></span>

-   <span data-ttu-id="8f499-113">La fonctionnalité sport a la même valeur dans les colonnes parentes Feature et Feature \_ de la table file.</span><span class="sxs-lookup"><span data-stu-id="8f499-113">The feature Sport has the same value in the Feature and Feature\_Parent columns of the File table.</span></span>
-   <span data-ttu-id="8f499-114">La fonctionnalité racine sport a le bit msidbFeatureAttributesFollowParent défini.</span><span class="sxs-lookup"><span data-stu-id="8f499-114">The root feature Sport has the msidbFeatureAttributesFollowParent bit set.</span></span>

<span data-ttu-id="8f499-115">Dans l’arborescence des fonctionnalités de cet exemple, sport est la fonctionnalité racine et un parent des fonctionnalités de la natation et du football.</span><span class="sxs-lookup"><span data-stu-id="8f499-115">In the feature tree of this example, Sport is the root feature and a parent of the Swimming and Football features.</span></span> <span data-ttu-id="8f499-116">Freestyle est une fonctionnalité enfant de la natation.</span><span class="sxs-lookup"><span data-stu-id="8f499-116">Freestyle is a child feature of Swimming.</span></span> <span data-ttu-id="8f499-117">TouchFootball est une fonctionnalité enfant du football.</span><span class="sxs-lookup"><span data-stu-id="8f499-117">TouchFootball is a child feature of Football.</span></span>

<span data-ttu-id="8f499-118">[Table des fonctionnalités](feature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="8f499-118">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="8f499-119">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="8f499-119">Feature</span></span>       | <span data-ttu-id="8f499-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="8f499-120">Attributes</span></span> | <span data-ttu-id="8f499-121">Parent de la fonctionnalité \_</span><span class="sxs-lookup"><span data-stu-id="8f499-121">Feature\_Parent</span></span> |
|---------------|------------|-----------------|
| <span data-ttu-id="8f499-122">Sport</span><span class="sxs-lookup"><span data-stu-id="8f499-122">Sport</span></span>         | <span data-ttu-id="8f499-123">4</span><span class="sxs-lookup"><span data-stu-id="8f499-123">4</span></span>          | <span data-ttu-id="8f499-124">Sport</span><span class="sxs-lookup"><span data-stu-id="8f499-124">Sport</span></span>           |
| <span data-ttu-id="8f499-125">Nage</span><span class="sxs-lookup"><span data-stu-id="8f499-125">Swimming</span></span>      | <span data-ttu-id="8f499-126">1</span><span class="sxs-lookup"><span data-stu-id="8f499-126">1</span></span>          | <span data-ttu-id="8f499-127">Sport</span><span class="sxs-lookup"><span data-stu-id="8f499-127">Sport</span></span>           |
| <span data-ttu-id="8f499-128">Terrain</span><span class="sxs-lookup"><span data-stu-id="8f499-128">Football</span></span>      | <span data-ttu-id="8f499-129">4</span><span class="sxs-lookup"><span data-stu-id="8f499-129">4</span></span>          | <span data-ttu-id="8f499-130">Sport</span><span class="sxs-lookup"><span data-stu-id="8f499-130">Sport</span></span>           |
| <span data-ttu-id="8f499-131">Freestyle</span><span class="sxs-lookup"><span data-stu-id="8f499-131">Freestyle</span></span>     | <span data-ttu-id="8f499-132">1</span><span class="sxs-lookup"><span data-stu-id="8f499-132">1</span></span>          | <span data-ttu-id="8f499-133">Nage</span><span class="sxs-lookup"><span data-stu-id="8f499-133">Swimming</span></span>        |
| <span data-ttu-id="8f499-134">TouchFootball</span><span class="sxs-lookup"><span data-stu-id="8f499-134">TouchFootball</span></span> | <span data-ttu-id="8f499-135">4</span><span class="sxs-lookup"><span data-stu-id="8f499-135">4</span></span>          | <span data-ttu-id="8f499-136">Terrain</span><span class="sxs-lookup"><span data-stu-id="8f499-136">Football</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8f499-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f499-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f499-138">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="8f499-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



