---
description: La classe CTransformInputPin implémente une broche d’entrée qui est utilisée par la classe CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: CTransformInputPin, classe (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531130"
---
# <a name="ctransforminputpin-class"></a><span data-ttu-id="1c988-103">CTransformInputPin, classe</span><span class="sxs-lookup"><span data-stu-id="1c988-103">CTransformInputPin class</span></span>

![hiérarchie de la classe ctransforminputpin](images/tfrm01.png)

<span data-ttu-id="1c988-105">La `CTransformInputPin` classe implémente une broche d’entrée qui est utilisée par la classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="1c988-105">The `CTransformInputPin` class implements an input pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="1c988-106">En règle générale, vous n’avez pas besoin de dériver de cette classe.</span><span class="sxs-lookup"><span data-stu-id="1c988-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="1c988-107">La plupart des méthodes de cette classe appellent les méthodes correspondantes sur la classe **CTransformFilter** , que vous pouvez substituer.</span><span class="sxs-lookup"><span data-stu-id="1c988-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="1c988-108">Si vous dérivez de cette classe, vous devez substituer la méthode [**CTransformFilter :: GetPin**](ctransformfilter-getpin.md) du filtre pour créer des instances de votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="1c988-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="1c988-109">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="1c988-109">Protected Member Variables</span></span>                                           | <span data-ttu-id="1c988-110">Description</span><span class="sxs-lookup"><span data-stu-id="1c988-110">Description</span></span>                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c988-111">**m \_ pTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="1c988-111">**m\_pTransformFilter**</span></span>](ctransforminputpin-m-ptransformfilter.md) | <span data-ttu-id="1c988-112">Pointeur désignant le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="1c988-112">Pointer to the owning filter.</span></span>                                                          |
| <span data-ttu-id="1c988-113">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="1c988-113">Public Methods</span></span>                                                       | <span data-ttu-id="1c988-114">Description</span><span class="sxs-lookup"><span data-stu-id="1c988-114">Description</span></span>                                                                            |
| [<span data-ttu-id="1c988-115">**CTransformInputPin**</span><span class="sxs-lookup"><span data-stu-id="1c988-115">**CTransformInputPin**</span></span>](ctransforminputpin-ctransforminputpin.md)  | <span data-ttu-id="1c988-116">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="1c988-116">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="1c988-117">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="1c988-117">**CheckConnect**</span></span>](ctransforminputpin-checkconnect.md)              | <span data-ttu-id="1c988-118">Détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="1c988-118">Determines whether a pin connection is suitable.</span></span>                                       |
| [<span data-ttu-id="1c988-119">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="1c988-119">**BreakConnect**</span></span>](ctransforminputpin-breakconnect.md)              | <span data-ttu-id="1c988-120">Libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="1c988-120">Releases the pin from a connection.</span></span>                                                    |
| [<span data-ttu-id="1c988-121">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="1c988-121">**CompleteConnect**</span></span>](ctransforminputpin-completeconnect.md)        | <span data-ttu-id="1c988-122">Termine une connexion à un autre code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="1c988-122">Completes a connection to another pin.</span></span>                                                 |
| [<span data-ttu-id="1c988-123">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="1c988-123">**CheckMediaType**</span></span>](ctransforminputpin-checkmediatype.md)          | <span data-ttu-id="1c988-124">Détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="1c988-124">Determines if the pin accepts a specific media type.</span></span>                                   |
| [<span data-ttu-id="1c988-125">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="1c988-125">**SetMediaType**</span></span>](ctransforminputpin-setmediatype.md)              | <span data-ttu-id="1c988-126">Définit le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="1c988-126">Sets the media type for the connection.</span></span>                                                |
| [<span data-ttu-id="1c988-127">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="1c988-127">**CheckStreaming**</span></span>](ctransforminputpin-checkstreaming.md)          | <span data-ttu-id="1c988-128">Détermine si le code confidentiel peut accepter des exemples.</span><span class="sxs-lookup"><span data-stu-id="1c988-128">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="1c988-129">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="1c988-129">Virtual.</span></span>                                |
| [<span data-ttu-id="1c988-130">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="1c988-130">**CurrentMediaType**</span></span>](ctransforminputpin-currentmediatype.md)      | <span data-ttu-id="1c988-131">Récupère le type de média pour la connexion de code confidentiel actuelle.</span><span class="sxs-lookup"><span data-stu-id="1c988-131">Retrieves the media type for the current pin connection.</span></span>                               |
| <span data-ttu-id="1c988-132">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="1c988-132">IPin Methods</span></span>                                                         | <span data-ttu-id="1c988-133">Description</span><span class="sxs-lookup"><span data-stu-id="1c988-133">Description</span></span>                                                                            |
| [<span data-ttu-id="1c988-134">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="1c988-134">**QueryId**</span></span>](ctransforminputpin-queryid.md)                        | <span data-ttu-id="1c988-135">Récupère un identificateur pour le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="1c988-135">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="1c988-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="1c988-136">**EndOfStream**</span></span>](ctransforminputpin-endofstream.md)                | <span data-ttu-id="1c988-137">Notifie le code confidentiel qu’aucune donnée supplémentaire n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="1c988-137">Notifies the pin that no additional data is expected.</span></span>                                  |
| [<span data-ttu-id="1c988-138">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="1c988-138">**BeginFlush**</span></span>](ctransforminputpin-beginflush.md)                  | <span data-ttu-id="1c988-139">Commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="1c988-139">Begins a flush operation.</span></span>                                                              |
| [<span data-ttu-id="1c988-140">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="1c988-140">**EndFlush**</span></span>](ctransforminputpin-endflush.md)                      | <span data-ttu-id="1c988-141">Termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="1c988-141">Ends a flush operation.</span></span>                                                                |
| [<span data-ttu-id="1c988-142">**NewSegment**</span><span class="sxs-lookup"><span data-stu-id="1c988-142">**NewSegment**</span></span>](ctransforminputpin-newsegment.md)                  | <span data-ttu-id="1c988-143">Avertit le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment.</span><span class="sxs-lookup"><span data-stu-id="1c988-143">Notifies the pin that media samples received after this call are grouped as a segment.</span></span> |
| <span data-ttu-id="1c988-144">Méthodes IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="1c988-144">IMemInputPin Methods</span></span>                                                 | <span data-ttu-id="1c988-145">Description</span><span class="sxs-lookup"><span data-stu-id="1c988-145">Description</span></span>                                                                            |
| [<span data-ttu-id="1c988-146">**Çoive**</span><span class="sxs-lookup"><span data-stu-id="1c988-146">**Receive**</span></span>](ctransforminputpin-receive.md)                        | <span data-ttu-id="1c988-147">Reçoit l’échantillon de média suivant dans le flux.</span><span class="sxs-lookup"><span data-stu-id="1c988-147">Receives the next media sample in the stream.</span></span>                                          |



 

## <a name="requirements"></a><span data-ttu-id="1c988-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c988-148">Requirements</span></span>



| <span data-ttu-id="1c988-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c988-149">Requirement</span></span> | <span data-ttu-id="1c988-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c988-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c988-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c988-151">Header</span></span><br/>  | <dl> <span data-ttu-id="1c988-152"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c988-152"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1c988-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1c988-153">Library</span></span><br/> | <dl> <span data-ttu-id="1c988-154"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c988-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




