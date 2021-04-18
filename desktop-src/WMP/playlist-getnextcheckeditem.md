---
title: PLAYLIST. getNextCheckedItem
description: La méthode getNextCheckedItem récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- Lecteur Windows Media PLAYLIST. getNextCheckedItem
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532920"
---
# <a name="playlistgetnextcheckeditem"></a><span data-ttu-id="9ed5d-104">PLAYLIST. getNextCheckedItem</span><span class="sxs-lookup"><span data-stu-id="9ed5d-104">PLAYLIST.getNextCheckedItem</span></span>

<span data-ttu-id="9ed5d-105">La méthode **getNextCheckedItem** récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ed5d-105">The **getNextCheckedItem** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="9ed5d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ed5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed5d-107"><span id="item"></span><span id="ITEM"></span>*fiche*</span><span class="sxs-lookup"><span data-stu-id="9ed5d-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="9ed5d-108">**Nombre** (**long**) indiquant l’index de l’élément à rechercher après.</span><span class="sxs-lookup"><span data-stu-id="9ed5d-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed5d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ed5d-109">Return Value</span></span>

<span data-ttu-id="9ed5d-110">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="9ed5d-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed5d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9ed5d-111">Remarks</span></span>

<span data-ttu-id="9ed5d-112">Lorsqu’il n’y a plus d’éléments activés, cette méthode retourne 1.</span><span class="sxs-lookup"><span data-stu-id="9ed5d-112">When there are no further checked items, this method returns  1.</span></span>

<span data-ttu-id="9ed5d-113">Cette méthode a été remplacée par **getNextCheckedItem2**, qui prend en charge les sélections imbriquées.</span><span class="sxs-lookup"><span data-stu-id="9ed5d-113">This method has been replaced by **getNextCheckedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed5d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ed5d-114">Requirements</span></span>



| <span data-ttu-id="9ed5d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ed5d-115">Requirement</span></span> | <span data-ttu-id="9ed5d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ed5d-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9ed5d-117">Version</span><span class="sxs-lookup"><span data-stu-id="9ed5d-117">Version</span></span><br/> | <span data-ttu-id="9ed5d-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="9ed5d-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ed5d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ed5d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed5d-120">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9ed5d-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="9ed5d-121">**PLAYLIST. getNextCheckedItem2**</span><span class="sxs-lookup"><span data-stu-id="9ed5d-121">**PLAYLIST.getNextCheckedItem2**</span></span>](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





