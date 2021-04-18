---
title: Head, élément
description: L’élément head contient des métadonnées qui s’appliquent à la sélection entière.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Élément head Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540501"
---
# <a name="head-element"></a><span data-ttu-id="99377-104">Head, élément</span><span class="sxs-lookup"><span data-stu-id="99377-104">head Element</span></span>

<span data-ttu-id="99377-105">L’élément **Head** contient des métadonnées qui s’appliquent à la sélection entière.</span><span class="sxs-lookup"><span data-stu-id="99377-105">The **head** element contains metadata that applies to the entire playlist.</span></span>

``` syntax
<head>
</head>
```

## <a name="attributes"></a><span data-ttu-id="99377-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="99377-106">Attributes</span></span>

<span data-ttu-id="99377-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="99377-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="99377-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="99377-108">Parent/Child Elements</span></span>



| <span data-ttu-id="99377-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="99377-109">Hierarchy</span></span> | <span data-ttu-id="99377-110">Éléments</span><span class="sxs-lookup"><span data-stu-id="99377-110">Elements</span></span>                                                  |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="99377-111">Parent</span><span class="sxs-lookup"><span data-stu-id="99377-111">Parent</span></span>    | [<span data-ttu-id="99377-112">SMIL</span><span class="sxs-lookup"><span data-stu-id="99377-112">smil</span></span>](smil-element.md)                                  |
| <span data-ttu-id="99377-113">Enfant</span><span class="sxs-lookup"><span data-stu-id="99377-113">Child</span></span>     | <span data-ttu-id="99377-114">[titre](title-element--wpl.md), [méta](meta-element.md)</span><span class="sxs-lookup"><span data-stu-id="99377-114">[title](title-element--wpl.md), [meta](meta-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="99377-115">Notes</span><span class="sxs-lookup"><span data-stu-id="99377-115">Remarks</span></span>

<span data-ttu-id="99377-116">En général, l’élément **Head** contient un élément **title** et un ou plusieurs éléments **meta** qui définissent les caractéristiques globales de la sélection.</span><span class="sxs-lookup"><span data-stu-id="99377-116">Typically the **head** element contains a **title** element and one or more **meta** elements that define global characteristics of the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="99377-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="99377-117">Examples</span></span>


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="99377-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99377-118">Requirements</span></span>



| <span data-ttu-id="99377-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99377-119">Requirement</span></span> | <span data-ttu-id="99377-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="99377-120">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="99377-121">Version</span><span class="sxs-lookup"><span data-stu-id="99377-121">Version</span></span><br/> | <span data-ttu-id="99377-122">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="99377-122">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99377-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99377-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99377-124">**Élément meta**</span><span class="sxs-lookup"><span data-stu-id="99377-124">**meta Element**</span></span>](meta-element.md)
</dt> <dt>

[<span data-ttu-id="99377-125">**title, élément (WPL)**</span><span class="sxs-lookup"><span data-stu-id="99377-125">**title Element (WPL)**</span></span>](title-element--wpl.md)
</dt> <dt>

[<span data-ttu-id="99377-126">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="99377-126">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





