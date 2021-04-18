---
description: Les propriétés exposées pour la collection WOWLegacyServers sont destinées à être identiques à la collection LegacyServers, à ceci près que la collection WOWLegacyServers est tirée du Registre 32 bits sur les ordinateurs 64 bits.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Collection WOWLegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536312"
---
# <a name="wowlegacyservers-collection"></a><span data-ttu-id="b08f0-103">Collection WOWLegacyServers</span><span class="sxs-lookup"><span data-stu-id="b08f0-103">WOWLegacyServers collection</span></span>

<span data-ttu-id="b08f0-104">Les propriétés exposées pour la collection **WOWLegacyServers** sont destinées à être identiques à la collection [**LegacyServers**](legacyservers.md) , à ceci près que la collection **WOWLegacyServers** est tirée du registre 32 bits sur les ordinateurs 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b08f0-104">Exposed properties for the **WOWLegacyServers** collection are intended to be identical to the [**LegacyServers**](legacyservers.md) collection except that the **WOWLegacyServers** collection is drawn from the 32-bit registry on 64-bit computers.</span></span>

<span data-ttu-id="b08f0-105">Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b08f0-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b08f0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b08f0-106">Members</span></span>

<span data-ttu-id="b08f0-107">La collection **WOWLegacyServers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b08f0-107">The **WOWLegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b08f0-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="b08f0-108">Related Collections</span></span>

<span data-ttu-id="b08f0-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="b08f0-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b08f0-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b08f0-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b08f0-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b08f0-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b08f0-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b08f0-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b08f0-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="b08f0-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b08f0-114">**Causes**</span><span class="sxs-lookup"><span data-stu-id="b08f0-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="b08f0-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b08f0-115">Properties</span></span>

<span data-ttu-id="b08f0-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="b08f0-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b08f0-117">NomClasse</span><span class="sxs-lookup"><span data-stu-id="b08f0-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="b08f0-118">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="b08f0-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="b08f0-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="b08f0-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="b08f0-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b08f0-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="b08f0-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="b08f0-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="b08f0-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="b08f0-122">ClassName</span></span>



| <span data-ttu-id="b08f0-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="b08f0-123">Entry</span></span> | <span data-ttu-id="b08f0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b08f0-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="b08f0-125">Description</span><span class="sxs-lookup"><span data-stu-id="b08f0-125">Description</span></span>    | <span data-ttu-id="b08f0-126">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="b08f0-126">The name of the class.</span></span> |
| <span data-ttu-id="b08f0-127">Accès</span><span class="sxs-lookup"><span data-stu-id="b08f0-127">Access</span></span>         | <span data-ttu-id="b08f0-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b08f0-128">ReadOnly</span></span>               |
| <span data-ttu-id="b08f0-129">Type</span><span class="sxs-lookup"><span data-stu-id="b08f0-129">Type</span></span>           | <span data-ttu-id="b08f0-130">String</span><span class="sxs-lookup"><span data-stu-id="b08f0-130">String</span></span>                 |
| <span data-ttu-id="b08f0-131">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b08f0-131">Default</span></span>        | <span data-ttu-id="b08f0-132">N/A</span><span class="sxs-lookup"><span data-stu-id="b08f0-132">N/A</span></span>                    |
| <span data-ttu-id="b08f0-133">Système minimal</span><span class="sxs-lookup"><span data-stu-id="b08f0-133">Minimum system</span></span> | <span data-ttu-id="b08f0-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b08f0-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="b08f0-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="b08f0-135">CLSID</span></span>



| <span data-ttu-id="b08f0-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="b08f0-136">Entry</span></span> | <span data-ttu-id="b08f0-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="b08f0-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08f0-138">Description</span><span class="sxs-lookup"><span data-stu-id="b08f0-138">Description</span></span>    | <span data-ttu-id="b08f0-139">GUID du composant.</span><span class="sxs-lookup"><span data-stu-id="b08f0-139">A GUID for the component.</span></span> <span data-ttu-id="b08f0-140">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="b08f0-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b08f0-141">Accès</span><span class="sxs-lookup"><span data-stu-id="b08f0-141">Access</span></span>         | <span data-ttu-id="b08f0-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b08f0-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="b08f0-143">Type</span><span class="sxs-lookup"><span data-stu-id="b08f0-143">Type</span></span>           | <span data-ttu-id="b08f0-144">String</span><span class="sxs-lookup"><span data-stu-id="b08f0-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="b08f0-145">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b08f0-145">Default</span></span>        | <span data-ttu-id="b08f0-146">N/A</span><span class="sxs-lookup"><span data-stu-id="b08f0-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="b08f0-147">Système minimal</span><span class="sxs-lookup"><span data-stu-id="b08f0-147">Minimum system</span></span> | <span data-ttu-id="b08f0-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b08f0-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="b08f0-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="b08f0-149">InprocServer32</span></span>



| <span data-ttu-id="b08f0-150">Entrée</span><span class="sxs-lookup"><span data-stu-id="b08f0-150">Entry</span></span> | <span data-ttu-id="b08f0-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="b08f0-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="b08f0-152">Description</span><span class="sxs-lookup"><span data-stu-id="b08f0-152">Description</span></span>    | <span data-ttu-id="b08f0-153">Chemin d’accès du fichier pour le composant.</span><span class="sxs-lookup"><span data-stu-id="b08f0-153">The file path for the component.</span></span> |
| <span data-ttu-id="b08f0-154">Accès</span><span class="sxs-lookup"><span data-stu-id="b08f0-154">Access</span></span>         | <span data-ttu-id="b08f0-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b08f0-155">ReadOnly</span></span>                         |
| <span data-ttu-id="b08f0-156">Type</span><span class="sxs-lookup"><span data-stu-id="b08f0-156">Type</span></span>           | <span data-ttu-id="b08f0-157">String</span><span class="sxs-lookup"><span data-stu-id="b08f0-157">String</span></span>                           |
| <span data-ttu-id="b08f0-158">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b08f0-158">Default</span></span>        | <span data-ttu-id="b08f0-159">N/A</span><span class="sxs-lookup"><span data-stu-id="b08f0-159">N/A</span></span>                              |
| <span data-ttu-id="b08f0-160">Système minimal</span><span class="sxs-lookup"><span data-stu-id="b08f0-160">Minimum system</span></span> | <span data-ttu-id="b08f0-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b08f0-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="b08f0-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b08f0-162">LocalServer32</span></span>



| <span data-ttu-id="b08f0-163">Entrée</span><span class="sxs-lookup"><span data-stu-id="b08f0-163">Entry</span></span> | <span data-ttu-id="b08f0-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="b08f0-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="b08f0-165">Description</span><span class="sxs-lookup"><span data-stu-id="b08f0-165">Description</span></span>    | <span data-ttu-id="b08f0-166">Spécifie le chemin d’accès complet à une application serveur locale 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b08f0-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="b08f0-167">Accès</span><span class="sxs-lookup"><span data-stu-id="b08f0-167">Access</span></span>         | <span data-ttu-id="b08f0-168">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b08f0-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="b08f0-169">Type</span><span class="sxs-lookup"><span data-stu-id="b08f0-169">Type</span></span>           | <span data-ttu-id="b08f0-170">String</span><span class="sxs-lookup"><span data-stu-id="b08f0-170">String</span></span>                                                        |
| <span data-ttu-id="b08f0-171">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b08f0-171">Default</span></span>        | <span data-ttu-id="b08f0-172">N/A</span><span class="sxs-lookup"><span data-stu-id="b08f0-172">N/A</span></span>                                                           |
| <span data-ttu-id="b08f0-173">Système minimal</span><span class="sxs-lookup"><span data-stu-id="b08f0-173">Minimum system</span></span> | <span data-ttu-id="b08f0-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b08f0-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="b08f0-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="b08f0-175">ProgID</span></span>



| <span data-ttu-id="b08f0-176">Entrée</span><span class="sxs-lookup"><span data-stu-id="b08f0-176">Entry</span></span> | <span data-ttu-id="b08f0-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="b08f0-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08f0-178">Description</span><span class="sxs-lookup"><span data-stu-id="b08f0-178">Description</span></span>    | <span data-ttu-id="b08f0-179">Nom identifiant le composant.</span><span class="sxs-lookup"><span data-stu-id="b08f0-179">A name identifying the component.</span></span> <span data-ttu-id="b08f0-180">Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="b08f0-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b08f0-181">Accès</span><span class="sxs-lookup"><span data-stu-id="b08f0-181">Access</span></span>         | <span data-ttu-id="b08f0-182">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b08f0-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="b08f0-183">Type</span><span class="sxs-lookup"><span data-stu-id="b08f0-183">Type</span></span>           | <span data-ttu-id="b08f0-184">String</span><span class="sxs-lookup"><span data-stu-id="b08f0-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="b08f0-185">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b08f0-185">Default</span></span>        | <span data-ttu-id="b08f0-186">N/A</span><span class="sxs-lookup"><span data-stu-id="b08f0-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="b08f0-187">Système minimal</span><span class="sxs-lookup"><span data-stu-id="b08f0-187">Minimum system</span></span> | <span data-ttu-id="b08f0-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b08f0-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="b08f0-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b08f0-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b08f0-190">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="b08f0-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
