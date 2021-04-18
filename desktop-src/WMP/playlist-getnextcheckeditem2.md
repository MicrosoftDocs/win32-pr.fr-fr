---
title: PLAYLIST. getNextCheckedItem2
description: La méthode getNextCheckedItem2 récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- Lecteur Windows Media PLAYLIST. getNextCheckedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540167"
---
# <a name="playlistgetnextcheckeditem2"></a><span data-ttu-id="cd03b-104">PLAYLIST. getNextCheckedItem2</span><span class="sxs-lookup"><span data-stu-id="cd03b-104">PLAYLIST.getNextCheckedItem2</span></span>

<span data-ttu-id="cd03b-105">La méthode **getNextCheckedItem2** récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd03b-105">The **getNextCheckedItem2** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="cd03b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd03b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd03b-107"><span id="item"></span><span id="ITEM"></span>*fiche*</span><span class="sxs-lookup"><span data-stu-id="cd03b-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="cd03b-108">**Nombre** (**long**) indiquant l’index de l’élément à rechercher après.</span><span class="sxs-lookup"><span data-stu-id="cd03b-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd03b-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cd03b-109">Return Value</span></span>

<span data-ttu-id="cd03b-110">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="cd03b-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd03b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cd03b-111">Remarks</span></span>

<span data-ttu-id="cd03b-112">Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **getNextCheckedItem** , qui ne peut pas.</span><span class="sxs-lookup"><span data-stu-id="cd03b-112">This method can work with nested playlists and replaces the **getNextCheckedItem** method, which cannot.</span></span> <span data-ttu-id="cd03b-113">Passe 1 dans le paramètre d' *élément* pour rechercher le premier élément activé.</span><span class="sxs-lookup"><span data-stu-id="cd03b-113">Pass  1 in the *item* parameter to find the first checked item.</span></span> <span data-ttu-id="cd03b-114">Lorsqu’il n’y a plus d’éléments activés, cette méthode retourne 1.</span><span class="sxs-lookup"><span data-stu-id="cd03b-114">When there are no further checked items, this method returns  1.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd03b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd03b-115">Requirements</span></span>



| <span data-ttu-id="cd03b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd03b-116">Requirement</span></span> | <span data-ttu-id="cd03b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd03b-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="cd03b-118">Version</span><span class="sxs-lookup"><span data-stu-id="cd03b-118">Version</span></span><br/> | <span data-ttu-id="cd03b-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cd03b-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd03b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd03b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd03b-121">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="cd03b-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="cd03b-122">**PLAYLIST. getNextCheckedItem**</span><span class="sxs-lookup"><span data-stu-id="cd03b-122">**PLAYLIST.getNextCheckedItem**</span></span>](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





