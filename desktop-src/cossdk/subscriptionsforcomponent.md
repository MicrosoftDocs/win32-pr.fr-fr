---
description: Contient un objet pour chaque abonnement de la collection de composants parents.
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: Collection SubscriptionsForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: c8334aa54b56a9dccaa7aa0787d8c997baf0445e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514525"
---
# <a name="subscriptionsforcomponent-collection"></a><span data-ttu-id="c5297-103">Collection SubscriptionsForComponent</span><span class="sxs-lookup"><span data-stu-id="c5297-103">SubscriptionsForComponent collection</span></span>

<span data-ttu-id="c5297-104">Contient un objet pour chaque abonnement de la collection de [**composants**](components.md) parents.</span><span class="sxs-lookup"><span data-stu-id="c5297-104">Contains an object for each subscription for the parent [**Components**](components.md) collection.</span></span>

<span data-ttu-id="c5297-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c5297-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="c5297-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c5297-106">Members</span></span>

<span data-ttu-id="c5297-107">La collection **SubscriptionsForComponent** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c5297-107">The **SubscriptionsForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="c5297-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="c5297-108">Related Collections</span></span>

<span data-ttu-id="c5297-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="c5297-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="c5297-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c5297-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="c5297-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="c5297-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="c5297-112">**PublisherProperties**</span><span class="sxs-lookup"><span data-stu-id="c5297-112">**PublisherProperties**</span></span>](publisherproperties.md)
-   [<span data-ttu-id="c5297-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="c5297-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="c5297-114">**SubscriberProperties**</span><span class="sxs-lookup"><span data-stu-id="c5297-114">**SubscriberProperties**</span></span>](subscriberproperties.md)

<span data-ttu-id="c5297-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="c5297-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="c5297-116">**Composants**</span><span class="sxs-lookup"><span data-stu-id="c5297-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="c5297-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c5297-117">Properties</span></span>

<span data-ttu-id="c5297-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="c5297-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="c5297-119">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-119">Description</span></span>](#description)
-   [<span data-ttu-id="c5297-120">Enabled</span><span class="sxs-lookup"><span data-stu-id="c5297-120">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="c5297-121">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="c5297-121">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="c5297-122">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="c5297-122">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="c5297-123">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="c5297-123">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="c5297-124">Identifiant</span><span class="sxs-lookup"><span data-stu-id="c5297-124">ID</span></span>](#subscriptionsforcomponent-collection)
-   [<span data-ttu-id="c5297-125">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="c5297-125">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="c5297-126">MachineName</span><span class="sxs-lookup"><span data-stu-id="c5297-126">MachineName</span></span>](#machinename)
-   [<span data-ttu-id="c5297-127">MethodName</span><span class="sxs-lookup"><span data-stu-id="c5297-127">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="c5297-128">Nom</span><span class="sxs-lookup"><span data-stu-id="c5297-128">Name</span></span>](#machinename)
-   [<span data-ttu-id="c5297-129">PerUser</span><span class="sxs-lookup"><span data-stu-id="c5297-129">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="c5297-130">PublisherID</span><span class="sxs-lookup"><span data-stu-id="c5297-130">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="c5297-131">Mis en file d'attente.</span><span class="sxs-lookup"><span data-stu-id="c5297-131">Queued</span></span>](#queued)
-   [<span data-ttu-id="c5297-132">SubscriberMoniker</span><span class="sxs-lookup"><span data-stu-id="c5297-132">SubscriberMoniker</span></span>](#subscribermoniker)
-   [<span data-ttu-id="c5297-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="c5297-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="c5297-134">UserName</span><span class="sxs-lookup"><span data-stu-id="c5297-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="c5297-135">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-135">Description</span></span>



| <span data-ttu-id="c5297-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-136">Entry</span></span> | <span data-ttu-id="c5297-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="c5297-138">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-138">Description</span></span>    | <span data-ttu-id="c5297-139">Description de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5297-139">A description for the subscription.</span></span> |
| <span data-ttu-id="c5297-140">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-140">Access</span></span>         | <span data-ttu-id="c5297-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-141">ReadWrite</span></span>                           |
| <span data-ttu-id="c5297-142">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-142">Type</span></span>           | <span data-ttu-id="c5297-143">String</span><span class="sxs-lookup"><span data-stu-id="c5297-143">String</span></span>                              |
| <span data-ttu-id="c5297-144">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-144">Default</span></span>        | <span data-ttu-id="c5297-145">""</span><span class="sxs-lookup"><span data-stu-id="c5297-145">""</span></span>                                  |
| <span data-ttu-id="c5297-146">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-146">Minimum system</span></span> | <span data-ttu-id="c5297-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="c5297-148">activé</span><span class="sxs-lookup"><span data-stu-id="c5297-148">Enabled</span></span>



| <span data-ttu-id="c5297-149">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-149">Entry</span></span> | <span data-ttu-id="c5297-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="c5297-151">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-151">Description</span></span>    | <span data-ttu-id="c5297-152">Indique si l’abonnement est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="c5297-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="c5297-153">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-153">Access</span></span>         | <span data-ttu-id="c5297-154">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="c5297-155">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-155">Type</span></span>           | <span data-ttu-id="c5297-156">Bool</span><span class="sxs-lookup"><span data-stu-id="c5297-156">Bool</span></span>                                                     |
| <span data-ttu-id="c5297-157">Default</span><span class="sxs-lookup"><span data-stu-id="c5297-157">Default</span></span>        | <span data-ttu-id="c5297-158">Vrai</span><span class="sxs-lookup"><span data-stu-id="c5297-158">True</span></span>                                                     |
| <span data-ttu-id="c5297-159">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-159">Minimum system</span></span> | <span data-ttu-id="c5297-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="c5297-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="c5297-161">EventClassPartitionID</span></span>



| <span data-ttu-id="c5297-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-162">Entry</span></span> | <span data-ttu-id="c5297-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-164">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-164">Description</span></span>    | <span data-ttu-id="c5297-165">Lors de l’abonnement à une classe d’événements, utilisé pour représenter le GUID de l’ID de partition contenant la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="c5297-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="c5297-166">Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente.</span><span class="sxs-lookup"><span data-stu-id="c5297-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="c5297-167">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-167">Access</span></span>         | <span data-ttu-id="c5297-168">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="c5297-169">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-169">Type</span></span>           | <span data-ttu-id="c5297-170">String</span><span class="sxs-lookup"><span data-stu-id="c5297-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="c5297-171">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-171">Default</span></span>        | <span data-ttu-id="c5297-172">NULL</span><span class="sxs-lookup"><span data-stu-id="c5297-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="c5297-173">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-173">Minimum system</span></span> | <span data-ttu-id="c5297-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5297-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="c5297-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="c5297-175">EventCLSID</span></span>



| <span data-ttu-id="c5297-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-176">Entry</span></span> | <span data-ttu-id="c5297-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-178">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-178">Description</span></span>    | <span data-ttu-id="c5297-179">CLSID de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="c5297-179">The CLSID for the event class.</span></span> <span data-ttu-id="c5297-180">Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="c5297-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="c5297-181">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-181">Access</span></span>         | <span data-ttu-id="c5297-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="c5297-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="c5297-183">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-183">Type</span></span>           | <span data-ttu-id="c5297-184">String</span><span class="sxs-lookup"><span data-stu-id="c5297-184">String</span></span>                                                                                       |
| <span data-ttu-id="c5297-185">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-185">Default</span></span>        | <span data-ttu-id="c5297-186">N/A</span><span class="sxs-lookup"><span data-stu-id="c5297-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="c5297-187">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-187">Minimum system</span></span> | <span data-ttu-id="c5297-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="c5297-189">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="c5297-189">FilterCriteria</span></span>



| <span data-ttu-id="c5297-190">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-190">Entry</span></span> | <span data-ttu-id="c5297-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-191">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-192">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-192">Description</span></span>    | <span data-ttu-id="c5297-193">Chaîne indiquant les critères de filtre.</span><span class="sxs-lookup"><span data-stu-id="c5297-193">A string indicating the filter criteria.</span></span> <span data-ttu-id="c5297-194">Peut être un CLSID pour une classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) .</span><span class="sxs-lookup"><span data-stu-id="c5297-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="c5297-195">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-195">Access</span></span>         | <span data-ttu-id="c5297-196">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-196">ReadWrite</span></span>                                                                                                        |
| <span data-ttu-id="c5297-197">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-197">Type</span></span>           | <span data-ttu-id="c5297-198">String</span><span class="sxs-lookup"><span data-stu-id="c5297-198">String</span></span>                                                                                                           |
| <span data-ttu-id="c5297-199">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-199">Default</span></span>        | <span data-ttu-id="c5297-200">N/A</span><span class="sxs-lookup"><span data-stu-id="c5297-200">N/A</span></span>                                                                                                              |
| <span data-ttu-id="c5297-201">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-201">Minimum system</span></span> | <span data-ttu-id="c5297-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-202">Windows 2000</span></span>                                                                                                     |



 

### <a name="id"></a><span data-ttu-id="c5297-203">id</span><span class="sxs-lookup"><span data-stu-id="c5297-203">ID</span></span>



| <span data-ttu-id="c5297-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-204">Entry</span></span> | <span data-ttu-id="c5297-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-206">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-206">Description</span></span>    | <span data-ttu-id="c5297-207">Identificateur de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5297-207">Identifier for the subscription.</span></span> <span data-ttu-id="c5297-208">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="c5297-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="c5297-209">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-209">Access</span></span>         | <span data-ttu-id="c5297-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="c5297-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="c5297-211">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-211">Type</span></span>           | <span data-ttu-id="c5297-212">String</span><span class="sxs-lookup"><span data-stu-id="c5297-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="c5297-213">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="c5297-214">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-214">Minimum system</span></span> | <span data-ttu-id="c5297-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="c5297-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="c5297-216">InterfaceID</span></span>



| <span data-ttu-id="c5297-217">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-217">Entry</span></span> | <span data-ttu-id="c5297-218">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-218">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="c5297-219">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-219">Description</span></span>    | <span data-ttu-id="c5297-220">IID de l’interface à laquelle s’abonner.</span><span class="sxs-lookup"><span data-stu-id="c5297-220">The IID for the interface subscribed to.</span></span> |
| <span data-ttu-id="c5297-221">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-221">Access</span></span>         | <span data-ttu-id="c5297-222">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-222">ReadWrite</span></span>                                |
| <span data-ttu-id="c5297-223">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-223">Type</span></span>           | <span data-ttu-id="c5297-224">String</span><span class="sxs-lookup"><span data-stu-id="c5297-224">String</span></span>                                   |
| <span data-ttu-id="c5297-225">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-225">Default</span></span>        | <span data-ttu-id="c5297-226">N/A</span><span class="sxs-lookup"><span data-stu-id="c5297-226">N/A</span></span>                                      |
| <span data-ttu-id="c5297-227">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-227">Minimum system</span></span> | <span data-ttu-id="c5297-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-228">Windows 2000</span></span>                             |



 

### <a name="machinename"></a><span data-ttu-id="c5297-229">MachineName</span><span class="sxs-lookup"><span data-stu-id="c5297-229">MachineName</span></span>



| <span data-ttu-id="c5297-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-230">Entry</span></span> | <span data-ttu-id="c5297-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-231">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-232">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-232">Description</span></span>    | <span data-ttu-id="c5297-233">Nom de l’ordinateur distant pour les abonnements aux classes d’événements sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c5297-233">A remote computer name for subscriptions to event classes on a remote computer.</span></span> |
| <span data-ttu-id="c5297-234">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-234">Access</span></span>         | <span data-ttu-id="c5297-235">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-235">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="c5297-236">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-236">Type</span></span>           | <span data-ttu-id="c5297-237">String</span><span class="sxs-lookup"><span data-stu-id="c5297-237">String</span></span>                                                                          |
| <span data-ttu-id="c5297-238">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-238">Default</span></span>        | <span data-ttu-id="c5297-239">""</span><span class="sxs-lookup"><span data-stu-id="c5297-239">""</span></span>                                                                              |
| <span data-ttu-id="c5297-240">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-240">Minimum system</span></span> | <span data-ttu-id="c5297-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-241">Windows 2000</span></span>                                                                    |



 

### <a name="methodname"></a><span data-ttu-id="c5297-242">MethodName</span><span class="sxs-lookup"><span data-stu-id="c5297-242">MethodName</span></span>



| <span data-ttu-id="c5297-243">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-243">Entry</span></span> | <span data-ttu-id="c5297-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-244">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="c5297-245">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-245">Description</span></span>    | <span data-ttu-id="c5297-246">Méthode sur l’interface à laquelle s’abonner.</span><span class="sxs-lookup"><span data-stu-id="c5297-246">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="c5297-247">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-247">Access</span></span>         | <span data-ttu-id="c5297-248">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-248">ReadWrite</span></span>                                    |
| <span data-ttu-id="c5297-249">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-249">Type</span></span>           | <span data-ttu-id="c5297-250">String</span><span class="sxs-lookup"><span data-stu-id="c5297-250">String</span></span>                                       |
| <span data-ttu-id="c5297-251">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-251">Default</span></span>        | <span data-ttu-id="c5297-252">N/A</span><span class="sxs-lookup"><span data-stu-id="c5297-252">N/A</span></span>                                          |
| <span data-ttu-id="c5297-253">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-253">Minimum system</span></span> | <span data-ttu-id="c5297-254">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-254">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="c5297-255">Nom</span><span class="sxs-lookup"><span data-stu-id="c5297-255">Name</span></span>



| <span data-ttu-id="c5297-256">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-256">Entry</span></span> | <span data-ttu-id="c5297-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-257">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-258">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-258">Description</span></span>    | <span data-ttu-id="c5297-259">Nom de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5297-259">Name for the subscription.</span></span> <span data-ttu-id="c5297-260">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="c5297-260">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="c5297-261">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-261">Access</span></span>         | <span data-ttu-id="c5297-262">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-262">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="c5297-263">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-263">Type</span></span>           | <span data-ttu-id="c5297-264">String</span><span class="sxs-lookup"><span data-stu-id="c5297-264">String</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="c5297-265">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-265">Default</span></span>        | <span data-ttu-id="c5297-266">« Nouvel abonnement »</span><span class="sxs-lookup"><span data-stu-id="c5297-266">"New Subscription"</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="c5297-267">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-267">Minimum system</span></span> | <span data-ttu-id="c5297-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-268">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="peruser"></a><span data-ttu-id="c5297-269">PerUser</span><span class="sxs-lookup"><span data-stu-id="c5297-269">PerUser</span></span>



| <span data-ttu-id="c5297-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-270">Entry</span></span> | <span data-ttu-id="c5297-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-271">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="c5297-272">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-272">Description</span></span>    | <span data-ttu-id="c5297-273">Indique si l’abonnement s’applique uniquement à un utilisateur donné, nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5297-273">Indicates whether the subscription applies only for a given user, UserName.</span></span> |
| <span data-ttu-id="c5297-274">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-274">Access</span></span>         | <span data-ttu-id="c5297-275">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-275">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="c5297-276">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-276">Type</span></span>           | <span data-ttu-id="c5297-277">Bool</span><span class="sxs-lookup"><span data-stu-id="c5297-277">Bool</span></span>                                                                        |
| <span data-ttu-id="c5297-278">Default</span><span class="sxs-lookup"><span data-stu-id="c5297-278">Default</span></span>        | <span data-ttu-id="c5297-279">False</span><span class="sxs-lookup"><span data-stu-id="c5297-279">False</span></span>                                                                       |
| <span data-ttu-id="c5297-280">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-280">Minimum system</span></span> | <span data-ttu-id="c5297-281">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-281">Windows 2000</span></span>                                                                |



 

### <a name="publisherid"></a><span data-ttu-id="c5297-282">PublisherID</span><span class="sxs-lookup"><span data-stu-id="c5297-282">PublisherID</span></span>



| <span data-ttu-id="c5297-283">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-283">Entry</span></span> | <span data-ttu-id="c5297-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-284">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-285">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-285">Description</span></span>    | <span data-ttu-id="c5297-286">ID du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="c5297-286">The ID for the publisher.</span></span> <span data-ttu-id="c5297-287">Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="c5297-287">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="c5297-288">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-288">Access</span></span>         | <span data-ttu-id="c5297-289">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="c5297-289">WriteOnce</span></span>                                                                               |
| <span data-ttu-id="c5297-290">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-290">Type</span></span>           | <span data-ttu-id="c5297-291">String</span><span class="sxs-lookup"><span data-stu-id="c5297-291">String</span></span>                                                                                  |
| <span data-ttu-id="c5297-292">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-292">Default</span></span>        | <span data-ttu-id="c5297-293">""</span><span class="sxs-lookup"><span data-stu-id="c5297-293">""</span></span>                                                                                      |
| <span data-ttu-id="c5297-294">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-294">Minimum system</span></span> | <span data-ttu-id="c5297-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-295">Windows 2000</span></span>                                                                            |



 

### <a name="queued"></a><span data-ttu-id="c5297-296">Mis en file d'attente.</span><span class="sxs-lookup"><span data-stu-id="c5297-296">Queued</span></span>



| <span data-ttu-id="c5297-297">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-297">Entry</span></span> | <span data-ttu-id="c5297-298">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-298">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="c5297-299">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-299">Description</span></span>    | <span data-ttu-id="c5297-300">Indique si l’abonnement est mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c5297-300">Indicates whether the subscription is queued.</span></span> |
| <span data-ttu-id="c5297-301">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-301">Access</span></span>         | <span data-ttu-id="c5297-302">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-302">ReadWrite</span></span>                                     |
| <span data-ttu-id="c5297-303">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-303">Type</span></span>           | <span data-ttu-id="c5297-304">Bool</span><span class="sxs-lookup"><span data-stu-id="c5297-304">Bool</span></span>                                          |
| <span data-ttu-id="c5297-305">Default</span><span class="sxs-lookup"><span data-stu-id="c5297-305">Default</span></span>        | <span data-ttu-id="c5297-306">False</span><span class="sxs-lookup"><span data-stu-id="c5297-306">False</span></span>                                         |
| <span data-ttu-id="c5297-307">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-307">Minimum system</span></span> | <span data-ttu-id="c5297-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-308">Windows 2000</span></span>                                  |



 

### <a name="subscribermoniker"></a><span data-ttu-id="c5297-309">SubscriberMoniker</span><span class="sxs-lookup"><span data-stu-id="c5297-309">SubscriberMoniker</span></span>



| <span data-ttu-id="c5297-310">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-310">Entry</span></span> | <span data-ttu-id="c5297-311">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-311">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-312">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-312">Description</span></span>    | <span data-ttu-id="c5297-313">Moniker d’un abonné marqué comme mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c5297-313">A moniker for a subscriber marked as Queued.</span></span> <span data-ttu-id="c5297-314">Une valeur par défaut est générée lorsque Queued est initialement défini sur true.</span><span class="sxs-lookup"><span data-stu-id="c5297-314">A default value is generated when Queued is initially set to True.</span></span> |
| <span data-ttu-id="c5297-315">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-315">Access</span></span>         | <span data-ttu-id="c5297-316">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-316">ReadWrite</span></span>                                                                                                       |
| <span data-ttu-id="c5297-317">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-317">Type</span></span>           | <span data-ttu-id="c5297-318">String</span><span class="sxs-lookup"><span data-stu-id="c5297-318">String</span></span>                                                                                                          |
| <span data-ttu-id="c5297-319">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-319">Default</span></span>        | <span data-ttu-id="c5297-320">N/A</span><span class="sxs-lookup"><span data-stu-id="c5297-320">N/A</span></span>                                                                                                             |
| <span data-ttu-id="c5297-321">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-321">Minimum system</span></span> | <span data-ttu-id="c5297-322">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-322">Windows 2000</span></span>                                                                                                    |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="c5297-323">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="c5297-323">SubscriberPartitionID</span></span>



| <span data-ttu-id="c5297-324">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-324">Entry</span></span> | <span data-ttu-id="c5297-325">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-325">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5297-326">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-326">Description</span></span>    | <span data-ttu-id="c5297-327">Lors de l’abonnement à une classe d’événements dans la même partition, utilisée pour représenter le GUID de l’ID de partition de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="c5297-327">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="c5297-328">Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente.</span><span class="sxs-lookup"><span data-stu-id="c5297-328">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="c5297-329">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-329">Access</span></span>         | <span data-ttu-id="c5297-330">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="c5297-330">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c5297-331">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-331">Type</span></span>           | <span data-ttu-id="c5297-332">String</span><span class="sxs-lookup"><span data-stu-id="c5297-332">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c5297-333">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-333">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="c5297-334">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-334">Minimum system</span></span> | <span data-ttu-id="c5297-335">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5297-335">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="c5297-336">UserName</span><span class="sxs-lookup"><span data-stu-id="c5297-336">UserName</span></span>



| <span data-ttu-id="c5297-337">Entrée</span><span class="sxs-lookup"><span data-stu-id="c5297-337">Entry</span></span> | <span data-ttu-id="c5297-338">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5297-338">Value</span></span> |
|----------------|--------------------------------------------------------------------------|
| <span data-ttu-id="c5297-339">Description</span><span class="sxs-lookup"><span data-stu-id="c5297-339">Description</span></span>    | <span data-ttu-id="c5297-340">Nom de l’utilisateur auquel s’applique l’abonnement, lorsque PerUser a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="c5297-340">The name of user that the subscription applies to, when PerUser is True.</span></span> |
| <span data-ttu-id="c5297-341">Accès</span><span class="sxs-lookup"><span data-stu-id="c5297-341">Access</span></span>         | <span data-ttu-id="c5297-342">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c5297-342">ReadWrite</span></span>                                                                |
| <span data-ttu-id="c5297-343">Type</span><span class="sxs-lookup"><span data-stu-id="c5297-343">Type</span></span>           | <span data-ttu-id="c5297-344">String</span><span class="sxs-lookup"><span data-stu-id="c5297-344">String</span></span>                                                                   |
| <span data-ttu-id="c5297-345">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c5297-345">Default</span></span>        | <span data-ttu-id="c5297-346">N/A</span><span class="sxs-lookup"><span data-stu-id="c5297-346">N/A</span></span>                                                                      |
| <span data-ttu-id="c5297-347">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c5297-347">Minimum system</span></span> | <span data-ttu-id="c5297-348">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c5297-348">Windows 2000</span></span>                                                             |



 

## <a name="see-also"></a><span data-ttu-id="c5297-349">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5297-349">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5297-350">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="c5297-350">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
