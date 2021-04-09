---
description: Contient un objet pour chaque propriété d’abonné de la collection SubscriptionsForComponent parente.
ms.assetid: 58c9edbd-1128-4b8c-bb5a-528c212aa6a7
title: Collection SubscriberProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7c7a563e3fd3e917812426e34debd87bfd534b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860970"
---
# <a name="subscriberproperties-collection"></a><span data-ttu-id="ec81d-103">Collection SubscriberProperties</span><span class="sxs-lookup"><span data-stu-id="ec81d-103">SubscriberProperties collection</span></span>

<span data-ttu-id="ec81d-104">Contient un objet pour chaque propriété d’abonné de la collection [**SubscriptionsForComponent**](subscriptionsforcomponent.md) parente.</span><span class="sxs-lookup"><span data-stu-id="ec81d-104">Contains an object for each subscriber property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="ec81d-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ec81d-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ec81d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ec81d-106">Members</span></span>

<span data-ttu-id="ec81d-107">La collection **SubscriberProperties** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ec81d-107">The **SubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ec81d-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="ec81d-108">Related Collections</span></span>

<span data-ttu-id="ec81d-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="ec81d-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ec81d-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ec81d-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ec81d-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ec81d-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ec81d-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ec81d-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ec81d-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="ec81d-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ec81d-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="ec81d-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="ec81d-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ec81d-115">Properties</span></span>

<span data-ttu-id="ec81d-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="ec81d-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ec81d-117">Nom</span><span class="sxs-lookup"><span data-stu-id="ec81d-117">Name</span></span>](#name)
-   [<span data-ttu-id="ec81d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec81d-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="ec81d-119">Nom</span><span class="sxs-lookup"><span data-stu-id="ec81d-119">Name</span></span>



| <span data-ttu-id="ec81d-120">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec81d-120">Entry</span></span> | <span data-ttu-id="ec81d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec81d-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec81d-122">Description</span><span class="sxs-lookup"><span data-stu-id="ec81d-122">Description</span></span>    | <span data-ttu-id="ec81d-123">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ec81d-123">The name of the property.</span></span> <span data-ttu-id="ec81d-124">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="ec81d-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ec81d-125">Accès</span><span class="sxs-lookup"><span data-stu-id="ec81d-125">Access</span></span>         | <span data-ttu-id="ec81d-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ec81d-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ec81d-127">Type</span><span class="sxs-lookup"><span data-stu-id="ec81d-127">Type</span></span>           | <span data-ttu-id="ec81d-128">String</span><span class="sxs-lookup"><span data-stu-id="ec81d-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ec81d-129">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ec81d-129">Default</span></span>        | <span data-ttu-id="ec81d-130">« Nouvelle propriété »</span><span class="sxs-lookup"><span data-stu-id="ec81d-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ec81d-131">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ec81d-131">Minimum system</span></span> | <span data-ttu-id="ec81d-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ec81d-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="ec81d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec81d-133">Value</span></span>



| <span data-ttu-id="ec81d-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="ec81d-134">Entry</span></span> | <span data-ttu-id="ec81d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec81d-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="ec81d-136">Description</span><span class="sxs-lookup"><span data-stu-id="ec81d-136">Description</span></span>    | <span data-ttu-id="ec81d-137">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ec81d-137">A value for the property.</span></span> |
| <span data-ttu-id="ec81d-138">Accès</span><span class="sxs-lookup"><span data-stu-id="ec81d-138">Access</span></span>         | <span data-ttu-id="ec81d-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ec81d-139">ReadWrite</span></span>                 |
| <span data-ttu-id="ec81d-140">Type</span><span class="sxs-lookup"><span data-stu-id="ec81d-140">Type</span></span>           | <span data-ttu-id="ec81d-141">Variante</span><span class="sxs-lookup"><span data-stu-id="ec81d-141">Variant</span></span>                   |
| <span data-ttu-id="ec81d-142">Default</span><span class="sxs-lookup"><span data-stu-id="ec81d-142">Default</span></span>        | <span data-ttu-id="ec81d-143">N/A</span><span class="sxs-lookup"><span data-stu-id="ec81d-143">N/A</span></span>                       |
| <span data-ttu-id="ec81d-144">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ec81d-144">Minimum system</span></span> | <span data-ttu-id="ec81d-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ec81d-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="ec81d-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec81d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec81d-147">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="ec81d-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
