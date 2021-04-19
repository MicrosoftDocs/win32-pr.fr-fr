---
title: Élément querySet
description: L’élément querySet contient des éléments qui définissent les éléments multimédias qui seront sélectionnés dans la bibliothèque.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Élément querySet lecteur Windows Media
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540007"
---
# <a name="queryset-element"></a><span data-ttu-id="bafbe-104">Élément querySet</span><span class="sxs-lookup"><span data-stu-id="bafbe-104">querySet Element</span></span>

<span data-ttu-id="bafbe-105">L’élément **querySet** contient des éléments qui définissent les éléments multimédias qui seront sélectionnés dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bafbe-105">The **querySet** element contains elements that define which media items will be selected from the library.</span></span>

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a><span data-ttu-id="bafbe-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="bafbe-106">Attributes</span></span>

<span data-ttu-id="bafbe-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="bafbe-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="bafbe-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="bafbe-108">Parent/Child Elements</span></span>



| <span data-ttu-id="bafbe-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="bafbe-109">Hierarchy</span></span> | <span data-ttu-id="bafbe-110">Éléments</span><span class="sxs-lookup"><span data-stu-id="bafbe-110">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="bafbe-111">Parent</span><span class="sxs-lookup"><span data-stu-id="bafbe-111">Parent</span></span>    | [<span data-ttu-id="bafbe-112">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="bafbe-112">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="bafbe-113">Enfant</span><span class="sxs-lookup"><span data-stu-id="bafbe-113">Child</span></span>     | [<span data-ttu-id="bafbe-114">sourceFilter</span><span class="sxs-lookup"><span data-stu-id="bafbe-114">sourceFilter</span></span>](sourcefilter-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="bafbe-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bafbe-115">Remarks</span></span>

<span data-ttu-id="bafbe-116">L’élément **querySet** spécifie les éléments multimédias à sélectionner à partir de la bibliothèque, sans tenir compte de la taille du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="bafbe-116">The **querySet** element specifies which media items should be selected from the library, without regard for the size of the result set.</span></span> <span data-ttu-id="bafbe-117">L’élément **Filter** , en revanche, limite la taille du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="bafbe-117">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="bafbe-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="bafbe-118">Examples</span></span>


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a><span data-ttu-id="bafbe-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bafbe-119">Requirements</span></span>



| <span data-ttu-id="bafbe-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bafbe-120">Requirement</span></span> | <span data-ttu-id="bafbe-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bafbe-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="bafbe-122">Version</span><span class="sxs-lookup"><span data-stu-id="bafbe-122">Version</span></span><br/> | <span data-ttu-id="bafbe-123">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bafbe-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bafbe-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bafbe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bafbe-125">**argument, élément**</span><span class="sxs-lookup"><span data-stu-id="bafbe-125">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="bafbe-126">**Élément Filter**</span><span class="sxs-lookup"><span data-stu-id="bafbe-126">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="bafbe-127">**fragment, élément**</span><span class="sxs-lookup"><span data-stu-id="bafbe-127">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="bafbe-128">**Élément smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="bafbe-128">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="bafbe-129">**Élément sourceFilter**</span><span class="sxs-lookup"><span data-stu-id="bafbe-129">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="bafbe-130">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="bafbe-130">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





