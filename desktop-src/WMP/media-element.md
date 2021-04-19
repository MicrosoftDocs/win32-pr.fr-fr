---
title: Élément multimédia
description: L’élément multimédia spécifie l’un des éléments multimédias dans une sélection.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Élément multimédia lecteur Windows Media
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532698"
---
# <a name="media-element"></a><span data-ttu-id="97ecf-104">Élément multimédia</span><span class="sxs-lookup"><span data-stu-id="97ecf-104">media Element</span></span>

<span data-ttu-id="97ecf-105">L’élément **multimédia** spécifie l’un des éléments multimédias dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="97ecf-105">The **media** element specifies one of the media items in a playlist.</span></span>

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a><span data-ttu-id="97ecf-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="97ecf-106">Attributes</span></span>



| <span data-ttu-id="97ecf-107">Terme</span><span class="sxs-lookup"><span data-stu-id="97ecf-107">Term</span></span>                                                                                                                       | <span data-ttu-id="97ecf-108">Description</span><span class="sxs-lookup"><span data-stu-id="97ecf-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97ecf-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="97ecf-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (required)</span></span> <br/> | <span data-ttu-id="97ecf-110">URL d’un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="97ecf-110">The URL of a media item.</span></span><br/>                                                              |
| <span data-ttu-id="97ecf-111"><span id="cid"></span><span id="CID"></span>**confirmation**</span><span class="sxs-lookup"><span data-stu-id="97ecf-111"><span id="cid"></span><span id="CID"></span>**cid**</span></span><br/>                                                             | <span data-ttu-id="97ecf-112">ID de contenu qui est unique à cet élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="97ecf-112">The content ID that is unique to this media item.</span></span><br/>                                     |
| <span data-ttu-id="97ecf-113"><span id="tid"></span><span id="TID"></span>**TID**</span><span class="sxs-lookup"><span data-stu-id="97ecf-113"><span id="tid"></span><span id="TID"></span>**tid**</span></span><br/>                                                             | <span data-ttu-id="97ecf-114">ID de suivi qui peut être utilisé pour effectuer le suivi de l’objet de système de fichiers pour cet élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="97ecf-114">The tracking ID that can be used to track the File System Object for this media item.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="97ecf-115">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="97ecf-115">Parent/Child Elements</span></span>



| <span data-ttu-id="97ecf-116">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="97ecf-116">Hierarchy</span></span> | <span data-ttu-id="97ecf-117">Éléments</span><span class="sxs-lookup"><span data-stu-id="97ecf-117">Elements</span></span>               |
|-----------|------------------------|
| <span data-ttu-id="97ecf-118">Parent</span><span class="sxs-lookup"><span data-stu-id="97ecf-118">Parent</span></span>    | [<span data-ttu-id="97ecf-119">séquentiel</span><span class="sxs-lookup"><span data-stu-id="97ecf-119">seq</span></span>](seq-element.md) |
| <span data-ttu-id="97ecf-120">Enfant</span><span class="sxs-lookup"><span data-stu-id="97ecf-120">Child</span></span>     | <span data-ttu-id="97ecf-121">Aucune</span><span class="sxs-lookup"><span data-stu-id="97ecf-121">None</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="97ecf-122">Notes</span><span class="sxs-lookup"><span data-stu-id="97ecf-122">Remarks</span></span>

<span data-ttu-id="97ecf-123">L’attribut **CID** (ID de contenu) est rempli par le lecteur Windows Media comme un moyen d’identifier de façon unique un morceau de contenu multimédia, même si ses attributs de métadonnées ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="97ecf-123">The **cid** attribute (the content ID) is populated by the Windows Media Player as a way to uniquely identify a piece of media content even if its metadata attributes have been changed.</span></span> <span data-ttu-id="97ecf-124">Cela permet de partager des sélections sur plusieurs ordinateurs, car le contenu peut être identifié sur un autre ordinateur, et le chemin d’accès peut être « réparé automatiquement » par la sélection Windows Media.</span><span class="sxs-lookup"><span data-stu-id="97ecf-124">This allows the sharing of playlists across computers, because the content can be identified on another computer, and the path to it can be "auto-repaired" by the Windows Media Playlist.</span></span> <span data-ttu-id="97ecf-125">L’attribut **TID** (l’ID de suivi) utilise le système de fichiers Windows pour réparer automatiquement le chemin d’accès au média si le nom ou l’emplacement du fichier est modifié.</span><span class="sxs-lookup"><span data-stu-id="97ecf-125">The **tid** attribute (the tracking ID) uses the Windows file system to auto-repair the path to the media if the name or location of the file is changed.</span></span>

## <a name="examples"></a><span data-ttu-id="97ecf-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="97ecf-126">Examples</span></span>


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a><span data-ttu-id="97ecf-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97ecf-127">Requirements</span></span>



| <span data-ttu-id="97ecf-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97ecf-128">Requirement</span></span> | <span data-ttu-id="97ecf-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="97ecf-129">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="97ecf-130">Version</span><span class="sxs-lookup"><span data-stu-id="97ecf-130">Version</span></span><br/> | <span data-ttu-id="97ecf-131">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="97ecf-131">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97ecf-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97ecf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ecf-133">**Seq, élément**</span><span class="sxs-lookup"><span data-stu-id="97ecf-133">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="97ecf-134">**Informations de référence sur les éléments de sélection Windows Media**</span><span class="sxs-lookup"><span data-stu-id="97ecf-134">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





