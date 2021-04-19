---
title: PLAYLIST. setSelectedState
description: La méthode setSelectedState spécifie que l’élément indexé dans la sélection est sélectionné.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- Lecteur Windows Media PLAYLIST. setSelectedState
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531153"
---
# <a name="playlistsetselectedstate"></a><span data-ttu-id="b3c46-104">PLAYLIST. setSelectedState</span><span class="sxs-lookup"><span data-stu-id="b3c46-104">PLAYLIST.setSelectedState</span></span>

<span data-ttu-id="b3c46-105">La méthode **setSelectedState** spécifie que l’élément indexé dans la sélection est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b3c46-105">The **setSelectedState** method specifies that the indexed item in the playlist is selected.</span></span>

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a><span data-ttu-id="b3c46-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3c46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c46-107"><span id="item"></span><span id="ITEM"></span>*fiche*</span><span class="sxs-lookup"><span data-stu-id="b3c46-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="b3c46-108">**Nombre** (**long**) indiquant l’index d’un élément dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="b3c46-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c46-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b3c46-109">Return Value</span></span>

<span data-ttu-id="b3c46-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b3c46-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c46-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b3c46-111">Remarks</span></span>

<span data-ttu-id="b3c46-112">Vous pouvez définir tous les éléments à l’état sélectionné en spécifiant 1 dans le paramètre *Item* .</span><span class="sxs-lookup"><span data-stu-id="b3c46-112">You can set all items to the selected state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="b3c46-113">Cette méthode a été remplacée par **setSelectedState2**, qui prend en charge les sélections imbriquées.</span><span class="sxs-lookup"><span data-stu-id="b3c46-113">This method has been replaced by **setSelectedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c46-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3c46-114">Requirements</span></span>



| <span data-ttu-id="b3c46-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3c46-115">Requirement</span></span> | <span data-ttu-id="b3c46-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c46-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b3c46-117">Version</span><span class="sxs-lookup"><span data-stu-id="b3c46-117">Version</span></span><br/> | <span data-ttu-id="b3c46-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="b3c46-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3c46-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c46-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c46-120">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="b3c46-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="b3c46-121">**PLAYLIST. setSelectedState2**</span><span class="sxs-lookup"><span data-stu-id="b3c46-121">**PLAYLIST.setSelectedState2**</span></span>](playlist-setselectedstate2.md)
</dt> </dl>

 

 





