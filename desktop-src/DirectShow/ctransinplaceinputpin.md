---
description: La classe CTransInPlaceInputPin implémente une broche d’entrée qui est utilisée par la classe CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: CTransInPlaceInputPin, classe (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532981"
---
# <a name="ctransinplaceinputpin-class"></a><span data-ttu-id="59d40-103">CTransInPlaceInputPin, classe</span><span class="sxs-lookup"><span data-stu-id="59d40-103">CTransInPlaceInputPin class</span></span>

![hiérarchie de la classe ctransinplaceinputpin](images/tsip01.png)

<span data-ttu-id="59d40-105">La `CTransInPlaceInputPin` classe implémente une broche d’entrée qui est utilisée par la classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="59d40-105">The `CTransInPlaceInputPin` class implements an input pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="59d40-106">En règle générale, vous n’avez pas besoin de dériver de cette classe.</span><span class="sxs-lookup"><span data-stu-id="59d40-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="59d40-107">Si vous le faites, vous devez substituer la méthode [**CTransInPlaceFilter :: GetPin**](ctransinplacefilter-getpin.md) du filtre pour créer des instances de votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="59d40-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="59d40-108">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="59d40-108">Protected Member Variables</span></span>                                                          | <span data-ttu-id="59d40-109">Description</span><span class="sxs-lookup"><span data-stu-id="59d40-109">Description</span></span>                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="59d40-110">**m \_ bReadOnly**</span><span class="sxs-lookup"><span data-stu-id="59d40-110">**m\_bReadOnly**</span></span>](ctransinplaceinputpin-m-breadonly.md)                           | <span data-ttu-id="59d40-111">Indicateur qui spécifie si le flux d’entrée est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="59d40-111">Flag that specifies whether the input stream is read-only.</span></span> |
| [<span data-ttu-id="59d40-112">**m \_ pTIPFilter**</span><span class="sxs-lookup"><span data-stu-id="59d40-112">**m\_pTIPFilter**</span></span>](ctransinplaceinputpin-m-ptipfilter.md)                         | <span data-ttu-id="59d40-113">Pointeur vers le filtre qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="59d40-113">Pointer to the filter that created this pin.</span></span>               |
| <span data-ttu-id="59d40-114">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="59d40-114">Public Methods</span></span>                                                                      | <span data-ttu-id="59d40-115">Description</span><span class="sxs-lookup"><span data-stu-id="59d40-115">Description</span></span>                                                |
| [<span data-ttu-id="59d40-116">**CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="59d40-116">**CTransInPlaceInputPin**</span></span>](ctransinplaceinputpin-ctransinplaceinputpin.md)        | <span data-ttu-id="59d40-117">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="59d40-117">Constructor method.</span></span>                                        |
| [<span data-ttu-id="59d40-118">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="59d40-118">**CheckMediaType**</span></span>](ctransinplaceinputpin-checkmediatype.md)                      | <span data-ttu-id="59d40-119">Détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="59d40-119">Determines if the pin accepts a specific media type.</span></span>       |
| [<span data-ttu-id="59d40-120">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="59d40-120">**PeekAllocator**</span></span>](ctransinplaceinputpin-peekallocator.md)                        | <span data-ttu-id="59d40-121">Récupère un pointeur vers l’allocateur du pin.</span><span class="sxs-lookup"><span data-stu-id="59d40-121">Retrieves a pointer to the pin's allocator.</span></span>                |
| [<span data-ttu-id="59d40-122">**Seulement**</span><span class="sxs-lookup"><span data-stu-id="59d40-122">**ReadOnly**</span></span>](ctransinplaceinputpin-readonly.md)                                  | <span data-ttu-id="59d40-123">Indique si le flux d’entrée est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="59d40-123">Indicates whether the input stream is read-only.</span></span>           |
| <span data-ttu-id="59d40-124">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="59d40-124">IPin Methods</span></span>                                                                        | <span data-ttu-id="59d40-125">Description</span><span class="sxs-lookup"><span data-stu-id="59d40-125">Description</span></span>                                                |
| [<span data-ttu-id="59d40-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="59d40-126">**EnumMediaTypes**</span></span>](ctransinplaceinputpin-enummediatypes.md)                      | <span data-ttu-id="59d40-127">Énumère les types de médias préférés du pin.</span><span class="sxs-lookup"><span data-stu-id="59d40-127">Enumerates the pin's preferred media types.</span></span>                |
| <span data-ttu-id="59d40-128">Méthodes IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="59d40-128">IMemInputPin Methods</span></span>                                                                | <span data-ttu-id="59d40-129">Description</span><span class="sxs-lookup"><span data-stu-id="59d40-129">Description</span></span>                                                |
| [<span data-ttu-id="59d40-130">**GetAllocator**</span><span class="sxs-lookup"><span data-stu-id="59d40-130">**GetAllocator**</span></span>](ctransinplaceinputpin-getallocator.md)                          | <span data-ttu-id="59d40-131">Récupère l’allocateur de mémoire proposé par ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="59d40-131">Retrieves the memory allocator proposed by this pin.</span></span>       |
| [<span data-ttu-id="59d40-132">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="59d40-132">**NotifyAllocator**</span></span>](ctransinplaceinputpin-notifyallocator.md)                    | <span data-ttu-id="59d40-133">Spécifie un allocateur pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="59d40-133">Specifies an allocator for the connection.</span></span>                 |
| [<span data-ttu-id="59d40-134">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="59d40-134">**GetAllocatorRequirements**</span></span>](ctransinplaceinputpin--getallocatorrequirements.md) | <span data-ttu-id="59d40-135">Récupère les propriétés d’allocateur demandées par le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="59d40-135">Retrieves the allocator properties requested by the pin.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="59d40-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59d40-136">Requirements</span></span>



| <span data-ttu-id="59d40-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59d40-137">Requirement</span></span> | <span data-ttu-id="59d40-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="59d40-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d40-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="59d40-139">Header</span></span><br/>  | <dl> <span data-ttu-id="59d40-140"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59d40-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59d40-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59d40-141">Library</span></span><br/> | <dl> <span data-ttu-id="59d40-142"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59d40-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




