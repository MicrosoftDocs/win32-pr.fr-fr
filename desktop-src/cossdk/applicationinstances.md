---
description: Récupère des informations sur les applications en cours d’exécution.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Collection ApplicationInstances
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483161"
---
# <a name="applicationinstances-collection"></a><span data-ttu-id="18568-103">Collection ApplicationInstances</span><span class="sxs-lookup"><span data-stu-id="18568-103">ApplicationInstances collection</span></span>

<span data-ttu-id="18568-104">Récupère des informations sur les applications en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="18568-104">Retrieves information regarding running applications.</span></span>

<span data-ttu-id="18568-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="18568-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="18568-106">Membres</span><span class="sxs-lookup"><span data-stu-id="18568-106">Members</span></span>

<span data-ttu-id="18568-107">La collection **ApplicationInstances** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="18568-107">The **ApplicationInstances** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="18568-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="18568-108">Related Collections</span></span>

<span data-ttu-id="18568-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="18568-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="18568-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="18568-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="18568-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="18568-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="18568-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="18568-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="18568-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="18568-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="18568-114">**Applications**</span><span class="sxs-lookup"><span data-stu-id="18568-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="18568-115">**Causes**</span><span class="sxs-lookup"><span data-stu-id="18568-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="18568-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18568-116">Properties</span></span>

<span data-ttu-id="18568-117">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="18568-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="18568-118">Application</span><span class="sxs-lookup"><span data-stu-id="18568-118">Application</span></span>](#applicationinstances-collection)
-   [<span data-ttu-id="18568-119">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="18568-119">HasRecycled</span></span>](#hasrecycled)
-   [<span data-ttu-id="18568-120">InstanceID</span><span class="sxs-lookup"><span data-stu-id="18568-120">InstanceID</span></span>](#instanceid)
-   [<span data-ttu-id="18568-121">IsPaused</span><span class="sxs-lookup"><span data-stu-id="18568-121">IsPaused</span></span>](#ispaused)
-   [<span data-ttu-id="18568-122">PartitionID</span><span class="sxs-lookup"><span data-stu-id="18568-122">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="18568-123">ProcessID</span><span class="sxs-lookup"><span data-stu-id="18568-123">ProcessID</span></span>](#processid)

### <a name="application"></a><span data-ttu-id="18568-124">Application</span><span class="sxs-lookup"><span data-stu-id="18568-124">Application</span></span>



| <span data-ttu-id="18568-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="18568-125">Entry</span></span> | <span data-ttu-id="18568-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="18568-126">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="18568-127">Description</span><span class="sxs-lookup"><span data-stu-id="18568-127">Description</span></span>    | <span data-ttu-id="18568-128">ID de l’application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="18568-128">The ID for the running application.</span></span> |
| <span data-ttu-id="18568-129">Accès</span><span class="sxs-lookup"><span data-stu-id="18568-129">Access</span></span>         | <span data-ttu-id="18568-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18568-130">ReadOnly</span></span>                            |
| <span data-ttu-id="18568-131">Type</span><span class="sxs-lookup"><span data-stu-id="18568-131">Type</span></span>           | <span data-ttu-id="18568-132">String</span><span class="sxs-lookup"><span data-stu-id="18568-132">String</span></span>                              |
| <span data-ttu-id="18568-133">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="18568-133">Default</span></span>        | <span data-ttu-id="18568-134">N/A</span><span class="sxs-lookup"><span data-stu-id="18568-134">N/A</span></span>                                 |
| <span data-ttu-id="18568-135">Système minimal</span><span class="sxs-lookup"><span data-stu-id="18568-135">Minimum system</span></span> | <span data-ttu-id="18568-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18568-136">Windows XP</span></span>                          |



 

### <a name="hasrecycled"></a><span data-ttu-id="18568-137">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="18568-137">HasRecycled</span></span>



| <span data-ttu-id="18568-138">Entrée</span><span class="sxs-lookup"><span data-stu-id="18568-138">Entry</span></span> | <span data-ttu-id="18568-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="18568-139">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="18568-140">Description</span><span class="sxs-lookup"><span data-stu-id="18568-140">Description</span></span>    | <span data-ttu-id="18568-141">Indique si l’instance d’application a été recyclée.</span><span class="sxs-lookup"><span data-stu-id="18568-141">Indicates whether the application instance has been recycled.</span></span> |
| <span data-ttu-id="18568-142">Accès</span><span class="sxs-lookup"><span data-stu-id="18568-142">Access</span></span>         | <span data-ttu-id="18568-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18568-143">ReadOnly</span></span>                                                      |
| <span data-ttu-id="18568-144">Type</span><span class="sxs-lookup"><span data-stu-id="18568-144">Type</span></span>           | <span data-ttu-id="18568-145">Bool</span><span class="sxs-lookup"><span data-stu-id="18568-145">Bool</span></span>                                                          |
| <span data-ttu-id="18568-146">Default</span><span class="sxs-lookup"><span data-stu-id="18568-146">Default</span></span>        | <span data-ttu-id="18568-147">False</span><span class="sxs-lookup"><span data-stu-id="18568-147">False</span></span>                                                         |
| <span data-ttu-id="18568-148">Système minimal</span><span class="sxs-lookup"><span data-stu-id="18568-148">Minimum system</span></span> | <span data-ttu-id="18568-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18568-149">Windows XP</span></span>                                                    |



 

### <a name="instanceid"></a><span data-ttu-id="18568-150">InstanceID</span><span class="sxs-lookup"><span data-stu-id="18568-150">InstanceID</span></span>



| <span data-ttu-id="18568-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="18568-151">Entry</span></span> | <span data-ttu-id="18568-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="18568-152">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18568-153">Description</span><span class="sxs-lookup"><span data-stu-id="18568-153">Description</span></span>    | <span data-ttu-id="18568-154">Identificateur global unique de l’instance de l’application.</span><span class="sxs-lookup"><span data-stu-id="18568-154">The globally unique identifier for the application instance.</span></span> <span data-ttu-id="18568-155">Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="18568-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="18568-156">Accès</span><span class="sxs-lookup"><span data-stu-id="18568-156">Access</span></span>         | <span data-ttu-id="18568-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18568-157">ReadOnly</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="18568-158">Type</span><span class="sxs-lookup"><span data-stu-id="18568-158">Type</span></span>           | <span data-ttu-id="18568-159">String</span><span class="sxs-lookup"><span data-stu-id="18568-159">String</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="18568-160">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="18568-160">Default</span></span>        | <span data-ttu-id="18568-161">N/A</span><span class="sxs-lookup"><span data-stu-id="18568-161">N/A</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="18568-162">Système minimal</span><span class="sxs-lookup"><span data-stu-id="18568-162">Minimum system</span></span> | <span data-ttu-id="18568-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18568-163">Windows XP</span></span>                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a><span data-ttu-id="18568-164">IsPaused</span><span class="sxs-lookup"><span data-stu-id="18568-164">IsPaused</span></span>



| <span data-ttu-id="18568-165">Entrée</span><span class="sxs-lookup"><span data-stu-id="18568-165">Entry</span></span> | <span data-ttu-id="18568-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="18568-166">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="18568-167">Description</span><span class="sxs-lookup"><span data-stu-id="18568-167">Description</span></span>    | <span data-ttu-id="18568-168">Indique si l’instance d’application est actuellement suspendue.</span><span class="sxs-lookup"><span data-stu-id="18568-168">Indicates whether the application instance is currently paused.</span></span> |
| <span data-ttu-id="18568-169">Accès</span><span class="sxs-lookup"><span data-stu-id="18568-169">Access</span></span>         | <span data-ttu-id="18568-170">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18568-170">ReadOnly</span></span>                                                        |
| <span data-ttu-id="18568-171">Type</span><span class="sxs-lookup"><span data-stu-id="18568-171">Type</span></span>           | <span data-ttu-id="18568-172">Bool</span><span class="sxs-lookup"><span data-stu-id="18568-172">Bool</span></span>                                                            |
| <span data-ttu-id="18568-173">Default</span><span class="sxs-lookup"><span data-stu-id="18568-173">Default</span></span>        | <span data-ttu-id="18568-174">False</span><span class="sxs-lookup"><span data-stu-id="18568-174">False</span></span>                                                           |
| <span data-ttu-id="18568-175">Système minimal</span><span class="sxs-lookup"><span data-stu-id="18568-175">Minimum system</span></span> | <span data-ttu-id="18568-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18568-176">Windows XP</span></span>                                                      |



 

### <a name="partitionid"></a><span data-ttu-id="18568-177">PartitionID</span><span class="sxs-lookup"><span data-stu-id="18568-177">PartitionID</span></span>



| <span data-ttu-id="18568-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="18568-178">Entry</span></span> | <span data-ttu-id="18568-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="18568-179">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="18568-180">Description</span><span class="sxs-lookup"><span data-stu-id="18568-180">Description</span></span>    | <span data-ttu-id="18568-181">ID de partition que l’application utilise.</span><span class="sxs-lookup"><span data-stu-id="18568-181">The partition ID that the application is using.</span></span> |
| <span data-ttu-id="18568-182">Accès</span><span class="sxs-lookup"><span data-stu-id="18568-182">Access</span></span>         | <span data-ttu-id="18568-183">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18568-183">ReadOnly</span></span>                                        |
| <span data-ttu-id="18568-184">Type</span><span class="sxs-lookup"><span data-stu-id="18568-184">Type</span></span>           | <span data-ttu-id="18568-185">String</span><span class="sxs-lookup"><span data-stu-id="18568-185">String</span></span>                                          |
| <span data-ttu-id="18568-186">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="18568-186">Default</span></span>        | <span data-ttu-id="18568-187">N/A</span><span class="sxs-lookup"><span data-stu-id="18568-187">N/A</span></span>                                             |
| <span data-ttu-id="18568-188">Système minimal</span><span class="sxs-lookup"><span data-stu-id="18568-188">Minimum system</span></span> | <span data-ttu-id="18568-189">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18568-189">Windows XP</span></span>                                      |



 

### <a name="processid"></a><span data-ttu-id="18568-190">ProcessID</span><span class="sxs-lookup"><span data-stu-id="18568-190">ProcessID</span></span>



| <span data-ttu-id="18568-191">Entrée</span><span class="sxs-lookup"><span data-stu-id="18568-191">Entry</span></span> | <span data-ttu-id="18568-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="18568-192">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="18568-193">Description</span><span class="sxs-lookup"><span data-stu-id="18568-193">Description</span></span>    | <span data-ttu-id="18568-194">ID de processus de l’instance de l’application.</span><span class="sxs-lookup"><span data-stu-id="18568-194">The process ID of the application instance.</span></span> |
| <span data-ttu-id="18568-195">Accès</span><span class="sxs-lookup"><span data-stu-id="18568-195">Access</span></span>         | <span data-ttu-id="18568-196">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18568-196">ReadOnly</span></span>                                    |
| <span data-ttu-id="18568-197">Type</span><span class="sxs-lookup"><span data-stu-id="18568-197">Type</span></span>           | <span data-ttu-id="18568-198">String</span><span class="sxs-lookup"><span data-stu-id="18568-198">String</span></span>                                      |
| <span data-ttu-id="18568-199">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="18568-199">Default</span></span>        | <span data-ttu-id="18568-200">N/A</span><span class="sxs-lookup"><span data-stu-id="18568-200">N/A</span></span>                                         |
| <span data-ttu-id="18568-201">Système minimal</span><span class="sxs-lookup"><span data-stu-id="18568-201">Minimum system</span></span> | <span data-ttu-id="18568-202">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18568-202">Windows XP</span></span>                                  |



 

## <a name="see-also"></a><span data-ttu-id="18568-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18568-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18568-204">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="18568-204">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
