---
description: Le modèle de classe CGenericList qui implémente une liste spécifique au type. Pour plus d’informations, consultez CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: CGenericList, classe (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529893"
---
# <a name="cgenericlist-class"></a><span data-ttu-id="4228f-104">CGenericList, classe</span><span class="sxs-lookup"><span data-stu-id="4228f-104">CGenericList class</span></span>

![hiérarchie de la classe cgenericlist](images/list01.png)

<span data-ttu-id="4228f-106">`CGenericList`Modèle de classe qui implémente une liste spécifique au type.</span><span class="sxs-lookup"><span data-stu-id="4228f-106">The `CGenericList` class template that implements a type-specific list.</span></span> <span data-ttu-id="4228f-107">Pour plus d’informations, consultez [**CBaseList**](cbaselist.md).</span><span class="sxs-lookup"><span data-stu-id="4228f-107">For more information, see [**CBaseList**](cbaselist.md).</span></span>

<span data-ttu-id="4228f-108">Pour utiliser ce modèle, déclarez une variable de type `CGenericList` avec un argument de modèle qui définit le type d’objet dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-108">To use this template, declare a variable of type `CGenericList` with a template argument that defines the type of object in the list.</span></span> <span data-ttu-id="4228f-109">Par exemple, l’instruction suivante déclare une liste d’objets [**CBaseFilter**](cbasefilter.md) :</span><span class="sxs-lookup"><span data-stu-id="4228f-109">For example, the following statement declares a list of [**CBaseFilter**](cbasefilter.md) objects:</span></span>


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



<span data-ttu-id="4228f-110">Pour plus de commodité, Wxlist. h définit les types de liste suivants :</span><span class="sxs-lookup"><span data-stu-id="4228f-110">For convenience, Wxlist.h defines the following list types:</span></span>

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| <span data-ttu-id="4228f-111">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="4228f-111">Public Methods</span></span>                                          | <span data-ttu-id="4228f-112">Description</span><span class="sxs-lookup"><span data-stu-id="4228f-112">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="4228f-113">**CGenericList**</span><span class="sxs-lookup"><span data-stu-id="4228f-113">**CGenericList**</span></span>](cgenericlist-cgenericlist.md)       | <span data-ttu-id="4228f-114">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="4228f-114">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="4228f-115">**~ CGenericList**</span><span class="sxs-lookup"><span data-stu-id="4228f-115">**~CGenericList**</span></span>](cgenericlist--cgenericlist.md)     | <span data-ttu-id="4228f-116">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="4228f-116">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="4228f-117">**GetHeadPosition**</span><span class="sxs-lookup"><span data-stu-id="4228f-117">**GetHeadPosition**</span></span>](cgenericlist-getheadposition.md) | <span data-ttu-id="4228f-118">Récupère la position du premier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-118">Retrieves the position of the first item in the list.</span></span>                    |
| [<span data-ttu-id="4228f-119">**GetTailPosition**</span><span class="sxs-lookup"><span data-stu-id="4228f-119">**GetTailPosition**</span></span>](cgenericlist-gettailposition.md) | <span data-ttu-id="4228f-120">Récupère la position du dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-120">Retrieves the position of the last item of the list.</span></span>                     |
| [<span data-ttu-id="4228f-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="4228f-121">**GetCount**</span></span>](cgenericlist-getcount.md)               | <span data-ttu-id="4228f-122">Récupère le nombre d’éléments dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-122">Retrieves the number of items in the list.</span></span>                               |
| [<span data-ttu-id="4228f-123">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="4228f-123">**GetNext**</span></span>](cgenericlist-getnext.md)                 | <span data-ttu-id="4228f-124">Récupère l’élément à la position spécifiée et avance la position.</span><span class="sxs-lookup"><span data-stu-id="4228f-124">Retrieves the item at the specified position, and advances the position.</span></span> |
| [<span data-ttu-id="4228f-125">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="4228f-125">**Get**</span></span>](cgenericlist-get.md)                         | <span data-ttu-id="4228f-126">Récupère l’élément à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4228f-126">Retrieves the item at the specified position.</span></span>                            |
| [<span data-ttu-id="4228f-127">**GetHead**</span><span class="sxs-lookup"><span data-stu-id="4228f-127">**GetHead**</span></span>](cgenericlist-gethead.md)                 | <span data-ttu-id="4228f-128">Récupère l’élément au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-128">Retrieves the item at the head of the list.</span></span>                              |
| [<span data-ttu-id="4228f-129">**RemoveHead**</span><span class="sxs-lookup"><span data-stu-id="4228f-129">**RemoveHead**</span></span>](cgenericlist-removehead.md)           | <span data-ttu-id="4228f-130">Supprime le premier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-130">Removes the first item in the list.</span></span>                                      |
| [<span data-ttu-id="4228f-131">**RemoveTail**</span><span class="sxs-lookup"><span data-stu-id="4228f-131">**RemoveTail**</span></span>](cgenericlist-removetail.md)           | <span data-ttu-id="4228f-132">Supprime le dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-132">Removes the last item in the list.</span></span>                                       |
| [<span data-ttu-id="4228f-133">**Installez**</span><span class="sxs-lookup"><span data-stu-id="4228f-133">**Remove**</span></span>](cgenericlist-remove.md)                   | <span data-ttu-id="4228f-134">Supprime l'élément à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4228f-134">Removes the item at the specified position.</span></span>                              |
| [<span data-ttu-id="4228f-135">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="4228f-135">**AddBefore**</span></span>](cgenericlist-addbefore.md)             | <span data-ttu-id="4228f-136">Insère un élément ou une liste avant la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4228f-136">Inserts an item or list before the specified position.</span></span>                   |
| [<span data-ttu-id="4228f-137">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="4228f-137">**AddAfter**</span></span>](cgenericlist-addafter.md)               | <span data-ttu-id="4228f-138">Insère un élément ou une liste après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4228f-138">Inserts an item or list after the specified position.</span></span>                    |
| [<span data-ttu-id="4228f-139">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="4228f-139">**AddHead**</span></span>](cgenericlist-addhead.md)                 | <span data-ttu-id="4228f-140">Ajoute un élément ou une liste au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-140">Adds an item or list to the front of the list.</span></span>                           |
| [<span data-ttu-id="4228f-141">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="4228f-141">**AddTail**</span></span>](cgenericlist-addtail.md)                 | <span data-ttu-id="4228f-142">Ajoute un élément ou une liste à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="4228f-142">Appends an item or list to the end of the list.</span></span>                          |
| [<span data-ttu-id="4228f-143">**Trouver**</span><span class="sxs-lookup"><span data-stu-id="4228f-143">**Find**</span></span>](cgenericlist-find.md)                       | <span data-ttu-id="4228f-144">Récupère la première position qui contient l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="4228f-144">Retrieves the first position that holds the specified item.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="4228f-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4228f-145">Requirements</span></span>



| <span data-ttu-id="4228f-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4228f-146">Requirement</span></span> | <span data-ttu-id="4228f-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="4228f-147">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4228f-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="4228f-148">Header</span></span><br/>  | <dl> <span data-ttu-id="4228f-149"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4228f-149"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4228f-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4228f-150">Library</span></span><br/> | <dl> <span data-ttu-id="4228f-151"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4228f-151"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




