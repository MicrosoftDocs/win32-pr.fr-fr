---
title: Élément Body
description: L’élément Body contient les éléments qui définissent le contenu d’une sélection.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Élément de corps Windows Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523436"
---
# <a name="body-element"></a><span data-ttu-id="acbac-104">Élément Body</span><span class="sxs-lookup"><span data-stu-id="acbac-104">body Element</span></span>

<span data-ttu-id="acbac-105">L’élément **Body** contient les éléments qui définissent le contenu d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="acbac-105">The **body** element contains the elements that define the contents of a playlist.</span></span>

``` syntax
<body>
</body>
```

## <a name="attributes"></a><span data-ttu-id="acbac-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="acbac-106">Attributes</span></span>

<span data-ttu-id="acbac-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="acbac-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="acbac-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="acbac-108">Parent/Child Elements</span></span>



| <span data-ttu-id="acbac-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="acbac-109">Hierarchy</span></span> | <span data-ttu-id="acbac-110">Éléments</span><span class="sxs-lookup"><span data-stu-id="acbac-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="acbac-111">Parent</span><span class="sxs-lookup"><span data-stu-id="acbac-111">Parent</span></span>    | [<span data-ttu-id="acbac-112">SMIL</span><span class="sxs-lookup"><span data-stu-id="acbac-112">smil</span></span>](smil-element.md) |
| <span data-ttu-id="acbac-113">Enfant</span><span class="sxs-lookup"><span data-stu-id="acbac-113">Child</span></span>     | [<span data-ttu-id="acbac-114">séquentiel</span><span class="sxs-lookup"><span data-stu-id="acbac-114">seq</span></span>](seq-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="acbac-115">Notes</span><span class="sxs-lookup"><span data-stu-id="acbac-115">Remarks</span></span>

<span data-ttu-id="acbac-116">Le contenu d’une sélection est organisé dans un élément **Seq** qui est contenu dans l’élément **Body** .</span><span class="sxs-lookup"><span data-stu-id="acbac-116">The contents of a playlist are organized within a **seq** element that is contained within the **body** element.</span></span> <span data-ttu-id="acbac-117">En général, il existe soit un élément **Seq** qui définit un ensemble statique d’éléments multimédias **et contient des éléments multimédias,** soit un élément qui définit un ensemble dynamique d’éléments multimédias et contient un élément **smartPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="acbac-117">Typically there is either one **seq** element that defines a static set of media items and contains **media** elements, or there is one that defines a dynamic set of media items and contains a **smartPlaylist** element.</span></span>

## <a name="examples"></a><span data-ttu-id="acbac-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="acbac-118">Examples</span></span>


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a><span data-ttu-id="acbac-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acbac-119">Requirements</span></span>



| <span data-ttu-id="acbac-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acbac-120">Requirement</span></span> | <span data-ttu-id="acbac-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="acbac-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="acbac-122">Version</span><span class="sxs-lookup"><span data-stu-id="acbac-122">Version</span></span><br/> | <span data-ttu-id="acbac-123">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="acbac-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="acbac-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acbac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acbac-125">**Élément multimédia**</span><span class="sxs-lookup"><span data-stu-id="acbac-125">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="acbac-126">**Seq, élément**</span><span class="sxs-lookup"><span data-stu-id="acbac-126">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="acbac-127">**Élément smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="acbac-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="acbac-128">**Élément smil**</span><span class="sxs-lookup"><span data-stu-id="acbac-128">**smil Element**</span></span>](smil-element.md)
</dt> <dt>

[<span data-ttu-id="acbac-129">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="acbac-129">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





