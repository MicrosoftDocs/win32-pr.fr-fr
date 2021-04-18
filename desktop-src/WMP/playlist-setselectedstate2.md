---
title: PLAYLIST. setSelectedState2
description: La méthode setSelectedState2 définit l’état sélectionné de l’élément avec l’index spécifié dans l’élément PLAYLIST.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- Lecteur Windows Media PLAYLIST. setSelectedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543194"
---
# <a name="playlistsetselectedstate2"></a><span data-ttu-id="0165f-104">PLAYLIST. setSelectedState2</span><span class="sxs-lookup"><span data-stu-id="0165f-104">PLAYLIST.setSelectedState2</span></span>

<span data-ttu-id="0165f-105">La méthode **setSelectedState2** définit l’état sélectionné de l’élément avec l’index spécifié dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="0165f-105">The **setSelectedState2** method sets the selected state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a><span data-ttu-id="0165f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0165f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0165f-107"><span id="item"></span><span id="ITEM"></span>*fiche*</span><span class="sxs-lookup"><span data-stu-id="0165f-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="0165f-108">**Nombre** (**long**) indiquant l’index d’un élément dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="0165f-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="0165f-109"><span id="selected"></span><span id="SELECTED"></span>*sélectionné*</span><span class="sxs-lookup"><span data-stu-id="0165f-109"><span id="selected"></span><span id="SELECTED"></span>*selected*</span></span>
</dt> <dd>

<span data-ttu-id="0165f-110">**Valeur booléenne** indiquant si l’élément spécifié doit être sélectionné (true) ou non sélectionné (false).</span><span class="sxs-lookup"><span data-stu-id="0165f-110">**Boolean** indicating whether the specified item is to be selected (true) or unselected (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0165f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0165f-111">Return Value</span></span>

<span data-ttu-id="0165f-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0165f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0165f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0165f-113">Remarks</span></span>

<span data-ttu-id="0165f-114">Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **setSelectedState** qui ne le peut pas.</span><span class="sxs-lookup"><span data-stu-id="0165f-114">This method can work with nested playlists and replaces the **setSelectedState** method which cannot.</span></span> <span data-ttu-id="0165f-115">Vous pouvez définir tous les éléments à l’État demandé en spécifiant 1 dans le paramètre *Item* .</span><span class="sxs-lookup"><span data-stu-id="0165f-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0165f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0165f-116">Requirements</span></span>



| <span data-ttu-id="0165f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0165f-117">Requirement</span></span> | <span data-ttu-id="0165f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0165f-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0165f-119">Version</span><span class="sxs-lookup"><span data-stu-id="0165f-119">Version</span></span><br/> | <span data-ttu-id="0165f-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0165f-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0165f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0165f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0165f-122">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="0165f-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="0165f-123">**PLAYLIST. setSelectedState**</span><span class="sxs-lookup"><span data-stu-id="0165f-123">**PLAYLIST.setSelectedState**</span></span>](playlist-setselectedstate.md)
</dt> </dl>

 

 





