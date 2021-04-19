---
description: La méthode AddTail ajoute une autre liste à la fin de cette liste.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Méthode CBaseList. AddTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545496"
---
# <a name="cbaselistaddtail-method"></a><span data-ttu-id="d617d-103">Méthode CBaseList. AddTail</span><span class="sxs-lookup"><span data-stu-id="d617d-103">CBaseList.AddTail method</span></span>

<span data-ttu-id="d617d-104">La `AddTail` méthode ajoute une autre liste à la fin de cette liste.</span><span class="sxs-lookup"><span data-stu-id="d617d-104">The `AddTail` method appends another list to the end of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d617d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d617d-105">Syntax</span></span>


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="d617d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d617d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d617d-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="d617d-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="d617d-108">Pointeur vers la liste à ajouter.</span><span class="sxs-lookup"><span data-stu-id="d617d-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d617d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d617d-109">Return value</span></span>

<span data-ttu-id="d617d-110">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d617d-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d617d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d617d-111">Remarks</span></span>

<span data-ttu-id="d617d-112">Si la méthode échoue, il se peut que certains éléments aient été ajoutés à la liste.</span><span class="sxs-lookup"><span data-stu-id="d617d-112">If the method fails, some items may have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="d617d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d617d-113">Requirements</span></span>



| <span data-ttu-id="d617d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d617d-114">Requirement</span></span> | <span data-ttu-id="d617d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d617d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d617d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d617d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d617d-117"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d617d-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d617d-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d617d-118">Library</span></span><br/> | <dl> <span data-ttu-id="d617d-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d617d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d617d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d617d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d617d-121">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="d617d-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




