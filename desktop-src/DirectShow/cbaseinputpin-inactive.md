---
description: 'CBaseInputPin. inactive, méthode : la méthode inactive indique au code confidentiel que le filtre n’est plus actif.'
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: CBaseInputPin. inactive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1324e9e2641e5e05bc3b0429ee269098c13d4bae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099727"
---
# <a name="cbaseinputpininactive-method"></a><span data-ttu-id="b35ae-103">CBaseInputPin. inactive, méthode</span><span class="sxs-lookup"><span data-stu-id="b35ae-103">CBaseInputPin.Inactive method</span></span>

<span data-ttu-id="b35ae-104">La `Inactive` méthode notifie le code confidentiel que le filtre n’est plus actif.</span><span class="sxs-lookup"><span data-stu-id="b35ae-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b35ae-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="b35ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b35ae-106">Parameters</span></span>

<span data-ttu-id="b35ae-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b35ae-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b35ae-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b35ae-108">Return value</span></span>

<span data-ttu-id="b35ae-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b35ae-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b35ae-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b35ae-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b35ae-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b35ae-111">Return code</span></span>                                                                                          | <span data-ttu-id="b35ae-112">Description</span><span class="sxs-lookup"><span data-stu-id="b35ae-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b35ae-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b35ae-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="b35ae-114">Réussite.</span><span class="sxs-lookup"><span data-stu-id="b35ae-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="b35ae-115"><dt>**VFW \_ E \_ aucun \_ allocateur**</dt></span><span class="sxs-lookup"><span data-stu-id="b35ae-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="b35ae-116">Aucun allocateur de mémoire n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="b35ae-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b35ae-117">Notes </span><span class="sxs-lookup"><span data-stu-id="b35ae-117">Remarks</span></span>

<span data-ttu-id="b35ae-118">Cette méthode remplace la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="b35ae-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="b35ae-119">Elle appelle la méthode [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) pour désallouer l’allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="b35ae-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="b35ae-120">Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.</span><span class="sxs-lookup"><span data-stu-id="b35ae-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b35ae-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b35ae-121">Requirements</span></span>



| <span data-ttu-id="b35ae-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b35ae-122">Requirement</span></span> | <span data-ttu-id="b35ae-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b35ae-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35ae-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b35ae-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b35ae-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b35ae-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b35ae-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b35ae-126">Library</span></span><br/> | <dl> <span data-ttu-id="b35ae-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b35ae-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b35ae-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b35ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35ae-129">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="b35ae-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




