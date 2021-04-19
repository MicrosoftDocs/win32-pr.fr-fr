---
description: La classe CImageAllocator implémente un allocateur qui gère les bitmaps indépendantes du périphérique (DIB) GDI. Cette classe dérive de la classe CBaseAllocator. Il crée des exemples de supports qui sont implémentés à l’aide de la classe CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: CImageAllocator, classe (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528643"
---
# <a name="cimageallocator-class"></a><span data-ttu-id="43b0b-105">CImageAllocator, classe</span><span class="sxs-lookup"><span data-stu-id="43b0b-105">CImageAllocator class</span></span>

![hiérarchie de la classe cimageallocator](images/wutil04.png)

<span data-ttu-id="43b0b-107">La `CImageAllocator` classe implémente un allocateur qui gère les bitmaps indépendantes du périphérique (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="43b0b-107">The `CImageAllocator` class implements an allocator that manages GDI device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="43b0b-108">Cette classe dérive de la classe [**CBaseAllocator**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="43b0b-108">This class derives from the [**CBaseAllocator**](cbaseallocator.md) class.</span></span> <span data-ttu-id="43b0b-109">Il crée des exemples de supports qui sont implémentés à l’aide de la classe [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="43b0b-109">It creates media samples that are implemented using the [**CImageSample**](cimagesample.md) class.</span></span>

<span data-ttu-id="43b0b-110">Un allocateur est partagé par deux broches connectées, mais appartient toujours à l’un des filtres de la connexion.</span><span class="sxs-lookup"><span data-stu-id="43b0b-110">An allocator is shared by two connected pins, but is always owned by one of the filters in the connection.</span></span> <span data-ttu-id="43b0b-111">Un filtre qui utilise `CImageAllocator` doit assurer le suivi de la façon dont l’allocateur a été fourni par lui-même ou par l’autre filtre.</span><span class="sxs-lookup"><span data-stu-id="43b0b-111">A filter that uses `CImageAllocator` must keep track of whether the allocator was provided by itself or by the other filter.</span></span> <span data-ttu-id="43b0b-112">Si l’allocateur a été fourni seul, le filtre propriétaire peut s’appuyer sur le fait que tous les échantillons de média de l’allocateur sont des objets **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="43b0b-112">If the allocator was provided by itself, the owning filter can rely on the fact that all media samples from the allocator are **CImageSample** objects.</span></span> <span data-ttu-id="43b0b-113">Il peut donc utiliser l’objet **CImageSample** pour obtenir des informations sur le DIB, qui est stocké dans une structure [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="43b0b-113">It can therefore use the **CImageSample** object to obtain information about the DIB, which is stored in a [**DIBDATA**](dibdata.md) structure.</span></span>

<span data-ttu-id="43b0b-114">Le filtre propriétaire doit appeler **NotifyMediaType** chaque fois que le type de média change.</span><span class="sxs-lookup"><span data-stu-id="43b0b-114">The owning filter should call **NotifyMediaType** whenever the media type changes.</span></span>



| <span data-ttu-id="43b0b-115">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="43b0b-115">Protected Member Variables</span></span>                                     | <span data-ttu-id="43b0b-116">Description</span><span class="sxs-lookup"><span data-stu-id="43b0b-116">Description</span></span>                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="43b0b-117">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="43b0b-117">**m\_pFilter**</span></span>](cimageallocator-m-pfilter.md)                | <span data-ttu-id="43b0b-118">Pointeur désignant le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="43b0b-118">Pointer to the owning filter.</span></span>                                            |
| [<span data-ttu-id="43b0b-119">**m \_ pMediaType**</span><span class="sxs-lookup"><span data-stu-id="43b0b-119">**m\_pMediaType**</span></span>](cimageallocator-m-pmediatype.md)          | <span data-ttu-id="43b0b-120">Pointeur vers le type de média actuel.</span><span class="sxs-lookup"><span data-stu-id="43b0b-120">Pointer to the current media type.</span></span>                                       |
| <span data-ttu-id="43b0b-121">Méthodes protégées</span><span class="sxs-lookup"><span data-stu-id="43b0b-121">Protected Methods</span></span>                                              | <span data-ttu-id="43b0b-122">Description</span><span class="sxs-lookup"><span data-stu-id="43b0b-122">Description</span></span>                                                              |
| [<span data-ttu-id="43b0b-123">**Utilis**</span><span class="sxs-lookup"><span data-stu-id="43b0b-123">**Alloc**</span></span>](cimageallocator-alloc.md)                         | <span data-ttu-id="43b0b-124">Alloue de la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="43b0b-124">Allocates memory for the buffers.</span></span>                                        |
| [<span data-ttu-id="43b0b-125">**CheckSizes**</span><span class="sxs-lookup"><span data-stu-id="43b0b-125">**CheckSizes**</span></span>](cimageallocator-checksizes.md)               | <span data-ttu-id="43b0b-126">Vérifie les propriétés d’allocateur par rapport au type de média actuel.</span><span class="sxs-lookup"><span data-stu-id="43b0b-126">Checks allocator properties against the current media type.</span></span>              |
| [<span data-ttu-id="43b0b-127">**CreateDIB**</span><span class="sxs-lookup"><span data-stu-id="43b0b-127">**CreateDIB**</span></span>](cimageallocator-createdib.md)                 | <span data-ttu-id="43b0b-128">Crée un DIB.</span><span class="sxs-lookup"><span data-stu-id="43b0b-128">Creates a DIB.</span></span>                                                           |
| [<span data-ttu-id="43b0b-129">**CreateImageSample**</span><span class="sxs-lookup"><span data-stu-id="43b0b-129">**CreateImageSample**</span></span>](cimageallocator-createimagesample.md) | <span data-ttu-id="43b0b-130">Crée un exemple de support.</span><span class="sxs-lookup"><span data-stu-id="43b0b-130">Creates a media sample.</span></span> <span data-ttu-id="43b0b-131">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="43b0b-131">Virtual.</span></span>                                         |
| [<span data-ttu-id="43b0b-132">**Gratuit**</span><span class="sxs-lookup"><span data-stu-id="43b0b-132">**Free**</span></span>](cimageallocator-free.md)                           | <span data-ttu-id="43b0b-133">Libère toute la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="43b0b-133">Releases all of the buffer memory.</span></span>                                       |
| <span data-ttu-id="43b0b-134">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="43b0b-134">Public Methods</span></span>                                                 | <span data-ttu-id="43b0b-135">Description</span><span class="sxs-lookup"><span data-stu-id="43b0b-135">Description</span></span>                                                              |
| [<span data-ttu-id="43b0b-136">**CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="43b0b-136">**CImageAllocator**</span></span>](cimageallocator-cimageallocator.md)     | <span data-ttu-id="43b0b-137">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="43b0b-137">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="43b0b-138">**NotifyMediaType**</span><span class="sxs-lookup"><span data-stu-id="43b0b-138">**NotifyMediaType**</span></span>](cimageallocator-notifymediatype.md)     | <span data-ttu-id="43b0b-139">Informe l’objet du type de média actuel.</span><span class="sxs-lookup"><span data-stu-id="43b0b-139">Informs the object of the current media type.</span></span>                            |
| <span data-ttu-id="43b0b-140">Méthodes IMemAllocator</span><span class="sxs-lookup"><span data-stu-id="43b0b-140">IMemAllocator Methods</span></span>                                          | <span data-ttu-id="43b0b-141">Description</span><span class="sxs-lookup"><span data-stu-id="43b0b-141">Description</span></span>                                                              |
| [<span data-ttu-id="43b0b-142">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="43b0b-142">**SetProperties**</span></span>](cimageallocator-setproperties.md)         | <span data-ttu-id="43b0b-143">Spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="43b0b-143">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="43b0b-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43b0b-144">Requirements</span></span>



| <span data-ttu-id="43b0b-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43b0b-145">Requirement</span></span> | <span data-ttu-id="43b0b-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="43b0b-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b0b-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="43b0b-147">Header</span></span><br/>  | <dl> <span data-ttu-id="43b0b-148"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43b0b-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43b0b-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43b0b-149">Library</span></span><br/> | <dl> <span data-ttu-id="43b0b-150"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43b0b-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b0b-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43b0b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b0b-152">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="43b0b-152">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




