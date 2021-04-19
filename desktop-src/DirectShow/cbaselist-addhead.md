---
description: La méthode AddHead insère une autre liste au début de cette liste.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Méthode CBaseList. AddHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532227"
---
# <a name="cbaselistaddhead-method"></a><span data-ttu-id="4fae7-103">Méthode CBaseList. AddHead</span><span class="sxs-lookup"><span data-stu-id="4fae7-103">CBaseList.AddHead method</span></span>

<span data-ttu-id="4fae7-104">La `AddHead` méthode insère une autre liste au début de cette liste.</span><span class="sxs-lookup"><span data-stu-id="4fae7-104">The `AddHead` method inserts another list at the front of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fae7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fae7-105">Syntax</span></span>


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="4fae7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fae7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fae7-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="4fae7-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="4fae7-108">Pointeur vers la liste des éléments à ajouter.</span><span class="sxs-lookup"><span data-stu-id="4fae7-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fae7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4fae7-109">Return value</span></span>

<span data-ttu-id="4fae7-110">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4fae7-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fae7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4fae7-111">Remarks</span></span>

<span data-ttu-id="4fae7-112">Si la méthode échoue, il se peut que certains éléments aient été ajoutés à la liste.</span><span class="sxs-lookup"><span data-stu-id="4fae7-112">If the method fails, some items might have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fae7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fae7-113">Requirements</span></span>



| <span data-ttu-id="4fae7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fae7-114">Requirement</span></span> | <span data-ttu-id="4fae7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fae7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fae7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fae7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4fae7-117"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fae7-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4fae7-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4fae7-118">Library</span></span><br/> | <dl> <span data-ttu-id="4fae7-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4fae7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fae7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fae7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fae7-121">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="4fae7-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




