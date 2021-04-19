---
description: La classe CBaseRendererInputPin implémente une broche d’entrée pour la classe CBaseRenderer. Sauf indication contraire, les méthodes de cette classe délèguent aux méthodes correspondantes sur la classe CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: CRendererInputPin, classe (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531122"
---
# <a name="crendererinputpin-class"></a><span data-ttu-id="57ad8-104">CRendererInputPin, classe</span><span class="sxs-lookup"><span data-stu-id="57ad8-104">CRendererInputPin class</span></span>

![hiérarchie de la classe crendererinput pin](images/rbase01.png)

<span data-ttu-id="57ad8-106">La classe **CBaseRendererInputPin** implémente une broche d’entrée pour la classe [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="57ad8-106">The **CBaseRendererInputPin** class implements an input pin for the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="57ad8-107">Sauf indication contraire, les méthodes de cette classe délèguent aux méthodes correspondantes sur la classe **CBaseRenderer** .</span><span class="sxs-lookup"><span data-stu-id="57ad8-107">Except where noted, the methods in this class delegate to corresponding methods on the **CBaseRenderer** class.</span></span>



| <span data-ttu-id="57ad8-108">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="57ad8-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="57ad8-109">Description</span><span class="sxs-lookup"><span data-stu-id="57ad8-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="57ad8-110">**m \_ pRenderer**</span><span class="sxs-lookup"><span data-stu-id="57ad8-110">**m\_pRenderer**</span></span>](crendererinputpin-m-prenderer.md)            | <span data-ttu-id="57ad8-111">Pointeur vers le filtre.</span><span class="sxs-lookup"><span data-stu-id="57ad8-111">Pointer to the filter.</span></span>                                                                 |
| <span data-ttu-id="57ad8-112">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="57ad8-112">Public Methods</span></span>                                                   | <span data-ttu-id="57ad8-113">Description</span><span class="sxs-lookup"><span data-stu-id="57ad8-113">Description</span></span>                                                                            |
| [<span data-ttu-id="57ad8-114">**CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="57ad8-114">**CRendererInputPin**</span></span>](crendererinputpin-crendererinputpin.md) | <span data-ttu-id="57ad8-115">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="57ad8-115">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="57ad8-116">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="57ad8-116">**BreakConnect**</span></span>](crendererinputpin-breakconnect.md)           | <span data-ttu-id="57ad8-117">Ajoute du code personnalisé lors de la rupture d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="57ad8-117">Adds customized code upon breaking a connection.</span></span>                                       |
| [<span data-ttu-id="57ad8-118">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="57ad8-118">**CompleteConnect**</span></span>](crendererinputpin-completeconnect.md)     | <span data-ttu-id="57ad8-119">Termine la connexion.</span><span class="sxs-lookup"><span data-stu-id="57ad8-119">Completes the connection.</span></span>                                                              |
| [<span data-ttu-id="57ad8-120">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="57ad8-120">**CheckMediaType**</span></span>](crendererinputpin-checkmediatype.md)       | <span data-ttu-id="57ad8-121">Détermine si le code confidentiel peut prendre en charge un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="57ad8-121">Determines if the pin can support a specific media type.</span></span>                               |
| [<span data-ttu-id="57ad8-122">**Proactive**</span><span class="sxs-lookup"><span data-stu-id="57ad8-122">**Active**</span></span>](crendererinputpin-active.md)                       | <span data-ttu-id="57ad8-123">Bascule le code PIN sur le mode actif (en pause ou en cours d’exécution).</span><span class="sxs-lookup"><span data-stu-id="57ad8-123">Switches the pin to the active (paused or running) mode.</span></span>                               |
| [<span data-ttu-id="57ad8-124">**Inactif**</span><span class="sxs-lookup"><span data-stu-id="57ad8-124">**Inactive**</span></span>](crendererinputpin-inactive.md)                   | <span data-ttu-id="57ad8-125">Bascule le code confidentiel vers un état inactif et libère la mémoire de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="57ad8-125">Switches the pin to an inactive state and releases the memory of the allocator.</span></span>        |
| [<span data-ttu-id="57ad8-126">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="57ad8-126">**SetMediaType**</span></span>](crendererinputpin-setmediatype.md)           | <span data-ttu-id="57ad8-127">Définit le type de média du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="57ad8-127">Sets the media type of the pin.</span></span>                                                        |
| [<span data-ttu-id="57ad8-128">**Allocateur**</span><span class="sxs-lookup"><span data-stu-id="57ad8-128">**Allocator**</span></span>](crendererinputpin-allocator.md)                 | <span data-ttu-id="57ad8-129">Récupère un pointeur vers l’allocateur de mémoire par défaut.</span><span class="sxs-lookup"><span data-stu-id="57ad8-129">Retrieves a pointer to the default memory allocator.</span></span>                                   |
| <span data-ttu-id="57ad8-130">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="57ad8-130">IPin Methods</span></span>                                                     | <span data-ttu-id="57ad8-131">Description</span><span class="sxs-lookup"><span data-stu-id="57ad8-131">Description</span></span>                                                                            |
| [<span data-ttu-id="57ad8-132">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="57ad8-132">**QueryId**</span></span>](crendererinputpin-queryid.md)                     | <span data-ttu-id="57ad8-133">Récupère un identificateur pour le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="57ad8-133">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="57ad8-134">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="57ad8-134">**EndOfStream**</span></span>](crendererinputpin-endofstream.md)             | <span data-ttu-id="57ad8-135">Informe le code confidentiel qu’aucune donnée supplémentaire n’est attendue tant qu’une nouvelle commande d’exécution n’est pas émise.</span><span class="sxs-lookup"><span data-stu-id="57ad8-135">Informs the pin that no additional data is expected until a new run command is issued.</span></span> |
| [<span data-ttu-id="57ad8-136">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="57ad8-136">**BeginFlush**</span></span>](crendererinputpin-beginflush.md)               | <span data-ttu-id="57ad8-137">Indique au code PIN de commencer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="57ad8-137">Informs the pin to begin a flush operation.</span></span>                                            |
| [<span data-ttu-id="57ad8-138">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="57ad8-138">**EndFlush**</span></span>](crendererinputpin-endflush.md)                   | <span data-ttu-id="57ad8-139">Informe le code confidentiel pour terminer une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="57ad8-139">Informs the pin to end a flush operation.</span></span>                                              |
| <span data-ttu-id="57ad8-140">Méthodes IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="57ad8-140">IMemInputPin Methods</span></span>                                             | <span data-ttu-id="57ad8-141">Description</span><span class="sxs-lookup"><span data-stu-id="57ad8-141">Description</span></span>                                                                            |
| [<span data-ttu-id="57ad8-142">**Çoive**</span><span class="sxs-lookup"><span data-stu-id="57ad8-142">**Receive**</span></span>](crendererinputpin-receive.md)                     | <span data-ttu-id="57ad8-143">Récupère le bloc de données suivant à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="57ad8-143">Retrieves the next block of data from the stream.</span></span>                                      |



 

## <a name="requirements"></a><span data-ttu-id="57ad8-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57ad8-144">Requirements</span></span>



| <span data-ttu-id="57ad8-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57ad8-145">Requirement</span></span> | <span data-ttu-id="57ad8-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="57ad8-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ad8-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="57ad8-147">Header</span></span><br/>  | <dl> <span data-ttu-id="57ad8-148"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57ad8-148"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57ad8-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="57ad8-149">Library</span></span><br/> | <dl> <span data-ttu-id="57ad8-150"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="57ad8-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




