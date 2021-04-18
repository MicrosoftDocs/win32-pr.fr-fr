---
description: La méthode RemoveTailI supprime le dernier élément de la liste.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Méthode CBaseList. RemoveTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543264"
---
# <a name="cbaselistremovetaili-method"></a><span data-ttu-id="2ce57-103">Méthode CBaseList. RemoveTailI</span><span class="sxs-lookup"><span data-stu-id="2ce57-103">CBaseList.RemoveTailI method</span></span>

<span data-ttu-id="2ce57-104">La `RemoveTailI` méthode supprime le dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="2ce57-104">The `RemoveTailI` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce57-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ce57-105">Syntax</span></span>


```C++
void* RemoveTailI();
```



## <a name="parameters"></a><span data-ttu-id="2ce57-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ce57-106">Parameters</span></span>

<span data-ttu-id="2ce57-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2ce57-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ce57-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ce57-108">Return value</span></span>

<span data-ttu-id="2ce57-109">Retourne un pointeur vers l’élément, ou **null** si la liste est vide.</span><span class="sxs-lookup"><span data-stu-id="2ce57-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce57-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2ce57-110">Remarks</span></span>

<span data-ttu-id="2ce57-111">Cette méthode supprime le nœud de liste, mais pas l’élément contenu dans le nœud.</span><span class="sxs-lookup"><span data-stu-id="2ce57-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce57-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ce57-112">Requirements</span></span>



| <span data-ttu-id="2ce57-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ce57-113">Requirement</span></span> | <span data-ttu-id="2ce57-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ce57-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce57-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ce57-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2ce57-116"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce57-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2ce57-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2ce57-117">Library</span></span><br/> | <dl> <span data-ttu-id="2ce57-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce57-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce57-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ce57-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce57-120">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="2ce57-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




