---
description: 'La méthode GetAllocator récupère l’allocateur de mémoire proposé par ce code confidentiel. Cette méthode implémente la méthode IMemInputPin :: GetAllocator.'
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
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532802"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="23892-104">Méthode CTransInPlaceInputPin. GetAllocator</span><span class="sxs-lookup"><span data-stu-id="23892-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="23892-105">La `GetAllocator` méthode récupère l’allocateur de mémoire proposé par ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="23892-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="23892-106">Cette méthode implémente la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="23892-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="23892-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23892-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="23892-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23892-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23892-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="23892-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="23892-110">Reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="23892-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23892-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23892-111">Return value</span></span>

<span data-ttu-id="23892-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23892-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="23892-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="23892-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="23892-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="23892-114">Return code</span></span>                                                                                          | <span data-ttu-id="23892-115">Description</span><span class="sxs-lookup"><span data-stu-id="23892-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="23892-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="23892-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="23892-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="23892-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="23892-118"><dt>**VFW \_ E \_ aucun \_ allocateur**</dt></span><span class="sxs-lookup"><span data-stu-id="23892-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="23892-119">Aucun allocateur n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="23892-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23892-120">Notes</span><span class="sxs-lookup"><span data-stu-id="23892-120">Remarks</span></span>

<span data-ttu-id="23892-121">Si la broche de sortie du filtre est connectée, cette méthode demande un allocateur à partir de la broche d’entrée du filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="23892-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="23892-122">Si la broche de sortie du filtre n’est pas connectée, cette méthode crée un allocateur temporaire.</span><span class="sxs-lookup"><span data-stu-id="23892-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="23892-123">Plus tard, lorsque la broche de sortie est connectée, le filtre reconnecte la broche d’entrée et renégocie l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="23892-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="23892-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23892-124">Requirements</span></span>



| <span data-ttu-id="23892-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23892-125">Requirement</span></span> | <span data-ttu-id="23892-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="23892-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23892-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="23892-127">Header</span></span><br/>  | <dl> <span data-ttu-id="23892-128"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23892-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="23892-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23892-129">Library</span></span><br/> | <dl> <span data-ttu-id="23892-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23892-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23892-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23892-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23892-132">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="23892-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




