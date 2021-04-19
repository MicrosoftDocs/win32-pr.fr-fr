---
title: Élément meta
description: L’élément Meta spécifie les métadonnées qui s’appliquent à la sélection entière.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Élément méta Windows Media Player
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537463"
---
# <a name="meta-element"></a><span data-ttu-id="ae005-104">Élément meta</span><span class="sxs-lookup"><span data-stu-id="ae005-104">meta Element</span></span>

<span data-ttu-id="ae005-105">L’élément **meta** spécifie les métadonnées qui s’appliquent à la sélection entière.</span><span class="sxs-lookup"><span data-stu-id="ae005-105">The **meta** element specifies metadata that applies to the entire playlist.</span></span>

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a><span data-ttu-id="ae005-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="ae005-106">Attributes</span></span>



| <span data-ttu-id="ae005-107">Terme</span><span class="sxs-lookup"><span data-stu-id="ae005-107">Term</span></span>                                                                       | <span data-ttu-id="ae005-108">Description</span><span class="sxs-lookup"><span data-stu-id="ae005-108">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae005-109"><span id="name"></span><span id="NAME"></span>**nomme**</span><span class="sxs-lookup"><span data-stu-id="ae005-109"><span id="name"></span><span id="NAME"></span>**name**</span></span><br/>          | <span data-ttu-id="ae005-110">Nom d’un élément de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ae005-110">The name of an item of metadata.</span></span><br/>                                                                                       |
| <span data-ttu-id="ae005-111"><span id="content"></span><span id="CONTENT"></span>**humidité**</span><span class="sxs-lookup"><span data-stu-id="ae005-111"><span id="content"></span><span id="CONTENT"></span>**content**</span></span><br/> | <span data-ttu-id="ae005-112">Valeur d’un élément de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ae005-112">The value of an item of metadata.</span></span> <span data-ttu-id="ae005-113">Par exemple, si l’attribut de nom est « genre », l’attribut de contenu peut être « Rock ».</span><span class="sxs-lookup"><span data-stu-id="ae005-113">For example, if the name attribute is "Genre" the content attribute could be "Rock".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="ae005-114">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="ae005-114">Parent/Child Elements</span></span>



| <span data-ttu-id="ae005-115">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="ae005-115">Hierarchy</span></span> | <span data-ttu-id="ae005-116">Éléments</span><span class="sxs-lookup"><span data-stu-id="ae005-116">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="ae005-117">Parent</span><span class="sxs-lookup"><span data-stu-id="ae005-117">Parent</span></span>    | [<span data-ttu-id="ae005-118">head</span><span class="sxs-lookup"><span data-stu-id="ae005-118">head</span></span>](head-element.md) |
| <span data-ttu-id="ae005-119">Enfant</span><span class="sxs-lookup"><span data-stu-id="ae005-119">Child</span></span>     | <span data-ttu-id="ae005-120">Aucune</span><span class="sxs-lookup"><span data-stu-id="ae005-120">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="ae005-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ae005-121">Remarks</span></span>

<span data-ttu-id="ae005-122">Le créateur d’une sélection Windows Media peut définir l’attribut Name d’un élément Meta sur n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="ae005-122">The creator of a Windows Media Playlist can set the name attribute of a meta element to any string.</span></span> <span data-ttu-id="ae005-123">La liste suivante répertorie des attributs de nom standard qui se trouvent dans les listes de sélection Windows Media créées par le lecteur Windows Media et d’autres composants Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae005-123">The following list shows some typical name attributes that are found in Windows Media Playlists created by Windows Media Player and other Microsoft components.</span></span>

-   <span data-ttu-id="ae005-124">Auteur</span><span class="sxs-lookup"><span data-stu-id="ae005-124">Author</span></span>
-   <span data-ttu-id="ae005-125">Category</span><span class="sxs-lookup"><span data-stu-id="ae005-125">Category</span></span>
-   <span data-ttu-id="ae005-126">Genre</span><span class="sxs-lookup"><span data-stu-id="ae005-126">Genre</span></span>
-   <span data-ttu-id="ae005-127">UserName</span><span class="sxs-lookup"><span data-stu-id="ae005-127">UserName</span></span>
-   <span data-ttu-id="ae005-128">UserRating</span><span class="sxs-lookup"><span data-stu-id="ae005-128">UserRating</span></span>
-   <span data-ttu-id="ae005-129">Générateur</span><span class="sxs-lookup"><span data-stu-id="ae005-129">Generator</span></span>

## <a name="examples"></a><span data-ttu-id="ae005-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="ae005-130">Examples</span></span>


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="ae005-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae005-131">Requirements</span></span>



| <span data-ttu-id="ae005-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae005-132">Requirement</span></span> | <span data-ttu-id="ae005-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae005-133">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="ae005-134">Version</span><span class="sxs-lookup"><span data-stu-id="ae005-134">Version</span></span><br/> | <span data-ttu-id="ae005-135">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ae005-135">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae005-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae005-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae005-137">**Head, élément**</span><span class="sxs-lookup"><span data-stu-id="ae005-137">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="ae005-138">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ae005-138">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





