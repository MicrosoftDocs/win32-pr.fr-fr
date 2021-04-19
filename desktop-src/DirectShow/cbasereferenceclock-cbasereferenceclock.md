---
description: Méthode de constructeur.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Constructeur CBaseReferenceClock. CBaseReferenceClock (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ad593d488e367ad6e902b0c931ffbfc3f741a53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529915"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="ce0ac-103">Constructeur CBaseReferenceClock. CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="ce0ac-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="ce0ac-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ce0ac-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce0ac-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="ce0ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce0ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce0ac-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ce0ac-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ce0ac-108">Pointeur vers une chaîne contenant le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ce0ac-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="ce0ac-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="ce0ac-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce0ac-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ce0ac-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ce0ac-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="ce0ac-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="ce0ac-112">Si l’objet est agrégé, passer un pointeur vers l’interface IUnknown de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="ce0ac-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="ce0ac-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ce0ac-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce0ac-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="ce0ac-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ce0ac-115">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce0ac-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ce0ac-116">Si une erreur se produit, la méthode retourne un code d’erreur dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ce0ac-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="ce0ac-117">N’affectez pas la **valeur null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ce0ac-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce0ac-118">*pSched*</span><span class="sxs-lookup"><span data-stu-id="ce0ac-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="ce0ac-119">Pointeur vers un objet [**CAMSchedule**](camschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="ce0ac-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="ce0ac-120">Si la **valeur est null**, cette méthode crée un nouvel objet **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="ce0ac-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce0ac-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce0ac-121">Requirements</span></span>



| <span data-ttu-id="ce0ac-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce0ac-122">Requirement</span></span> | <span data-ttu-id="ce0ac-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce0ac-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0ac-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce0ac-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ce0ac-125"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce0ac-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ce0ac-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce0ac-126">Library</span></span><br/> | <dl> <span data-ttu-id="ce0ac-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce0ac-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce0ac-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce0ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0ac-129">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="ce0ac-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




