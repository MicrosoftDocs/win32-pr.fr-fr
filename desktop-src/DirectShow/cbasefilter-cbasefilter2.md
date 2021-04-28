---
description: Méthode de constructeur de constructeur CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID).
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
ms.openlocfilehash: b621bdb3f6a15ae950959a65eba8841bde399b81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099827"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="73667-103">Constructeur CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)</span><span class="sxs-lookup"><span data-stu-id="73667-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="73667-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="73667-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="73667-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73667-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="73667-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73667-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="73667-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="73667-108">Pointeur vers une chaîne contenant le nom du filtre, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="73667-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="73667-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="73667-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="73667-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="73667-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="73667-111">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="73667-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="73667-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="73667-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="73667-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="73667-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="73667-114">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="73667-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="73667-115">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="73667-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="73667-116">Identificateur de classe (CLSID) du filtre.</span><span class="sxs-lookup"><span data-stu-id="73667-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73667-117">Notes </span><span class="sxs-lookup"><span data-stu-id="73667-117">Remarks</span></span>

<span data-ttu-id="73667-118">Pour l’objet de section critique, vous pouvez généralement effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="73667-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="73667-119">Dérivez une classe qui hérite à la fois de **CBaseFilter** et de **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="73667-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="73667-120">Pour *pLock*, transmettez le `this` pointeur.</span><span class="sxs-lookup"><span data-stu-id="73667-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="73667-121">Dérivez une classe qui hérite de **CBaseFilter** et qui contient une variable membre **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="73667-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="73667-122">Pour *pLock*, transmettez l’adresse de cette variable.</span><span class="sxs-lookup"><span data-stu-id="73667-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="73667-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73667-123">Requirements</span></span>



| <span data-ttu-id="73667-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73667-124">Requirement</span></span> | <span data-ttu-id="73667-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="73667-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73667-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="73667-126">Header</span></span><br/>  | <dl> <span data-ttu-id="73667-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73667-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="73667-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="73667-128">Library</span></span><br/> | <dl> <span data-ttu-id="73667-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="73667-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73667-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73667-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73667-131">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="73667-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




