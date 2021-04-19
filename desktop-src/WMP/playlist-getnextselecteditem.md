---
title: PLAYLIST. getNextSelectedItem
description: La méthode getNextSelectedItem récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Lecteur Windows Media PLAYLIST. getNextSelectedItem
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523879"
---
# <a name="playlistgetnextselecteditem"></a><span data-ttu-id="2709e-104">PLAYLIST. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="2709e-104">PLAYLIST.getNextSelectedItem</span></span>

<span data-ttu-id="2709e-105">La méthode **getNextSelectedItem** récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="2709e-105">The **getNextSelectedItem** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="2709e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2709e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2709e-107"><span id="item"></span><span id="ITEM"></span>*fiche*</span><span class="sxs-lookup"><span data-stu-id="2709e-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="2709e-108">**Nombre** (**long**) indiquant l’index de l’élément à rechercher après.</span><span class="sxs-lookup"><span data-stu-id="2709e-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2709e-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2709e-109">Return Value</span></span>

<span data-ttu-id="2709e-110">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="2709e-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2709e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2709e-111">Remarks</span></span>

<span data-ttu-id="2709e-112">Si aucun autre élément n’est sélectionné, cette méthode retourne 1.</span><span class="sxs-lookup"><span data-stu-id="2709e-112">When there are no further selected items, this method returns  1.</span></span>

<span data-ttu-id="2709e-113">Cette méthode a été remplacée par **getNextSelectedItem2**, qui prend en charge les sélections imbriquées.</span><span class="sxs-lookup"><span data-stu-id="2709e-113">This method has been replaced by **getNextSelectedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="2709e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2709e-114">Requirements</span></span>



| <span data-ttu-id="2709e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2709e-115">Requirement</span></span> | <span data-ttu-id="2709e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2709e-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2709e-117">Version</span><span class="sxs-lookup"><span data-stu-id="2709e-117">Version</span></span><br/> | <span data-ttu-id="2709e-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="2709e-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2709e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2709e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2709e-120">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="2709e-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="2709e-121">**PLAYLIST. getNextSelectedItem2**</span><span class="sxs-lookup"><span data-stu-id="2709e-121">**PLAYLIST.getNextSelectedItem2**</span></span>](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





