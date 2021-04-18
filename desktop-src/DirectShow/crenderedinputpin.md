---
description: La classe CRenderedInputPin est une classe de base pour l’implémentation d’une broche d’entrée sur un convertisseur.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: CRenderedInputPin, classe (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540312"
---
# <a name="crenderedinputpin-class"></a><span data-ttu-id="7e191-103">CRenderedInputPin, classe</span><span class="sxs-lookup"><span data-stu-id="7e191-103">CRenderedInputPin class</span></span>

![hiérarchie de la classe crenderedinputpin](images/rbase04.png)

<span data-ttu-id="7e191-105">La classe **CRenderedInputPin** est une classe de base pour l’implémentation d’une broche d’entrée sur un convertisseur.</span><span class="sxs-lookup"><span data-stu-id="7e191-105">The **CRenderedInputPin** class is a base class for implementing an input pin on a renderer.</span></span> <span data-ttu-id="7e191-106">Cette classe est conçue pour les filtres de convertisseur qui ne dérivent pas de la classe [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="7e191-106">This class is designed for renderer filters that do not derive from the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="7e191-107">(Les filtres qui dérivent de **CBaseRenderer** doivent utiliser la classe [**CRendererInputPin**](crendererinputpin.md) pour la broche d’entrée.)</span><span class="sxs-lookup"><span data-stu-id="7e191-107">(Filters that derive from **CBaseRenderer** should use the [**CRendererInputPin**](crendererinputpin.md) class for the input pin.)</span></span>

<span data-ttu-id="7e191-108">Pour utiliser cette classe, vous devez effectuer au moins ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7e191-108">To use this class, you must do at least the following:</span></span>

-   <span data-ttu-id="7e191-109">Déclarez une nouvelle classe pin qui hérite de **CRenderedInputPin**.</span><span class="sxs-lookup"><span data-stu-id="7e191-109">Declare a new pin class that inherits **CRenderedInputPin**.</span></span>
-   <span data-ttu-id="7e191-110">Dans votre classe pin, déclarez un objet de section critique pour conserver le verrou de streaming.</span><span class="sxs-lookup"><span data-stu-id="7e191-110">In your pin class, declare a critical section object to hold the streaming lock.</span></span> <span data-ttu-id="7e191-111">Vous pouvez utiliser la classe [**CCritSec**](ccritsec.md) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="7e191-111">You can use the [**CCritSec**](ccritsec.md) class for this purpose.</span></span> <span data-ttu-id="7e191-112">Pour plus d’informations, consultez [threads et sections critiques](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="7e191-112">For more information, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>
-   <span data-ttu-id="7e191-113">Remplacez [**CRenderedInputPin :: EndOfStream**](crenderedinputpin-endofstream.md) pour conserver le verrou de streaming.</span><span class="sxs-lookup"><span data-stu-id="7e191-113">Override [**CRenderedInputPin::EndOfStream**](crenderedinputpin-endofstream.md) to hold the streaming lock.</span></span>
-   <span data-ttu-id="7e191-114">Implémentez les méthodes [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md)et [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="7e191-114">Implement the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md), and [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) methods.</span></span>
-   <span data-ttu-id="7e191-115">Dans votre filtre, implémentez [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) pour retourner une instance de votre classe pin.</span><span class="sxs-lookup"><span data-stu-id="7e191-115">In your filter, implement [**CBaseFilter::GetPin**](cbasefilter-getpin.md) to return an instance of your pin class.</span></span>

<span data-ttu-id="7e191-116">Vous pouvez utiliser cette classe dans un convertisseur qui a plusieurs broches d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7e191-116">You can use this class in a renderer that has more than one input pin.</span></span> <span data-ttu-id="7e191-117">Cette classe hérite de la classe [**CBaseInputPin**](cbaseinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="7e191-117">This class inherits the [**CBaseInputPin**](cbaseinputpin.md) class.</span></span>



| <span data-ttu-id="7e191-118">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="7e191-118">Protected Member Variables</span></span>                                            | <span data-ttu-id="7e191-119">Description</span><span class="sxs-lookup"><span data-stu-id="7e191-119">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e191-120">**m \_ bAtEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="7e191-120">**m\_bAtEndOfStream**</span></span>](crenderedinputpin-m-batendofstream.md)       | <span data-ttu-id="7e191-121">Indique si la fin du flux a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="7e191-121">Indicates whether the end of the stream was reached.</span></span>                                                         |
| [<span data-ttu-id="7e191-122">**m \_ bCompleteNotified**</span><span class="sxs-lookup"><span data-stu-id="7e191-122">**m\_bCompleteNotified**</span></span>](crenderedinputpin-m-bcompletenotified.md) | <span data-ttu-id="7e191-123">Indique si le code pin a envoyé un événement [**EC \_ complet**](ec-complete.md) au gestionnaire du graphique de filtres.</span><span class="sxs-lookup"><span data-stu-id="7e191-123">Indicates whether the pin has sent an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> |
| <span data-ttu-id="7e191-124">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="7e191-124">Public Methods</span></span>                                                        | <span data-ttu-id="7e191-125">Description</span><span class="sxs-lookup"><span data-stu-id="7e191-125">Description</span></span>                                                                                                  |
| [<span data-ttu-id="7e191-126">**Actif**</span><span class="sxs-lookup"><span data-stu-id="7e191-126">**Active**</span></span>](crenderedinputpin-active.md)                            | <span data-ttu-id="7e191-127">Notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="7e191-127">Notifies the pin that the filter is now active.</span></span>                                                              |
| [<span data-ttu-id="7e191-128">**CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="7e191-128">**CRenderedInputPin**</span></span>](crenderedinputpin-crenderedinputpin.md)      | <span data-ttu-id="7e191-129">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="7e191-129">Constructor method.</span></span>                                                                                          |
| [<span data-ttu-id="7e191-130">**Utilisez**</span><span class="sxs-lookup"><span data-stu-id="7e191-130">**Run**</span></span>](crenderedinputpin-run.md)                                  | <span data-ttu-id="7e191-131">Notifie le code confidentiel que le filtre est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7e191-131">Notifies the pin that the filter is now running.</span></span>                                                             |
| <span data-ttu-id="7e191-132">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="7e191-132">IPin Methods</span></span>                                                          | <span data-ttu-id="7e191-133">Description</span><span class="sxs-lookup"><span data-stu-id="7e191-133">Description</span></span>                                                                                                  |
| [<span data-ttu-id="7e191-134">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="7e191-134">**EndFlush**</span></span>](crenderedinputpin-endflush.md)                        | <span data-ttu-id="7e191-135">Termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="7e191-135">Ends a flush operation.</span></span>                                                                                      |
| [<span data-ttu-id="7e191-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="7e191-136">**EndOfStream**</span></span>](crenderedinputpin-endofstream.md)                  | <span data-ttu-id="7e191-137">Indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue tant que le filtre n’a pas reçu une nouvelle commande Run.</span><span class="sxs-lookup"><span data-stu-id="7e191-137">Notifies the pin that no additional data is expected until the filter receives a new run command.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="7e191-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e191-138">Requirements</span></span>



| <span data-ttu-id="7e191-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e191-139">Requirement</span></span> | <span data-ttu-id="7e191-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e191-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e191-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e191-141">Header</span></span><br/>  | <dl> <span data-ttu-id="7e191-142"><dt>Amextra. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e191-142"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7e191-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7e191-143">Library</span></span><br/> | <dl> <span data-ttu-id="7e191-144"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7e191-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




