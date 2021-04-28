---
description: 'Méthode CTransInPlaceInputPin. GetAllocator : la méthode GetAllocator récupère l’allocateur de mémoire proposé par ce code confidentiel. Cette méthode implémente la méthode IMemInputPin :: GetAllocator.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Méthode CTransInPlaceInputPin. GetAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2472630d69119f33653d831386af615718274d99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084657"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="603f8-104">Méthode CTransInPlaceInputPin. GetAllocator</span><span class="sxs-lookup"><span data-stu-id="603f8-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="603f8-105">La `GetAllocator` méthode récupère l’allocateur de mémoire proposé par ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="603f8-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="603f8-106">Cette méthode implémente la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="603f8-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="603f8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="603f8-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="603f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="603f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603f8-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="603f8-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="603f8-110">Reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="603f8-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603f8-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="603f8-111">Return value</span></span>

<span data-ttu-id="603f8-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="603f8-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="603f8-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="603f8-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="603f8-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="603f8-114">Return code</span></span>                                                                                          | <span data-ttu-id="603f8-115">Description</span><span class="sxs-lookup"><span data-stu-id="603f8-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="603f8-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="603f8-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="603f8-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="603f8-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="603f8-118"><dt>**VFW \_ E \_ aucun \_ allocateur**</dt></span><span class="sxs-lookup"><span data-stu-id="603f8-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="603f8-119">Aucun allocateur n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="603f8-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="603f8-120">Notes </span><span class="sxs-lookup"><span data-stu-id="603f8-120">Remarks</span></span>

<span data-ttu-id="603f8-121">Si la broche de sortie du filtre est connectée, cette méthode demande un allocateur à partir de la broche d’entrée du filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="603f8-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="603f8-122">Si la broche de sortie du filtre n’est pas connectée, cette méthode crée un allocateur temporaire.</span><span class="sxs-lookup"><span data-stu-id="603f8-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="603f8-123">Plus tard, lorsque la broche de sortie est connectée, le filtre reconnecte la broche d’entrée et renégocie l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="603f8-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="603f8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="603f8-124">Requirements</span></span>



| <span data-ttu-id="603f8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="603f8-125">Requirement</span></span> | <span data-ttu-id="603f8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="603f8-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="603f8-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="603f8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="603f8-128"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="603f8-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="603f8-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="603f8-129">Library</span></span><br/> | <dl> <span data-ttu-id="603f8-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="603f8-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603f8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603f8-132">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="603f8-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




