---
title: Élément sourceFilter
description: L’élément sourceFilter contient des éléments qui sélectionnent des éléments dans une bibliothèque.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Élément sourceFilter lecteur Windows Media
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525606"
---
# <a name="sourcefilter-element"></a><span data-ttu-id="eade5-104">Élément sourceFilter</span><span class="sxs-lookup"><span data-stu-id="eade5-104">sourceFilter Element</span></span>

<span data-ttu-id="eade5-105">L’élément **sourceFilter** contient des éléments qui sélectionnent des éléments dans une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="eade5-105">The **sourceFilter** element contains elements that select items from a library.</span></span>

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a><span data-ttu-id="eade5-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="eade5-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="eade5-107"><span id="type"></span><span id="TYPE"></span>**entrer**</span><span class="sxs-lookup"><span data-stu-id="eade5-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="eade5-108">Type de l’objet Filter.</span><span class="sxs-lookup"><span data-stu-id="eade5-108">The type of filter object.</span></span> <span data-ttu-id="eade5-109">Il n’existe pas de valeurs prédéfinies pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="eade5-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="eade5-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eade5-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="eade5-111">GUID qui identifie de façon unique l’objet de filtre source.</span><span class="sxs-lookup"><span data-stu-id="eade5-111">The GUID that uniquely identifies the source filter object.</span></span> <span data-ttu-id="eade5-112">Les méthodes de l’objet de filtre source sont appelées pour interpréter les éléments de **fragment** contenus dans l’élément **sourceFilter** .</span><span class="sxs-lookup"><span data-stu-id="eade5-112">The source filter object's methods are invoked to interpret the **fragment** elements contained in the **sourceFilter** element.</span></span>



| <span data-ttu-id="eade5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="eade5-113">Value</span></span>                                  | <span data-ttu-id="eade5-114">Description</span><span class="sxs-lookup"><span data-stu-id="eade5-114">Description</span></span>                                              |
|----------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="eade5-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span><span class="sxs-lookup"><span data-stu-id="eade5-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span></span> | <span data-ttu-id="eade5-116">GUID du filtre source « musique dans ma bibliothèque ».</span><span class="sxs-lookup"><span data-stu-id="eade5-116">The GUID for the "Music in my library" source filter.</span></span>    |
| <span data-ttu-id="eade5-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span><span class="sxs-lookup"><span data-stu-id="eade5-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span></span> | <span data-ttu-id="eade5-118">GUID du filtre source « vidéo dans ma bibliothèque ».</span><span class="sxs-lookup"><span data-stu-id="eade5-118">The GUID for the "Video in my library" source filter.</span></span>    |
| <span data-ttu-id="eade5-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span><span class="sxs-lookup"><span data-stu-id="eade5-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span></span> | <span data-ttu-id="eade5-120">GUID du filtre source « images dans ma bibliothèque ».</span><span class="sxs-lookup"><span data-stu-id="eade5-120">The GUID for the "Pictures in my library" source filter.</span></span> |
| <span data-ttu-id="eade5-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span><span class="sxs-lookup"><span data-stu-id="eade5-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span></span> | <span data-ttu-id="eade5-122">GUID du filtre source « émissions TV dans ma bibliothèque ».</span><span class="sxs-lookup"><span data-stu-id="eade5-122">The GUID for the "TV shows in my library" source filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="eade5-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nom** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eade5-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="eade5-124">Nom de l’objet de filtre.</span><span class="sxs-lookup"><span data-stu-id="eade5-124">The name of the filter object.</span></span>



| <span data-ttu-id="eade5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="eade5-125">Value</span></span>                  | <span data-ttu-id="eade5-126">Description</span><span class="sxs-lookup"><span data-stu-id="eade5-126">Description</span></span>                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eade5-127">Musique dans ma bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eade5-127">Music in my library</span></span>    | <span data-ttu-id="eade5-128">Objet de filtre qui sélectionne des éléments spécifiés à partir de l’ensemble d’éléments musicaux dans la bibliothèque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eade5-128">A filter object that selects specified items from the set of music items in the user's library.</span></span> |
| <span data-ttu-id="eade5-129">Vidéo dans ma bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eade5-129">Video in my library</span></span>    | <span data-ttu-id="eade5-130">Objet de filtre qui sélectionne des éléments spécifiés à partir de l’ensemble d’éléments vidéo dans la bibliothèque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eade5-130">A filter object that selects specified items from the set of video items in the user's library.</span></span> |
| <span data-ttu-id="eade5-131">Images dans ma bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eade5-131">Pictures in my library</span></span> | <span data-ttu-id="eade5-132">Objet de filtre qui sélectionne des éléments spécifiés à partir de l’ensemble d’éléments de photo dans la bibliothèque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eade5-132">A filter object that selects specified items from the set of photo items in the user's library.</span></span> |
| <span data-ttu-id="eade5-133">Émissions TV dans ma bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eade5-133">TV shows in my library</span></span> | <span data-ttu-id="eade5-134">Objet de filtre qui sélectionne des éléments spécifiés à partir de l’ensemble d’éléments TV dans la bibliothèque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eade5-134">A filter object that selects specified items from the set of TV items in the user's library.</span></span>    |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="eade5-135">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="eade5-135">Parent/Child Elements</span></span>



| <span data-ttu-id="eade5-136">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="eade5-136">Hierarchy</span></span> | <span data-ttu-id="eade5-137">Éléments</span><span class="sxs-lookup"><span data-stu-id="eade5-137">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="eade5-138">Parent</span><span class="sxs-lookup"><span data-stu-id="eade5-138">Parent</span></span>    | [<span data-ttu-id="eade5-139">querySet</span><span class="sxs-lookup"><span data-stu-id="eade5-139">querySet</span></span>](queryset-element.md) |
| <span data-ttu-id="eade5-140">Enfant</span><span class="sxs-lookup"><span data-stu-id="eade5-140">Child</span></span>     | [<span data-ttu-id="eade5-141">échantillon</span><span class="sxs-lookup"><span data-stu-id="eade5-141">fragment</span></span>](fragment-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="eade5-142">Notes</span><span class="sxs-lookup"><span data-stu-id="eade5-142">Remarks</span></span>

<span data-ttu-id="eade5-143">L’élément **sourceFilter** sélectionne des éléments de la bibliothèque sans tenir compte de la taille du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="eade5-143">The **sourceFilter** element selects items from the library without regard for the size of the result set.</span></span> <span data-ttu-id="eade5-144">L’élément **Filter** , en revanche, limite la taille du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="eade5-144">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="eade5-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="eade5-145">Examples</span></span>


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
    name = "Music in my library">
        <fragment name = "Genre">
            <argument name = "condition">Is</argument>
            <argument name = "value">Rock</argument>
        </fragment>
        <fragment name = "Album Artist">
            <argument name = "condition">Is Not</argument>
            <argument name = "value">Brenda Diaz</argument>
        </fragment>
</sourceFilter>
```



## <a name="requirements"></a><span data-ttu-id="eade5-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eade5-146">Requirements</span></span>



| <span data-ttu-id="eade5-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eade5-147">Requirement</span></span> | <span data-ttu-id="eade5-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="eade5-148">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="eade5-149">Version</span><span class="sxs-lookup"><span data-stu-id="eade5-149">Version</span></span><br/> | <span data-ttu-id="eade5-150">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="eade5-150">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eade5-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eade5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eade5-152">**Élément Filter**</span><span class="sxs-lookup"><span data-stu-id="eade5-152">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="eade5-153">**fragment, élément**</span><span class="sxs-lookup"><span data-stu-id="eade5-153">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="eade5-154">**Élément querySet**</span><span class="sxs-lookup"><span data-stu-id="eade5-154">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="eade5-155">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="eade5-155">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





