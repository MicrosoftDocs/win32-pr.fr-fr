---
description: La classe CEnumMediaTypes implémente un énumérateur pour les types de média préférés.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: CEnumMediaTypes, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530990"
---
# <a name="cenummediatypes-class"></a><span data-ttu-id="88588-103">CEnumMediaTypes, classe</span><span class="sxs-lookup"><span data-stu-id="88588-103">CEnumMediaTypes class</span></span>

![hiérarchie de la classe cenummediatypes](images/filter04.png)

<span data-ttu-id="88588-105">La `CEnumMediaTypes` classe implémente un énumérateur pour les types de média préférés.</span><span class="sxs-lookup"><span data-stu-id="88588-105">The `CEnumMediaTypes` class implements an enumerator for preferred media types.</span></span>

<span data-ttu-id="88588-106">Cette classe implémente l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="88588-106">This class implements the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="88588-107">Il appelle les méthodes [**CBasePin**](cbasepin.md) suivantes :</span><span class="sxs-lookup"><span data-stu-id="88588-107">It calls the following [**CBasePin**](cbasepin.md) methods:</span></span>

-   <span data-ttu-id="88588-108">[**CBasePin :: GetMediaType**](cbasepin-getmediatype.md): récupère un type de média, référencé par un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="88588-108">[**CBasePin::GetMediaType**](cbasepin-getmediatype.md):Retrieves a media type, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="88588-109">[**CBasePin :: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): détermine si l’ensemble de types préférés a changé.</span><span class="sxs-lookup"><span data-stu-id="88588-109">[**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): Determines whether the set of preferred types has changed.</span></span>

<span data-ttu-id="88588-110">Chaque fois qu’un code PIN modifie sa liste de types de médias préférés, le code PIN incrémente le numéro de version du type de média.</span><span class="sxs-lookup"><span data-stu-id="88588-110">Whenever a pin alters its list of preferred media types, the pin increments the media-type version number.</span></span> <span data-ttu-id="88588-111">Dans ce cas, l’objet énumérateur n’est plus synchronisé avec le code confidentiel, et les méthodes de la classe retournent VFW \_ E \_ enum non \_ \_ \_ synchronisé.</span><span class="sxs-lookup"><span data-stu-id="88588-111">When this happens, the enumerator object is no longer synchronized with the pin, and the class methods return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="88588-112">Appelez la méthode [**CEnumMediaTypes :: Reset**](cenummediatypes-reset.md) pour resynchroniser l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="88588-112">Call the [**CEnumMediaTypes::Reset**](cenummediatypes-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="88588-113">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="88588-113">Public Methods</span></span>                                               | <span data-ttu-id="88588-114">Description</span><span class="sxs-lookup"><span data-stu-id="88588-114">Description</span></span>                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="88588-115">**CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="88588-115">**CEnumMediaTypes**</span></span>](cenummediatypes-cenummediatypes.md)   | <span data-ttu-id="88588-116">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="88588-116">Constructor method.</span></span>                                             |
| [<span data-ttu-id="88588-117">**~ CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="88588-117">**~CEnumMediaTypes**</span></span>](cenummediatypes--cenummediatypes.md) | <span data-ttu-id="88588-118">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="88588-118">Destructor method.</span></span> <span data-ttu-id="88588-119">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="88588-119">Virtual.</span></span>                                     |
| <span data-ttu-id="88588-120">Méthodes IEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="88588-120">IEnumMediaTypes Methods</span></span>                                      | <span data-ttu-id="88588-121">Description</span><span class="sxs-lookup"><span data-stu-id="88588-121">Description</span></span>                                                     |
| [<span data-ttu-id="88588-122">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="88588-122">**Clone**</span></span>](cenummediatypes-clone.md)                       | <span data-ttu-id="88588-123">Fait une copie de l’énumérateur avec le même état d’énumération.</span><span class="sxs-lookup"><span data-stu-id="88588-123">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="88588-124">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="88588-124">**Next**</span></span>](cenummediatypes-next.md)                         | <span data-ttu-id="88588-125">Récupère un nombre spécifié de types de médias.</span><span class="sxs-lookup"><span data-stu-id="88588-125">Retrieves a specified number of media types.</span></span>                    |
| [<span data-ttu-id="88588-126">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="88588-126">**Reset**</span></span>](cenummediatypes-reset.md)                       | <span data-ttu-id="88588-127">Réinitialise la séquence d'énumération au début.</span><span class="sxs-lookup"><span data-stu-id="88588-127">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="88588-128">**Saut**</span><span class="sxs-lookup"><span data-stu-id="88588-128">**Skip**</span></span>](cenummediatypes-skip.md)                         | <span data-ttu-id="88588-129">Ignore un nombre spécifié de types de médias.</span><span class="sxs-lookup"><span data-stu-id="88588-129">Skips over a specified number of media types.</span></span>                   |



 

## <a name="requirements"></a><span data-ttu-id="88588-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88588-130">Requirements</span></span>



| <span data-ttu-id="88588-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88588-131">Requirement</span></span> | <span data-ttu-id="88588-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="88588-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88588-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="88588-133">Header</span></span><br/>  | <dl> <span data-ttu-id="88588-134"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88588-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88588-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88588-135">Library</span></span><br/> | <dl> <span data-ttu-id="88588-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="88588-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




