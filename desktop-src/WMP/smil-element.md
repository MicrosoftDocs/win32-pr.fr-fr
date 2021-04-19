---
title: Élément smil
description: L’élément smil est toujours l’élément de niveau supérieur dans un fichier de sélection Windows Media (WPL). Il spécifie que le fichier utilise la syntaxe et la grammaire du langage SMIL (Synchronized Multimedia Integration Language).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Élément smil lecteur Windows Media
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541459"
---
# <a name="smil-element"></a><span data-ttu-id="fd69f-105">Élément smil</span><span class="sxs-lookup"><span data-stu-id="fd69f-105">smil Element</span></span>

<span data-ttu-id="fd69f-106">L’élément **SMIL** est toujours l’élément de niveau supérieur dans un fichier de sélection Windows Media (WPL).</span><span class="sxs-lookup"><span data-stu-id="fd69f-106">The **smil** element is always the top level element in a Windows Media Playlist (WPL) file.</span></span> <span data-ttu-id="fd69f-107">Il spécifie que le fichier utilise la syntaxe et la grammaire du langage SMIL (Synchronized Multimedia Integration Language).</span><span class="sxs-lookup"><span data-stu-id="fd69f-107">It specifies that the file uses SMIL (Synchronized Multimedia Integration Language) syntax and grammar.</span></span>

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a><span data-ttu-id="fd69f-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="fd69f-108">Attributes</span></span>

<span data-ttu-id="fd69f-109">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="fd69f-109">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="fd69f-110">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="fd69f-110">Parent/Child Elements</span></span>



| <span data-ttu-id="fd69f-111">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="fd69f-111">Hierarchy</span></span> | <span data-ttu-id="fd69f-112">Éléments</span><span class="sxs-lookup"><span data-stu-id="fd69f-112">Elements</span></span>                                           |
|-----------|----------------------------------------------------|
| <span data-ttu-id="fd69f-113">Parent</span><span class="sxs-lookup"><span data-stu-id="fd69f-113">Parent</span></span>    | <span data-ttu-id="fd69f-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="fd69f-114">None</span></span>                                               |
| <span data-ttu-id="fd69f-115">Enfant</span><span class="sxs-lookup"><span data-stu-id="fd69f-115">Child</span></span>     | <span data-ttu-id="fd69f-116">[Head](head-element.md), [corps](body-element.md)</span><span class="sxs-lookup"><span data-stu-id="fd69f-116">[head](head-element.md), [body](body-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fd69f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fd69f-117">Remarks</span></span>

<span data-ttu-id="fd69f-118">Chaque playlist Windows Media doit avoir l’élément **SMIL** à sa racine.</span><span class="sxs-lookup"><span data-stu-id="fd69f-118">Every Windows Media Playlist must have the **smil** element at its root.</span></span>

## <a name="examples"></a><span data-ttu-id="fd69f-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="fd69f-119">Examples</span></span>


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a><span data-ttu-id="fd69f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd69f-120">Requirements</span></span>



| <span data-ttu-id="fd69f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd69f-121">Requirement</span></span> | <span data-ttu-id="fd69f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd69f-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="fd69f-123">Version</span><span class="sxs-lookup"><span data-stu-id="fd69f-123">Version</span></span><br/> | <span data-ttu-id="fd69f-124">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fd69f-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd69f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd69f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd69f-126">**Élément Body**</span><span class="sxs-lookup"><span data-stu-id="fd69f-126">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="fd69f-127">**Head, élément**</span><span class="sxs-lookup"><span data-stu-id="fd69f-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="fd69f-128">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fd69f-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





