---
description: Méthode constructeur CSourceSeeking. CSourceSeeking.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Constructeur CSourceSeeking. CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098817"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="0fcc5-103">Constructeur CSourceSeeking. CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="0fcc5-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="0fcc5-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fcc5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fcc5-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="0fcc5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fcc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fcc5-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="0fcc5-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0fcc5-108">Pointeur vers une chaîne contenant le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="0fcc5-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0fcc5-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fcc5-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="0fcc5-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0fcc5-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="0fcc5-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0fcc5-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0fcc5-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="0fcc5-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0fcc5-115">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0fcc5-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="0fcc5-116">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="0fcc5-117">*pLock*</span><span class="sxs-lookup"><span data-stu-id="0fcc5-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="0fcc5-118">Pointeur vers un objet [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="0fcc5-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="0fcc5-119">Dans votre classe dérivée, déclarez une variable membre **CCritSec** et utilisez son adresse pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="0fcc5-120">La `CSourceSeeking` classe utilise cette section critique pour synchroniser l’accès aux heures de début et de fin, la durée et la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="0fcc5-121">Chaque fois que vous accédez à ces variables dans votre classe dérivée, maintenez ce verrou.</span><span class="sxs-lookup"><span data-stu-id="0fcc5-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fcc5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fcc5-122">Requirements</span></span>



| <span data-ttu-id="0fcc5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fcc5-123">Requirement</span></span> | <span data-ttu-id="0fcc5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fcc5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcc5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fcc5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0fcc5-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fcc5-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0fcc5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0fcc5-127">Library</span></span><br/> | <dl> <span data-ttu-id="0fcc5-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0fcc5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fcc5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fcc5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fcc5-130">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="0fcc5-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




