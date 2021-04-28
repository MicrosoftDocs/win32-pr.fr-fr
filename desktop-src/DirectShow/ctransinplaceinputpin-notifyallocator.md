---
description: 'Méthode CTransInPlaceInputPin. NotifyAllocator : la méthode NotifyAllocator spécifie un allocateur pour la connexion. Cette méthode implémente la méthode IMemInputPin :: NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Méthode CTransInPlaceInputPin. NotifyAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca15be5dc1893a393e6052832cc7522f27355eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094747"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="b4f7b-104">Méthode CTransInPlaceInputPin. NotifyAllocator</span><span class="sxs-lookup"><span data-stu-id="b4f7b-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="b4f7b-105">La `NotifyAllocator` méthode spécifie un allocateur pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="b4f7b-106">Cette méthode implémente la méthode [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="b4f7b-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f7b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4f7b-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="b4f7b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4f7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f7b-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="b4f7b-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="b4f7b-110">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b4f7b-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="b4f7b-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="b4f7b-112">Indicateur qui spécifie si les exemples de cet allocateur sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="b4f7b-113">Si la **valeur est true**, les exemples sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f7b-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4f7b-114">Return value</span></span>

<span data-ttu-id="b4f7b-115">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4f7b-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b4f7b-116">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4f7b-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b4f7b-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4f7b-117">Return code</span></span>                                                                               | <span data-ttu-id="b4f7b-118">Description</span><span class="sxs-lookup"><span data-stu-id="b4f7b-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="b4f7b-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4f7b-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b4f7b-120">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="b4f7b-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="b4f7b-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="b4f7b-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="b4f7b-122">Échec</span><span class="sxs-lookup"><span data-stu-id="b4f7b-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="b4f7b-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b4f7b-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b4f7b-124">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="b4f7b-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4f7b-125">Notes </span><span class="sxs-lookup"><span data-stu-id="b4f7b-125">Remarks</span></span>

<span data-ttu-id="b4f7b-126">Le filtre tente d’utiliser le même allocateur pour les deux connexions de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="b4f7b-127">Si la broche de sortie n’est pas connectée, la broche d’entrée accepte automatiquement l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="b4f7b-128">Lorsque la broche de sortie est connectée, le filtre reconnecte la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="b4f7b-129">À ce stade, le filtre réessaiera d’utiliser un allocateur unique.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="b4f7b-130">Si la broche de sortie est connectée, la broche d’entrée accepte l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="b4f7b-131">La broche de sortie utilise également le même allocateur.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="b4f7b-132">Il appelle `NotifyAllocator` sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="b4f7b-133">Le cas précédent a l’exception suivante :</span><span class="sxs-lookup"><span data-stu-id="b4f7b-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="b4f7b-134">Si l’allocateur proposé est en lecture seule (autrement dit, si le paramètre *bReadOnly* a la **valeur true**) et que le filtre doit modifier les exemples, le filtre doit utiliser deux allocateurs différents.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="b4f7b-135">Dans ce cas, si le filtre en amont propose d’utiliser l’allocateur du filtre en aval, la méthode renvoie E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="b4f7b-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f7b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4f7b-136">Requirements</span></span>



| <span data-ttu-id="b4f7b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4f7b-137">Requirement</span></span> | <span data-ttu-id="b4f7b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f7b-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f7b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4f7b-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b4f7b-140"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4f7b-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b4f7b-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4f7b-141">Library</span></span><br/> | <dl> <span data-ttu-id="b4f7b-142"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b4f7b-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4f7b-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4f7b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f7b-144">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="b4f7b-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




