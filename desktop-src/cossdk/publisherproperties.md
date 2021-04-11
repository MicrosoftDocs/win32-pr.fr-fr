---
description: Contient un objet pour chaque propriété de serveur de publication pour la collection SubscriptionsForComponent parente.
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: Collection PublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: bdab3e8143ea3d35d07adb5caa73639fcb568cd1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110899"
---
# <a name="publisherproperties-collection"></a><span data-ttu-id="4a28f-103">Collection PublisherProperties</span><span class="sxs-lookup"><span data-stu-id="4a28f-103">PublisherProperties collection</span></span>

<span data-ttu-id="4a28f-104">Contient un objet pour chaque propriété de serveur de publication pour la collection [**SubscriptionsForComponent**](subscriptionsforcomponent.md) parente.</span><span class="sxs-lookup"><span data-stu-id="4a28f-104">Contains an object for each publisher property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="4a28f-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="4a28f-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4a28f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4a28f-106">Members</span></span>

<span data-ttu-id="4a28f-107">La collection **PublisherProperties** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4a28f-107">The **PublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4a28f-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="4a28f-108">Related Collections</span></span>

<span data-ttu-id="4a28f-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="4a28f-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4a28f-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4a28f-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4a28f-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4a28f-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4a28f-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4a28f-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="4a28f-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="4a28f-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4a28f-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="4a28f-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="4a28f-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4a28f-115">Properties</span></span>

<span data-ttu-id="4a28f-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="4a28f-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4a28f-117">Nom</span><span class="sxs-lookup"><span data-stu-id="4a28f-117">Name</span></span>](#name)
-   [<span data-ttu-id="4a28f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a28f-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="4a28f-119">Nom</span><span class="sxs-lookup"><span data-stu-id="4a28f-119">Name</span></span>



| <span data-ttu-id="4a28f-120">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a28f-120">Entry</span></span> | <span data-ttu-id="4a28f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a28f-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a28f-122">Description</span><span class="sxs-lookup"><span data-stu-id="4a28f-122">Description</span></span>    | <span data-ttu-id="4a28f-123">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4a28f-123">The name of the property.</span></span> <span data-ttu-id="4a28f-124">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="4a28f-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4a28f-125">Accès</span><span class="sxs-lookup"><span data-stu-id="4a28f-125">Access</span></span>         | <span data-ttu-id="4a28f-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="4a28f-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4a28f-127">Type</span><span class="sxs-lookup"><span data-stu-id="4a28f-127">Type</span></span>           | <span data-ttu-id="4a28f-128">String</span><span class="sxs-lookup"><span data-stu-id="4a28f-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4a28f-129">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4a28f-129">Default</span></span>        | <span data-ttu-id="4a28f-130">« Nouvelle propriété »</span><span class="sxs-lookup"><span data-stu-id="4a28f-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="4a28f-131">Système minimal</span><span class="sxs-lookup"><span data-stu-id="4a28f-131">Minimum system</span></span> | <span data-ttu-id="4a28f-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4a28f-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="4a28f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a28f-133">Value</span></span>



| <span data-ttu-id="4a28f-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a28f-134">Entry</span></span> | <span data-ttu-id="4a28f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a28f-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="4a28f-136">Description</span><span class="sxs-lookup"><span data-stu-id="4a28f-136">Description</span></span>    | <span data-ttu-id="4a28f-137">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4a28f-137">A value for the property.</span></span> |
| <span data-ttu-id="4a28f-138">Accès</span><span class="sxs-lookup"><span data-stu-id="4a28f-138">Access</span></span>         | <span data-ttu-id="4a28f-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4a28f-139">ReadWrite</span></span>                 |
| <span data-ttu-id="4a28f-140">Type</span><span class="sxs-lookup"><span data-stu-id="4a28f-140">Type</span></span>           | <span data-ttu-id="4a28f-141">Variante</span><span class="sxs-lookup"><span data-stu-id="4a28f-141">Variant</span></span>                   |
| <span data-ttu-id="4a28f-142">Default</span><span class="sxs-lookup"><span data-stu-id="4a28f-142">Default</span></span>        | <span data-ttu-id="4a28f-143">N/A</span><span class="sxs-lookup"><span data-stu-id="4a28f-143">N/A</span></span>                       |
| <span data-ttu-id="4a28f-144">Système minimal</span><span class="sxs-lookup"><span data-stu-id="4a28f-144">Minimum system</span></span> | <span data-ttu-id="4a28f-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4a28f-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="4a28f-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a28f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a28f-147">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="4a28f-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
