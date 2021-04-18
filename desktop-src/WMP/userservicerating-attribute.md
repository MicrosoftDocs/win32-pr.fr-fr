---
title: Attribut UserServiceRating
description: L’attribut UserServiceRating est réservé pour une utilisation ultérieure.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Attribut UserServiceRating lecteur Windows Media
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523012"
---
# <a name="userservicerating-attribute"></a><span data-ttu-id="d253d-104">Attribut UserServiceRating</span><span class="sxs-lookup"><span data-stu-id="d253d-104">UserServiceRating Attribute</span></span>

<span data-ttu-id="d253d-105">L’attribut **UserServiceRating** est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d253d-105">The **UserServiceRating** attribute is reserved for future use.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d253d-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="d253d-106">Applies To</span></span>

-   [<span data-ttu-id="d253d-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="d253d-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="d253d-108">Sélections</span><span class="sxs-lookup"><span data-stu-id="d253d-108">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="d253d-109">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="d253d-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="d253d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d253d-110">Remarks</span></span>

<span data-ttu-id="d253d-111">Les évaluations des utilisateurs sont représentées par des valeurs entières, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d253d-111">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="d253d-112">Quand vous spécifiez une valeur, utilisez l’une des valeurs de la colonne valeur d’écriture.</span><span class="sxs-lookup"><span data-stu-id="d253d-112">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="d253d-113">Lorsque vous récupérez des valeurs, vous pouvez utiliser les plages de la colonne lecture des valeurs pour déterminer le nombre d’étoiles.</span><span class="sxs-lookup"><span data-stu-id="d253d-113">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="d253d-114">Rating</span><span class="sxs-lookup"><span data-stu-id="d253d-114">Rating</span></span>  | <span data-ttu-id="d253d-115">Valeur d’écriture</span><span class="sxs-lookup"><span data-stu-id="d253d-115">Writing value</span></span> | <span data-ttu-id="d253d-116">Lecture des valeurs</span><span class="sxs-lookup"><span data-stu-id="d253d-116">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="d253d-117">Absence</span><span class="sxs-lookup"><span data-stu-id="d253d-117">Unrated</span></span> | <span data-ttu-id="d253d-118">0</span><span class="sxs-lookup"><span data-stu-id="d253d-118">0</span></span>             | <span data-ttu-id="d253d-119">0</span><span class="sxs-lookup"><span data-stu-id="d253d-119">0</span></span>              |
| <span data-ttu-id="d253d-120">1 étoile</span><span class="sxs-lookup"><span data-stu-id="d253d-120">1 star</span></span>  | <span data-ttu-id="d253d-121">1</span><span class="sxs-lookup"><span data-stu-id="d253d-121">1</span></span>             | <span data-ttu-id="d253d-122">1 à 12</span><span class="sxs-lookup"><span data-stu-id="d253d-122">1 to 12</span></span>        |
| <span data-ttu-id="d253d-123">2 étoiles</span><span class="sxs-lookup"><span data-stu-id="d253d-123">2 stars</span></span> | <span data-ttu-id="d253d-124">25</span><span class="sxs-lookup"><span data-stu-id="d253d-124">25</span></span>            | <span data-ttu-id="d253d-125">13 à 37</span><span class="sxs-lookup"><span data-stu-id="d253d-125">13 to 37</span></span>       |
| <span data-ttu-id="d253d-126">3 étoiles</span><span class="sxs-lookup"><span data-stu-id="d253d-126">3 stars</span></span> | <span data-ttu-id="d253d-127">50</span><span class="sxs-lookup"><span data-stu-id="d253d-127">50</span></span>            | <span data-ttu-id="d253d-128">38 à 62</span><span class="sxs-lookup"><span data-stu-id="d253d-128">38 to 62</span></span>       |
| <span data-ttu-id="d253d-129">4 étoiles</span><span class="sxs-lookup"><span data-stu-id="d253d-129">4 stars</span></span> | <span data-ttu-id="d253d-130">75</span><span class="sxs-lookup"><span data-stu-id="d253d-130">75</span></span>            | <span data-ttu-id="d253d-131">63 à 86</span><span class="sxs-lookup"><span data-stu-id="d253d-131">63 to 86</span></span>       |
| <span data-ttu-id="d253d-132">5 étoiles</span><span class="sxs-lookup"><span data-stu-id="d253d-132">5 stars</span></span> | <span data-ttu-id="d253d-133">99</span><span class="sxs-lookup"><span data-stu-id="d253d-133">99</span></span>            | <span data-ttu-id="d253d-134">87 à 99</span><span class="sxs-lookup"><span data-stu-id="d253d-134">87 to 99</span></span>       |



 

<span data-ttu-id="d253d-135">Cet attribut est stocké uniquement dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d253d-135">This attribute is stored only in the library.</span></span>

<span data-ttu-id="d253d-136">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="d253d-136">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d253d-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d253d-137">Requirements</span></span>



| <span data-ttu-id="d253d-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d253d-138">Requirement</span></span> | <span data-ttu-id="d253d-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d253d-139">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="d253d-140">Version</span><span class="sxs-lookup"><span data-stu-id="d253d-140">Version</span></span><br/> | <span data-ttu-id="d253d-141">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d253d-141">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d253d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d253d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d253d-143">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="d253d-143">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





