---
title: Élément Filter
description: L’élément Filter contient des éléments qui limitent la taille d’une sélection, la durée d’une sélection ou le nombre d’éléments multimédias dans une sélection.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Élément de filtre Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537449"
---
# <a name="filter-element"></a><span data-ttu-id="0c6a0-104">Élément Filter</span><span class="sxs-lookup"><span data-stu-id="0c6a0-104">filter Element</span></span>

<span data-ttu-id="0c6a0-105">L’élément **Filter** contient des éléments qui limitent la taille d’une sélection, la durée d’une sélection ou le nombre d’éléments multimédias dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-105">The **filter** element contains elements that limit the size of a playlist, duration of a playlist, or number of media items in a playlist.</span></span>

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a><span data-ttu-id="0c6a0-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="0c6a0-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="0c6a0-107"><span id="type"></span><span id="TYPE"></span>**entrer**</span><span class="sxs-lookup"><span data-stu-id="0c6a0-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="0c6a0-108">Type de l’objet Filter.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-108">The type of filter object.</span></span> <span data-ttu-id="0c6a0-109">Il n’existe pas de valeurs prédéfinies pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="0c6a0-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="0c6a0-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="0c6a0-111">GUID qui identifie de façon unique un objet filtre.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-111">The GUID that uniquely identifies a filter object.</span></span> <span data-ttu-id="0c6a0-112">Les méthodes de l’objet de filtre sont appelées pour interpréter les éléments de **fragment** contenus dans l’élément de **filtre** .</span><span class="sxs-lookup"><span data-stu-id="0c6a0-112">The filter object's methods are invoked to interpret the **fragment** elements contained in the **filter** element.</span></span>



| <span data-ttu-id="0c6a0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c6a0-113">Value</span></span>                                  | <span data-ttu-id="0c6a0-114">Description</span><span class="sxs-lookup"><span data-stu-id="0c6a0-114">Description</span></span>                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c6a0-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span><span class="sxs-lookup"><span data-stu-id="0c6a0-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span></span> | <span data-ttu-id="0c6a0-116">ID du filtre « filtre de sélection automatique Microsoft--limite les sélections automatiques par nombre, taille ou durée ».</span><span class="sxs-lookup"><span data-stu-id="0c6a0-116">The id for the "Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration" filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0c6a0-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nom** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="0c6a0-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="0c6a0-118">Nom de l’objet de filtre.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-118">The name of the filter object.</span></span>



| <span data-ttu-id="0c6a0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c6a0-119">Value</span></span>                                                                              | <span data-ttu-id="0c6a0-120">Description</span><span class="sxs-lookup"><span data-stu-id="0c6a0-120">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="0c6a0-121">Filtre de sélection automatique Microsoft--limite les sélections automatiques par nombre, taille ou durée</span><span class="sxs-lookup"><span data-stu-id="0c6a0-121">Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration</span></span> | <span data-ttu-id="0c6a0-122">Limite les sélections automatiques par nombre, taille ou durée.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-122">Limits auto playlists by count, size, or duration.</span></span> |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="0c6a0-123">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="0c6a0-123">Parent/Child Elements</span></span>



| <span data-ttu-id="0c6a0-124">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="0c6a0-124">Hierarchy</span></span> | <span data-ttu-id="0c6a0-125">Éléments</span><span class="sxs-lookup"><span data-stu-id="0c6a0-125">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="0c6a0-126">Parent</span><span class="sxs-lookup"><span data-stu-id="0c6a0-126">Parent</span></span>    | [<span data-ttu-id="0c6a0-127">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="0c6a0-127">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="0c6a0-128">Enfant</span><span class="sxs-lookup"><span data-stu-id="0c6a0-128">Child</span></span>     | [<span data-ttu-id="0c6a0-129">échantillon</span><span class="sxs-lookup"><span data-stu-id="0c6a0-129">fragment</span></span>](fragment-element.md)           |



 

## <a name="remarks"></a><span data-ttu-id="0c6a0-130">Notes</span><span class="sxs-lookup"><span data-stu-id="0c6a0-130">Remarks</span></span>

<span data-ttu-id="0c6a0-131">L’élément **Filter** n’ajoute pas d’éléments multimédias à une sélection ; Il supprime simplement ou filtre le contenu qui a été sélectionné par l’élément **sourceFilter** .</span><span class="sxs-lookup"><span data-stu-id="0c6a0-131">The **filter** element does not add any media elements to a playlist; it simply removes or filters out content that was selected by the **sourceFilter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="0c6a0-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="0c6a0-132">Examples</span></span>


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a><span data-ttu-id="0c6a0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c6a0-133">Requirements</span></span>



| <span data-ttu-id="0c6a0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c6a0-134">Requirement</span></span> | <span data-ttu-id="0c6a0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c6a0-135">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="0c6a0-136">Version</span><span class="sxs-lookup"><span data-stu-id="0c6a0-136">Version</span></span><br/> | <span data-ttu-id="0c6a0-137">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-137">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c6a0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c6a0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c6a0-139">**argument, élément**</span><span class="sxs-lookup"><span data-stu-id="0c6a0-139">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="0c6a0-140">**fragment, élément**</span><span class="sxs-lookup"><span data-stu-id="0c6a0-140">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="0c6a0-141">**Élément smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="0c6a0-141">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="0c6a0-142">**Élément sourceFilter**</span><span class="sxs-lookup"><span data-stu-id="0c6a0-142">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="0c6a0-143">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0c6a0-143">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





