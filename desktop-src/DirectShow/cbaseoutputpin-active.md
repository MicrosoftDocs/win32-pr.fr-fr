---
description: 'CBaseOutputPin. active, méthode : la méthode active indique au code confidentiel que le filtre est maintenant actif.'
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: CBaseOutputPin. active, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096207"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="8b3cc-103">CBaseOutputPin. active, méthode</span><span class="sxs-lookup"><span data-stu-id="8b3cc-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="8b3cc-104">La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="8b3cc-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b3cc-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="8b3cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b3cc-106">Parameters</span></span>

<span data-ttu-id="8b3cc-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8b3cc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b3cc-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b3cc-108">Return value</span></span>

<span data-ttu-id="8b3cc-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b3cc-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8b3cc-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8b3cc-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="8b3cc-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8b3cc-111">Return code</span></span>                                                                                          | <span data-ttu-id="8b3cc-112">Description</span><span class="sxs-lookup"><span data-stu-id="8b3cc-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8b3cc-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cc-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="8b3cc-114">Réussite.</span><span class="sxs-lookup"><span data-stu-id="8b3cc-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="8b3cc-115"><dt>**VFW \_ E \_ aucun \_ allocateur**</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cc-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="8b3cc-116">Aucun allocateur n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="8b3cc-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b3cc-117">Notes </span><span class="sxs-lookup"><span data-stu-id="8b3cc-117">Remarks</span></span>

<span data-ttu-id="8b3cc-118">Cette méthode remplace la méthode [**CBasePin :: active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="8b3cc-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="8b3cc-119">Elle appelle la méthode [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) sur l’allocateur pour allouer de la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="8b3cc-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="8b3cc-120">Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.</span><span class="sxs-lookup"><span data-stu-id="8b3cc-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b3cc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b3cc-121">Requirements</span></span>



| <span data-ttu-id="8b3cc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b3cc-122">Requirement</span></span> | <span data-ttu-id="8b3cc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b3cc-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3cc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b3cc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8b3cc-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cc-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8b3cc-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b3cc-126">Library</span></span><br/> | <dl> <span data-ttu-id="8b3cc-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8b3cc-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b3cc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b3cc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3cc-129">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="8b3cc-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




