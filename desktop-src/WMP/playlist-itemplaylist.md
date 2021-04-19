---
title: PLAYLIST. itemPlaylist
description: L’attribut itemPlaylist récupère la sélection de l’élément multimédia qui est affiché à l’index donné dans l’élément PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- Lecteur Windows Media PLAYLIST. itemPlaylist
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543323"
---
# <a name="playlistitemplaylist"></a><span data-ttu-id="8ad96-104">PLAYLIST. itemPlaylist</span><span class="sxs-lookup"><span data-stu-id="8ad96-104">PLAYLIST.itemPlaylist</span></span>

<span data-ttu-id="8ad96-105">L’attribut **itemPlaylist** récupère la sélection de l’élément multimédia qui est affiché à l’index donné dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="8ad96-105">The **itemPlaylist** attribute retrieves the playlist for the media item that is displayed at the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a><span data-ttu-id="8ad96-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="8ad96-106">Possible Values</span></span>

<span data-ttu-id="8ad96-107">Cet attribut est un objet de **sélection** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8ad96-107">This attribute is a read-only **Playlist** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ad96-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ad96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ad96-109"><span id="index"></span><span id="INDEX"></span>*évaluer*</span><span class="sxs-lookup"><span data-stu-id="8ad96-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="8ad96-110">**Nombre**(**long**) contenant l’index d’un élément de sélection.</span><span class="sxs-lookup"><span data-stu-id="8ad96-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ad96-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8ad96-111">Remarks</span></span>

<span data-ttu-id="8ad96-112">La propriété **itemPlaylist** retourne l’objet playlist qui est développé dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="8ad96-112">The **itemPlaylist** property will return the playlist object that is expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="8ad96-113">Par exemple, s’il existe deux sélections imbriquées qui ne sont pas développées dans l’élément **playlist** et qui contiennent trois clips multimédias, **itemPlaylist**(1) retourne la sélection parente qui contient les deux sélections imbriquées.</span><span class="sxs-lookup"><span data-stu-id="8ad96-113">For example, if there are two nested playlists that are not expanded in the **PLAYLIST** element, and that contain three media clips each, **itemPlaylist**(1) will return the parent playlist that contains the two nested playlists.</span></span> <span data-ttu-id="8ad96-114">Si la deuxième sélection est développée, **itemPlaylist**(1) retourne la deuxième sélection.</span><span class="sxs-lookup"><span data-stu-id="8ad96-114">If the second playlist is expanded, **itemPlaylist**(1) will return the second playlist.</span></span> <span data-ttu-id="8ad96-115">Si les deux sélections sont développées, **itemPlaylist**(1) retourne la première sélection.</span><span class="sxs-lookup"><span data-stu-id="8ad96-115">If both playlists are expanded, **itemPlaylist**(1) will return the first playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ad96-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ad96-116">Requirements</span></span>



| <span data-ttu-id="8ad96-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ad96-117">Requirement</span></span> | <span data-ttu-id="8ad96-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ad96-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8ad96-119">Version</span><span class="sxs-lookup"><span data-stu-id="8ad96-119">Version</span></span><br/> | <span data-ttu-id="8ad96-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8ad96-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ad96-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ad96-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad96-122">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="8ad96-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="8ad96-123">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="8ad96-123">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





