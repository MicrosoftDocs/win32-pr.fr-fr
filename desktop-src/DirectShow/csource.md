---
description: La classe CSource est une classe de base pour l’implémentation de filtres sources. Un filtre dérivé de CSource contient une ou plusieurs broches de sortie dérivées de la classe CSourceStream. Chaque broche de sortie crée un thread de travail qui pousse les exemples de média en aval.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Classe CSource (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538125"
---
# <a name="csource-class"></a><span data-ttu-id="047b0-105">CSource, classe</span><span class="sxs-lookup"><span data-stu-id="047b0-105">CSource class</span></span>

![hiérarchie de la classe CSource](images/source01.png)

<span data-ttu-id="047b0-107">La classe **CSource** est une classe de base pour l’implémentation de filtres sources.</span><span class="sxs-lookup"><span data-stu-id="047b0-107">The **CSource** class is a base class for implementing source filters.</span></span> <span data-ttu-id="047b0-108">Un filtre dérivé de **CSource** contient une ou plusieurs broches de sortie dérivées de la classe [**CSourceStream**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="047b0-108">A filter derived from **CSource** contains one or more output pins derived from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="047b0-109">Chaque broche de sortie crée un thread de travail qui pousse les exemples de média en aval.</span><span class="sxs-lookup"><span data-stu-id="047b0-109">Each output pin creates a worker thread that pushes media samples downstream.</span></span>

> [!Note]  
> <span data-ttu-id="047b0-110">La classe **CSource** est conçue pour prendre en charge le modèle push pour le workflow de données.</span><span class="sxs-lookup"><span data-stu-id="047b0-110">The **CSource** class is designed to support the push model for data flow.</span></span> <span data-ttu-id="047b0-111">Cette classe n’est pas recommandée pour créer des filtres de lecteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="047b0-111">This class is not recommended for creating file-reader filters.</span></span> <span data-ttu-id="047b0-112">Les lecteurs de fichiers doivent prendre en charge le modèle d’extraction par le biais de l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="047b0-112">File readers should support the pull model, through the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="047b0-113">Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="047b0-113">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

 



| <span data-ttu-id="047b0-114">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="047b0-114">Protected Member Variables</span></span>                     | <span data-ttu-id="047b0-115">Description</span><span class="sxs-lookup"><span data-stu-id="047b0-115">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="047b0-116">**m \_ iPins**</span><span class="sxs-lookup"><span data-stu-id="047b0-116">**m\_iPins**</span></span>](csource-m-ipins.md)            | <span data-ttu-id="047b0-117">Nombre de broches sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="047b0-117">Number of pins on the filter.</span></span>                                |
| [<span data-ttu-id="047b0-118">**m \_ paStreams**</span><span class="sxs-lookup"><span data-stu-id="047b0-118">**m\_paStreams**</span></span>](csource-m-pastreams.md)    | <span data-ttu-id="047b0-119">Tableau de codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="047b0-119">Array of pins.</span></span>                                               |
| [<span data-ttu-id="047b0-120">**m \_ cStateLock**</span><span class="sxs-lookup"><span data-stu-id="047b0-120">**m\_cStateLock**</span></span>](csource-m-cstatelock.md)  | <span data-ttu-id="047b0-121">Objet de section critique qui protège l’état du filtre.</span><span class="sxs-lookup"><span data-stu-id="047b0-121">Critical section object that protects the filter state.</span></span>      |
| <span data-ttu-id="047b0-122">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="047b0-122">Public Methods</span></span>                                 | <span data-ttu-id="047b0-123">Description</span><span class="sxs-lookup"><span data-stu-id="047b0-123">Description</span></span>                                                  |
| [<span data-ttu-id="047b0-124">**CSource**</span><span class="sxs-lookup"><span data-stu-id="047b0-124">**CSource**</span></span>](csource-csource.md)             | <span data-ttu-id="047b0-125">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="047b0-125">Constructor method.</span></span>                                          |
| [<span data-ttu-id="047b0-126">**~ CSource**</span><span class="sxs-lookup"><span data-stu-id="047b0-126">**~CSource**</span></span>](csource--csource.md)           | <span data-ttu-id="047b0-127">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="047b0-127">Destructor method.</span></span>                                           |
| [<span data-ttu-id="047b0-128">**GetPinCount**</span><span class="sxs-lookup"><span data-stu-id="047b0-128">**GetPinCount**</span></span>](csource-getpincount.md)     | <span data-ttu-id="047b0-129">Récupère le nombre de broches sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="047b0-129">Retrieves the number of pins on the filter.</span></span>                  |
| [<span data-ttu-id="047b0-130">**GetPin**</span><span class="sxs-lookup"><span data-stu-id="047b0-130">**GetPin**</span></span>](csource-getpin.md)               | <span data-ttu-id="047b0-131">Récupère un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="047b0-131">Retrieves a pin.</span></span>                                             |
| [<span data-ttu-id="047b0-132">**pStateLock**</span><span class="sxs-lookup"><span data-stu-id="047b0-132">**pStateLock**</span></span>](csource--pstatelock.md)      | <span data-ttu-id="047b0-133">Récupère un pointeur vers l’objet de section critique du filtre.</span><span class="sxs-lookup"><span data-stu-id="047b0-133">Retrieves a pointer to the filter's critical section object.</span></span> |
| [<span data-ttu-id="047b0-134">**AddPin**</span><span class="sxs-lookup"><span data-stu-id="047b0-134">**AddPin**</span></span>](csource-addpin.md)               | <span data-ttu-id="047b0-135">Ajoute une nouvelle broche de sortie au filtre.</span><span class="sxs-lookup"><span data-stu-id="047b0-135">Adds a new output pin to the filter.</span></span>                         |
| [<span data-ttu-id="047b0-136">**RemovePin**</span><span class="sxs-lookup"><span data-stu-id="047b0-136">**RemovePin**</span></span>](csource-removepin.md)         | <span data-ttu-id="047b0-137">Supprime un pin spécifié du filtre.</span><span class="sxs-lookup"><span data-stu-id="047b0-137">Removes a specified pin from the filter.</span></span>                     |
| [<span data-ttu-id="047b0-138">**FindPinNumber**</span><span class="sxs-lookup"><span data-stu-id="047b0-138">**FindPinNumber**</span></span>](csource-findpinnumber.md) | <span data-ttu-id="047b0-139">Récupère le numéro d’un pin spécifié sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="047b0-139">Retrieves the number of a specified pin on the filter.</span></span>       |
| <span data-ttu-id="047b0-140">Méthodes IBaseFilter</span><span class="sxs-lookup"><span data-stu-id="047b0-140">IBaseFilter Methods</span></span>                            | <span data-ttu-id="047b0-141">Description</span><span class="sxs-lookup"><span data-stu-id="047b0-141">Description</span></span>                                                  |
| [<span data-ttu-id="047b0-142">**FindPin**</span><span class="sxs-lookup"><span data-stu-id="047b0-142">**FindPin**</span></span>](csource-findpin.md)             | <span data-ttu-id="047b0-143">Récupère le code confidentiel avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="047b0-143">Retrieves the pin with the specified identifier.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="047b0-144">Notes</span><span class="sxs-lookup"><span data-stu-id="047b0-144">Remarks</span></span>

<span data-ttu-id="047b0-145">Pour implémenter une broche de sortie, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="047b0-145">To implement an output pin, do the following:</span></span>

-   <span data-ttu-id="047b0-146">Dérivez une classe de [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="047b0-146">Derive a class from [**CSourceStream**](csourcestream.md).</span></span>
-   <span data-ttu-id="047b0-147">Substituez la méthode [**CSourceStream :: GetMediaType**](csourcestream-getmediatype.md) et éventuellement la méthode [**CSourceStream :: CheckMediaType**](csourcestream-checkmediatype.md) , qui valide les types de média pour le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="047b0-147">Override the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method and possibly the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method, which validate media types for the pin.</span></span>
-   <span data-ttu-id="047b0-148">Implémentez la méthode [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , qui retourne les exigences de mémoire tampon du pin.</span><span class="sxs-lookup"><span data-stu-id="047b0-148">Implement the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method, which returns the pin's buffer requirements.</span></span>
-   <span data-ttu-id="047b0-149">Implémentez la méthode [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md) , qui remplit un exemple de mémoire tampon de média avec des données.</span><span class="sxs-lookup"><span data-stu-id="047b0-149">Implement the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which fills a media sample buffer with data.</span></span>

<span data-ttu-id="047b0-150">Pour implémenter le filtre, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="047b0-150">To implement the filter, do the following:</span></span>

-   <span data-ttu-id="047b0-151">Dérivez une classe de **CSource**.</span><span class="sxs-lookup"><span data-stu-id="047b0-151">Derive a class from **CSource**.</span></span>
-   <span data-ttu-id="047b0-152">Dans le constructeur, créez une ou plusieurs broches de sortie dérivées de [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="047b0-152">In the constructor, create one or more output pins derived from [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="047b0-153">Les codes confidentiels s’ajoutent automatiquement au filtre dans leurs méthodes de constructeur et se suppriment dans leurs méthodes de destructeur.</span><span class="sxs-lookup"><span data-stu-id="047b0-153">The pins automatically add themselves to the filter in their constructor methods, and remove themselves in their destructor methods.</span></span>

<span data-ttu-id="047b0-154">Pour synchroniser l’état de filtre entre plusieurs threads, appelez la méthode [**CSource ::P statelock**](csource--pstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="047b0-154">To synchronize the filter state among multiple threads, call the [**CSource::pStateLock**](csource--pstatelock.md) method.</span></span> <span data-ttu-id="047b0-155">Cette méthode retourne un pointeur vers la section critique de l’état de filtre.</span><span class="sxs-lookup"><span data-stu-id="047b0-155">This method returns a pointer to the filter-state critical section.</span></span> <span data-ttu-id="047b0-156">Utilisez la classe [**CAutoLock**](cautolock.md) pour contenir la section critique.</span><span class="sxs-lookup"><span data-stu-id="047b0-156">Use the [**CAutoLock**](cautolock.md) class to hold the critical section.</span></span> <span data-ttu-id="047b0-157">À partir d’un code confidentiel, vous pouvez accéder à **pStateLock** à partir de la variable membre [**CBasePin :: m \_ pFilter**](cbasepin-m-pfilter.md) du pin, comme suit :</span><span class="sxs-lookup"><span data-stu-id="047b0-157">From a pin, you can access **pStateLock** from the pin's [**CBasePin::m\_pFilter**](cbasepin-m-pfilter.md) member variable, as follows:</span></span>


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a><span data-ttu-id="047b0-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="047b0-158">Requirements</span></span>



| <span data-ttu-id="047b0-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="047b0-159">Requirement</span></span> | <span data-ttu-id="047b0-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="047b0-160">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047b0-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="047b0-161">Header</span></span><br/>  | <dl> <span data-ttu-id="047b0-162"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="047b0-162"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="047b0-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="047b0-163">Library</span></span><br/> | <dl> <span data-ttu-id="047b0-164"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="047b0-164"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047b0-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="047b0-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047b0-166">Écriture de filtres source</span><span class="sxs-lookup"><span data-stu-id="047b0-166">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




