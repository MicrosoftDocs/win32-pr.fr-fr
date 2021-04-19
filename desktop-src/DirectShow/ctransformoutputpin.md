---
description: La classe CTransformOutputPin implémente une broche de sortie qui est utilisée par la classe CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: CTransformOutputPin, classe (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535024"
---
# <a name="ctransformoutputpin-class"></a><span data-ttu-id="166c8-103">CTransformOutputPin, classe</span><span class="sxs-lookup"><span data-stu-id="166c8-103">CTransformOutputPin class</span></span>

![hiérarchie de la classe ctransformoutputpin](images/tfrm02.png)

<span data-ttu-id="166c8-105">La `CTransformOutputPin` classe implémente une broche de sortie qui est utilisée par la classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="166c8-105">The `CTransformOutputPin` class implements an output pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="166c8-106">En règle générale, vous n’avez pas besoin de dériver de cette classe.</span><span class="sxs-lookup"><span data-stu-id="166c8-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="166c8-107">La plupart des méthodes de cette classe appellent les méthodes correspondantes sur la classe **CTransformFilter** , que vous pouvez substituer.</span><span class="sxs-lookup"><span data-stu-id="166c8-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="166c8-108">Si vous dérivez de cette classe, vous devez substituer la méthode [**CTransformFilter :: GetPin**](ctransformfilter-getpin.md) du filtre pour créer des instances de votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="166c8-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>

<span data-ttu-id="166c8-109">Cette classe expose les interfaces **IMediaSeeking** et **IMediaPosition** via l’objet [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="166c8-109">This class exposes the **IMediaSeeking** and **IMediaPosition** interfaces through the [**CPosPassThru**](cpospassthru.md) object.</span></span> <span data-ttu-id="166c8-110">Elle transmet toutes les demandes de recherche au filtre suivant en amont.</span><span class="sxs-lookup"><span data-stu-id="166c8-110">It passes all seek requests to the next filter upstream.</span></span>



| <span data-ttu-id="166c8-111">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="166c8-111">Protected Member Variables</span></span>                                               | <span data-ttu-id="166c8-112">Description</span><span class="sxs-lookup"><span data-stu-id="166c8-112">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="166c8-113">**m \_ pTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="166c8-113">**m\_pTransformFilter**</span></span>](ctransformoutputpin-m-ptransformfilter.md)    | <span data-ttu-id="166c8-114">Pointeur désignant le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="166c8-114">Pointer to the owning filter.</span></span>                            |
| <span data-ttu-id="166c8-115">Variables membres publiques</span><span class="sxs-lookup"><span data-stu-id="166c8-115">Public Member Variables</span></span>                                                  | <span data-ttu-id="166c8-116">Description</span><span class="sxs-lookup"><span data-stu-id="166c8-116">Description</span></span>                                              |
| [<span data-ttu-id="166c8-117">**m \_ pPosition**</span><span class="sxs-lookup"><span data-stu-id="166c8-117">**m\_pPosition**</span></span>](ctransformoutputpin-m-pposition.md)                  | <span data-ttu-id="166c8-118">Objet d’assistance pour passer les commandes de recherche en amont.</span><span class="sxs-lookup"><span data-stu-id="166c8-118">Helper object to pass seek commands upstream.</span></span>            |
| <span data-ttu-id="166c8-119">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="166c8-119">Public Methods</span></span>                                                           | <span data-ttu-id="166c8-120">Description</span><span class="sxs-lookup"><span data-stu-id="166c8-120">Description</span></span>                                              |
| [<span data-ttu-id="166c8-121">**CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="166c8-121">**CTransformOutputPin**</span></span>](ctransformoutputpin-ctransformoutputpin.md)   | <span data-ttu-id="166c8-122">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="166c8-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="166c8-123">**~ CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="166c8-123">**~CTransformOutputPin**</span></span>](ctransformoutputpin--ctransformoutputpin.md) | <span data-ttu-id="166c8-124">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="166c8-124">Destructor method.</span></span>                                       |
| [<span data-ttu-id="166c8-125">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="166c8-125">**CheckConnect**</span></span>](ctransformoutputpin-checkconnect.md)                 | <span data-ttu-id="166c8-126">Détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="166c8-126">Determines whether a pin connection is suitable.</span></span>         |
| [<span data-ttu-id="166c8-127">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="166c8-127">**BreakConnect**</span></span>](ctransformoutputpin-breakconnect.md)                 | <span data-ttu-id="166c8-128">Libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="166c8-128">Releases the pin from a connection.</span></span>                      |
| [<span data-ttu-id="166c8-129">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="166c8-129">**CompleteConnect**</span></span>](ctransformoutputpin-completeconnect.md)           | <span data-ttu-id="166c8-130">Termine une connexion à un autre code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="166c8-130">Completes a connection to another pin.</span></span>                   |
| [<span data-ttu-id="166c8-131">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="166c8-131">**CheckMediaType**</span></span>](ctransformoutputpin-checkmediatype.md)             | <span data-ttu-id="166c8-132">Détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="166c8-132">Determines if the pin accepts a specific media type.</span></span>     |
| [<span data-ttu-id="166c8-133">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="166c8-133">**SetMediaType**</span></span>](ctransformoutputpin-setmediatype.md)                 | <span data-ttu-id="166c8-134">Définit le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="166c8-134">Sets the media type for the connection.</span></span>                  |
| [<span data-ttu-id="166c8-135">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="166c8-135">**DecideBufferSize**</span></span>](ctransformoutputpin-decidebuffersize.md)         | <span data-ttu-id="166c8-136">Définit les exigences de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="166c8-136">Sets the buffer requirements.</span></span>                            |
| [<span data-ttu-id="166c8-137">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="166c8-137">**GetMediaType**</span></span>](ctransformoutputpin-getmediatype.md)                 | <span data-ttu-id="166c8-138">Récupère un type de média par défaut, par valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="166c8-138">Retrieves a preferred media type, by index value.</span></span>        |
| [<span data-ttu-id="166c8-139">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="166c8-139">**CurrentMediaType**</span></span>](ctransformoutputpin-currentmediatype.md)         | <span data-ttu-id="166c8-140">Récupère le type de média pour la connexion de code confidentiel actuelle.</span><span class="sxs-lookup"><span data-stu-id="166c8-140">Retrieves the media type for the current pin connection.</span></span> |
| <span data-ttu-id="166c8-141">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="166c8-141">IPin Methods</span></span>                                                             | <span data-ttu-id="166c8-142">Description</span><span class="sxs-lookup"><span data-stu-id="166c8-142">Description</span></span>                                              |
| [<span data-ttu-id="166c8-143">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="166c8-143">**QueryId**</span></span>](ctransformoutputpin-queryid.md)                           | <span data-ttu-id="166c8-144">Récupère un identificateur pour le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="166c8-144">Retrieves an identifier for the pin.</span></span>                     |
| <span data-ttu-id="166c8-145">Méthodes IQualityControl</span><span class="sxs-lookup"><span data-stu-id="166c8-145">IQualityControl Methods</span></span>                                                  | <span data-ttu-id="166c8-146">Description</span><span class="sxs-lookup"><span data-stu-id="166c8-146">Description</span></span>                                              |
| [<span data-ttu-id="166c8-147">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="166c8-147">**Notify**</span></span>](ctransformoutputpin-notify.md)                             | <span data-ttu-id="166c8-148">Notifie le code confidentiel qu’une modification de qualité est demandée.</span><span class="sxs-lookup"><span data-stu-id="166c8-148">Notifies the pin that a quality change is requested.</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="166c8-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="166c8-149">Requirements</span></span>



| <span data-ttu-id="166c8-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="166c8-150">Requirement</span></span> | <span data-ttu-id="166c8-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="166c8-151">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="166c8-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="166c8-152">Header</span></span><br/>  | <dl> <span data-ttu-id="166c8-153"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="166c8-153"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="166c8-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="166c8-154">Library</span></span><br/> | <dl> <span data-ttu-id="166c8-155"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="166c8-155"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




