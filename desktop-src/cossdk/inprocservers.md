---
description: Contient la liste des serveurs in-process inscrits auprès du système. Elle contient un objet pour chaque composant qui est inscrit en tant que serveur in-process.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Collection InprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515149"
---
# <a name="inprocservers-collection"></a><span data-ttu-id="08adf-104">Collection InprocServers</span><span class="sxs-lookup"><span data-stu-id="08adf-104">InprocServers collection</span></span>

<span data-ttu-id="08adf-105">Contient la liste des serveurs in-process inscrits auprès du système.</span><span class="sxs-lookup"><span data-stu-id="08adf-105">Contains a list of the in-process servers registered with the system.</span></span> <span data-ttu-id="08adf-106">Elle contient un objet pour chaque composant qui est inscrit en tant que serveur in-process.</span><span class="sxs-lookup"><span data-stu-id="08adf-106">It contains an object for each component that is registered as an in-process server.</span></span>

<span data-ttu-id="08adf-107">Cette collection prend en charge la méthode [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mais pas la méthode [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="08adf-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="08adf-108">Pour installer ou importer des composants dans une application, utilisez des méthodes sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="08adf-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="08adf-109">Membres</span><span class="sxs-lookup"><span data-stu-id="08adf-109">Members</span></span>

<span data-ttu-id="08adf-110">La collection **InprocServers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="08adf-110">The **InprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="08adf-111">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="08adf-111">Related Collections</span></span>

<span data-ttu-id="08adf-112">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="08adf-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="08adf-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="08adf-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="08adf-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="08adf-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="08adf-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="08adf-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="08adf-116">**Causes**</span><span class="sxs-lookup"><span data-stu-id="08adf-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="08adf-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08adf-117">Properties</span></span>

<span data-ttu-id="08adf-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="08adf-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="08adf-119">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="08adf-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="08adf-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="08adf-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="08adf-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="08adf-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="08adf-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="08adf-122">CLSID</span></span>



| <span data-ttu-id="08adf-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="08adf-123">Entry</span></span> | <span data-ttu-id="08adf-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="08adf-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08adf-125">Description</span><span class="sxs-lookup"><span data-stu-id="08adf-125">Description</span></span>    | <span data-ttu-id="08adf-126">GUID du composant.</span><span class="sxs-lookup"><span data-stu-id="08adf-126">A GUID for the component.</span></span> <span data-ttu-id="08adf-127">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="08adf-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="08adf-128">Accès</span><span class="sxs-lookup"><span data-stu-id="08adf-128">Access</span></span>         | <span data-ttu-id="08adf-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08adf-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="08adf-130">Type</span><span class="sxs-lookup"><span data-stu-id="08adf-130">Type</span></span>           | <span data-ttu-id="08adf-131">String</span><span class="sxs-lookup"><span data-stu-id="08adf-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="08adf-132">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="08adf-132">Default</span></span>        | <span data-ttu-id="08adf-133">N/A</span><span class="sxs-lookup"><span data-stu-id="08adf-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="08adf-134">Système minimal</span><span class="sxs-lookup"><span data-stu-id="08adf-134">Minimum system</span></span> | <span data-ttu-id="08adf-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08adf-135">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="inprocserver32"></a><span data-ttu-id="08adf-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="08adf-136">InprocServer32</span></span>



| <span data-ttu-id="08adf-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="08adf-137">Entry</span></span> | <span data-ttu-id="08adf-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="08adf-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="08adf-139">Description</span><span class="sxs-lookup"><span data-stu-id="08adf-139">Description</span></span>    | <span data-ttu-id="08adf-140">Chemin d’accès du fichier pour le composant.</span><span class="sxs-lookup"><span data-stu-id="08adf-140">The file path for the component.</span></span> |
| <span data-ttu-id="08adf-141">Accès</span><span class="sxs-lookup"><span data-stu-id="08adf-141">Access</span></span>         | <span data-ttu-id="08adf-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08adf-142">ReadOnly</span></span>                         |
| <span data-ttu-id="08adf-143">Type</span><span class="sxs-lookup"><span data-stu-id="08adf-143">Type</span></span>           | <span data-ttu-id="08adf-144">String</span><span class="sxs-lookup"><span data-stu-id="08adf-144">String</span></span>                           |
| <span data-ttu-id="08adf-145">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="08adf-145">Default</span></span>        | <span data-ttu-id="08adf-146">N/A</span><span class="sxs-lookup"><span data-stu-id="08adf-146">N/A</span></span>                              |
| <span data-ttu-id="08adf-147">Système minimal</span><span class="sxs-lookup"><span data-stu-id="08adf-147">Minimum system</span></span> | <span data-ttu-id="08adf-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08adf-148">Windows 2000</span></span>                     |



 

### <a name="progid"></a><span data-ttu-id="08adf-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="08adf-149">ProgID</span></span>



| <span data-ttu-id="08adf-150">Entrée</span><span class="sxs-lookup"><span data-stu-id="08adf-150">Entry</span></span> | <span data-ttu-id="08adf-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="08adf-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08adf-152">Description</span><span class="sxs-lookup"><span data-stu-id="08adf-152">Description</span></span>    | <span data-ttu-id="08adf-153">Nom identifiant le composant.</span><span class="sxs-lookup"><span data-stu-id="08adf-153">A name identifying the component.</span></span> <span data-ttu-id="08adf-154">Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="08adf-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="08adf-155">Accès</span><span class="sxs-lookup"><span data-stu-id="08adf-155">Access</span></span>         | <span data-ttu-id="08adf-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08adf-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="08adf-157">Type</span><span class="sxs-lookup"><span data-stu-id="08adf-157">Type</span></span>           | <span data-ttu-id="08adf-158">String</span><span class="sxs-lookup"><span data-stu-id="08adf-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="08adf-159">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="08adf-159">Default</span></span>        | <span data-ttu-id="08adf-160">N/A</span><span class="sxs-lookup"><span data-stu-id="08adf-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="08adf-161">Système minimal</span><span class="sxs-lookup"><span data-stu-id="08adf-161">Minimum system</span></span> | <span data-ttu-id="08adf-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08adf-162">Windows 2000</span></span>                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="08adf-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08adf-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08adf-164">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="08adf-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
