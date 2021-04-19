---
description: La classe CMediaPosition gère les méthodes IDispatch de l’interface double IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: CMediaPosition, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543791"
---
# <a name="cmediaposition-class"></a><span data-ttu-id="052d5-103">CMediaPosition, classe</span><span class="sxs-lookup"><span data-stu-id="052d5-103">CMediaPosition class</span></span>

![hiérarchie de la classe cmediaposition](images/cutil14.png)

<span data-ttu-id="052d5-105">La classe **CMediaPosition** gère les méthodes **IDispatch** de l’interface double [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="052d5-105">The **CMediaPosition** class handles the **IDispatch** methods of the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) dual interface.</span></span>

<span data-ttu-id="052d5-106">Cette classe hérite de l’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , mais ne l’implémente pas.</span><span class="sxs-lookup"><span data-stu-id="052d5-106">This class inherits the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface but does not implement it.</span></span> <span data-ttu-id="052d5-107">Il implémente **IDispatch** par le biais de la classe [**CBaseDispatch**](cbasedispatch.md) et de la bibliothèque de types DirectShow.</span><span class="sxs-lookup"><span data-stu-id="052d5-107">It implements **IDispatch** through the [**CBaseDispatch**](cbasedispatch.md) class and the DirectShow type library.</span></span> <span data-ttu-id="052d5-108">N’utilisez pas cette classe directement.</span><span class="sxs-lookup"><span data-stu-id="052d5-108">Do not use this class directly.</span></span> <span data-ttu-id="052d5-109">Utilisez plutôt l’une des classes suivantes :</span><span class="sxs-lookup"><span data-stu-id="052d5-109">Instead, use one of the following classes:</span></span>

-   <span data-ttu-id="052d5-110">Filtres sources : utilisez la classe de base [**CSourceSeeking**](csourceseeking.md) pour implémenter la recherche.</span><span class="sxs-lookup"><span data-stu-id="052d5-110">Source filters: Use the [**CSourceSeeking**](csourceseeking.md) base class to implement seeking.</span></span>
-   <span data-ttu-id="052d5-111">Filtres de transformation : utilisez la classe [**CPosPassThru**](cpospassthru.md) pour transmettre les commandes de recherche en amont.</span><span class="sxs-lookup"><span data-stu-id="052d5-111">Transform filters: Use the [**CPosPassThru**](cpospassthru.md) class to pass seeking commands upstream.</span></span>
-   <span data-ttu-id="052d5-112">Convertisseurs : utilisez la classe [**CRendererPosPassThru**](crendererpospassthru.md) pour transmettre les commandes de recherche en amont.</span><span class="sxs-lookup"><span data-stu-id="052d5-112">Renderers: Use the [**CRendererPosPassThru**](crendererpospassthru.md) class to pass seeking commands upstream.</span></span>



| <span data-ttu-id="052d5-113">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="052d5-113">Public Methods</span></span>                                              | <span data-ttu-id="052d5-114">Description</span><span class="sxs-lookup"><span data-stu-id="052d5-114">Description</span></span>                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="052d5-115">**CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="052d5-115">**CMediaPosition**</span></span>](cmediaposition-cmediaposition.md)     | <span data-ttu-id="052d5-116">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="052d5-116">Constructor method.</span></span>                                                                                                 |
| <span data-ttu-id="052d5-117">Méthodes IDispatch</span><span class="sxs-lookup"><span data-stu-id="052d5-117">IDispatch Methods</span></span>                                           | <span data-ttu-id="052d5-118">Description</span><span class="sxs-lookup"><span data-stu-id="052d5-118">Description</span></span>                                                                                                         |
| [<span data-ttu-id="052d5-119">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="052d5-119">**GetIDsOfNames**</span></span>](cmediaposition-getidsofnames.md)       | <span data-ttu-id="052d5-120">Mappe un ensemble de noms à un ensemble correspondant de DISPID.</span><span class="sxs-lookup"><span data-stu-id="052d5-120">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="052d5-121">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="052d5-121">**GetTypeInfo**</span></span>](cmediaposition-gettypeinfo.md)           | <span data-ttu-id="052d5-122">Récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.</span><span class="sxs-lookup"><span data-stu-id="052d5-122">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="052d5-123">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="052d5-123">**GetTypeInfoCount**</span></span>](cmediaposition-gettypeinfocount.md) | <span data-ttu-id="052d5-124">Récupère le nombre d’interfaces d’informations de type fourni par l’objet.</span><span class="sxs-lookup"><span data-stu-id="052d5-124">Retrieves the number of type information interfaces the object provides.</span></span>                                            |
| [<span data-ttu-id="052d5-125">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="052d5-125">**Invoke**</span></span>](cmediaposition-invoke.md)                     | <span data-ttu-id="052d5-126">Fournit l’accès aux propriétés et aux méthodes exposées par l’objet.</span><span class="sxs-lookup"><span data-stu-id="052d5-126">Provides access to properties and methods exposed by the object.</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="052d5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="052d5-127">Requirements</span></span>



| <span data-ttu-id="052d5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="052d5-128">Requirement</span></span> | <span data-ttu-id="052d5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="052d5-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="052d5-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="052d5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="052d5-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="052d5-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="052d5-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="052d5-132">Library</span></span><br/> | <dl> <span data-ttu-id="052d5-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="052d5-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="052d5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="052d5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="052d5-135">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="052d5-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




