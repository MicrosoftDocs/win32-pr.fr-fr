---
title: PLAYLIST. setCheckedState2
description: La méthode setCheckedState2 définit l’état activé de l’élément avec l’index spécifié dans l’élément PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- Lecteur Windows Media PLAYLIST. setCheckedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528613"
---
# <a name="playlistsetcheckedstate2"></a><span data-ttu-id="19084-104">PLAYLIST. setCheckedState2</span><span class="sxs-lookup"><span data-stu-id="19084-104">PLAYLIST.setCheckedState2</span></span>

<span data-ttu-id="19084-105">La méthode **setCheckedState2** définit l’état activé de l’élément avec l’index spécifié dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="19084-105">The **setCheckedState2** method sets the checked state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a><span data-ttu-id="19084-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19084-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19084-107"><span id="item"></span><span id="ITEM"></span>*fiche*</span><span class="sxs-lookup"><span data-stu-id="19084-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="19084-108">**Nombre** (**long**) indiquant l’index de l’élément de sélection à activer ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="19084-108">**Number** (**long**) indicating the index of the playlist item to be checked or unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="19084-109"><span id="checked"></span><span id="CHECKED"></span>*désactivé*</span><span class="sxs-lookup"><span data-stu-id="19084-109"><span id="checked"></span><span id="CHECKED"></span>*checked*</span></span>
</dt> <dd>

<span data-ttu-id="19084-110">**Valeur booléenne** indiquant si l’élément spécifié doit être activé (true) ou désactivé (false).</span><span class="sxs-lookup"><span data-stu-id="19084-110">**Boolean** indicating whether the specified item is to be checked (true) or unchecked (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19084-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="19084-111">Return Value</span></span>

<span data-ttu-id="19084-112">Cette méthode retourne une **valeur booléenne**.</span><span class="sxs-lookup"><span data-stu-id="19084-112">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="19084-113">Notes</span><span class="sxs-lookup"><span data-stu-id="19084-113">Remarks</span></span>

<span data-ttu-id="19084-114">Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **setCheckedState** , qui ne peut pas.</span><span class="sxs-lookup"><span data-stu-id="19084-114">This method can work with nested playlists and replaces the **setCheckedState** method, which cannot.</span></span> <span data-ttu-id="19084-115">Vous pouvez définir tous les éléments à l’État demandé en spécifiant 1 dans le paramètre *Item* .</span><span class="sxs-lookup"><span data-stu-id="19084-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="19084-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19084-116">Requirements</span></span>



| <span data-ttu-id="19084-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19084-117">Requirement</span></span> | <span data-ttu-id="19084-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="19084-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="19084-119">Version</span><span class="sxs-lookup"><span data-stu-id="19084-119">Version</span></span><br/> | <span data-ttu-id="19084-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="19084-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19084-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19084-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19084-122">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="19084-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="19084-123">**PLAYLIST. setCheckedState**</span><span class="sxs-lookup"><span data-stu-id="19084-123">**PLAYLIST.setCheckedState**</span></span>](playlist-setcheckedstate.md)
</dt> </dl>

 

 





