---
description: Spécifie les applications contenues dans chaque partition.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Collection partitions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749077"
---
# <a name="partitions-collection"></a><span data-ttu-id="08536-103">Collection partitions</span><span class="sxs-lookup"><span data-stu-id="08536-103">Partitions collection</span></span>

<span data-ttu-id="08536-104">Spécifie les applications contenues dans chaque partition.</span><span class="sxs-lookup"><span data-stu-id="08536-104">Specifies the applications contained within each partition.</span></span>

<span data-ttu-id="08536-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="08536-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="08536-106">Membres</span><span class="sxs-lookup"><span data-stu-id="08536-106">Members</span></span>

<span data-ttu-id="08536-107">La collection **partitions** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="08536-107">The **Partitions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="08536-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="08536-108">Related Collections</span></span>

<span data-ttu-id="08536-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="08536-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="08536-110">**Applications**</span><span class="sxs-lookup"><span data-stu-id="08536-110">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="08536-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="08536-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="08536-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="08536-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="08536-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="08536-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="08536-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="08536-114">**RolesForPartition**</span></span>](rolesforpartition.md)

<span data-ttu-id="08536-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="08536-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="08536-116">**Causes**</span><span class="sxs-lookup"><span data-stu-id="08536-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="08536-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08536-117">Properties</span></span>

<span data-ttu-id="08536-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="08536-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="08536-119">Modifiables</span><span class="sxs-lookup"><span data-stu-id="08536-119">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="08536-120">Supprimé</span><span class="sxs-lookup"><span data-stu-id="08536-120">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="08536-121">Description</span><span class="sxs-lookup"><span data-stu-id="08536-121">Description</span></span>](#description)
-   [<span data-ttu-id="08536-122">Identifiant</span><span class="sxs-lookup"><span data-stu-id="08536-122">ID</span></span>](#partitions-collection)
-   [<span data-ttu-id="08536-123">Nom</span><span class="sxs-lookup"><span data-stu-id="08536-123">Name</span></span>](#name)

### <a name="changeable"></a><span data-ttu-id="08536-124">Modifiables</span><span class="sxs-lookup"><span data-stu-id="08536-124">Changeable</span></span>



| <span data-ttu-id="08536-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="08536-125">Entry</span></span> | <span data-ttu-id="08536-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="08536-126">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="08536-127">Description</span><span class="sxs-lookup"><span data-stu-id="08536-127">Description</span></span>    | <span data-ttu-id="08536-128">Détermine si cette partition peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="08536-128">Determines whether this partition is changeable.</span></span> |
| <span data-ttu-id="08536-129">Accès</span><span class="sxs-lookup"><span data-stu-id="08536-129">Access</span></span>         | <span data-ttu-id="08536-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08536-130">ReadWrite</span></span>                                        |
| <span data-ttu-id="08536-131">Type</span><span class="sxs-lookup"><span data-stu-id="08536-131">Type</span></span>           | <span data-ttu-id="08536-132">Bool</span><span class="sxs-lookup"><span data-stu-id="08536-132">Bool</span></span>                                             |
| <span data-ttu-id="08536-133">Default</span><span class="sxs-lookup"><span data-stu-id="08536-133">Default</span></span>        | <span data-ttu-id="08536-134">Vrai</span><span class="sxs-lookup"><span data-stu-id="08536-134">True</span></span>                                             |
| <span data-ttu-id="08536-135">Système minimal</span><span class="sxs-lookup"><span data-stu-id="08536-135">Minimum system</span></span> | <span data-ttu-id="08536-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08536-136">Windows Server 2003</span></span>                              |



 

### <a name="deleteable"></a><span data-ttu-id="08536-137">Supprimé</span><span class="sxs-lookup"><span data-stu-id="08536-137">Deleteable</span></span>



| <span data-ttu-id="08536-138">Entrée</span><span class="sxs-lookup"><span data-stu-id="08536-138">Entry</span></span> | <span data-ttu-id="08536-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="08536-139">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="08536-140">Description</span><span class="sxs-lookup"><span data-stu-id="08536-140">Description</span></span>    | <span data-ttu-id="08536-141">Détermine si cette partition peut être supprimée.</span><span class="sxs-lookup"><span data-stu-id="08536-141">Determines whether this partition can be deleted.</span></span> |
| <span data-ttu-id="08536-142">Accès</span><span class="sxs-lookup"><span data-stu-id="08536-142">Access</span></span>         | <span data-ttu-id="08536-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08536-143">ReadWrite</span></span>                                         |
| <span data-ttu-id="08536-144">Type</span><span class="sxs-lookup"><span data-stu-id="08536-144">Type</span></span>           | <span data-ttu-id="08536-145">Bool</span><span class="sxs-lookup"><span data-stu-id="08536-145">Bool</span></span>                                              |
| <span data-ttu-id="08536-146">Default</span><span class="sxs-lookup"><span data-stu-id="08536-146">Default</span></span>        | <span data-ttu-id="08536-147">Vrai</span><span class="sxs-lookup"><span data-stu-id="08536-147">True</span></span>                                              |
| <span data-ttu-id="08536-148">Système minimal</span><span class="sxs-lookup"><span data-stu-id="08536-148">Minimum system</span></span> | <span data-ttu-id="08536-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08536-149">Windows Server 2003</span></span>                               |



 

### <a name="description"></a><span data-ttu-id="08536-150">Description</span><span class="sxs-lookup"><span data-stu-id="08536-150">Description</span></span>



| <span data-ttu-id="08536-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="08536-151">Entry</span></span> | <span data-ttu-id="08536-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="08536-152">Value</span></span> |
|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="08536-153">Description</span><span class="sxs-lookup"><span data-stu-id="08536-153">Description</span></span>    | <span data-ttu-id="08536-154">Cette propriété représente la description identifiant la partition.</span><span class="sxs-lookup"><span data-stu-id="08536-154">This property represents the description identifying the partition.</span></span> |
| <span data-ttu-id="08536-155">Accès</span><span class="sxs-lookup"><span data-stu-id="08536-155">Access</span></span>         | <span data-ttu-id="08536-156">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08536-156">ReadWrite</span></span>                                                           |
| <span data-ttu-id="08536-157">Type</span><span class="sxs-lookup"><span data-stu-id="08536-157">Type</span></span>           | <span data-ttu-id="08536-158">String</span><span class="sxs-lookup"><span data-stu-id="08536-158">String</span></span>                                                              |
| <span data-ttu-id="08536-159">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="08536-159">Default</span></span>        | <span data-ttu-id="08536-160">""</span><span class="sxs-lookup"><span data-stu-id="08536-160">""</span></span>                                                                  |
| <span data-ttu-id="08536-161">Système minimal</span><span class="sxs-lookup"><span data-stu-id="08536-161">Minimum system</span></span> | <span data-ttu-id="08536-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08536-162">Windows Server 2003</span></span>                                                 |



 

### <a name="id"></a><span data-ttu-id="08536-163">id</span><span class="sxs-lookup"><span data-stu-id="08536-163">ID</span></span>



| <span data-ttu-id="08536-164">Entrée</span><span class="sxs-lookup"><span data-stu-id="08536-164">Entry</span></span> | <span data-ttu-id="08536-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="08536-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08536-166">Description</span><span class="sxs-lookup"><span data-stu-id="08536-166">Description</span></span>    | <span data-ttu-id="08536-167">GUID représentant la partition.</span><span class="sxs-lookup"><span data-stu-id="08536-167">A GUID representing the partition.</span></span> <span data-ttu-id="08536-168">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="08536-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="08536-169">Accès</span><span class="sxs-lookup"><span data-stu-id="08536-169">Access</span></span>         | <span data-ttu-id="08536-170">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="08536-170">WriteOnce</span></span>                                                                                                                                                          |
| <span data-ttu-id="08536-171">Type</span><span class="sxs-lookup"><span data-stu-id="08536-171">Type</span></span>           | <span data-ttu-id="08536-172">String</span><span class="sxs-lookup"><span data-stu-id="08536-172">String</span></span>                                                                                                                                                             |
| <span data-ttu-id="08536-173">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="08536-173">Default</span></span>        | <Generated>                                                                                                                                                  |
| <span data-ttu-id="08536-174">Système minimal</span><span class="sxs-lookup"><span data-stu-id="08536-174">Minimum system</span></span> | <span data-ttu-id="08536-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08536-175">Windows Server 2003</span></span>                                                                                                                                                |



 

### <a name="name"></a><span data-ttu-id="08536-176">Nom</span><span class="sxs-lookup"><span data-stu-id="08536-176">Name</span></span>



| <span data-ttu-id="08536-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="08536-177">Entry</span></span> | <span data-ttu-id="08536-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="08536-178">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08536-179">Description</span><span class="sxs-lookup"><span data-stu-id="08536-179">Description</span></span>    | <span data-ttu-id="08536-180">Représente le nom de la partition.</span><span class="sxs-lookup"><span data-stu-id="08536-180">Represents the partition name.</span></span> <span data-ttu-id="08536-181">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="08536-181">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="08536-182">Accès</span><span class="sxs-lookup"><span data-stu-id="08536-182">Access</span></span>         | <span data-ttu-id="08536-183">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08536-183">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="08536-184">Type</span><span class="sxs-lookup"><span data-stu-id="08536-184">Type</span></span>           | <span data-ttu-id="08536-185">String</span><span class="sxs-lookup"><span data-stu-id="08536-185">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="08536-186">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="08536-186">Default</span></span>        | <span data-ttu-id="08536-187">« Nouvelle partition »</span><span class="sxs-lookup"><span data-stu-id="08536-187">"New Partition"</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="08536-188">Système minimal</span><span class="sxs-lookup"><span data-stu-id="08536-188">Minimum system</span></span> | <span data-ttu-id="08536-189">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08536-189">Windows Server 2003</span></span>                                                                                                                                                                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="08536-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08536-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08536-191">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="08536-191">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
