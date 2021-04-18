---
description: La méthode RemoveHeadI supprime le premier élément de la liste.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Méthode CBaseList. RemoveHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528898"
---
# <a name="cbaselistremoveheadi-method"></a><span data-ttu-id="3f7dc-103">Méthode CBaseList. RemoveHeadI</span><span class="sxs-lookup"><span data-stu-id="3f7dc-103">CBaseList.RemoveHeadI method</span></span>

<span data-ttu-id="3f7dc-104">La `RemoveHeadI` méthode supprime le premier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-104">The `RemoveHeadI` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f7dc-105">Syntax</span></span>


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a><span data-ttu-id="3f7dc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f7dc-106">Parameters</span></span>

<span data-ttu-id="3f7dc-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f7dc-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f7dc-108">Return value</span></span>

<span data-ttu-id="3f7dc-109">Retourne un pointeur vers l’élément, ou **null** si la liste est vide.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f7dc-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3f7dc-110">Remarks</span></span>

<span data-ttu-id="3f7dc-111">Cette méthode supprime le nœud de liste, mais pas l’élément contenu dans le nœud.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f7dc-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f7dc-112">Requirements</span></span>



| <span data-ttu-id="3f7dc-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f7dc-113">Requirement</span></span> | <span data-ttu-id="3f7dc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f7dc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7dc-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f7dc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3f7dc-116"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f7dc-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3f7dc-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f7dc-117">Library</span></span><br/> | <dl> <span data-ttu-id="3f7dc-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3f7dc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f7dc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f7dc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7dc-120">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="3f7dc-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




