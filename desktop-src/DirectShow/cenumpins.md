---
description: La classe CEnumPins implémente un énumérateur pour les codes confidentiels.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: CEnumPins, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533365"
---
# <a name="cenumpins-class"></a><span data-ttu-id="e8f57-103">CEnumPins, classe</span><span class="sxs-lookup"><span data-stu-id="e8f57-103">CEnumPins class</span></span>

![hiérarchie de la classe cenumpins](images/filter03.png)

<span data-ttu-id="e8f57-105">La `CEnumPins` classe implémente un énumérateur pour les codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="e8f57-105">The `CEnumPins` class implements an enumerator for pins.</span></span>

<span data-ttu-id="e8f57-106">Cette classe implémente l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="e8f57-106">This class implements the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="e8f57-107">Il appelle les méthodes [**CBaseFilter**](cbasefilter.md) suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8f57-107">It calls the following [**CBaseFilter**](cbasefilter.md) methods:</span></span>

-   <span data-ttu-id="e8f57-108">[**CBaseFilter :: GetPin**](cbasefilter-getpin.md): récupère un code confidentiel sur le filtre, référencé par un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="e8f57-108">[**CBaseFilter::GetPin**](cbasefilter-getpin.md): Retrieves a pin on the filter, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="e8f57-109">[**CBaseFilter :: GetPinCount**](cbasefilter-getpincount.md): récupère le nombre total de broches sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="e8f57-109">[**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md): Retrieves the total number of pins on the filter.</span></span>
-   <span data-ttu-id="e8f57-110">[**CBaseFilter :: GetPinVersion**](cbasefilter-getpinversion.md): détermine si les broches ont changé.</span><span class="sxs-lookup"><span data-stu-id="e8f57-110">[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md): Determines whether the pins have changed.</span></span>

<span data-ttu-id="e8f57-111">Si le filtre crée ou détruit dynamiquement des broches, il incrémente la version du code confidentiel chaque fois que les codes confidentiels changent.</span><span class="sxs-lookup"><span data-stu-id="e8f57-111">If the filter dynamically creates or destroys pins, it increments the pin version whenever the pins change.</span></span> <span data-ttu-id="e8f57-112">Si le numéro de version change, l’objet énumérateur n’est plus synchronisé avec le filtre.</span><span class="sxs-lookup"><span data-stu-id="e8f57-112">If the version number changes, the enumerator object is no longer synchronized with the filter.</span></span> <span data-ttu-id="e8f57-113">Une fois l’énumérateur désynchronisé, les méthodes de `CEnumPins` retournent \_ les \_ enums VFW E non \_ \_ \_ synchronisés.</span><span class="sxs-lookup"><span data-stu-id="e8f57-113">Once the enumerator is out of sync, the methods in `CEnumPins` return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="e8f57-114">Appelez la méthode [**CEnumPins :: Reset**](cenumpins-reset.md) pour resynchroniser l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="e8f57-114">Call the [**CEnumPins::Reset**](cenumpins-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="e8f57-115">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="e8f57-115">Public Methods</span></span>                             | <span data-ttu-id="e8f57-116">Description</span><span class="sxs-lookup"><span data-stu-id="e8f57-116">Description</span></span>                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="e8f57-117">**CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="e8f57-117">**CEnumPins**</span></span>](cenumpins-cenumpins.md)   | <span data-ttu-id="e8f57-118">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="e8f57-118">Constructor method.</span></span>                                             |
| [<span data-ttu-id="e8f57-119">**~ CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="e8f57-119">**~CEnumPins**</span></span>](cenumpins--cenumpins.md) | <span data-ttu-id="e8f57-120">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="e8f57-120">Destructor method.</span></span> <span data-ttu-id="e8f57-121">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="e8f57-121">Virtual.</span></span>                                     |
| <span data-ttu-id="e8f57-122">Méthodes IEnumPins</span><span class="sxs-lookup"><span data-stu-id="e8f57-122">IEnumPins Methods</span></span>                          | <span data-ttu-id="e8f57-123">Description</span><span class="sxs-lookup"><span data-stu-id="e8f57-123">Description</span></span>                                                     |
| [<span data-ttu-id="e8f57-124">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="e8f57-124">**Clone**</span></span>](cenumpins-clone.md)           | <span data-ttu-id="e8f57-125">Fait une copie de l’énumérateur avec le même état d’énumération.</span><span class="sxs-lookup"><span data-stu-id="e8f57-125">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="e8f57-126">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="e8f57-126">**Next**</span></span>](cenumpins-next.md)             | <span data-ttu-id="e8f57-127">Récupère un nombre spécifié de broches.</span><span class="sxs-lookup"><span data-stu-id="e8f57-127">Retrieves a specified number of pins.</span></span>                           |
| [<span data-ttu-id="e8f57-128">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="e8f57-128">**Reset**</span></span>](cenumpins-reset.md)           | <span data-ttu-id="e8f57-129">Réinitialise la séquence d'énumération au début.</span><span class="sxs-lookup"><span data-stu-id="e8f57-129">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="e8f57-130">**Saut**</span><span class="sxs-lookup"><span data-stu-id="e8f57-130">**Skip**</span></span>](cenumpins-skip.md)             | <span data-ttu-id="e8f57-131">Ignore un nombre spécifié de broches.</span><span class="sxs-lookup"><span data-stu-id="e8f57-131">Skips over a specified number of pins.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="e8f57-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8f57-132">Requirements</span></span>



| <span data-ttu-id="e8f57-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8f57-133">Requirement</span></span> | <span data-ttu-id="e8f57-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8f57-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f57-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8f57-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e8f57-136"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8f57-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8f57-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e8f57-137">Library</span></span><br/> | <dl> <span data-ttu-id="e8f57-138"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e8f57-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




