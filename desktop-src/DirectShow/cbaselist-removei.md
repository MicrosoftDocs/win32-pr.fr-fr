---
description: La méthode Removei supprime l’élément à la position spécifiée.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: CBaseList. Removei, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537591"
---
# <a name="cbaselistremovei-method"></a><span data-ttu-id="b14f7-103">CBaseList. Removei, méthode</span><span class="sxs-lookup"><span data-stu-id="b14f7-103">CBaseList.RemoveI method</span></span>

<span data-ttu-id="b14f7-104">La `RemoveI` méthode supprime l’élément à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b14f7-104">The `RemoveI` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="b14f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b14f7-105">Syntax</span></span>


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="b14f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b14f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b14f7-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="b14f7-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="b14f7-108">Valeur de POSITION indiquant l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b14f7-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b14f7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b14f7-109">Return value</span></span>

<span data-ttu-id="b14f7-110">Retourne un pointeur vers l’élément.</span><span class="sxs-lookup"><span data-stu-id="b14f7-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b14f7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b14f7-111">Remarks</span></span>

<span data-ttu-id="b14f7-112">Cette méthode supprime le nœud de la liste, mais ne supprime pas l’élément contenu dans ce nœud.</span><span class="sxs-lookup"><span data-stu-id="b14f7-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="b14f7-113">Si *pos* a la **valeur null**, la méthode retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b14f7-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b14f7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b14f7-114">Requirements</span></span>



| <span data-ttu-id="b14f7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b14f7-115">Requirement</span></span> | <span data-ttu-id="b14f7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b14f7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b14f7-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b14f7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b14f7-118"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b14f7-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b14f7-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b14f7-119">Library</span></span><br/> | <dl> <span data-ttu-id="b14f7-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b14f7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b14f7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b14f7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14f7-122">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="b14f7-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




