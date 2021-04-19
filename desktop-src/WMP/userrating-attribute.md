---
title: Attribut UserRating
description: L’attribut UserRating est l’évaluation spécifiée par l’utilisateur dans la bibliothèque.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Attribut UserRating lecteur Windows Media
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545326"
---
# <a name="userrating-attribute"></a><span data-ttu-id="c15f8-104">Attribut UserRating</span><span class="sxs-lookup"><span data-stu-id="c15f8-104">UserRating Attribute</span></span>

<span data-ttu-id="c15f8-105">L’attribut **UserRating** est l’évaluation spécifiée par l’utilisateur dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c15f8-105">The **UserRating** attribute is the rating specified by the user in the library.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c15f8-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="c15f8-106">Applies To</span></span>

-   [<span data-ttu-id="c15f8-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="c15f8-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="c15f8-108">Autres éléments</span><span class="sxs-lookup"><span data-stu-id="c15f8-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="c15f8-109">Éléments de photo</span><span class="sxs-lookup"><span data-stu-id="c15f8-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="c15f8-110">Sélections</span><span class="sxs-lookup"><span data-stu-id="c15f8-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="c15f8-111">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="c15f8-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="c15f8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c15f8-112">Remarks</span></span>

<span data-ttu-id="c15f8-113">Les évaluations des utilisateurs sont représentées par des valeurs entières, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c15f8-113">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="c15f8-114">Quand vous spécifiez une valeur, utilisez l’une des valeurs de la colonne valeur d’écriture.</span><span class="sxs-lookup"><span data-stu-id="c15f8-114">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="c15f8-115">Lorsque vous récupérez des valeurs, vous pouvez utiliser les plages de la colonne lecture des valeurs pour déterminer le nombre d’étoiles.</span><span class="sxs-lookup"><span data-stu-id="c15f8-115">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="c15f8-116">Rating</span><span class="sxs-lookup"><span data-stu-id="c15f8-116">Rating</span></span>  | <span data-ttu-id="c15f8-117">Valeur d’écriture</span><span class="sxs-lookup"><span data-stu-id="c15f8-117">Writing value</span></span> | <span data-ttu-id="c15f8-118">Lecture des valeurs</span><span class="sxs-lookup"><span data-stu-id="c15f8-118">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="c15f8-119">Absence</span><span class="sxs-lookup"><span data-stu-id="c15f8-119">Unrated</span></span> | <span data-ttu-id="c15f8-120">0</span><span class="sxs-lookup"><span data-stu-id="c15f8-120">0</span></span>             | <span data-ttu-id="c15f8-121">0</span><span class="sxs-lookup"><span data-stu-id="c15f8-121">0</span></span>              |
| <span data-ttu-id="c15f8-122">1 étoile</span><span class="sxs-lookup"><span data-stu-id="c15f8-122">1 star</span></span>  | <span data-ttu-id="c15f8-123">1</span><span class="sxs-lookup"><span data-stu-id="c15f8-123">1</span></span>             | <span data-ttu-id="c15f8-124">1 à 12</span><span class="sxs-lookup"><span data-stu-id="c15f8-124">1 to 12</span></span>        |
| <span data-ttu-id="c15f8-125">2 étoiles</span><span class="sxs-lookup"><span data-stu-id="c15f8-125">2 stars</span></span> | <span data-ttu-id="c15f8-126">25</span><span class="sxs-lookup"><span data-stu-id="c15f8-126">25</span></span>            | <span data-ttu-id="c15f8-127">13 à 37</span><span class="sxs-lookup"><span data-stu-id="c15f8-127">13 to 37</span></span>       |
| <span data-ttu-id="c15f8-128">3 étoiles</span><span class="sxs-lookup"><span data-stu-id="c15f8-128">3 stars</span></span> | <span data-ttu-id="c15f8-129">50</span><span class="sxs-lookup"><span data-stu-id="c15f8-129">50</span></span>            | <span data-ttu-id="c15f8-130">38 à 62</span><span class="sxs-lookup"><span data-stu-id="c15f8-130">38 to 62</span></span>       |
| <span data-ttu-id="c15f8-131">4 étoiles</span><span class="sxs-lookup"><span data-stu-id="c15f8-131">4 stars</span></span> | <span data-ttu-id="c15f8-132">75</span><span class="sxs-lookup"><span data-stu-id="c15f8-132">75</span></span>            | <span data-ttu-id="c15f8-133">63 à 86</span><span class="sxs-lookup"><span data-stu-id="c15f8-133">63 to 86</span></span>       |
| <span data-ttu-id="c15f8-134">5 étoiles</span><span class="sxs-lookup"><span data-stu-id="c15f8-134">5 stars</span></span> | <span data-ttu-id="c15f8-135">99</span><span class="sxs-lookup"><span data-stu-id="c15f8-135">99</span></span>            | <span data-ttu-id="c15f8-136">87 à 99</span><span class="sxs-lookup"><span data-stu-id="c15f8-136">87 to 99</span></span>       |



 

<span data-ttu-id="c15f8-137">Cet attribut est stocké uniquement dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c15f8-137">This attribute is stored only in the library.</span></span>

<span data-ttu-id="c15f8-138">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c15f8-138">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15f8-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c15f8-139">Requirements</span></span>



| <span data-ttu-id="c15f8-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c15f8-140">Requirement</span></span> | <span data-ttu-id="c15f8-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="c15f8-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c15f8-142">Version</span><span class="sxs-lookup"><span data-stu-id="c15f8-142">Version</span></span><br/> | <span data-ttu-id="c15f8-143">Lecteur Windows Media série 9 ou version ultérieure (l’élément photo est pris en charge uniquement dans le lecteur Windows Media 10 ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="c15f8-143">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c15f8-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c15f8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15f8-145">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="c15f8-145">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





