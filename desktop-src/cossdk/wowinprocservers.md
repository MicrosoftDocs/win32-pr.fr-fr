---
description: Contient la liste des serveurs in-process inscrits auprès du système pour les composants 32 bits sur les ordinateurs 64 bits. Elle contient un objet pour chaque composant.
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: Collection WOWInprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 43fceababaf6ced44a1ba3aef020900ed1afe4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523236"
---
# <a name="wowinprocservers-collection"></a><span data-ttu-id="937f3-104">Collection WOWInprocServers</span><span class="sxs-lookup"><span data-stu-id="937f3-104">WOWInprocServers collection</span></span>

<span data-ttu-id="937f3-105">Contient la liste des serveurs in-process inscrits auprès du système pour les composants 32 bits sur les ordinateurs 64 bits.</span><span class="sxs-lookup"><span data-stu-id="937f3-105">Contains a list of the in-process servers registered with the system for 32-bit components on 64-bit computers.</span></span> <span data-ttu-id="937f3-106">Elle contient un objet pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="937f3-106">It contains an object for each component.</span></span>

<span data-ttu-id="937f3-107">Cette collection prend en charge la méthode [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mais pas la méthode [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="937f3-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="937f3-108">Pour installer ou importer des composants dans une application, utilisez des méthodes sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="937f3-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="937f3-109">Membres</span><span class="sxs-lookup"><span data-stu-id="937f3-109">Members</span></span>

<span data-ttu-id="937f3-110">La collection **WOWInprocServers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="937f3-110">The **WOWInprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="937f3-111">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="937f3-111">Related Collections</span></span>

<span data-ttu-id="937f3-112">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="937f3-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="937f3-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="937f3-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="937f3-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="937f3-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="937f3-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="937f3-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="937f3-116">**Causes**</span><span class="sxs-lookup"><span data-stu-id="937f3-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="937f3-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="937f3-117">Properties</span></span>

<span data-ttu-id="937f3-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="937f3-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="937f3-119">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="937f3-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="937f3-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="937f3-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="937f3-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="937f3-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="937f3-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="937f3-122">CLSID</span></span>



| <span data-ttu-id="937f3-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="937f3-123">Entry</span></span> | <span data-ttu-id="937f3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="937f3-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="937f3-125">Description</span><span class="sxs-lookup"><span data-stu-id="937f3-125">Description</span></span>    | <span data-ttu-id="937f3-126">GUID du composant.</span><span class="sxs-lookup"><span data-stu-id="937f3-126">A GUID for the component.</span></span> <span data-ttu-id="937f3-127">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="937f3-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="937f3-128">Accès</span><span class="sxs-lookup"><span data-stu-id="937f3-128">Access</span></span>         | <span data-ttu-id="937f3-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="937f3-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="937f3-130">Type</span><span class="sxs-lookup"><span data-stu-id="937f3-130">Type</span></span>           | <span data-ttu-id="937f3-131">String</span><span class="sxs-lookup"><span data-stu-id="937f3-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="937f3-132">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="937f3-132">Default</span></span>        | <span data-ttu-id="937f3-133">N/A</span><span class="sxs-lookup"><span data-stu-id="937f3-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="937f3-134">Système minimal</span><span class="sxs-lookup"><span data-stu-id="937f3-134">Minimum system</span></span> | <span data-ttu-id="937f3-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="937f3-135">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="937f3-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="937f3-136">InprocServer32</span></span>



| <span data-ttu-id="937f3-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="937f3-137">Entry</span></span> | <span data-ttu-id="937f3-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="937f3-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="937f3-139">Description</span><span class="sxs-lookup"><span data-stu-id="937f3-139">Description</span></span>    | <span data-ttu-id="937f3-140">Chemin d’accès du fichier pour le composant.</span><span class="sxs-lookup"><span data-stu-id="937f3-140">The file path for the component.</span></span> |
| <span data-ttu-id="937f3-141">Accès</span><span class="sxs-lookup"><span data-stu-id="937f3-141">Access</span></span>         | <span data-ttu-id="937f3-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="937f3-142">ReadOnly</span></span>                         |
| <span data-ttu-id="937f3-143">Type</span><span class="sxs-lookup"><span data-stu-id="937f3-143">Type</span></span>           | <span data-ttu-id="937f3-144">String</span><span class="sxs-lookup"><span data-stu-id="937f3-144">String</span></span>                           |
| <span data-ttu-id="937f3-145">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="937f3-145">Default</span></span>        | <span data-ttu-id="937f3-146">N/A</span><span class="sxs-lookup"><span data-stu-id="937f3-146">N/A</span></span>                              |
| <span data-ttu-id="937f3-147">Système minimal</span><span class="sxs-lookup"><span data-stu-id="937f3-147">Minimum system</span></span> | <span data-ttu-id="937f3-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="937f3-148">Windows XP</span></span>                       |



 

### <a name="progid"></a><span data-ttu-id="937f3-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="937f3-149">ProgID</span></span>



| <span data-ttu-id="937f3-150">Entrée</span><span class="sxs-lookup"><span data-stu-id="937f3-150">Entry</span></span> | <span data-ttu-id="937f3-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="937f3-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="937f3-152">Description</span><span class="sxs-lookup"><span data-stu-id="937f3-152">Description</span></span>    | <span data-ttu-id="937f3-153">Nom identifiant le composant.</span><span class="sxs-lookup"><span data-stu-id="937f3-153">A name identifying the component.</span></span> <span data-ttu-id="937f3-154">Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="937f3-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="937f3-155">Accès</span><span class="sxs-lookup"><span data-stu-id="937f3-155">Access</span></span>         | <span data-ttu-id="937f3-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="937f3-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="937f3-157">Type</span><span class="sxs-lookup"><span data-stu-id="937f3-157">Type</span></span>           | <span data-ttu-id="937f3-158">String</span><span class="sxs-lookup"><span data-stu-id="937f3-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="937f3-159">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="937f3-159">Default</span></span>        | <span data-ttu-id="937f3-160">N/A</span><span class="sxs-lookup"><span data-stu-id="937f3-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="937f3-161">Système minimal</span><span class="sxs-lookup"><span data-stu-id="937f3-161">Minimum system</span></span> | <span data-ttu-id="937f3-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="937f3-162">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="937f3-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="937f3-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="937f3-164">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="937f3-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
