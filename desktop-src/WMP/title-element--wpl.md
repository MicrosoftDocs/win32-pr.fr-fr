---
title: title, élément (WPL)
description: L’élément title spécifie un titre pour la sélection.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- title, élément (WPL) lecteur Windows Media
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524047"
---
# <a name="title-element-wpl"></a><span data-ttu-id="7a6e2-104">title, élément (WPL)</span><span class="sxs-lookup"><span data-stu-id="7a6e2-104">title Element (WPL)</span></span>

<span data-ttu-id="7a6e2-105">L’élément **title** spécifie un titre pour la sélection.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-105">The **title** element specifies a title for the playlist.</span></span>

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a><span data-ttu-id="7a6e2-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="7a6e2-106">Attributes</span></span>

<span data-ttu-id="7a6e2-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="7a6e2-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="7a6e2-108">Parent/Child Elements</span></span>



| <span data-ttu-id="7a6e2-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="7a6e2-109">Hierarchy</span></span> | <span data-ttu-id="7a6e2-110">Éléments</span><span class="sxs-lookup"><span data-stu-id="7a6e2-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="7a6e2-111">Parent</span><span class="sxs-lookup"><span data-stu-id="7a6e2-111">Parent</span></span>    | [<span data-ttu-id="7a6e2-112">head</span><span class="sxs-lookup"><span data-stu-id="7a6e2-112">head</span></span>](head-element.md) |
| <span data-ttu-id="7a6e2-113">Enfant</span><span class="sxs-lookup"><span data-stu-id="7a6e2-113">Child</span></span>     | <span data-ttu-id="7a6e2-114">Aucune</span><span class="sxs-lookup"><span data-stu-id="7a6e2-114">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="7a6e2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7a6e2-115">Remarks</span></span>

<span data-ttu-id="7a6e2-116">Lorsque vous choisissez un titre pour une sélection Windows Media (WPL), considérez que le contenu de la sélection peut être dynamique.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-116">When choosing a title for a Windows Media Playlist (WPL), consider that the content of the playlist can be dynamic.</span></span> <span data-ttu-id="7a6e2-117">Une bonne approche consiste à baser le titre sur la logique dans les éléments d' **argument** , car c’est ce qui définit le contenu de la sélection.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-117">A good approach is to base the title on the logic in the **argument** elements because this is what defines the content of the playlist.</span></span> <span data-ttu-id="7a6e2-118">Voici des exemples : « mes chansons favorites de 1966 » ou « chansons de danse que je n’ai pas jouées récemment ».</span><span class="sxs-lookup"><span data-stu-id="7a6e2-118">Examples of this are "My Favorite Rock Songs from 1966" or "Dance Songs That I Haven't Played Recently".</span></span>

## <a name="examples"></a><span data-ttu-id="7a6e2-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="7a6e2-119">Examples</span></span>


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a><span data-ttu-id="7a6e2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a6e2-120">Requirements</span></span>



| <span data-ttu-id="7a6e2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a6e2-121">Requirement</span></span> | <span data-ttu-id="7a6e2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a6e2-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="7a6e2-123">Version</span><span class="sxs-lookup"><span data-stu-id="7a6e2-123">Version</span></span><br/> | <span data-ttu-id="7a6e2-124">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7a6e2-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a6e2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a6e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a6e2-126">**argument, élément**</span><span class="sxs-lookup"><span data-stu-id="7a6e2-126">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="7a6e2-127">**Head, élément**</span><span class="sxs-lookup"><span data-stu-id="7a6e2-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="7a6e2-128">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7a6e2-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





