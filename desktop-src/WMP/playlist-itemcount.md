---
title: PLAYLIST. itemCount
description: L’attribut itemCount récupère le nombre d’éléments actuellement affichés dans l’élément PLAYLIST.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- PLAYLIST. itemCount lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528829"
---
# <a name="playlistitemcount"></a><span data-ttu-id="21898-104">PLAYLIST. itemCount</span><span class="sxs-lookup"><span data-stu-id="21898-104">PLAYLIST.itemCount</span></span>

<span data-ttu-id="21898-105">L’attribut **ItemCount** récupère le nombre d’éléments actuellement affichés dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="21898-105">The **itemCount** attribute retrieves the number of items currently displayed in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a><span data-ttu-id="21898-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="21898-106">Possible Values</span></span>

<span data-ttu-id="21898-107">Cet attribut est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="21898-107">This attribute is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="21898-108">Notes</span><span class="sxs-lookup"><span data-stu-id="21898-108">Remarks</span></span>

<span data-ttu-id="21898-109">La propriété **ItemCount** compte le nombre total d’éléments développés.</span><span class="sxs-lookup"><span data-stu-id="21898-109">The **itemCount** property will count the total number of expanded items.</span></span> <span data-ttu-id="21898-110">Par exemple, s’il existe deux sélections contenant chacune trois éléments multimédias, **ItemCount** retourne 2 si les sélections ne sont pas développées.</span><span class="sxs-lookup"><span data-stu-id="21898-110">For example, if there are two playlists that contain three media items each, **itemCount** will return 2 if the playlists are not expanded.</span></span> <span data-ttu-id="21898-111">Si seule la première sélection est développée, **ItemCount** retourne 4.</span><span class="sxs-lookup"><span data-stu-id="21898-111">If only the first playlist is expanded, **itemCount** will return 4.</span></span> <span data-ttu-id="21898-112">Si les deux sélections sont développées, **ItemCount** retourne 6.</span><span class="sxs-lookup"><span data-stu-id="21898-112">If both playlists are expanded, **itemCount** will return 6.</span></span>

## <a name="requirements"></a><span data-ttu-id="21898-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21898-113">Requirements</span></span>



| <span data-ttu-id="21898-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21898-114">Requirement</span></span> | <span data-ttu-id="21898-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="21898-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="21898-116">Version</span><span class="sxs-lookup"><span data-stu-id="21898-116">Version</span></span><br/> | <span data-ttu-id="21898-117">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="21898-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21898-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21898-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21898-119">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="21898-119">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





