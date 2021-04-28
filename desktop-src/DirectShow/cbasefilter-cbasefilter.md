---
description: Méthode de constructeur de constructeur CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ).
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID, HRESULT *), constructeur (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120107"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="ebf11-103">Constructeur CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* )</span><span class="sxs-lookup"><span data-stu-id="ebf11-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="ebf11-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ebf11-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf11-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf11-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ebf11-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebf11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf11-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ebf11-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf11-108">Pointeur vers une chaîne contenant le nom du filtre, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="ebf11-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="ebf11-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ebf11-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf11-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="ebf11-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="ebf11-111">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="ebf11-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ebf11-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ebf11-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ebf11-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="ebf11-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf11-114">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="ebf11-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="ebf11-115">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="ebf11-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf11-116">Identificateur de classe (CLSID) du filtre.</span><span class="sxs-lookup"><span data-stu-id="ebf11-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="ebf11-117">*phr*</span><span class="sxs-lookup"><span data-stu-id="ebf11-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf11-118">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ebf11-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ebf11-119">Le constructeur ignore ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ebf11-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebf11-120">Notes </span><span class="sxs-lookup"><span data-stu-id="ebf11-120">Remarks</span></span>

<span data-ttu-id="ebf11-121">Pour l’objet de section critique, vous pouvez généralement effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ebf11-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="ebf11-122">Dérivez une classe qui hérite à la fois de **CBaseFilter** et de **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="ebf11-123">Pour *pLock*, transmettez le `this` pointeur.</span><span class="sxs-lookup"><span data-stu-id="ebf11-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="ebf11-124">Dérivez une classe qui hérite de **CBaseFilter** et qui contient une variable membre **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="ebf11-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="ebf11-125">Pour *pLock*, transmettez l’adresse de cette variable.</span><span class="sxs-lookup"><span data-stu-id="ebf11-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf11-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf11-126">Requirements</span></span>



| <span data-ttu-id="ebf11-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebf11-127">Requirement</span></span> | <span data-ttu-id="ebf11-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf11-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf11-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebf11-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ebf11-130"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebf11-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ebf11-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ebf11-131">Library</span></span><br/> | <dl> <span data-ttu-id="ebf11-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ebf11-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf11-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf11-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf11-134">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="ebf11-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




