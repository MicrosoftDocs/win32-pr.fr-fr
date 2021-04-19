---
title: Seq, élément
description: L’élément SEQ contient des éléments qui définissent une sélection statique ou des éléments qui définissent une sélection intelligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Seq, élément Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542263"
---
# <a name="seq-element"></a><span data-ttu-id="72e9a-104">Seq, élément</span><span class="sxs-lookup"><span data-stu-id="72e9a-104">seq Element</span></span>

<span data-ttu-id="72e9a-105">L’élément **Seq** contient des éléments qui définissent une sélection statique ou des éléments qui définissent une sélection intelligente.</span><span class="sxs-lookup"><span data-stu-id="72e9a-105">The **seq** element contains elements that define a static playlist or elements that define a smart playlist.</span></span>

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a><span data-ttu-id="72e9a-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="72e9a-106">Attributes</span></span>

<span data-ttu-id="72e9a-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="72e9a-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="72e9a-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="72e9a-108">Parent/Child Elements</span></span>



| <span data-ttu-id="72e9a-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="72e9a-109">Hierarchy</span></span> | <span data-ttu-id="72e9a-110">Éléments</span><span class="sxs-lookup"><span data-stu-id="72e9a-110">Elements</span></span>                                                               |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="72e9a-111">Parent</span><span class="sxs-lookup"><span data-stu-id="72e9a-111">Parent</span></span>    | [<span data-ttu-id="72e9a-112">body</span><span class="sxs-lookup"><span data-stu-id="72e9a-112">body</span></span>](body-element.md)                                               |
| <span data-ttu-id="72e9a-113">Enfant</span><span class="sxs-lookup"><span data-stu-id="72e9a-113">Child</span></span>     | <span data-ttu-id="72e9a-114">[média](media-element.md), [smartPlaylist](smartplaylist-element.md)</span><span class="sxs-lookup"><span data-stu-id="72e9a-114">[media](media-element.md), [smartPlaylist](smartplaylist-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="72e9a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="72e9a-115">Remarks</span></span>

<span data-ttu-id="72e9a-116">Lorsqu’un élément **Seq** contient uniquement des éléments **multimédias** qui font référence à des éléments multimédias spécifiques, la sélection est considérée comme statique.</span><span class="sxs-lookup"><span data-stu-id="72e9a-116">When a **seq** element only contains **media** elements that reference specific media items, the playlist is considered to be static.</span></span> <span data-ttu-id="72e9a-117">Lorsqu’un élément **Seq** contient un élément **smartPlaylist** , il est considéré comme une sélection « intelligente » dynamique.</span><span class="sxs-lookup"><span data-stu-id="72e9a-117">When a **seq** element contains a **smartPlaylist** element, it is considered to be a dynamic "smart" playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="72e9a-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="72e9a-118">Examples</span></span>


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a><span data-ttu-id="72e9a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72e9a-119">Requirements</span></span>



| <span data-ttu-id="72e9a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72e9a-120">Requirement</span></span> | <span data-ttu-id="72e9a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="72e9a-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="72e9a-122">Version</span><span class="sxs-lookup"><span data-stu-id="72e9a-122">Version</span></span><br/> | <span data-ttu-id="72e9a-123">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="72e9a-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72e9a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72e9a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e9a-125">**Élément Body**</span><span class="sxs-lookup"><span data-stu-id="72e9a-125">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="72e9a-126">**Élément multimédia**</span><span class="sxs-lookup"><span data-stu-id="72e9a-126">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="72e9a-127">**Élément smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="72e9a-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="72e9a-128">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="72e9a-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





