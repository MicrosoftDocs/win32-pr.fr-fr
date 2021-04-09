---
description: Contient un objet pour chaque abonnement temporaire. Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Collection TransientSubscriptions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861285"
---
# <a name="transientsubscriptions-collection"></a><span data-ttu-id="e87ec-104">Collection TransientSubscriptions</span><span class="sxs-lookup"><span data-stu-id="e87ec-104">TransientSubscriptions collection</span></span>

<span data-ttu-id="e87ec-105">Contient un objet pour chaque abonnement temporaire.</span><span class="sxs-lookup"><span data-stu-id="e87ec-105">Contains an object for each transient subscription.</span></span> <span data-ttu-id="e87ec-106">Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.</span><span class="sxs-lookup"><span data-stu-id="e87ec-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="e87ec-107">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="e87ec-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="e87ec-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e87ec-108">Members</span></span>

<span data-ttu-id="e87ec-109">La collection **TransientSubscriptions** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e87ec-109">The **TransientSubscriptions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="e87ec-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="e87ec-110">Related Collections</span></span>

<span data-ttu-id="e87ec-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="e87ec-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="e87ec-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e87ec-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="e87ec-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="e87ec-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="e87ec-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e87ec-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="e87ec-115">**TransientPublisherProperties**</span><span class="sxs-lookup"><span data-stu-id="e87ec-115">**TransientPublisherProperties**</span></span>](transientpublisherproperties.md)
-   [<span data-ttu-id="e87ec-116">**TransientSubscriberProperties**</span><span class="sxs-lookup"><span data-stu-id="e87ec-116">**TransientSubscriberProperties**</span></span>](transientsubscriberproperties.md)

<span data-ttu-id="e87ec-117">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="e87ec-117">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="e87ec-118">**Causes**</span><span class="sxs-lookup"><span data-stu-id="e87ec-118">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="e87ec-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e87ec-119">Properties</span></span>

<span data-ttu-id="e87ec-120">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="e87ec-120">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="e87ec-121">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-121">Description</span></span>](#description)
-   [<span data-ttu-id="e87ec-122">Enabled</span><span class="sxs-lookup"><span data-stu-id="e87ec-122">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="e87ec-123">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="e87ec-123">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="e87ec-124">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="e87ec-124">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="e87ec-125">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="e87ec-125">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="e87ec-126">Identifiant</span><span class="sxs-lookup"><span data-stu-id="e87ec-126">ID</span></span>](#transientsubscriptions-collection)
-   [<span data-ttu-id="e87ec-127">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="e87ec-127">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="e87ec-128">MethodName</span><span class="sxs-lookup"><span data-stu-id="e87ec-128">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="e87ec-129">Nom</span><span class="sxs-lookup"><span data-stu-id="e87ec-129">Name</span></span>](#methodname)
-   [<span data-ttu-id="e87ec-130">PerUser</span><span class="sxs-lookup"><span data-stu-id="e87ec-130">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="e87ec-131">PublisherID</span><span class="sxs-lookup"><span data-stu-id="e87ec-131">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="e87ec-132">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="e87ec-132">SubscriberInterface</span></span>](#subscriberinterface)
-   [<span data-ttu-id="e87ec-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="e87ec-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="e87ec-134">UserName</span><span class="sxs-lookup"><span data-stu-id="e87ec-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="e87ec-135">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-135">Description</span></span>



| <span data-ttu-id="e87ec-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-136">Entry</span></span> | <span data-ttu-id="e87ec-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="e87ec-138">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-138">Description</span></span>    | <span data-ttu-id="e87ec-139">Description de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="e87ec-139">A description for the subscription.</span></span> |
| <span data-ttu-id="e87ec-140">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-140">Access</span></span>         | <span data-ttu-id="e87ec-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-141">ReadWrite</span></span>                           |
| <span data-ttu-id="e87ec-142">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-142">Type</span></span>           | <span data-ttu-id="e87ec-143">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-143">String</span></span>                              |
| <span data-ttu-id="e87ec-144">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-144">Default</span></span>        | <span data-ttu-id="e87ec-145">""</span><span class="sxs-lookup"><span data-stu-id="e87ec-145">""</span></span>                                  |
| <span data-ttu-id="e87ec-146">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-146">Minimum system</span></span> | <span data-ttu-id="e87ec-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="e87ec-148">activé</span><span class="sxs-lookup"><span data-stu-id="e87ec-148">Enabled</span></span>



| <span data-ttu-id="e87ec-149">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-149">Entry</span></span> | <span data-ttu-id="e87ec-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="e87ec-151">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-151">Description</span></span>    | <span data-ttu-id="e87ec-152">Indique si l’abonnement est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="e87ec-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="e87ec-153">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-153">Access</span></span>         | <span data-ttu-id="e87ec-154">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="e87ec-155">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-155">Type</span></span>           | <span data-ttu-id="e87ec-156">Bool</span><span class="sxs-lookup"><span data-stu-id="e87ec-156">Bool</span></span>                                                     |
| <span data-ttu-id="e87ec-157">Default</span><span class="sxs-lookup"><span data-stu-id="e87ec-157">Default</span></span>        | <span data-ttu-id="e87ec-158">Vrai</span><span class="sxs-lookup"><span data-stu-id="e87ec-158">True</span></span>                                                     |
| <span data-ttu-id="e87ec-159">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-159">Minimum system</span></span> | <span data-ttu-id="e87ec-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="e87ec-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="e87ec-161">EventClassPartitionID</span></span>



| <span data-ttu-id="e87ec-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-162">Entry</span></span> | <span data-ttu-id="e87ec-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-164">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-164">Description</span></span>    | <span data-ttu-id="e87ec-165">Lors de l’abonnement à une classe d’événements, utilisé pour représenter le GUID de l’ID de partition contenant la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="e87ec-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="e87ec-166">Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente.</span><span class="sxs-lookup"><span data-stu-id="e87ec-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="e87ec-167">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-167">Access</span></span>         | <span data-ttu-id="e87ec-168">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="e87ec-169">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-169">Type</span></span>           | <span data-ttu-id="e87ec-170">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="e87ec-171">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-171">Default</span></span>        | <span data-ttu-id="e87ec-172">NULL</span><span class="sxs-lookup"><span data-stu-id="e87ec-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="e87ec-173">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-173">Minimum system</span></span> | <span data-ttu-id="e87ec-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e87ec-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="e87ec-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="e87ec-175">EventCLSID</span></span>



| <span data-ttu-id="e87ec-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-176">Entry</span></span> | <span data-ttu-id="e87ec-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-178">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-178">Description</span></span>    | <span data-ttu-id="e87ec-179">CLSID de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="e87ec-179">The CLSID for the event class.</span></span> <span data-ttu-id="e87ec-180">Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="e87ec-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="e87ec-181">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-181">Access</span></span>         | <span data-ttu-id="e87ec-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e87ec-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="e87ec-183">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-183">Type</span></span>           | <span data-ttu-id="e87ec-184">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-184">String</span></span>                                                                                       |
| <span data-ttu-id="e87ec-185">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-185">Default</span></span>        | <span data-ttu-id="e87ec-186">N/A</span><span class="sxs-lookup"><span data-stu-id="e87ec-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="e87ec-187">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-187">Minimum system</span></span> | <span data-ttu-id="e87ec-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="e87ec-189">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="e87ec-189">FilterCriteria</span></span>



| <span data-ttu-id="e87ec-190">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-190">Entry</span></span> | <span data-ttu-id="e87ec-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-191">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-192">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-192">Description</span></span>    | <span data-ttu-id="e87ec-193">Chaîne qui indique les critères de filtre.</span><span class="sxs-lookup"><span data-stu-id="e87ec-193">A string that indicates the filter criteria.</span></span> <span data-ttu-id="e87ec-194">Peut être un CLSID pour une classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) .</span><span class="sxs-lookup"><span data-stu-id="e87ec-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="e87ec-195">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-195">Access</span></span>         | <span data-ttu-id="e87ec-196">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-196">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="e87ec-197">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-197">Type</span></span>           | <span data-ttu-id="e87ec-198">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-198">String</span></span>                                                                                                               |
| <span data-ttu-id="e87ec-199">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-199">Default</span></span>        | <span data-ttu-id="e87ec-200">N/A</span><span class="sxs-lookup"><span data-stu-id="e87ec-200">N/A</span></span>                                                                                                                  |
| <span data-ttu-id="e87ec-201">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-201">Minimum system</span></span> | <span data-ttu-id="e87ec-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-202">Windows 2000</span></span>                                                                                                         |



 

### <a name="id"></a><span data-ttu-id="e87ec-203">id</span><span class="sxs-lookup"><span data-stu-id="e87ec-203">ID</span></span>



| <span data-ttu-id="e87ec-204">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-204">Entry</span></span> | <span data-ttu-id="e87ec-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-206">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-206">Description</span></span>    | <span data-ttu-id="e87ec-207">Identificateur de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="e87ec-207">Identifier for the subscription.</span></span> <span data-ttu-id="e87ec-208">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="e87ec-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e87ec-209">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-209">Access</span></span>         | <span data-ttu-id="e87ec-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e87ec-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="e87ec-211">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-211">Type</span></span>           | <span data-ttu-id="e87ec-212">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="e87ec-213">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="e87ec-214">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-214">Minimum system</span></span> | <span data-ttu-id="e87ec-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="e87ec-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="e87ec-216">InterfaceID</span></span>



| <span data-ttu-id="e87ec-217">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-217">Entry</span></span> | <span data-ttu-id="e87ec-218">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-218">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="e87ec-219">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-219">Description</span></span>    | <span data-ttu-id="e87ec-220">IID pour lequel l’interface est abonnée.</span><span class="sxs-lookup"><span data-stu-id="e87ec-220">IID for interface subscribed to.</span></span> |
| <span data-ttu-id="e87ec-221">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-221">Access</span></span>         | <span data-ttu-id="e87ec-222">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e87ec-222">WriteOnce</span></span>                        |
| <span data-ttu-id="e87ec-223">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-223">Type</span></span>           | <span data-ttu-id="e87ec-224">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-224">String</span></span>                           |
| <span data-ttu-id="e87ec-225">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-225">Default</span></span>        | <span data-ttu-id="e87ec-226">N/A</span><span class="sxs-lookup"><span data-stu-id="e87ec-226">N/A</span></span>                              |
| <span data-ttu-id="e87ec-227">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-227">Minimum system</span></span> | <span data-ttu-id="e87ec-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-228">Windows 2000</span></span>                     |



 

### <a name="methodname"></a><span data-ttu-id="e87ec-229">MethodName</span><span class="sxs-lookup"><span data-stu-id="e87ec-229">MethodName</span></span>



| <span data-ttu-id="e87ec-230">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-230">Entry</span></span> | <span data-ttu-id="e87ec-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-231">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="e87ec-232">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-232">Description</span></span>    | <span data-ttu-id="e87ec-233">Méthode sur l’interface à laquelle s’abonner.</span><span class="sxs-lookup"><span data-stu-id="e87ec-233">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="e87ec-234">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-234">Access</span></span>         | <span data-ttu-id="e87ec-235">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-235">ReadWrite</span></span>                                    |
| <span data-ttu-id="e87ec-236">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-236">Type</span></span>           | <span data-ttu-id="e87ec-237">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-237">String</span></span>                                       |
| <span data-ttu-id="e87ec-238">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-238">Default</span></span>        | <span data-ttu-id="e87ec-239">N/A</span><span class="sxs-lookup"><span data-stu-id="e87ec-239">N/A</span></span>                                          |
| <span data-ttu-id="e87ec-240">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-240">Minimum system</span></span> | <span data-ttu-id="e87ec-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-241">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="e87ec-242">Nom</span><span class="sxs-lookup"><span data-stu-id="e87ec-242">Name</span></span>



| <span data-ttu-id="e87ec-243">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-243">Entry</span></span> | <span data-ttu-id="e87ec-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-244">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-245">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-245">Description</span></span>    | <span data-ttu-id="e87ec-246">Nom de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="e87ec-246">The name for the subscription.</span></span> <span data-ttu-id="e87ec-247">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="e87ec-247">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e87ec-248">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-248">Access</span></span>         | <span data-ttu-id="e87ec-249">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-249">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="e87ec-250">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-250">Type</span></span>           | <span data-ttu-id="e87ec-251">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-251">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="e87ec-252">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-252">Default</span></span>        | <span data-ttu-id="e87ec-253">« Nouvel abonnement »</span><span class="sxs-lookup"><span data-stu-id="e87ec-253">"New Subscription"</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="e87ec-254">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-254">Minimum system</span></span> | <span data-ttu-id="e87ec-255">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-255">Windows 2000</span></span>                                                                                                                                                                                                                           |



 

### <a name="peruser"></a><span data-ttu-id="e87ec-256">PerUser</span><span class="sxs-lookup"><span data-stu-id="e87ec-256">PerUser</span></span>



| <span data-ttu-id="e87ec-257">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-257">Entry</span></span> | <span data-ttu-id="e87ec-258">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-258">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-259">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-259">Description</span></span>    | <span data-ttu-id="e87ec-260">Indique si l’abonnement s’applique uniquement à un utilisateur donné, représenté par la propriété UserName.</span><span class="sxs-lookup"><span data-stu-id="e87ec-260">Indicates whether the subscription applies only for a given user, represented by the UserName property.</span></span> |
| <span data-ttu-id="e87ec-261">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-261">Access</span></span>         | <span data-ttu-id="e87ec-262">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-262">ReadWrite</span></span>                                                                                               |
| <span data-ttu-id="e87ec-263">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-263">Type</span></span>           | <span data-ttu-id="e87ec-264">Bool</span><span class="sxs-lookup"><span data-stu-id="e87ec-264">Bool</span></span>                                                                                                    |
| <span data-ttu-id="e87ec-265">Default</span><span class="sxs-lookup"><span data-stu-id="e87ec-265">Default</span></span>        | <span data-ttu-id="e87ec-266">False</span><span class="sxs-lookup"><span data-stu-id="e87ec-266">False</span></span>                                                                                                   |
| <span data-ttu-id="e87ec-267">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-267">Minimum system</span></span> | <span data-ttu-id="e87ec-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-268">Windows 2000</span></span>                                                                                            |



 

### <a name="publisherid"></a><span data-ttu-id="e87ec-269">PublisherID</span><span class="sxs-lookup"><span data-stu-id="e87ec-269">PublisherID</span></span>



| <span data-ttu-id="e87ec-270">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-270">Entry</span></span> | <span data-ttu-id="e87ec-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-271">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-272">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-272">Description</span></span>    | <span data-ttu-id="e87ec-273">ID du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="e87ec-273">ID for the publisher.</span></span> <span data-ttu-id="e87ec-274">Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="e87ec-274">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="e87ec-275">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-275">Access</span></span>         | <span data-ttu-id="e87ec-276">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e87ec-276">WriteOnce</span></span>                                                                           |
| <span data-ttu-id="e87ec-277">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-277">Type</span></span>           | <span data-ttu-id="e87ec-278">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-278">String</span></span>                                                                              |
| <span data-ttu-id="e87ec-279">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-279">Default</span></span>        | <span data-ttu-id="e87ec-280">""</span><span class="sxs-lookup"><span data-stu-id="e87ec-280">""</span></span>                                                                                  |
| <span data-ttu-id="e87ec-281">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-281">Minimum system</span></span> | <span data-ttu-id="e87ec-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-282">Windows 2000</span></span>                                                                        |



 

### <a name="subscriberinterface"></a><span data-ttu-id="e87ec-283">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="e87ec-283">SubscriberInterface</span></span>



| <span data-ttu-id="e87ec-284">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-284">Entry</span></span> | <span data-ttu-id="e87ec-285">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-285">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="e87ec-286">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-286">Description</span></span>    | <span data-ttu-id="e87ec-287">Pointeur vers l’interface de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="e87ec-287">A pointer to the subscriber's interface.</span></span> |
| <span data-ttu-id="e87ec-288">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-288">Access</span></span>         | <span data-ttu-id="e87ec-289">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-289">ReadWrite</span></span>                                |
| <span data-ttu-id="e87ec-290">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-290">Type</span></span>           | <span data-ttu-id="e87ec-291">Variante</span><span class="sxs-lookup"><span data-stu-id="e87ec-291">Variant</span></span>                                  |
| <span data-ttu-id="e87ec-292">Default</span><span class="sxs-lookup"><span data-stu-id="e87ec-292">Default</span></span>        | <span data-ttu-id="e87ec-293">N/A</span><span class="sxs-lookup"><span data-stu-id="e87ec-293">N/A</span></span>                                      |
| <span data-ttu-id="e87ec-294">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-294">Minimum system</span></span> | <span data-ttu-id="e87ec-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-295">Windows 2000</span></span>                             |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="e87ec-296">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="e87ec-296">SubscriberPartitionID</span></span>



| <span data-ttu-id="e87ec-297">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-297">Entry</span></span> | <span data-ttu-id="e87ec-298">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-298">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-299">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-299">Description</span></span>    | <span data-ttu-id="e87ec-300">Lors de l’abonnement à une classe d’événements dans la même partition, utilisée pour représenter le GUID de l’ID de partition de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="e87ec-300">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="e87ec-301">Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente.</span><span class="sxs-lookup"><span data-stu-id="e87ec-301">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="e87ec-302">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-302">Access</span></span>         | <span data-ttu-id="e87ec-303">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e87ec-303">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e87ec-304">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-304">Type</span></span>           | <span data-ttu-id="e87ec-305">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-305">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="e87ec-306">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-306">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="e87ec-307">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-307">Minimum system</span></span> | <span data-ttu-id="e87ec-308">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e87ec-308">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="e87ec-309">UserName</span><span class="sxs-lookup"><span data-stu-id="e87ec-309">UserName</span></span>



| <span data-ttu-id="e87ec-310">Entrée</span><span class="sxs-lookup"><span data-stu-id="e87ec-310">Entry</span></span> | <span data-ttu-id="e87ec-311">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87ec-311">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e87ec-312">Description</span><span class="sxs-lookup"><span data-stu-id="e87ec-312">Description</span></span>    | <span data-ttu-id="e87ec-313">Nom de l’utilisateur auquel s’applique l’abonnement lorsque PerUser a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="e87ec-313">The name of user that the subscription applies to when PerUser is True.</span></span> |
| <span data-ttu-id="e87ec-314">Accès</span><span class="sxs-lookup"><span data-stu-id="e87ec-314">Access</span></span>         | <span data-ttu-id="e87ec-315">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e87ec-315">ReadWrite</span></span>                                                               |
| <span data-ttu-id="e87ec-316">Type</span><span class="sxs-lookup"><span data-stu-id="e87ec-316">Type</span></span>           | <span data-ttu-id="e87ec-317">String</span><span class="sxs-lookup"><span data-stu-id="e87ec-317">String</span></span>                                                                  |
| <span data-ttu-id="e87ec-318">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e87ec-318">Default</span></span>        | <span data-ttu-id="e87ec-319">N/A</span><span class="sxs-lookup"><span data-stu-id="e87ec-319">N/A</span></span>                                                                     |
| <span data-ttu-id="e87ec-320">Système minimal</span><span class="sxs-lookup"><span data-stu-id="e87ec-320">Minimum system</span></span> | <span data-ttu-id="e87ec-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e87ec-321">Windows 2000</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="e87ec-322">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e87ec-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e87ec-323">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="e87ec-323">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
