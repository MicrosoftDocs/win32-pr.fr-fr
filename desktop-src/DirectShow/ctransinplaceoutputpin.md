---
description: La classe CTransInPlaceOutputPin implémente une broche de sortie qui est utilisée par la classe CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: CTransInPlaceOutputPin, classe (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528048"
---
# <a name="ctransinplaceoutputpin-class"></a><span data-ttu-id="90642-103">CTransInPlaceOutputPin, classe</span><span class="sxs-lookup"><span data-stu-id="90642-103">CTransInPlaceOutputPin class</span></span>

![hiérarchie de la classe ctransinplaceoutputpin](images/tsip02.png)

<span data-ttu-id="90642-105">La `CTransInPlaceOutputPin` classe implémente une broche de sortie qui est utilisée par la classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="90642-105">The `CTransInPlaceOutputPin` class implements an output pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="90642-106">En règle générale, vous n’avez pas besoin de dériver de cette classe.</span><span class="sxs-lookup"><span data-stu-id="90642-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="90642-107">Si vous le faites, vous devez substituer la méthode [**CTransInPlaceFilter :: GetPin**](ctransinplacefilter-getpin.md) du filtre pour créer des instances de votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="90642-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="90642-108">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="90642-108">Protected Member Variables</span></span>                                                      | <span data-ttu-id="90642-109">Description</span><span class="sxs-lookup"><span data-stu-id="90642-109">Description</span></span>                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="90642-110">**m \_ pTIPFilter**</span><span class="sxs-lookup"><span data-stu-id="90642-110">**m\_pTIPFilter**</span></span>](ctransinplaceoutputpin-m-ptipfilter.md)                    | <span data-ttu-id="90642-111">Pointeur vers le filtre qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="90642-111">Pointer to the filter that created this pin.</span></span>         |
| <span data-ttu-id="90642-112">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="90642-112">Public Methods</span></span>                                                                  | <span data-ttu-id="90642-113">Description</span><span class="sxs-lookup"><span data-stu-id="90642-113">Description</span></span>                                          |
| [<span data-ttu-id="90642-114">**CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="90642-114">**CTransInPlaceOutputPin**</span></span>](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | <span data-ttu-id="90642-115">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="90642-115">Constructor method.</span></span>                                  |
| [<span data-ttu-id="90642-116">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="90642-116">**CheckMediaType**</span></span>](ctransinplaceoutputpin-checkmediatype.md)                 | <span data-ttu-id="90642-117">Détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="90642-117">Determines if the pin accepts a specific media type.</span></span> |
| [<span data-ttu-id="90642-118">**SetAllocator**</span><span class="sxs-lookup"><span data-stu-id="90642-118">**SetAllocator**</span></span>](ctransinplaceoutputpin-setallocator.md)                     | <span data-ttu-id="90642-119">Spécifie un allocateur pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="90642-119">Specifies an allocator for the connection.</span></span>           |
| [<span data-ttu-id="90642-120">**ConnectedIMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="90642-120">**ConnectedIMemInputPin**</span></span>](ctransinplaceoutputpin-connectedimeminputpin.md)   | <span data-ttu-id="90642-121">Récupère un pointeur vers la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="90642-121">Retrieves a pointer to the downstream input pin.</span></span>     |
| [<span data-ttu-id="90642-122">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="90642-122">**PeekAllocator**</span></span>](ctransinplaceoutputpin-peekallocator.md)                   | <span data-ttu-id="90642-123">Récupère un pointeur vers l’allocateur du pin.</span><span class="sxs-lookup"><span data-stu-id="90642-123">Retrieves a pointer to the pin's allocator.</span></span>          |
| <span data-ttu-id="90642-124">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="90642-124">IPin Methods</span></span>                                                                    | <span data-ttu-id="90642-125">Description</span><span class="sxs-lookup"><span data-stu-id="90642-125">Description</span></span>                                          |
| [<span data-ttu-id="90642-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="90642-126">**EnumMediaTypes**</span></span>](ctransinplaceoutputpin-enummediatypes.md)                 | <span data-ttu-id="90642-127">Énumère les types de médias préférés du pin.</span><span class="sxs-lookup"><span data-stu-id="90642-127">Enumerates the pin's preferred media types.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="90642-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90642-128">Requirements</span></span>



| <span data-ttu-id="90642-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90642-129">Requirement</span></span> | <span data-ttu-id="90642-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="90642-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90642-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="90642-131">Header</span></span><br/>  | <dl> <span data-ttu-id="90642-132"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90642-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="90642-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="90642-133">Library</span></span><br/> | <dl> <span data-ttu-id="90642-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="90642-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




