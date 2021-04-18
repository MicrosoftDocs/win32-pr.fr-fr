---
description: La méthode PREV récupère la position précédente dans la liste.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: CBaseList. prev, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526104"
---
# <a name="cbaselistprev-method"></a><span data-ttu-id="9d2e9-103">CBaseList. prev, méthode</span><span class="sxs-lookup"><span data-stu-id="9d2e9-103">CBaseList.Prev method</span></span>

<span data-ttu-id="9d2e9-104">La `Prev` méthode récupère la position précédente dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-104">The `Prev` method retrieves the previous position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d2e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d2e9-105">Syntax</span></span>


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="9d2e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d2e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d2e9-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="9d2e9-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="9d2e9-108">Valeur de POSITION.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d2e9-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d2e9-109">Return value</span></span>

<span data-ttu-id="9d2e9-110">Retourne l’indicateur de position qui est le précédent à la position spécifiée dans *pos*.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-110">Returns the position indicator that is previous to the position specified in *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d2e9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9d2e9-111">Remarks</span></span>

<span data-ttu-id="9d2e9-112">Si *pos* est la première position dans la liste, la méthode retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-112">If *pos* is the first position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="9d2e9-113">Si *pos* a la **valeur null**, la méthode retourne la dernière position dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9d2e9-113">If *pos* is **NULL**, the method returns the last position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d2e9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d2e9-114">Requirements</span></span>



| <span data-ttu-id="9d2e9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d2e9-115">Requirement</span></span> | <span data-ttu-id="9d2e9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d2e9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d2e9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d2e9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9d2e9-118"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d2e9-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9d2e9-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d2e9-119">Library</span></span><br/> | <dl> <span data-ttu-id="9d2e9-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9d2e9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d2e9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d2e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d2e9-122">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="9d2e9-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




