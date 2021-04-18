---
title: PLAYLIST. getNextSelectedItem2
description: La méthode getNextSelectedItem2 récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- Lecteur Windows Media PLAYLIST. getNextSelectedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540166"
---
# <a name="playlistgetnextselecteditem2"></a><span data-ttu-id="ed6e1-104">PLAYLIST. getNextSelectedItem2</span><span class="sxs-lookup"><span data-stu-id="ed6e1-104">PLAYLIST.getNextSelectedItem2</span></span>

<span data-ttu-id="ed6e1-105">La méthode **getNextSelectedItem2** récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-105">The **getNextSelectedItem2** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="ed6e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed6e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed6e1-107"><span id="item"></span><span id="ITEM"></span>*fiche*</span><span class="sxs-lookup"><span data-stu-id="ed6e1-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="ed6e1-108">**Nombre** (**long**) indiquant l’index de l’élément à rechercher après.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed6e1-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ed6e1-109">Return Value</span></span>

<span data-ttu-id="ed6e1-110">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="ed6e1-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed6e1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ed6e1-111">Remarks</span></span>

<span data-ttu-id="ed6e1-112">Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **getNextSelectedItem** , qui ne peut pas.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-112">This method can work with nested playlists and replaces the **getNextSelectedItem** method, which cannot.</span></span> <span data-ttu-id="ed6e1-113">Passe 1 dans le paramètre *Item* pour rechercher le premier élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-113">Pass  1 in the *item* parameter to find the first selected item.</span></span> <span data-ttu-id="ed6e1-114">Si aucun autre élément n’est sélectionné,-1 est retourné.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-114">When there are no further selected items, -1 is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed6e1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed6e1-115">Requirements</span></span>



| <span data-ttu-id="ed6e1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed6e1-116">Requirement</span></span> | <span data-ttu-id="ed6e1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed6e1-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ed6e1-118">Version</span><span class="sxs-lookup"><span data-stu-id="ed6e1-118">Version</span></span><br/> | <span data-ttu-id="ed6e1-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ed6e1-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed6e1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed6e1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed6e1-121">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="ed6e1-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="ed6e1-122">**PLAYLIST. getNextSelectedItem**</span><span class="sxs-lookup"><span data-stu-id="ed6e1-122">**PLAYLIST.getNextSelectedItem**</span></span>](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





