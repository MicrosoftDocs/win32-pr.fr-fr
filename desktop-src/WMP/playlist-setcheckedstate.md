---
title: PLAYLIST. setCheckedState
description: La méthode setCheckedState spécifie que l’élément indexé dans la sélection est coché.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- Lecteur Windows Media PLAYLIST. setCheckedState
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539546"
---
# <a name="playlistsetcheckedstate"></a><span data-ttu-id="91eaf-104">PLAYLIST. setCheckedState</span><span class="sxs-lookup"><span data-stu-id="91eaf-104">PLAYLIST.setCheckedState</span></span>

<span data-ttu-id="91eaf-105">La méthode **setCheckedState** spécifie que l’élément indexé dans la sélection est coché.</span><span class="sxs-lookup"><span data-stu-id="91eaf-105">The **setCheckedState** method specifies that the indexed item in the playlist is checked.</span></span>

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a><span data-ttu-id="91eaf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91eaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91eaf-107"><span id="item"></span><span id="ITEM"></span>*fiche*</span><span class="sxs-lookup"><span data-stu-id="91eaf-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="91eaf-108">**Nombre** (**long**) indiquant l’index de l’élément de sélection à vérifier.</span><span class="sxs-lookup"><span data-stu-id="91eaf-108">**Number** (**long**) indicating the index of the playlist item to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91eaf-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91eaf-109">Return Value</span></span>

<span data-ttu-id="91eaf-110">Cette méthode retourne une **valeur booléenne**.</span><span class="sxs-lookup"><span data-stu-id="91eaf-110">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="91eaf-111">Notes</span><span class="sxs-lookup"><span data-stu-id="91eaf-111">Remarks</span></span>

<span data-ttu-id="91eaf-112">Vous pouvez définir tous les éléments à l’état activé en spécifiant 1 dans le paramètre *Item* .</span><span class="sxs-lookup"><span data-stu-id="91eaf-112">You can set all items to the checked state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="91eaf-113">Cette méthode a été remplacée par **setCheckedState2**, qui prend en charge les sélections imbriquées.</span><span class="sxs-lookup"><span data-stu-id="91eaf-113">This method has been replaced by **setCheckedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="91eaf-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91eaf-114">Requirements</span></span>



| <span data-ttu-id="91eaf-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91eaf-115">Requirement</span></span> | <span data-ttu-id="91eaf-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="91eaf-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="91eaf-117">Version</span><span class="sxs-lookup"><span data-stu-id="91eaf-117">Version</span></span><br/> | <span data-ttu-id="91eaf-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="91eaf-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91eaf-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91eaf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91eaf-120">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="91eaf-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="91eaf-121">**PLAYLIST. setCheckedState2**</span><span class="sxs-lookup"><span data-stu-id="91eaf-121">**PLAYLIST.setCheckedState2**</span></span>](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





