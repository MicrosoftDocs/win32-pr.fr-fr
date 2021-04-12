---
description: La collection de rôles est toujours liée à un objet dans la collection d’applications. Elle contient un objet pour chaque rôle affecté à l’application à laquelle elle est associée.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Collection de rôles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201100"
---
# <a name="roles-collection"></a><span data-ttu-id="c480d-104">Collection de rôles</span><span class="sxs-lookup"><span data-stu-id="c480d-104">Roles collection</span></span>

<span data-ttu-id="c480d-105">La collection de **rôles** est toujours liée à un objet dans la collection d' [**applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="c480d-105">The **Roles** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="c480d-106">Elle contient un objet pour chaque rôle affecté à l’application à laquelle elle est associée.</span><span class="sxs-lookup"><span data-stu-id="c480d-106">It holds an object for each role assigned to the application to which it is related.</span></span>

<span data-ttu-id="c480d-107">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c480d-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="c480d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c480d-108">Members</span></span>

<span data-ttu-id="c480d-109">La collection **roles** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c480d-109">The **Roles** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="c480d-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="c480d-110">Related Collections</span></span>

<span data-ttu-id="c480d-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="c480d-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="c480d-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c480d-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="c480d-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="c480d-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="c480d-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="c480d-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="c480d-115">**UsersInRole**</span><span class="sxs-lookup"><span data-stu-id="c480d-115">**UsersInRole**</span></span>](usersinrole.md)

<span data-ttu-id="c480d-116">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="c480d-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="c480d-117">**Applications**</span><span class="sxs-lookup"><span data-stu-id="c480d-117">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="c480d-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c480d-118">Properties</span></span>

<span data-ttu-id="c480d-119">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="c480d-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="c480d-120">Description</span><span class="sxs-lookup"><span data-stu-id="c480d-120">Description</span></span>](#description)
-   [<span data-ttu-id="c480d-121">Nom</span><span class="sxs-lookup"><span data-stu-id="c480d-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="c480d-122">Description</span><span class="sxs-lookup"><span data-stu-id="c480d-122">Description</span></span>



| <span data-ttu-id="c480d-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="c480d-123">Entry</span></span> | <span data-ttu-id="c480d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c480d-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="c480d-125">Description</span><span class="sxs-lookup"><span data-stu-id="c480d-125">Description</span></span>    | <span data-ttu-id="c480d-126">Description du rôle.</span><span class="sxs-lookup"><span data-stu-id="c480d-126">A description of the role.</span></span> |
| <span data-ttu-id="c480d-127">Accès</span><span class="sxs-lookup"><span data-stu-id="c480d-127">Access</span></span>         | <span data-ttu-id="c480d-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c480d-128">ReadWrite</span></span>                  |
| <span data-ttu-id="c480d-129">Type</span><span class="sxs-lookup"><span data-stu-id="c480d-129">Type</span></span>           | <span data-ttu-id="c480d-130">String</span><span class="sxs-lookup"><span data-stu-id="c480d-130">String</span></span>                     |
| <span data-ttu-id="c480d-131">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c480d-131">Default</span></span>        | <span data-ttu-id="c480d-132">""</span><span class="sxs-lookup"><span data-stu-id="c480d-132">""</span></span>                         |
| <span data-ttu-id="c480d-133">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c480d-133">Minimum system</span></span> | <span data-ttu-id="c480d-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c480d-134">Windows 2000</span></span>               |



 

### <a name="name"></a><span data-ttu-id="c480d-135">Nom</span><span class="sxs-lookup"><span data-stu-id="c480d-135">Name</span></span>



| <span data-ttu-id="c480d-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="c480d-136">Entry</span></span> | <span data-ttu-id="c480d-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c480d-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c480d-138">Description</span><span class="sxs-lookup"><span data-stu-id="c480d-138">Description</span></span>    | <span data-ttu-id="c480d-139">Nom du rôle.</span><span class="sxs-lookup"><span data-stu-id="c480d-139">The role name.</span></span> <span data-ttu-id="c480d-140">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="c480d-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="c480d-141">Accès</span><span class="sxs-lookup"><span data-stu-id="c480d-141">Access</span></span>         | <span data-ttu-id="c480d-142">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="c480d-142">WriteOnce</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c480d-143">Type</span><span class="sxs-lookup"><span data-stu-id="c480d-143">Type</span></span>           | <span data-ttu-id="c480d-144">String</span><span class="sxs-lookup"><span data-stu-id="c480d-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c480d-145">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c480d-145">Default</span></span>        | <span data-ttu-id="c480d-146">« Nouveau rôle »</span><span class="sxs-lookup"><span data-stu-id="c480d-146">"New Role"</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c480d-147">Système minimal</span><span class="sxs-lookup"><span data-stu-id="c480d-147">Minimum system</span></span> | <span data-ttu-id="c480d-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c480d-148">Windows 2000</span></span>                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="c480d-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c480d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c480d-150">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="c480d-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
