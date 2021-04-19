---
description: La méthode MoveToTail fractionne la liste et ajoute la partie d’en-tête à la fin d’une autre liste.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Méthode CBaseList. MoveToTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539276"
---
# <a name="cbaselistmovetotail-method"></a><span data-ttu-id="e6d5d-103">Méthode CBaseList. MoveToTail</span><span class="sxs-lookup"><span data-stu-id="e6d5d-103">CBaseList.MoveToTail method</span></span>

<span data-ttu-id="e6d5d-104">La `MoveToTail` méthode fractionne la liste et ajoute la partie d’en-tête à la fin d’une autre liste.</span><span class="sxs-lookup"><span data-stu-id="e6d5d-104">The `MoveToTail` method splits the list and appends the head portion to the tail of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d5d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6d5d-105">Syntax</span></span>


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="e6d5d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6d5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d5d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="e6d5d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d5d-108">Indicateur de position qui marque le fractionnement dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e6d5d-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="e6d5d-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="e6d5d-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d5d-110">Pointeur vers une autre liste.</span><span class="sxs-lookup"><span data-stu-id="e6d5d-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d5d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6d5d-111">Return value</span></span>

<span data-ttu-id="e6d5d-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e6d5d-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6d5d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e6d5d-113">Remarks</span></span>

<span data-ttu-id="e6d5d-114">Cette méthode fractionne la liste après la position spécifiée par le paramètre *pos* .</span><span class="sxs-lookup"><span data-stu-id="e6d5d-114">This method splits the list after the position specified by the *pos* parameter.</span></span> <span data-ttu-id="e6d5d-115">La partie fin reste dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e6d5d-115">The tail portion remains in the list.</span></span> <span data-ttu-id="e6d5d-116">La partie Head est ajoutée à la fin de l’autre liste.</span><span class="sxs-lookup"><span data-stu-id="e6d5d-116">The head portion is appended to the tail of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d5d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6d5d-117">Requirements</span></span>



| <span data-ttu-id="e6d5d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6d5d-118">Requirement</span></span> | <span data-ttu-id="e6d5d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6d5d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d5d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6d5d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e6d5d-121"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d5d-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e6d5d-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6d5d-122">Library</span></span><br/> | <dl> <span data-ttu-id="e6d5d-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d5d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6d5d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6d5d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d5d-125">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="e6d5d-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




