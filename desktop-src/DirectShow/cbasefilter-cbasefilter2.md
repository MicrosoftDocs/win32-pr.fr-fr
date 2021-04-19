---
description: Méthode de constructeur.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID), constructeur (Amfilter. h)
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
ms.openlocfilehash: 40ac48a1fd28b9b50a8f1fa9c698ea5db49d97b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539522"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="a93aa-103">Constructeur CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)</span><span class="sxs-lookup"><span data-stu-id="a93aa-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="a93aa-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="a93aa-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a93aa-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="a93aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a93aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a93aa-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="a93aa-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a93aa-108">Pointeur vers une chaîne contenant le nom du filtre, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="a93aa-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="a93aa-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="a93aa-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a93aa-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="a93aa-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="a93aa-111">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="a93aa-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="a93aa-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="a93aa-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a93aa-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="a93aa-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="a93aa-114">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="a93aa-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="a93aa-115">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="a93aa-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="a93aa-116">Identificateur de classe (CLSID) du filtre.</span><span class="sxs-lookup"><span data-stu-id="a93aa-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a93aa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a93aa-117">Remarks</span></span>

<span data-ttu-id="a93aa-118">Pour l’objet de section critique, vous pouvez généralement effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a93aa-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="a93aa-119">Dérivez une classe qui hérite à la fois de **CBaseFilter** et de **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="a93aa-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="a93aa-120">Pour *pLock*, transmettez le `this` pointeur.</span><span class="sxs-lookup"><span data-stu-id="a93aa-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="a93aa-121">Dérivez une classe qui hérite de **CBaseFilter** et qui contient une variable membre **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="a93aa-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="a93aa-122">Pour *pLock*, transmettez l’adresse de cette variable.</span><span class="sxs-lookup"><span data-stu-id="a93aa-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a93aa-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a93aa-123">Requirements</span></span>



| <span data-ttu-id="a93aa-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a93aa-124">Requirement</span></span> | <span data-ttu-id="a93aa-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a93aa-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a93aa-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a93aa-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a93aa-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a93aa-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a93aa-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a93aa-128">Library</span></span><br/> | <dl> <span data-ttu-id="a93aa-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a93aa-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a93aa-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a93aa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93aa-131">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="a93aa-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




