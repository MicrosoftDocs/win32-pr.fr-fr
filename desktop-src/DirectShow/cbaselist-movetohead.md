---
description: La méthode MoveToHead fractionne la liste et insère la partie de la fin à l’en-tête d’une autre liste.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Méthode CBaseList. MoveToHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539688"
---
# <a name="cbaselistmovetohead-method"></a><span data-ttu-id="00ea7-103">Méthode CBaseList. MoveToHead</span><span class="sxs-lookup"><span data-stu-id="00ea7-103">CBaseList.MoveToHead method</span></span>

<span data-ttu-id="00ea7-104">La `MoveToHead` méthode fractionne la liste et insère la partie de la fin à l’en-tête d’une autre liste.</span><span class="sxs-lookup"><span data-stu-id="00ea7-104">The `MoveToHead` method splits the list and inserts the tail portion at the head of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ea7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00ea7-105">Syntax</span></span>


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="00ea7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00ea7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ea7-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="00ea7-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="00ea7-108">Indicateur de position qui marque le fractionnement dans la liste.</span><span class="sxs-lookup"><span data-stu-id="00ea7-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="00ea7-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="00ea7-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="00ea7-110">Pointeur vers une autre liste.</span><span class="sxs-lookup"><span data-stu-id="00ea7-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ea7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00ea7-111">Return value</span></span>

<span data-ttu-id="00ea7-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="00ea7-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ea7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="00ea7-113">Remarks</span></span>

<span data-ttu-id="00ea7-114">Cette méthode fractionne la liste avant la position spécifiée par le paramètre *pos* .</span><span class="sxs-lookup"><span data-stu-id="00ea7-114">This method splits the list before the position specified by the *pos* parameter.</span></span> <span data-ttu-id="00ea7-115">La partie Head reste dans la liste.</span><span class="sxs-lookup"><span data-stu-id="00ea7-115">The head portion remains in the list.</span></span> <span data-ttu-id="00ea7-116">La partie fin est insérée au début de l’autre liste.</span><span class="sxs-lookup"><span data-stu-id="00ea7-116">The tail portion is inserted at the head of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="00ea7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00ea7-117">Requirements</span></span>



| <span data-ttu-id="00ea7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00ea7-118">Requirement</span></span> | <span data-ttu-id="00ea7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="00ea7-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ea7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="00ea7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="00ea7-121"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00ea7-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="00ea7-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="00ea7-122">Library</span></span><br/> | <dl> <span data-ttu-id="00ea7-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="00ea7-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00ea7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00ea7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ea7-125">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="00ea7-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




