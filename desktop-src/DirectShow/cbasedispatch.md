---
description: La classe CBaseDispatch est une classe de base pour l’implémentation de l’interface IDispatch dans un filtre DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: CBaseDispatch, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524007"
---
# <a name="cbasedispatch-class"></a><span data-ttu-id="0a5fd-103">CBaseDispatch, classe</span><span class="sxs-lookup"><span data-stu-id="0a5fd-103">CBaseDispatch class</span></span>

![hiérarchie de la classe cbasedispatch](images/cutil01.png)

<span data-ttu-id="0a5fd-105">La classe **CBaseDispatch** est une classe de base pour l’implémentation de l’interface **IDispatch** dans un filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-105">The **CBaseDispatch** class is a base class for implementing the **IDispatch** interface in a DirectShow filter.</span></span>

<span data-ttu-id="0a5fd-106">Cette classe est limitée à la prise en charge des interfaces compatibles Automation exportées par la bibliothèque de types DirectShow, QuartzTypeLib.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-106">This class is limited to supporting the Automation-compatible interfaces exported by the DirectShow type library, QuartzTypeLib.</span></span> <span data-ttu-id="0a5fd-107">Par exemple, les classes [**CMediaControl**](cmediacontrol.md) et [**CMediaPosition**](cmediaposition.md) utilisent **CBaseDispatch** pour implémenter [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectivement.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-107">For example, the [**CMediaControl**](cmediacontrol.md) and [**CMediaPosition**](cmediaposition.md) classes use **CBaseDispatch** to implement [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectively.</span></span> <span data-ttu-id="0a5fd-108">En raison de cette limitation, il n’y a probablement aucune raison d’utiliser **CBaseDispatch** directement dans vos propres filtres.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-108">Because of this limitation, there is probably no reason to use **CBaseDispatch** directly in your own filters.</span></span>

<span data-ttu-id="0a5fd-109">Pour utiliser cette classe, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0a5fd-109">To use this class, do the following:</span></span>

-   <span data-ttu-id="0a5fd-110">Déclarez une nouvelle classe qui prend en charge **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-110">Declare a new class that supports **IDispatch**.</span></span>
-   <span data-ttu-id="0a5fd-111">Donnez à votre nouvelle classe une variable membre privée de type **CBaseDispatch**.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-111">Give your new class a private member variable of type **CBaseDispatch**.</span></span>
-   <span data-ttu-id="0a5fd-112">Implémentez les méthodes **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="0a5fd-112">Implement the **IDispatch** methods.</span></span>
-   <span data-ttu-id="0a5fd-113">Dans vos méthodes **IDispatch** , appelez les méthodes **CBaseDispatch** .</span><span class="sxs-lookup"><span data-stu-id="0a5fd-113">In your **IDispatch** methods, call the **CBaseDispatch** methods.</span></span>

<span data-ttu-id="0a5fd-114">Pour plus d’informations, reportez-vous au code source de l’un des exemples de classes déclarés dans Ctlutil. h.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-114">For more details, refer to the source code for any of the sample classes declared in Ctlutil.h.</span></span>



| <span data-ttu-id="0a5fd-115">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="0a5fd-115">Public Methods</span></span>                                             | <span data-ttu-id="0a5fd-116">Description</span><span class="sxs-lookup"><span data-stu-id="0a5fd-116">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a5fd-117">**CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="0a5fd-117">**CBaseDispatch**</span></span>](cbasedispatch-cbasedispatch.md)       | <span data-ttu-id="0a5fd-118">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-118">Constructor method.</span></span>                                                                                                 |
| [<span data-ttu-id="0a5fd-119">**~ CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="0a5fd-119">**~CBaseDispatch**</span></span>](cbasedispatch--cbasedispatch.md)     | <span data-ttu-id="0a5fd-120">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-120">Destructor method.</span></span>                                                                                                  |
| [<span data-ttu-id="0a5fd-121">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="0a5fd-121">**GetIDsOfNames**</span></span>](cbasedispatch-getidsofnames.md)       | <span data-ttu-id="0a5fd-122">Mappe un ensemble de noms à un ensemble correspondant de DISPID.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-122">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="0a5fd-123">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="0a5fd-123">**GetTypeInfo**</span></span>](cbasedispatch-gettypeinfo.md)           | <span data-ttu-id="0a5fd-124">Récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-124">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="0a5fd-125">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="0a5fd-125">**GetTypeInfoCount**</span></span>](cbasedispatch-gettypeinfocount.md) | <span data-ttu-id="0a5fd-126">Récupère le nombre d’interfaces d’informations de type fourni par l’objet.</span><span class="sxs-lookup"><span data-stu-id="0a5fd-126">Retrieves the number of type information interfaces the object provides.</span></span>                                            |



 

## <a name="requirements"></a><span data-ttu-id="0a5fd-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a5fd-127">Requirements</span></span>



| <span data-ttu-id="0a5fd-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a5fd-128">Requirement</span></span> | <span data-ttu-id="0a5fd-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a5fd-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a5fd-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a5fd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0a5fd-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a5fd-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a5fd-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a5fd-132">Library</span></span><br/> | <dl> <span data-ttu-id="0a5fd-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0a5fd-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a5fd-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a5fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a5fd-135">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a5fd-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




