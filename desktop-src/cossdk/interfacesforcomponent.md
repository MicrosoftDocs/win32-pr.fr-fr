---
description: Contient un objet pour chaque interface exposée par le composant auquel la collection est associée.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Collection InterfacesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110910"
---
# <a name="interfacesforcomponent-collection"></a><span data-ttu-id="72ff8-103">Collection InterfacesForComponent</span><span class="sxs-lookup"><span data-stu-id="72ff8-103">InterfacesForComponent collection</span></span>

<span data-ttu-id="72ff8-104">Contient un objet pour chaque interface exposée par le composant auquel la collection est associée.</span><span class="sxs-lookup"><span data-stu-id="72ff8-104">Contains an object for each interface exposed by the component to which the collection is related.</span></span>

<span data-ttu-id="72ff8-105">Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="72ff8-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="72ff8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="72ff8-106">Members</span></span>

<span data-ttu-id="72ff8-107">La collection **InterfacesForComponent** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="72ff8-107">The **InterfacesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="72ff8-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="72ff8-108">Related Collections</span></span>

<span data-ttu-id="72ff8-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="72ff8-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="72ff8-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="72ff8-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="72ff8-111">**MethodsForInterface**</span><span class="sxs-lookup"><span data-stu-id="72ff8-111">**MethodsForInterface**</span></span>](methodsforinterface.md)
-   [<span data-ttu-id="72ff8-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="72ff8-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="72ff8-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="72ff8-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="72ff8-114">**RolesForInterface**</span><span class="sxs-lookup"><span data-stu-id="72ff8-114">**RolesForInterface**</span></span>](rolesforinterface.md)

<span data-ttu-id="72ff8-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="72ff8-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="72ff8-116">**Composants**</span><span class="sxs-lookup"><span data-stu-id="72ff8-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="72ff8-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72ff8-117">Properties</span></span>

<span data-ttu-id="72ff8-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="72ff8-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="72ff8-119">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="72ff8-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="72ff8-120">Description</span><span class="sxs-lookup"><span data-stu-id="72ff8-120">Description</span></span>](#description)
-   [<span data-ttu-id="72ff8-121">IID</span><span class="sxs-lookup"><span data-stu-id="72ff8-121">IID</span></span>](#iid)
-   [<span data-ttu-id="72ff8-122">Nom</span><span class="sxs-lookup"><span data-stu-id="72ff8-122">Name</span></span>](#name)
-   [<span data-ttu-id="72ff8-123">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="72ff8-123">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="72ff8-124">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="72ff8-124">QueueingSupported</span></span>](#queueingsupported)

### <a name="clsid"></a><span data-ttu-id="72ff8-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="72ff8-125">CLSID</span></span>



| <span data-ttu-id="72ff8-126">Entrée</span><span class="sxs-lookup"><span data-stu-id="72ff8-126">Entry</span></span> | <span data-ttu-id="72ff8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ff8-127">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="72ff8-128">Description</span><span class="sxs-lookup"><span data-stu-id="72ff8-128">Description</span></span>    | <span data-ttu-id="72ff8-129">GUID du composant.</span><span class="sxs-lookup"><span data-stu-id="72ff8-129">A GUID for the component.</span></span> |
| <span data-ttu-id="72ff8-130">Accès</span><span class="sxs-lookup"><span data-stu-id="72ff8-130">Access</span></span>         | <span data-ttu-id="72ff8-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72ff8-131">ReadOnly</span></span>                  |
| <span data-ttu-id="72ff8-132">Type</span><span class="sxs-lookup"><span data-stu-id="72ff8-132">Type</span></span>           | <span data-ttu-id="72ff8-133">String</span><span class="sxs-lookup"><span data-stu-id="72ff8-133">String</span></span>                    |
| <span data-ttu-id="72ff8-134">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="72ff8-134">Default</span></span>        | <span data-ttu-id="72ff8-135">N/A</span><span class="sxs-lookup"><span data-stu-id="72ff8-135">N/A</span></span>                       |
| <span data-ttu-id="72ff8-136">Système minimal</span><span class="sxs-lookup"><span data-stu-id="72ff8-136">Minimum system</span></span> | <span data-ttu-id="72ff8-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="72ff8-137">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="72ff8-138">Description</span><span class="sxs-lookup"><span data-stu-id="72ff8-138">Description</span></span>



| <span data-ttu-id="72ff8-139">Entrée</span><span class="sxs-lookup"><span data-stu-id="72ff8-139">Entry</span></span> | <span data-ttu-id="72ff8-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ff8-140">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="72ff8-141">Description</span><span class="sxs-lookup"><span data-stu-id="72ff8-141">Description</span></span>    | <span data-ttu-id="72ff8-142">Description de l’interface.</span><span class="sxs-lookup"><span data-stu-id="72ff8-142">A description for the interface.</span></span> |
| <span data-ttu-id="72ff8-143">Accès</span><span class="sxs-lookup"><span data-stu-id="72ff8-143">Access</span></span>         | <span data-ttu-id="72ff8-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72ff8-144">ReadWrite</span></span>                        |
| <span data-ttu-id="72ff8-145">Type</span><span class="sxs-lookup"><span data-stu-id="72ff8-145">Type</span></span>           | <span data-ttu-id="72ff8-146">String</span><span class="sxs-lookup"><span data-stu-id="72ff8-146">String</span></span>                           |
| <span data-ttu-id="72ff8-147">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="72ff8-147">Default</span></span>        | <span data-ttu-id="72ff8-148">""</span><span class="sxs-lookup"><span data-stu-id="72ff8-148">""</span></span>                               |
| <span data-ttu-id="72ff8-149">Système minimal</span><span class="sxs-lookup"><span data-stu-id="72ff8-149">Minimum system</span></span> | <span data-ttu-id="72ff8-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="72ff8-150">Windows 2000</span></span>                     |



 

### <a name="iid"></a><span data-ttu-id="72ff8-151">IID</span><span class="sxs-lookup"><span data-stu-id="72ff8-151">IID</span></span>



| <span data-ttu-id="72ff8-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="72ff8-152">Entry</span></span> | <span data-ttu-id="72ff8-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ff8-153">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ff8-154">Description</span><span class="sxs-lookup"><span data-stu-id="72ff8-154">Description</span></span>    | <span data-ttu-id="72ff8-155">GUID de l’interface.</span><span class="sxs-lookup"><span data-stu-id="72ff8-155">A GUID for the interface.</span></span> <span data-ttu-id="72ff8-156">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="72ff8-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="72ff8-157">Accès</span><span class="sxs-lookup"><span data-stu-id="72ff8-157">Access</span></span>         | <span data-ttu-id="72ff8-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72ff8-158">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="72ff8-159">Type</span><span class="sxs-lookup"><span data-stu-id="72ff8-159">Type</span></span>           | <span data-ttu-id="72ff8-160">String</span><span class="sxs-lookup"><span data-stu-id="72ff8-160">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="72ff8-161">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="72ff8-161">Default</span></span>        | <span data-ttu-id="72ff8-162">N/A</span><span class="sxs-lookup"><span data-stu-id="72ff8-162">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="72ff8-163">Système minimal</span><span class="sxs-lookup"><span data-stu-id="72ff8-163">Minimum system</span></span> | <span data-ttu-id="72ff8-164">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="72ff8-164">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="name"></a><span data-ttu-id="72ff8-165">Nom</span><span class="sxs-lookup"><span data-stu-id="72ff8-165">Name</span></span>



| <span data-ttu-id="72ff8-166">Entrée</span><span class="sxs-lookup"><span data-stu-id="72ff8-166">Entry</span></span> | <span data-ttu-id="72ff8-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ff8-167">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ff8-168">Description</span><span class="sxs-lookup"><span data-stu-id="72ff8-168">Description</span></span>    | <span data-ttu-id="72ff8-169">Nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="72ff8-169">A name for the interface.</span></span> <span data-ttu-id="72ff8-170">Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="72ff8-170">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="72ff8-171">Accès</span><span class="sxs-lookup"><span data-stu-id="72ff8-171">Access</span></span>         | <span data-ttu-id="72ff8-172">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72ff8-172">ReadOnly</span></span>                                                                                                                                                    |
| <span data-ttu-id="72ff8-173">Type</span><span class="sxs-lookup"><span data-stu-id="72ff8-173">Type</span></span>           | <span data-ttu-id="72ff8-174">String</span><span class="sxs-lookup"><span data-stu-id="72ff8-174">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="72ff8-175">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="72ff8-175">Default</span></span>        | <span data-ttu-id="72ff8-176">N/A</span><span class="sxs-lookup"><span data-stu-id="72ff8-176">N/A</span></span>                                                                                                                                                         |
| <span data-ttu-id="72ff8-177">Système minimal</span><span class="sxs-lookup"><span data-stu-id="72ff8-177">Minimum system</span></span> | <span data-ttu-id="72ff8-178">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="72ff8-178">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="queuingenabled"></a><span data-ttu-id="72ff8-179">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="72ff8-179">QueuingEnabled</span></span>



| <span data-ttu-id="72ff8-180">Entrée</span><span class="sxs-lookup"><span data-stu-id="72ff8-180">Entry</span></span> | <span data-ttu-id="72ff8-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ff8-181">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ff8-182">Description</span><span class="sxs-lookup"><span data-stu-id="72ff8-182">Description</span></span>    | <span data-ttu-id="72ff8-183">Marque l’interface comme étant en file d’attente et peut être définie à l’aide du kit de développement logiciel (SDK) administrateur ou de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="72ff8-183">Marks the interface as queuable and can be set by using the Admin SDK or Component Services administrative tool.</span></span> <span data-ttu-id="72ff8-184">Toutefois, seule une interface dont l’indicateur de mise **en file d’attente est pris en charge** peut définir l’indicateur de mise en **file d’attente activé** .</span><span class="sxs-lookup"><span data-stu-id="72ff8-184">However, only an interface that has the **Queuing Supported** flag set can have the **Queuing Enabled** flag set.</span></span> |
| <span data-ttu-id="72ff8-185">Accès</span><span class="sxs-lookup"><span data-stu-id="72ff8-185">Access</span></span>         | <span data-ttu-id="72ff8-186">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72ff8-186">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="72ff8-187">Type</span><span class="sxs-lookup"><span data-stu-id="72ff8-187">Type</span></span>           | <span data-ttu-id="72ff8-188">Bool</span><span class="sxs-lookup"><span data-stu-id="72ff8-188">Bool</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="72ff8-189">Default</span><span class="sxs-lookup"><span data-stu-id="72ff8-189">Default</span></span>        | <span data-ttu-id="72ff8-190">False</span><span class="sxs-lookup"><span data-stu-id="72ff8-190">False</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="72ff8-191">Système minimal</span><span class="sxs-lookup"><span data-stu-id="72ff8-191">Minimum system</span></span> | <span data-ttu-id="72ff8-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="72ff8-192">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a><span data-ttu-id="72ff8-193">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="72ff8-193">QueueingSupported</span></span>



| <span data-ttu-id="72ff8-194">Entrée</span><span class="sxs-lookup"><span data-stu-id="72ff8-194">Entry</span></span> | <span data-ttu-id="72ff8-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ff8-195">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ff8-196">Description</span><span class="sxs-lookup"><span data-stu-id="72ff8-196">Description</span></span>    | <span data-ttu-id="72ff8-197">L’interface prend en charge la mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="72ff8-197">Interface supports queuing.</span></span> <span data-ttu-id="72ff8-198">Pour qu’une interface prenne en charge la mise en file d’attente, toutes les méthodes doivent avoir uniquement des paramètres in.</span><span class="sxs-lookup"><span data-stu-id="72ff8-198">For an interface to support queuing, all methods should have only in parameters.</span></span> <span data-ttu-id="72ff8-199">La mise **en file d’attente** est exposée en tant que propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="72ff8-199">**Queuing Supported** is exposed as a read-only property.</span></span> |
| <span data-ttu-id="72ff8-200">Accès</span><span class="sxs-lookup"><span data-stu-id="72ff8-200">Access</span></span>         | <span data-ttu-id="72ff8-201">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72ff8-201">ReadOnly</span></span>                                                                                                                                                               |
| <span data-ttu-id="72ff8-202">Type</span><span class="sxs-lookup"><span data-stu-id="72ff8-202">Type</span></span>           | <span data-ttu-id="72ff8-203">Bool</span><span class="sxs-lookup"><span data-stu-id="72ff8-203">Bool</span></span>                                                                                                                                                                   |
| <span data-ttu-id="72ff8-204">Default</span><span class="sxs-lookup"><span data-stu-id="72ff8-204">Default</span></span>        | <span data-ttu-id="72ff8-205">False</span><span class="sxs-lookup"><span data-stu-id="72ff8-205">False</span></span>                                                                                                                                                                  |
| <span data-ttu-id="72ff8-206">Système minimal</span><span class="sxs-lookup"><span data-stu-id="72ff8-206">Minimum system</span></span> | <span data-ttu-id="72ff8-207">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="72ff8-207">Windows 2000</span></span>                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="72ff8-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72ff8-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ff8-209">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="72ff8-209">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
