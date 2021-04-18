---
description: Identique à la collection InprocServers, à ceci près que cette collection comprend également des serveurs locaux.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Collection LegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536311"
---
# <a name="legacyservers-collection"></a><span data-ttu-id="44b19-103">Collection LegacyServers</span><span class="sxs-lookup"><span data-stu-id="44b19-103">LegacyServers collection</span></span>

<span data-ttu-id="44b19-104">Identique à la collection [**InprocServers**](inprocservers.md) , à ceci près que cette collection comprend également des serveurs locaux.</span><span class="sxs-lookup"><span data-stu-id="44b19-104">Identical to the [**InprocServers**](inprocservers.md) collection except that this collection also includes local servers.</span></span>

<span data-ttu-id="44b19-105">Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="44b19-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="44b19-106">Membres</span><span class="sxs-lookup"><span data-stu-id="44b19-106">Members</span></span>

<span data-ttu-id="44b19-107">La collection **LegacyServers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="44b19-107">The **LegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="44b19-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="44b19-108">Related Collections</span></span>

<span data-ttu-id="44b19-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="44b19-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="44b19-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44b19-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="44b19-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="44b19-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="44b19-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="44b19-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="44b19-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="44b19-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="44b19-114">**Causes**</span><span class="sxs-lookup"><span data-stu-id="44b19-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="44b19-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="44b19-115">Properties</span></span>

<span data-ttu-id="44b19-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="44b19-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="44b19-117">NomClasse</span><span class="sxs-lookup"><span data-stu-id="44b19-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="44b19-118">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="44b19-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="44b19-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="44b19-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="44b19-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="44b19-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="44b19-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="44b19-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="44b19-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="44b19-122">ClassName</span></span>



| <span data-ttu-id="44b19-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="44b19-123">Entry</span></span> | <span data-ttu-id="44b19-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="44b19-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="44b19-125">Description</span><span class="sxs-lookup"><span data-stu-id="44b19-125">Description</span></span>    | <span data-ttu-id="44b19-126">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="44b19-126">The name of the class.</span></span> |
| <span data-ttu-id="44b19-127">Accès</span><span class="sxs-lookup"><span data-stu-id="44b19-127">Access</span></span>         | <span data-ttu-id="44b19-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44b19-128">ReadOnly</span></span>               |
| <span data-ttu-id="44b19-129">Type</span><span class="sxs-lookup"><span data-stu-id="44b19-129">Type</span></span>           | <span data-ttu-id="44b19-130">String</span><span class="sxs-lookup"><span data-stu-id="44b19-130">String</span></span>                 |
| <span data-ttu-id="44b19-131">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="44b19-131">Default</span></span>        | <span data-ttu-id="44b19-132">N/A</span><span class="sxs-lookup"><span data-stu-id="44b19-132">N/A</span></span>                    |
| <span data-ttu-id="44b19-133">Système minimal</span><span class="sxs-lookup"><span data-stu-id="44b19-133">Minimum system</span></span> | <span data-ttu-id="44b19-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="44b19-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="44b19-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="44b19-135">CLSID</span></span>



| <span data-ttu-id="44b19-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="44b19-136">Entry</span></span> | <span data-ttu-id="44b19-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="44b19-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b19-138">Description</span><span class="sxs-lookup"><span data-stu-id="44b19-138">Description</span></span>    | <span data-ttu-id="44b19-139">GUID du composant.</span><span class="sxs-lookup"><span data-stu-id="44b19-139">A GUID for the component.</span></span> <span data-ttu-id="44b19-140">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="44b19-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="44b19-141">Accès</span><span class="sxs-lookup"><span data-stu-id="44b19-141">Access</span></span>         | <span data-ttu-id="44b19-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44b19-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="44b19-143">Type</span><span class="sxs-lookup"><span data-stu-id="44b19-143">Type</span></span>           | <span data-ttu-id="44b19-144">String</span><span class="sxs-lookup"><span data-stu-id="44b19-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="44b19-145">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="44b19-145">Default</span></span>        | <span data-ttu-id="44b19-146">N/A</span><span class="sxs-lookup"><span data-stu-id="44b19-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="44b19-147">Système minimal</span><span class="sxs-lookup"><span data-stu-id="44b19-147">Minimum system</span></span> | <span data-ttu-id="44b19-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="44b19-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="44b19-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="44b19-149">InprocServer32</span></span>



| <span data-ttu-id="44b19-150">Entrée</span><span class="sxs-lookup"><span data-stu-id="44b19-150">Entry</span></span> | <span data-ttu-id="44b19-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="44b19-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="44b19-152">Description</span><span class="sxs-lookup"><span data-stu-id="44b19-152">Description</span></span>    | <span data-ttu-id="44b19-153">Chemin d’accès du fichier pour le composant.</span><span class="sxs-lookup"><span data-stu-id="44b19-153">The file path for the component.</span></span> |
| <span data-ttu-id="44b19-154">Accès</span><span class="sxs-lookup"><span data-stu-id="44b19-154">Access</span></span>         | <span data-ttu-id="44b19-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44b19-155">ReadOnly</span></span>                         |
| <span data-ttu-id="44b19-156">Type</span><span class="sxs-lookup"><span data-stu-id="44b19-156">Type</span></span>           | <span data-ttu-id="44b19-157">String</span><span class="sxs-lookup"><span data-stu-id="44b19-157">String</span></span>                           |
| <span data-ttu-id="44b19-158">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="44b19-158">Default</span></span>        | <span data-ttu-id="44b19-159">N/A</span><span class="sxs-lookup"><span data-stu-id="44b19-159">N/A</span></span>                              |
| <span data-ttu-id="44b19-160">Système minimal</span><span class="sxs-lookup"><span data-stu-id="44b19-160">Minimum system</span></span> | <span data-ttu-id="44b19-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="44b19-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="44b19-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="44b19-162">LocalServer32</span></span>



| <span data-ttu-id="44b19-163">Entrée</span><span class="sxs-lookup"><span data-stu-id="44b19-163">Entry</span></span> | <span data-ttu-id="44b19-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="44b19-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="44b19-165">Description</span><span class="sxs-lookup"><span data-stu-id="44b19-165">Description</span></span>    | <span data-ttu-id="44b19-166">Spécifie le chemin d’accès complet à une application serveur locale 32 bits.</span><span class="sxs-lookup"><span data-stu-id="44b19-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="44b19-167">Accès</span><span class="sxs-lookup"><span data-stu-id="44b19-167">Access</span></span>         | <span data-ttu-id="44b19-168">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44b19-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="44b19-169">Type</span><span class="sxs-lookup"><span data-stu-id="44b19-169">Type</span></span>           | <span data-ttu-id="44b19-170">String</span><span class="sxs-lookup"><span data-stu-id="44b19-170">String</span></span>                                                        |
| <span data-ttu-id="44b19-171">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="44b19-171">Default</span></span>        | <span data-ttu-id="44b19-172">N/A</span><span class="sxs-lookup"><span data-stu-id="44b19-172">N/A</span></span>                                                           |
| <span data-ttu-id="44b19-173">Système minimal</span><span class="sxs-lookup"><span data-stu-id="44b19-173">Minimum system</span></span> | <span data-ttu-id="44b19-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="44b19-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="44b19-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="44b19-175">ProgID</span></span>



| <span data-ttu-id="44b19-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="44b19-176">Entry</span></span> | <span data-ttu-id="44b19-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="44b19-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b19-178">Description</span><span class="sxs-lookup"><span data-stu-id="44b19-178">Description</span></span>    | <span data-ttu-id="44b19-179">Nom identifiant le composant.</span><span class="sxs-lookup"><span data-stu-id="44b19-179">A name identifying the component.</span></span> <span data-ttu-id="44b19-180">Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="44b19-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="44b19-181">Accès</span><span class="sxs-lookup"><span data-stu-id="44b19-181">Access</span></span>         | <span data-ttu-id="44b19-182">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44b19-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="44b19-183">Type</span><span class="sxs-lookup"><span data-stu-id="44b19-183">Type</span></span>           | <span data-ttu-id="44b19-184">String</span><span class="sxs-lookup"><span data-stu-id="44b19-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="44b19-185">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="44b19-185">Default</span></span>        | <span data-ttu-id="44b19-186">N/A</span><span class="sxs-lookup"><span data-stu-id="44b19-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="44b19-187">Système minimal</span><span class="sxs-lookup"><span data-stu-id="44b19-187">Minimum system</span></span> | <span data-ttu-id="44b19-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="44b19-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="44b19-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44b19-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b19-190">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="44b19-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
