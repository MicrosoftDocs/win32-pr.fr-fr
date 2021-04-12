---
description: Récupère des informations d’erreur étendues concernant les méthodes qui traitent plusieurs objets, tels que remplir et SaveChanges sur l’objet COMAdminCatalogCollection, et les méthodes pour installer, importer ou exporter des applications ou des composants sur l’objet COMAdminCatalog.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: ErrorInfo, collection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483608"
---
# <a name="errorinfo-collection"></a><span data-ttu-id="bbb90-103">ErrorInfo, collection</span><span class="sxs-lookup"><span data-stu-id="bbb90-103">ErrorInfo collection</span></span>

<span data-ttu-id="bbb90-104">Récupère des informations d’erreur étendues concernant les méthodes qui traitent plusieurs objets, tels que [**remplir**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) et [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , et les méthodes pour installer, importer ou exporter des applications ou des composants sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb90-104">Retrieves extended error information regarding methods that deal with multiple objects, such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, and methods to install, import, or export applications or components on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

<span data-ttu-id="bbb90-105">Utilisez la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) sur un [**COMAdminCatalogCollection**](comadmincatalogcollection.md) pour accéder à la collection **errorInfo** associée à la collection d’origine qui a une erreur.</span><span class="sxs-lookup"><span data-stu-id="bbb90-105">Use the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) to access the **ErrorInfo** collection associated with the original collection that has an error.</span></span>

<span data-ttu-id="bbb90-106">Vous devez appeler [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) sur **errorInfo** immédiatement après qu’une erreur s’est produite ; dans le cas contraire, les informations sur l’erreur sont perdues.</span><span class="sxs-lookup"><span data-stu-id="bbb90-106">You must call [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on **ErrorInfo** immediately after an error occurs; otherwise, the error information is lost.</span></span>

<span data-ttu-id="bbb90-107">Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb90-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="bbb90-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bbb90-108">Members</span></span>

<span data-ttu-id="bbb90-109">La collection **errorInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bbb90-109">The **ErrorInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="bbb90-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="bbb90-110">Related Collections</span></span>

<span data-ttu-id="bbb90-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="bbb90-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="bbb90-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="bbb90-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="bbb90-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="bbb90-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="bbb90-114">Vous pouvez accéder à cette collection à partir de chaque collection à l’exception de **errorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**root**](root.md)et [**WOWInprocServers**](wowinprocservers.md).</span><span class="sxs-lookup"><span data-stu-id="bbb90-114">You can navigate to this collection from every collection except for **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md), and [**WOWInprocServers**](wowinprocservers.md).</span></span>

## <a name="properties"></a><span data-ttu-id="bbb90-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bbb90-115">Properties</span></span>

<span data-ttu-id="bbb90-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="bbb90-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="bbb90-117">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="bbb90-117">ErrorCode</span></span>](#errorcode)
-   [<span data-ttu-id="bbb90-118">MajorRef</span><span class="sxs-lookup"><span data-stu-id="bbb90-118">MajorRef</span></span>](#majorref)
-   [<span data-ttu-id="bbb90-119">MinorRef</span><span class="sxs-lookup"><span data-stu-id="bbb90-119">MinorRef</span></span>](#minorref)
-   [<span data-ttu-id="bbb90-120">Nom</span><span class="sxs-lookup"><span data-stu-id="bbb90-120">Name</span></span>](#name)

### <a name="errorcode"></a><span data-ttu-id="bbb90-121">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="bbb90-121">ErrorCode</span></span>



| <span data-ttu-id="bbb90-122">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbb90-122">Entry</span></span> | <span data-ttu-id="bbb90-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbb90-123">Value</span></span> |
|----------------|----------------------------------------|
| <span data-ttu-id="bbb90-124">Description</span><span class="sxs-lookup"><span data-stu-id="bbb90-124">Description</span></span>    | <span data-ttu-id="bbb90-125">Code d'erreur pour l'objet ou le fichier.</span><span class="sxs-lookup"><span data-stu-id="bbb90-125">The error code for the object or file.</span></span> |
| <span data-ttu-id="bbb90-126">Accès</span><span class="sxs-lookup"><span data-stu-id="bbb90-126">Access</span></span>         | <span data-ttu-id="bbb90-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbb90-127">ReadOnly</span></span>                               |
| <span data-ttu-id="bbb90-128">Type</span><span class="sxs-lookup"><span data-stu-id="bbb90-128">Type</span></span>           | <span data-ttu-id="bbb90-129">String</span><span class="sxs-lookup"><span data-stu-id="bbb90-129">String</span></span>                                 |
| <span data-ttu-id="bbb90-130">Default</span><span class="sxs-lookup"><span data-stu-id="bbb90-130">Default</span></span>        | <span data-ttu-id="bbb90-131">None</span><span class="sxs-lookup"><span data-stu-id="bbb90-131">None</span></span>                                   |
| <span data-ttu-id="bbb90-132">Système minimal</span><span class="sxs-lookup"><span data-stu-id="bbb90-132">Minimum system</span></span> | <span data-ttu-id="bbb90-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bbb90-133">Windows 2000</span></span>                           |



 

### <a name="majorref"></a><span data-ttu-id="bbb90-134">MajorRef</span><span class="sxs-lookup"><span data-stu-id="bbb90-134">MajorRef</span></span>



| <span data-ttu-id="bbb90-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbb90-135">Entry</span></span> | <span data-ttu-id="bbb90-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbb90-136">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb90-137">Description</span><span class="sxs-lookup"><span data-stu-id="bbb90-137">Description</span></span>    | <span data-ttu-id="bbb90-138">Valeur de la propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) pour l’objet qui contient une erreur.</span><span class="sxs-lookup"><span data-stu-id="bbb90-138">The [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property value for the object that has an error.</span></span> <span data-ttu-id="bbb90-139">Par exemple, si un appel de [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) pour une collection échoue sur un objet particulier dans la collection, la valeur de la propriété de **clé** pour cet objet est signalée comme valeur MajorRef.</span><span class="sxs-lookup"><span data-stu-id="bbb90-139">For example, if a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) call for a collection fails on a particular object in the collection, the **Key** property value for that object is reported as the MajorRef value.</span></span> <span data-ttu-id="bbb90-140">Utilisez cette propriété pour examiner l’élément qui ne parvient pas à mettre à jour ou pour trouver le composant ou la DLL dont l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="bbb90-140">Use this property to look at the item that fails to update or to find the component or DLL that fails to install.</span></span> |
| <span data-ttu-id="bbb90-141">Accès</span><span class="sxs-lookup"><span data-stu-id="bbb90-141">Access</span></span>         | <span data-ttu-id="bbb90-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbb90-142">ReadOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bbb90-143">Type</span><span class="sxs-lookup"><span data-stu-id="bbb90-143">Type</span></span>           | <span data-ttu-id="bbb90-144">String</span><span class="sxs-lookup"><span data-stu-id="bbb90-144">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="bbb90-145">Default</span><span class="sxs-lookup"><span data-stu-id="bbb90-145">Default</span></span>        | <span data-ttu-id="bbb90-146">None</span><span class="sxs-lookup"><span data-stu-id="bbb90-146">None</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="bbb90-147">Système minimal</span><span class="sxs-lookup"><span data-stu-id="bbb90-147">Minimum system</span></span> | <span data-ttu-id="bbb90-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bbb90-148">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a><span data-ttu-id="bbb90-149">MinorRef</span><span class="sxs-lookup"><span data-stu-id="bbb90-149">MinorRef</span></span>



| <span data-ttu-id="bbb90-150">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbb90-150">Entry</span></span> | <span data-ttu-id="bbb90-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbb90-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb90-152">Description</span><span class="sxs-lookup"><span data-stu-id="bbb90-152">Description</span></span>    | <span data-ttu-id="bbb90-153">Spécification précise de l’élément qui a une erreur, telle qu’un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="bbb90-153">A precise specification of the item that has an error, such as a property name.</span></span> <span data-ttu-id="bbb90-154">Si plusieurs erreurs se produisent ou dans des contextes où cela ne s’applique pas, MinorRef est <Invalid> .</span><span class="sxs-lookup"><span data-stu-id="bbb90-154">If multiple errors occur or in contexts in which this doesn't apply, MinorRef is <Invalid>.</span></span> |
| <span data-ttu-id="bbb90-155">Accès</span><span class="sxs-lookup"><span data-stu-id="bbb90-155">Access</span></span>         | <span data-ttu-id="bbb90-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbb90-156">ReadOnly</span></span>                                                                                                                                                                          |
| <span data-ttu-id="bbb90-157">Type</span><span class="sxs-lookup"><span data-stu-id="bbb90-157">Type</span></span>           | <span data-ttu-id="bbb90-158">String</span><span class="sxs-lookup"><span data-stu-id="bbb90-158">String</span></span>                                                                                                                                                                            |
| <span data-ttu-id="bbb90-159">Default</span><span class="sxs-lookup"><span data-stu-id="bbb90-159">Default</span></span>        | <span data-ttu-id="bbb90-160">None</span><span class="sxs-lookup"><span data-stu-id="bbb90-160">None</span></span>                                                                                                                                                                              |
| <span data-ttu-id="bbb90-161">Système minimal</span><span class="sxs-lookup"><span data-stu-id="bbb90-161">Minimum system</span></span> | <span data-ttu-id="bbb90-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bbb90-162">Windows 2000</span></span>                                                                                                                                                                      |



 

### <a name="name"></a><span data-ttu-id="bbb90-163">Nom</span><span class="sxs-lookup"><span data-stu-id="bbb90-163">Name</span></span>



| <span data-ttu-id="bbb90-164">Entrée</span><span class="sxs-lookup"><span data-stu-id="bbb90-164">Entry</span></span> | <span data-ttu-id="bbb90-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbb90-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb90-166">Description</span><span class="sxs-lookup"><span data-stu-id="bbb90-166">Description</span></span>    | <span data-ttu-id="bbb90-167">Nom de l’objet ou du fichier qui contient une erreur.</span><span class="sxs-lookup"><span data-stu-id="bbb90-167">The name of the object or file that has an error.</span></span> <span data-ttu-id="bbb90-168">Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="bbb90-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="bbb90-169">Accès</span><span class="sxs-lookup"><span data-stu-id="bbb90-169">Access</span></span>         | <span data-ttu-id="bbb90-170">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbb90-170">ReadOnly</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="bbb90-171">Type</span><span class="sxs-lookup"><span data-stu-id="bbb90-171">Type</span></span>           | <span data-ttu-id="bbb90-172">String</span><span class="sxs-lookup"><span data-stu-id="bbb90-172">String</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="bbb90-173">Default</span><span class="sxs-lookup"><span data-stu-id="bbb90-173">Default</span></span>        | <span data-ttu-id="bbb90-174">None</span><span class="sxs-lookup"><span data-stu-id="bbb90-174">None</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="bbb90-175">Système minimal</span><span class="sxs-lookup"><span data-stu-id="bbb90-175">Minimum system</span></span> | <span data-ttu-id="bbb90-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bbb90-176">Windows 2000</span></span>                                                                                                                                                                                                             |



 

## <a name="see-also"></a><span data-ttu-id="bbb90-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbb90-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb90-178">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="bbb90-178">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
