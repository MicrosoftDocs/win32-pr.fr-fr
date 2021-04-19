---
description: Méthode de constructeur.
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
ms.openlocfilehash: 309e926ddf001cf9933b19334992f5210fc7f17b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537604"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="122c4-103">Constructeur CSourceSeeking. CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="122c4-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="122c4-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="122c4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="122c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="122c4-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="122c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="122c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="122c4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="122c4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="122c4-108">Pointeur vers une chaîne contenant le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="122c4-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="122c4-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="122c4-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="122c4-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="122c4-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="122c4-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="122c4-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="122c4-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="122c4-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="122c4-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="122c4-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="122c4-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="122c4-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="122c4-115">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="122c4-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="122c4-116">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="122c4-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="122c4-117">*pLock*</span><span class="sxs-lookup"><span data-stu-id="122c4-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="122c4-118">Pointeur vers un objet [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="122c4-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="122c4-119">Dans votre classe dérivée, déclarez une variable membre **CCritSec** et utilisez son adresse pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="122c4-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="122c4-120">La `CSourceSeeking` classe utilise cette section critique pour synchroniser l’accès aux heures de début et de fin, la durée et la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="122c4-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="122c4-121">Chaque fois que vous accédez à ces variables dans votre classe dérivée, maintenez ce verrou.</span><span class="sxs-lookup"><span data-stu-id="122c4-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="122c4-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="122c4-122">Requirements</span></span>



| <span data-ttu-id="122c4-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="122c4-123">Requirement</span></span> | <span data-ttu-id="122c4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="122c4-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="122c4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="122c4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="122c4-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="122c4-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="122c4-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="122c4-127">Library</span></span><br/> | <dl> <span data-ttu-id="122c4-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="122c4-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="122c4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="122c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="122c4-130">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="122c4-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




