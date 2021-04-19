---
title: Élément smartPlaylist
description: L’élément smartPlaylist contient la partie définie dynamiquement d’une sélection.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Élément smartPlaylist lecteur Windows Media
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544111"
---
# <a name="smartplaylist-element"></a><span data-ttu-id="65f59-104">Élément smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="65f59-104">smartPlaylist Element</span></span>

<span data-ttu-id="65f59-105">L’élément **smartPlaylist** contient la partie définie dynamiquement d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="65f59-105">The **smartPlaylist** element contains the dynamically defined portion of a playlist.</span></span>

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a><span data-ttu-id="65f59-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="65f59-106">Attributes</span></span>



| <span data-ttu-id="65f59-107">Terme</span><span class="sxs-lookup"><span data-stu-id="65f59-107">Term</span></span>                                                                                                                                   | <span data-ttu-id="65f59-108">Description</span><span class="sxs-lookup"><span data-stu-id="65f59-108">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f59-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="65f59-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (required)</span></span> <br/> | <span data-ttu-id="65f59-110">Nombre décimal représentant le numéro de version du schéma de la sélection intelligente.</span><span class="sxs-lookup"><span data-stu-id="65f59-110">The decimal number representing the version number of the smart playlist schema.</span></span> <span data-ttu-id="65f59-111">Défini sur 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="65f59-111">Set to 1.0.0.0.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="65f59-112">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="65f59-112">Parent/Child Elements</span></span>



| <span data-ttu-id="65f59-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="65f59-113">Hierarchy</span></span> | <span data-ttu-id="65f59-114">Éléments</span><span class="sxs-lookup"><span data-stu-id="65f59-114">Elements</span></span>                                                       |
|-----------|----------------------------------------------------------------|
| <span data-ttu-id="65f59-115">Parent</span><span class="sxs-lookup"><span data-stu-id="65f59-115">Parent</span></span>    | [<span data-ttu-id="65f59-116">séquentiel</span><span class="sxs-lookup"><span data-stu-id="65f59-116">seq</span></span>](seq-element.md)                                         |
| <span data-ttu-id="65f59-117">Enfant</span><span class="sxs-lookup"><span data-stu-id="65f59-117">Child</span></span>     | <span data-ttu-id="65f59-118">[querySet](queryset-element.md), [filtre](filter-element.md)</span><span class="sxs-lookup"><span data-stu-id="65f59-118">[querySet](queryset-element.md), [filter](filter-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="65f59-119">Notes</span><span class="sxs-lookup"><span data-stu-id="65f59-119">Remarks</span></span>

<span data-ttu-id="65f59-120">Un élément **smartPlaylist** contient généralement un élément **querySet** et peut également contenir un élément **Filter** .</span><span class="sxs-lookup"><span data-stu-id="65f59-120">A **smartPlaylist** element typically contains a **querySet** element and can also contain a **filter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="65f59-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="65f59-121">Examples</span></span>


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
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
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a><span data-ttu-id="65f59-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65f59-122">Requirements</span></span>



| <span data-ttu-id="65f59-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65f59-123">Requirement</span></span> | <span data-ttu-id="65f59-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="65f59-124">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="65f59-125">Version</span><span class="sxs-lookup"><span data-stu-id="65f59-125">Version</span></span><br/> | <span data-ttu-id="65f59-126">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="65f59-126">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65f59-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65f59-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f59-128">**argument, élément**</span><span class="sxs-lookup"><span data-stu-id="65f59-128">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="65f59-129">**Élément Filter**</span><span class="sxs-lookup"><span data-stu-id="65f59-129">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="65f59-130">**fragment, élément**</span><span class="sxs-lookup"><span data-stu-id="65f59-130">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="65f59-131">**Élément querySet**</span><span class="sxs-lookup"><span data-stu-id="65f59-131">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="65f59-132">**Seq, élément**</span><span class="sxs-lookup"><span data-stu-id="65f59-132">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="65f59-133">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="65f59-133">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





