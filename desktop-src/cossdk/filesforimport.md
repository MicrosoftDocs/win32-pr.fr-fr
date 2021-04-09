---
description: Récupère des informations pour les applications qui sont importées.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Collection FilesForImport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111027"
---
# <a name="filesforimport-collection"></a><span data-ttu-id="ccbaf-103">Collection FilesForImport</span><span class="sxs-lookup"><span data-stu-id="ccbaf-103">FilesForImport collection</span></span>

<span data-ttu-id="ccbaf-104">Récupère des informations pour les applications qui sont importées.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-104">Retrieves information for applications that are imported.</span></span>

<span data-ttu-id="ccbaf-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ccbaf-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ccbaf-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ccbaf-106">Members</span></span>

<span data-ttu-id="ccbaf-107">La collection **FilesForImport** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-107">The **FilesForImport** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ccbaf-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="ccbaf-108">Related Collections</span></span>

<span data-ttu-id="ccbaf-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="ccbaf-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ccbaf-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ccbaf-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ccbaf-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ccbaf-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ccbaf-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ccbaf-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ccbaf-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="ccbaf-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ccbaf-114">**Causes**</span><span class="sxs-lookup"><span data-stu-id="ccbaf-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="ccbaf-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ccbaf-115">Properties</span></span>

<span data-ttu-id="ccbaf-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="ccbaf-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ccbaf-117">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-117">ApplicationFileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="ccbaf-118">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-118">ApplicationName</span></span>](#applicationname)
-   [<span data-ttu-id="ccbaf-119">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-119">Description</span></span>](#partitiondescription)
-   [<span data-ttu-id="ccbaf-120">FileName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-120">FileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="ccbaf-121">HasUsers</span><span class="sxs-lookup"><span data-stu-id="ccbaf-121">HasUsers</span></span>](#hasusers)
-   [<span data-ttu-id="ccbaf-122">Proxy</span><span class="sxs-lookup"><span data-stu-id="ccbaf-122">IsProxy</span></span>](#isproxy)
-   [<span data-ttu-id="ccbaf-123">IsService</span><span class="sxs-lookup"><span data-stu-id="ccbaf-123">IsService</span></span>](#isservice)
-   [<span data-ttu-id="ccbaf-124">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="ccbaf-124">PartitionDescription</span></span>](#partitiondescription)
-   [<span data-ttu-id="ccbaf-125">PartitionID</span><span class="sxs-lookup"><span data-stu-id="ccbaf-125">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="ccbaf-126">PartitionName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-126">PartitionName</span></span>](#partitionname)

### <a name="applicationfilename"></a><span data-ttu-id="ccbaf-127">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-127">ApplicationFileName</span></span>



| <span data-ttu-id="ccbaf-128">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-128">Entry</span></span> | <span data-ttu-id="ccbaf-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ccbaf-130">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-130">Description</span></span>    | <span data-ttu-id="ccbaf-131">Nom du fichier MSI qui contient l’application qui peut être importée.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-131">The name of the MSI file that contains the application that can be imported.</span></span> |
| <span data-ttu-id="ccbaf-132">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-132">Access</span></span>         | <span data-ttu-id="ccbaf-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-133">ReadOnly</span></span>                                                                     |
| <span data-ttu-id="ccbaf-134">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-134">Type</span></span>           | <span data-ttu-id="ccbaf-135">String</span><span class="sxs-lookup"><span data-stu-id="ccbaf-135">String</span></span>                                                                       |
| <span data-ttu-id="ccbaf-136">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ccbaf-136">Default</span></span>        | <span data-ttu-id="ccbaf-137">N/A</span><span class="sxs-lookup"><span data-stu-id="ccbaf-137">N/A</span></span>                                                                          |
| <span data-ttu-id="ccbaf-138">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-138">Minimum system</span></span> | <span data-ttu-id="ccbaf-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccbaf-139">Windows XP</span></span>                                                                   |



 

### <a name="applicationname"></a><span data-ttu-id="ccbaf-140">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-140">ApplicationName</span></span>



| <span data-ttu-id="ccbaf-141">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-141">Entry</span></span> | <span data-ttu-id="ccbaf-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-142">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="ccbaf-143">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-143">Description</span></span>    | <span data-ttu-id="ccbaf-144">Le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-144">The name of the application.</span></span> |
| <span data-ttu-id="ccbaf-145">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-145">Access</span></span>         | <span data-ttu-id="ccbaf-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-146">ReadOnly</span></span>                     |
| <span data-ttu-id="ccbaf-147">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-147">Type</span></span>           | <span data-ttu-id="ccbaf-148">String</span><span class="sxs-lookup"><span data-stu-id="ccbaf-148">String</span></span>                       |
| <span data-ttu-id="ccbaf-149">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ccbaf-149">Default</span></span>        | <span data-ttu-id="ccbaf-150">""</span><span class="sxs-lookup"><span data-stu-id="ccbaf-150">""</span></span>                           |
| <span data-ttu-id="ccbaf-151">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-151">Minimum system</span></span> | <span data-ttu-id="ccbaf-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccbaf-152">Windows XP</span></span>                   |



 

### <a name="description"></a><span data-ttu-id="ccbaf-153">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-153">Description</span></span>



| <span data-ttu-id="ccbaf-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-154">Entry</span></span> | <span data-ttu-id="ccbaf-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-155">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="ccbaf-156">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-156">Description</span></span>    | <span data-ttu-id="ccbaf-157">Description de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-157">A description of the application.</span></span> |
| <span data-ttu-id="ccbaf-158">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-158">Access</span></span>         | <span data-ttu-id="ccbaf-159">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-159">ReadOnly</span></span>                          |
| <span data-ttu-id="ccbaf-160">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-160">Type</span></span>           | <span data-ttu-id="ccbaf-161">String</span><span class="sxs-lookup"><span data-stu-id="ccbaf-161">String</span></span>                            |
| <span data-ttu-id="ccbaf-162">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ccbaf-162">Default</span></span>        | <span data-ttu-id="ccbaf-163">""</span><span class="sxs-lookup"><span data-stu-id="ccbaf-163">""</span></span>                                |
| <span data-ttu-id="ccbaf-164">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-164">Minimum system</span></span> | <span data-ttu-id="ccbaf-165">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccbaf-165">Windows XP</span></span>                        |



 

### <a name="filename"></a><span data-ttu-id="ccbaf-166">FileName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-166">FileName</span></span>



| <span data-ttu-id="ccbaf-167">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-167">Entry</span></span> | <span data-ttu-id="ccbaf-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-168">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccbaf-169">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-169">Description</span></span>    | <span data-ttu-id="ccbaf-170">Nom de la DLL ou du fichier EXE qui contient l’application.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-170">The name of the DLL or EXE file that contains the application.</span></span> <span data-ttu-id="ccbaf-171">Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-171">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ccbaf-172">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-172">Access</span></span>         | <span data-ttu-id="ccbaf-173">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-173">ReadOnly</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="ccbaf-174">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-174">Type</span></span>           | <span data-ttu-id="ccbaf-175">String</span><span class="sxs-lookup"><span data-stu-id="ccbaf-175">String</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="ccbaf-176">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ccbaf-176">Default</span></span>        | <span data-ttu-id="ccbaf-177">""</span><span class="sxs-lookup"><span data-stu-id="ccbaf-177">""</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="ccbaf-178">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-178">Minimum system</span></span> | <span data-ttu-id="ccbaf-179">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccbaf-179">Windows XP</span></span>                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a><span data-ttu-id="ccbaf-180">HasUsers</span><span class="sxs-lookup"><span data-stu-id="ccbaf-180">HasUsers</span></span>



| <span data-ttu-id="ccbaf-181">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-181">Entry</span></span> | <span data-ttu-id="ccbaf-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-182">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="ccbaf-183">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-183">Description</span></span>    | <span data-ttu-id="ccbaf-184">Indique si l’application possède des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-184">Indicates whether the application has any users.</span></span> |
| <span data-ttu-id="ccbaf-185">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-185">Access</span></span>         | <span data-ttu-id="ccbaf-186">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-186">ReadOnly</span></span>                                         |
| <span data-ttu-id="ccbaf-187">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-187">Type</span></span>           | <span data-ttu-id="ccbaf-188">Bool</span><span class="sxs-lookup"><span data-stu-id="ccbaf-188">Bool</span></span>                                             |
| <span data-ttu-id="ccbaf-189">Default</span><span class="sxs-lookup"><span data-stu-id="ccbaf-189">Default</span></span>        | <span data-ttu-id="ccbaf-190">False</span><span class="sxs-lookup"><span data-stu-id="ccbaf-190">False</span></span>                                            |
| <span data-ttu-id="ccbaf-191">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-191">Minimum system</span></span> | <span data-ttu-id="ccbaf-192">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccbaf-192">Windows XP</span></span>                                       |



 

### <a name="isproxy"></a><span data-ttu-id="ccbaf-193">Proxy</span><span class="sxs-lookup"><span data-stu-id="ccbaf-193">IsProxy</span></span>



| <span data-ttu-id="ccbaf-194">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-194">Entry</span></span> | <span data-ttu-id="ccbaf-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-195">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="ccbaf-196">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-196">Description</span></span>    | <span data-ttu-id="ccbaf-197">Indique si l’application est un proxy.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-197">Indicates whether the application is a proxy.</span></span> |
| <span data-ttu-id="ccbaf-198">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-198">Access</span></span>         | <span data-ttu-id="ccbaf-199">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-199">ReadOnly</span></span>                                      |
| <span data-ttu-id="ccbaf-200">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-200">Type</span></span>           | <span data-ttu-id="ccbaf-201">Bool</span><span class="sxs-lookup"><span data-stu-id="ccbaf-201">Bool</span></span>                                          |
| <span data-ttu-id="ccbaf-202">Default</span><span class="sxs-lookup"><span data-stu-id="ccbaf-202">Default</span></span>        | <span data-ttu-id="ccbaf-203">False</span><span class="sxs-lookup"><span data-stu-id="ccbaf-203">False</span></span>                                         |
| <span data-ttu-id="ccbaf-204">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-204">Minimum system</span></span> | <span data-ttu-id="ccbaf-205">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccbaf-205">Windows XP</span></span>                                    |



 

### <a name="isservice"></a><span data-ttu-id="ccbaf-206">IsService</span><span class="sxs-lookup"><span data-stu-id="ccbaf-206">IsService</span></span>



| <span data-ttu-id="ccbaf-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-207">Entry</span></span> | <span data-ttu-id="ccbaf-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-208">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="ccbaf-209">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-209">Description</span></span>    | <span data-ttu-id="ccbaf-210">Indique si l’application est un service.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-210">Indicates whether the application is a service.</span></span> |
| <span data-ttu-id="ccbaf-211">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-211">Access</span></span>         | <span data-ttu-id="ccbaf-212">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-212">ReadOnly</span></span>                                        |
| <span data-ttu-id="ccbaf-213">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-213">Type</span></span>           | <span data-ttu-id="ccbaf-214">Bool</span><span class="sxs-lookup"><span data-stu-id="ccbaf-214">Bool</span></span>                                            |
| <span data-ttu-id="ccbaf-215">Default</span><span class="sxs-lookup"><span data-stu-id="ccbaf-215">Default</span></span>        | <span data-ttu-id="ccbaf-216">False</span><span class="sxs-lookup"><span data-stu-id="ccbaf-216">False</span></span>                                           |
| <span data-ttu-id="ccbaf-217">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-217">Minimum system</span></span> | <span data-ttu-id="ccbaf-218">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccbaf-218">Windows XP</span></span>                                      |



 

### <a name="partitiondescription"></a><span data-ttu-id="ccbaf-219">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="ccbaf-219">PartitionDescription</span></span>



| <span data-ttu-id="ccbaf-220">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-220">Entry</span></span> | <span data-ttu-id="ccbaf-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-221">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="ccbaf-222">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-222">Description</span></span>    | <span data-ttu-id="ccbaf-223">Description de la partition de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-223">A description of the application's partition.</span></span> |
| <span data-ttu-id="ccbaf-224">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-224">Access</span></span>         | <span data-ttu-id="ccbaf-225">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-225">ReadOnly</span></span>                                      |
| <span data-ttu-id="ccbaf-226">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-226">Type</span></span>           | <span data-ttu-id="ccbaf-227">String</span><span class="sxs-lookup"><span data-stu-id="ccbaf-227">String</span></span>                                        |
| <span data-ttu-id="ccbaf-228">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ccbaf-228">Default</span></span>        | <span data-ttu-id="ccbaf-229">""</span><span class="sxs-lookup"><span data-stu-id="ccbaf-229">""</span></span>                                            |
| <span data-ttu-id="ccbaf-230">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-230">Minimum system</span></span> | <span data-ttu-id="ccbaf-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ccbaf-231">Windows Server 2003</span></span>                           |



 

### <a name="partitionid"></a><span data-ttu-id="ccbaf-232">PartitionID</span><span class="sxs-lookup"><span data-stu-id="ccbaf-232">PartitionID</span></span>



| <span data-ttu-id="ccbaf-233">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-233">Entry</span></span> | <span data-ttu-id="ccbaf-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-234">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="ccbaf-235">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-235">Description</span></span>    | <span data-ttu-id="ccbaf-236">GUID de la partition de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-236">The GUID of the application's partition.</span></span> |
| <span data-ttu-id="ccbaf-237">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-237">Access</span></span>         | <span data-ttu-id="ccbaf-238">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-238">ReadOnly</span></span>                                 |
| <span data-ttu-id="ccbaf-239">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-239">Type</span></span>           | <span data-ttu-id="ccbaf-240">String</span><span class="sxs-lookup"><span data-stu-id="ccbaf-240">String</span></span>                                   |
| <span data-ttu-id="ccbaf-241">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ccbaf-241">Default</span></span>        | <span data-ttu-id="ccbaf-242">""</span><span class="sxs-lookup"><span data-stu-id="ccbaf-242">""</span></span>                                       |
| <span data-ttu-id="ccbaf-243">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-243">Minimum system</span></span> | <span data-ttu-id="ccbaf-244">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ccbaf-244">Windows Server 2003</span></span>                      |



 

### <a name="partitionname"></a><span data-ttu-id="ccbaf-245">PartitionName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-245">PartitionName</span></span>



| <span data-ttu-id="ccbaf-246">Entrée</span><span class="sxs-lookup"><span data-stu-id="ccbaf-246">Entry</span></span> | <span data-ttu-id="ccbaf-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbaf-247">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="ccbaf-248">Description</span><span class="sxs-lookup"><span data-stu-id="ccbaf-248">Description</span></span>    | <span data-ttu-id="ccbaf-249">Nom de la partition de l’application.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-249">The name of the application's partition.</span></span> |
| <span data-ttu-id="ccbaf-250">Accès</span><span class="sxs-lookup"><span data-stu-id="ccbaf-250">Access</span></span>         | <span data-ttu-id="ccbaf-251">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccbaf-251">ReadOnly</span></span>                                 |
| <span data-ttu-id="ccbaf-252">Type</span><span class="sxs-lookup"><span data-stu-id="ccbaf-252">Type</span></span>           | <span data-ttu-id="ccbaf-253">String</span><span class="sxs-lookup"><span data-stu-id="ccbaf-253">String</span></span>                                   |
| <span data-ttu-id="ccbaf-254">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ccbaf-254">Default</span></span>        | <span data-ttu-id="ccbaf-255">""</span><span class="sxs-lookup"><span data-stu-id="ccbaf-255">""</span></span>                                       |
| <span data-ttu-id="ccbaf-256">Système minimal</span><span class="sxs-lookup"><span data-stu-id="ccbaf-256">Minimum system</span></span> | <span data-ttu-id="ccbaf-257">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ccbaf-257">Windows Server 2003</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="ccbaf-258">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccbaf-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccbaf-259">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="ccbaf-259">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
