---
title: Attribut UserEffectiveRating
description: L’attribut UserEffectiveRating est l’évaluation calculée par le lecteur Windows Media en fonction de la fréquence à laquelle l’élément a été lu.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Attribut UserEffectiveRating lecteur Windows Media
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540367"
---
# <a name="usereffectiverating-attribute"></a><span data-ttu-id="1ed66-104">Attribut UserEffectiveRating</span><span class="sxs-lookup"><span data-stu-id="1ed66-104">UserEffectiveRating Attribute</span></span>

<span data-ttu-id="1ed66-105">L’attribut **UserEffectiveRating** est l’évaluation calculée par le lecteur Windows Media en fonction de la fréquence à laquelle l’élément a été lu.</span><span class="sxs-lookup"><span data-stu-id="1ed66-105">The **UserEffectiveRating** attribute is the rating computed by Windows Media Player based on how often the item has been played.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1ed66-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="1ed66-106">Applies To</span></span>

-   [<span data-ttu-id="1ed66-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="1ed66-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="1ed66-108">Autres éléments</span><span class="sxs-lookup"><span data-stu-id="1ed66-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="1ed66-109">Sélections</span><span class="sxs-lookup"><span data-stu-id="1ed66-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="1ed66-110">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="1ed66-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1ed66-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1ed66-111">Remarks</span></span>

<span data-ttu-id="1ed66-112">Les évaluations des utilisateurs sont représentées par des valeurs entières, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1ed66-112">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="1ed66-113">Quand vous spécifiez une valeur, utilisez l’une des valeurs de la colonne valeur d’écriture.</span><span class="sxs-lookup"><span data-stu-id="1ed66-113">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="1ed66-114">Lorsque vous récupérez des valeurs, vous pouvez utiliser les plages de la colonne lecture des valeurs pour déterminer le nombre d’étoiles.</span><span class="sxs-lookup"><span data-stu-id="1ed66-114">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="1ed66-115">Rating</span><span class="sxs-lookup"><span data-stu-id="1ed66-115">Rating</span></span>  | <span data-ttu-id="1ed66-116">Valeur d’écriture</span><span class="sxs-lookup"><span data-stu-id="1ed66-116">Writing value</span></span> | <span data-ttu-id="1ed66-117">Lecture des valeurs</span><span class="sxs-lookup"><span data-stu-id="1ed66-117">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="1ed66-118">Absence</span><span class="sxs-lookup"><span data-stu-id="1ed66-118">Unrated</span></span> | <span data-ttu-id="1ed66-119">0</span><span class="sxs-lookup"><span data-stu-id="1ed66-119">0</span></span>             | <span data-ttu-id="1ed66-120">0</span><span class="sxs-lookup"><span data-stu-id="1ed66-120">0</span></span>              |
| <span data-ttu-id="1ed66-121">1 étoile</span><span class="sxs-lookup"><span data-stu-id="1ed66-121">1 star</span></span>  | <span data-ttu-id="1ed66-122">1</span><span class="sxs-lookup"><span data-stu-id="1ed66-122">1</span></span>             | <span data-ttu-id="1ed66-123">1 à 12</span><span class="sxs-lookup"><span data-stu-id="1ed66-123">1 to 12</span></span>        |
| <span data-ttu-id="1ed66-124">2 étoiles</span><span class="sxs-lookup"><span data-stu-id="1ed66-124">2 stars</span></span> | <span data-ttu-id="1ed66-125">25</span><span class="sxs-lookup"><span data-stu-id="1ed66-125">25</span></span>            | <span data-ttu-id="1ed66-126">13 à 37</span><span class="sxs-lookup"><span data-stu-id="1ed66-126">13 to 37</span></span>       |
| <span data-ttu-id="1ed66-127">3 étoiles</span><span class="sxs-lookup"><span data-stu-id="1ed66-127">3 stars</span></span> | <span data-ttu-id="1ed66-128">50</span><span class="sxs-lookup"><span data-stu-id="1ed66-128">50</span></span>            | <span data-ttu-id="1ed66-129">38 à 62</span><span class="sxs-lookup"><span data-stu-id="1ed66-129">38 to 62</span></span>       |
| <span data-ttu-id="1ed66-130">4 étoiles</span><span class="sxs-lookup"><span data-stu-id="1ed66-130">4 stars</span></span> | <span data-ttu-id="1ed66-131">75</span><span class="sxs-lookup"><span data-stu-id="1ed66-131">75</span></span>            | <span data-ttu-id="1ed66-132">63 à 86</span><span class="sxs-lookup"><span data-stu-id="1ed66-132">63 to 86</span></span>       |
| <span data-ttu-id="1ed66-133">5 étoiles</span><span class="sxs-lookup"><span data-stu-id="1ed66-133">5 stars</span></span> | <span data-ttu-id="1ed66-134">99</span><span class="sxs-lookup"><span data-stu-id="1ed66-134">99</span></span>            | <span data-ttu-id="1ed66-135">87 à 99</span><span class="sxs-lookup"><span data-stu-id="1ed66-135">87 to 99</span></span>       |



 

<span data-ttu-id="1ed66-136">Cet attribut est stocké uniquement dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1ed66-136">This attribute is stored only in the library.</span></span>

<span data-ttu-id="1ed66-137">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1ed66-137">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed66-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ed66-138">Requirements</span></span>



| <span data-ttu-id="1ed66-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ed66-139">Requirement</span></span> | <span data-ttu-id="1ed66-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ed66-140">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1ed66-141">Version</span><span class="sxs-lookup"><span data-stu-id="1ed66-141">Version</span></span><br/> | <span data-ttu-id="1ed66-142">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1ed66-142">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ed66-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ed66-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed66-144">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="1ed66-144">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





