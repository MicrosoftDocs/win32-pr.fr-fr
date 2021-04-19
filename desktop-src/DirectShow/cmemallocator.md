---
description: Implémente un allocateur qui prend en charge l’interface IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: CMemAllocator, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542610"
---
# <a name="cmemallocator-class"></a><span data-ttu-id="3613c-103">CMemAllocator, classe</span><span class="sxs-lookup"><span data-stu-id="3613c-103">CMemAllocator class</span></span>

![hiérarchie de la classe cmemallocator](images/filter10.png)

<span data-ttu-id="3613c-105">Implémente un allocateur qui prend en charge l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="3613c-105">Implements an allocator that supports the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="3613c-106">Cette classe dérive de [**CBaseAllocator**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="3613c-106">This class derives from [**CBaseAllocator**](cbaseallocator.md).</span></span> <span data-ttu-id="3613c-107">Pour plus d’informations sur les allocators, reportez-vous à la documentation de [**CBaseAllocator**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="3613c-107">For more information about allocators, refer to the documentation for [**CBaseAllocator**](cbaseallocator.md).</span></span>



| <span data-ttu-id="3613c-108">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="3613c-108">Protected Member Variables</span></span>                              | <span data-ttu-id="3613c-109">Description</span><span class="sxs-lookup"><span data-stu-id="3613c-109">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="3613c-110">**m \_ pbuffer**</span><span class="sxs-lookup"><span data-stu-id="3613c-110">**m\_pBuffer**</span></span>](cmemallocator-m-pbuffer.md)           | <span data-ttu-id="3613c-111">Pointeur vers le bloc de mémoire qui contient les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="3613c-111">Pointer to the memory block that contains the buffers.</span></span>                   |
| <span data-ttu-id="3613c-112">Méthodes protégées</span><span class="sxs-lookup"><span data-stu-id="3613c-112">Protected Methods</span></span>                                       | <span data-ttu-id="3613c-113">Description</span><span class="sxs-lookup"><span data-stu-id="3613c-113">Description</span></span>                                                              |
| [<span data-ttu-id="3613c-114">**Gratuit**</span><span class="sxs-lookup"><span data-stu-id="3613c-114">**Free**</span></span>](cmemallocator-free.md)                      | <span data-ttu-id="3613c-115">Méthode d’espace réservé ; appelée pendant une opération de dévalidation.</span><span class="sxs-lookup"><span data-stu-id="3613c-115">Placeholder method; called during a decommit operation.</span></span>                  |
| [<span data-ttu-id="3613c-116">**ReallyFree**</span><span class="sxs-lookup"><span data-stu-id="3613c-116">**ReallyFree**</span></span>](cmemallocator-reallyfree.md)          | <span data-ttu-id="3613c-117">Libère la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="3613c-117">Releases the memory for the buffers.</span></span>                                     |
| [<span data-ttu-id="3613c-118">**Utilis**</span><span class="sxs-lookup"><span data-stu-id="3613c-118">**Alloc**</span></span>](cmemallocator-alloc.md)                    | <span data-ttu-id="3613c-119">Alloue de la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="3613c-119">Allocates memory for the buffers.</span></span>                                        |
| <span data-ttu-id="3613c-120">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="3613c-120">Public Methods</span></span>                                          | <span data-ttu-id="3613c-121">Description</span><span class="sxs-lookup"><span data-stu-id="3613c-121">Description</span></span>                                                              |
| [<span data-ttu-id="3613c-122">**CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="3613c-122">**CMemAllocator**</span></span>](cmemallocator-cmemallocator.md)    | <span data-ttu-id="3613c-123">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="3613c-123">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="3613c-124">**~ CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="3613c-124">**~ CMemAllocator**</span></span>](cmemallocator--cmemallocator.md) | <span data-ttu-id="3613c-125">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="3613c-125">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="3613c-126">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="3613c-126">**CreateInstance**</span></span>](cmemallocator-createinstance.md)  | <span data-ttu-id="3613c-127">Crée une nouvelle instance de la classe **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="3613c-127">Creates a new instance of the **CMemAllocator** class.</span></span>                   |
| <span data-ttu-id="3613c-128">Méthodes IMemAllocator</span><span class="sxs-lookup"><span data-stu-id="3613c-128">IMemAllocator Methods</span></span>                                   | <span data-ttu-id="3613c-129">Description</span><span class="sxs-lookup"><span data-stu-id="3613c-129">Description</span></span>                                                              |
| [<span data-ttu-id="3613c-130">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="3613c-130">**SetProperties**</span></span>](cmemallocator-setproperties.md)    | <span data-ttu-id="3613c-131">Spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3613c-131">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3613c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3613c-132">Requirements</span></span>



| <span data-ttu-id="3613c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3613c-133">Requirement</span></span> | <span data-ttu-id="3613c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="3613c-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3613c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="3613c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="3613c-136"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3613c-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3613c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3613c-137">Library</span></span><br/> | <dl> <span data-ttu-id="3613c-138"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3613c-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3613c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3613c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3613c-140">Fourniture d’un allocateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="3613c-140">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
</dt> </dl>

 

 




