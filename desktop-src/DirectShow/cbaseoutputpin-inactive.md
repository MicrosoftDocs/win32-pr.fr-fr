---
description: La méthode inactive indique au code confidentiel que le filtre n’est plus actif.
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: CBaseOutputPin. inactive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afec15e295e5c14cfb3d9efa6e733d1dc288b319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540654"
---
# <a name="cbaseoutputpininactive-method"></a><span data-ttu-id="16e86-103">CBaseOutputPin. inactive, méthode</span><span class="sxs-lookup"><span data-stu-id="16e86-103">CBaseOutputPin.Inactive method</span></span>

<span data-ttu-id="16e86-104">La `Inactive` méthode notifie le code confidentiel que le filtre n’est plus actif.</span><span class="sxs-lookup"><span data-stu-id="16e86-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e86-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16e86-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="16e86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16e86-106">Parameters</span></span>

<span data-ttu-id="16e86-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="16e86-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16e86-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16e86-108">Return value</span></span>

<span data-ttu-id="16e86-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16e86-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="16e86-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="16e86-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="16e86-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="16e86-111">Return code</span></span>                                                                                          | <span data-ttu-id="16e86-112">Description</span><span class="sxs-lookup"><span data-stu-id="16e86-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="16e86-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="16e86-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="16e86-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="16e86-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="16e86-115"><dt>**VFW \_ E \_ aucun \_ allocateur**</dt></span><span class="sxs-lookup"><span data-stu-id="16e86-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="16e86-116">Aucun allocateur de mémoire n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="16e86-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16e86-117">Notes</span><span class="sxs-lookup"><span data-stu-id="16e86-117">Remarks</span></span>

<span data-ttu-id="16e86-118">Cette méthode remplace la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="16e86-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="16e86-119">Elle appelle la méthode [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) pour désallouer l’allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="16e86-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="16e86-120">Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.</span><span class="sxs-lookup"><span data-stu-id="16e86-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e86-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16e86-121">Requirements</span></span>



| <span data-ttu-id="16e86-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16e86-122">Requirement</span></span> | <span data-ttu-id="16e86-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="16e86-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16e86-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="16e86-124">Header</span></span><br/>  | <dl> <span data-ttu-id="16e86-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16e86-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="16e86-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16e86-126">Library</span></span><br/> | <dl> <span data-ttu-id="16e86-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="16e86-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e86-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16e86-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e86-129">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="16e86-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




