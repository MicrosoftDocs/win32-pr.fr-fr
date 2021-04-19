---
description: Méthode de constructeur.
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
ms.openlocfilehash: b4d8806c9b4103c06eb58e11547e83fc933d5d3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532628"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="f5bd3-103">Constructeur CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* )</span><span class="sxs-lookup"><span data-stu-id="f5bd3-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="f5bd3-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5bd3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5bd3-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f5bd3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5bd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5bd3-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f5bd3-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f5bd3-108">Pointeur vers une chaîne contenant le nom du filtre, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="f5bd3-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="f5bd3-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f5bd3-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="f5bd3-111">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="f5bd3-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f5bd3-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="f5bd3-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="f5bd3-114">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="f5bd3-115">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="f5bd3-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="f5bd3-116">Identificateur de classe (CLSID) du filtre.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="f5bd3-117">*phr*</span><span class="sxs-lookup"><span data-stu-id="f5bd3-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f5bd3-118">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5bd3-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="f5bd3-119">Le constructeur ignore ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5bd3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f5bd3-120">Remarks</span></span>

<span data-ttu-id="f5bd3-121">Pour l’objet de section critique, vous pouvez généralement effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5bd3-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="f5bd3-122">Dérivez une classe qui hérite à la fois de **CBaseFilter** et de **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="f5bd3-123">Pour *pLock*, transmettez le `this` pointeur.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="f5bd3-124">Dérivez une classe qui hérite de **CBaseFilter** et qui contient une variable membre **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="f5bd3-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="f5bd3-125">Pour *pLock*, transmettez l’adresse de cette variable.</span><span class="sxs-lookup"><span data-stu-id="f5bd3-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5bd3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5bd3-126">Requirements</span></span>



| <span data-ttu-id="f5bd3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5bd3-127">Requirement</span></span> | <span data-ttu-id="f5bd3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5bd3-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bd3-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5bd3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f5bd3-130"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5bd3-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f5bd3-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5bd3-131">Library</span></span><br/> | <dl> <span data-ttu-id="f5bd3-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f5bd3-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5bd3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5bd3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bd3-134">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f5bd3-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




