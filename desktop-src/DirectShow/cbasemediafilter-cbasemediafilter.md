---
description: Méthode constructeur CBaseMediaFilter. CBaseMediaFilter.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Constructeur CBaseMediaFilter. CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096317"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="59c61-103">Constructeur CBaseMediaFilter. CBaseMediaFilter</span><span class="sxs-lookup"><span data-stu-id="59c61-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="59c61-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="59c61-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c61-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59c61-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="59c61-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59c61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c61-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="59c61-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="59c61-108">Pointeur vers une chaîne contenant le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="59c61-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="59c61-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="59c61-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="59c61-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="59c61-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="59c61-111">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="59c61-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="59c61-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="59c61-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59c61-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="59c61-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="59c61-114">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="59c61-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="59c61-115">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="59c61-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="59c61-116">Identificateur de classe de l’objet.</span><span class="sxs-lookup"><span data-stu-id="59c61-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59c61-117">Notes </span><span class="sxs-lookup"><span data-stu-id="59c61-117">Remarks</span></span>

<span data-ttu-id="59c61-118">Si un autre objet contient ou agrège l' `CBaseMediaFilter` objet, le verrou **CCritSec** peut être externe à l' `CBaseMediaFilter` objet.</span><span class="sxs-lookup"><span data-stu-id="59c61-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="59c61-119">Dans ce cas, transmettez un pointeur vers le verrou dans *pLock*.</span><span class="sxs-lookup"><span data-stu-id="59c61-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="59c61-120">Dans le cas contraire, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="59c61-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="59c61-121">Dérivez une classe qui hérite à la fois `CBaseMediaFilter` de et de **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="59c61-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="59c61-122">Pour *pLock*, transmettez le pointeur this.</span><span class="sxs-lookup"><span data-stu-id="59c61-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="59c61-123">Dérivez une classe qui hérite de `CBaseMediaFilter` et contient une variable membre **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="59c61-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="59c61-124">Pour *pLock*, transmettez l’adresse de cette variable.</span><span class="sxs-lookup"><span data-stu-id="59c61-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c61-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59c61-125">Requirements</span></span>



| <span data-ttu-id="59c61-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59c61-126">Requirement</span></span> | <span data-ttu-id="59c61-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c61-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c61-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="59c61-128">Header</span></span><br/>  | <dl> <span data-ttu-id="59c61-129"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59c61-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="59c61-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59c61-130">Library</span></span><br/> | <dl> <span data-ttu-id="59c61-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59c61-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c61-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c61-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c61-133">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="59c61-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




