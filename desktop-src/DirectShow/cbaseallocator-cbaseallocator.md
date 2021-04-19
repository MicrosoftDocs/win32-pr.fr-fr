---
description: Méthode de constructeur.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Constructeur CBaseAllocator. CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525113"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="9070e-103">Constructeur CBaseAllocator. CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="9070e-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="9070e-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="9070e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9070e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9070e-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="9070e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9070e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9070e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="9070e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="9070e-108">Pointeur vers une chaîne contenant le nom de débogage de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="9070e-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="9070e-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="9070e-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="9070e-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="9070e-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="9070e-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="9070e-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="9070e-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="9070e-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="9070e-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="9070e-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9070e-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="9070e-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9070e-115">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9070e-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="9070e-116">Définissez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="9070e-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="9070e-117">Si le constructeur échoue, la valeur est définie sur un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9070e-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="9070e-118">*à la vente*</span><span class="sxs-lookup"><span data-stu-id="9070e-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="9070e-119">Valeur booléenne indiquant s’il faut créer un sémaphore.</span><span class="sxs-lookup"><span data-stu-id="9070e-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="9070e-120">Si la **valeur est true**, l’allocateur crée un sémaphore ([**CBaseAllocator :: m \_ hSem**](cbaseallocator-m-hsem.md)), qui est signalé chaque fois qu’un exemple devient disponible.</span><span class="sxs-lookup"><span data-stu-id="9070e-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="9070e-121">Affectez la valeur **false** si vous implémentez une classe dérivée qui ne requiert pas de sémaphore.</span><span class="sxs-lookup"><span data-stu-id="9070e-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="9070e-122">*fEnableReleaseCallback*</span><span class="sxs-lookup"><span data-stu-id="9070e-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="9070e-123">Valeur booléenne indiquant si le mécanisme de rappel de mise en version est activé.</span><span class="sxs-lookup"><span data-stu-id="9070e-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="9070e-124">Définissez la valeur sur **true** si vous souhaitez fournir une interface de rappel, qui est appelée lorsque les mémoires tampons sont libérées.</span><span class="sxs-lookup"><span data-stu-id="9070e-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="9070e-125">Spécifiez le rappel en appelant la méthode [**CBaseAllocator :: SetNotify**](cbaseallocator-setnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="9070e-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9070e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9070e-126">Requirements</span></span>



| <span data-ttu-id="9070e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9070e-127">Requirement</span></span> | <span data-ttu-id="9070e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9070e-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9070e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9070e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9070e-130"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9070e-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9070e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9070e-131">Library</span></span><br/> | <dl> <span data-ttu-id="9070e-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9070e-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9070e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9070e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9070e-134">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="9070e-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




