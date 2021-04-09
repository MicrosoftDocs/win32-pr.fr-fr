---
description: La collection RolesForPartition est toujours associée à un objet dans la collection partitions. Il contient un objet pour chaque rôle affecté à la partition à laquelle il est associé.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Collection RolesForPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110390"
---
# <a name="rolesforpartition-collection"></a><span data-ttu-id="2d62d-104">Collection RolesForPartition</span><span class="sxs-lookup"><span data-stu-id="2d62d-104">RolesForPartition collection</span></span>

<span data-ttu-id="2d62d-105">La collection **RolesForPartition** est toujours associée à un objet dans la collection [**partitions**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="2d62d-105">The **RolesForPartition** collection is always related to an object in the [**Partitions**](partitions.md) collection.</span></span> <span data-ttu-id="2d62d-106">Il contient un objet pour chaque rôle affecté à la partition à laquelle il est associé.</span><span class="sxs-lookup"><span data-stu-id="2d62d-106">It holds an object for each role assigned to the partition to which it is related.</span></span>

<span data-ttu-id="2d62d-107">Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="2d62d-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="2d62d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2d62d-108">Members</span></span>

<span data-ttu-id="2d62d-109">La collection **RolesForPartition** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2d62d-109">The **RolesForPartition** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="2d62d-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="2d62d-110">Related Collections</span></span>

<span data-ttu-id="2d62d-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="2d62d-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="2d62d-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2d62d-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="2d62d-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="2d62d-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="2d62d-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="2d62d-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="2d62d-115">**UsersInPartitionRole**</span><span class="sxs-lookup"><span data-stu-id="2d62d-115">**UsersInPartitionRole**</span></span>](usersinpartitionrole.md)

<span data-ttu-id="2d62d-116">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="2d62d-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="2d62d-117">**Partitions**</span><span class="sxs-lookup"><span data-stu-id="2d62d-117">**Partitions**</span></span>](partitions.md)

## <a name="properties"></a><span data-ttu-id="2d62d-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d62d-118">Properties</span></span>

<span data-ttu-id="2d62d-119">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="2d62d-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="2d62d-120">Description</span><span class="sxs-lookup"><span data-stu-id="2d62d-120">Description</span></span>](#description)
-   [<span data-ttu-id="2d62d-121">Nom</span><span class="sxs-lookup"><span data-stu-id="2d62d-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="2d62d-122">Description</span><span class="sxs-lookup"><span data-stu-id="2d62d-122">Description</span></span>



| <span data-ttu-id="2d62d-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d62d-123">Entry</span></span> | <span data-ttu-id="2d62d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d62d-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="2d62d-125">Description</span><span class="sxs-lookup"><span data-stu-id="2d62d-125">Description</span></span>    | <span data-ttu-id="2d62d-126">Description du rôle.</span><span class="sxs-lookup"><span data-stu-id="2d62d-126">A description of the role.</span></span> |
| <span data-ttu-id="2d62d-127">Accès</span><span class="sxs-lookup"><span data-stu-id="2d62d-127">Access</span></span>         | <span data-ttu-id="2d62d-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d62d-128">ReadOnly</span></span>                   |
| <span data-ttu-id="2d62d-129">Type</span><span class="sxs-lookup"><span data-stu-id="2d62d-129">Type</span></span>           | <span data-ttu-id="2d62d-130">String</span><span class="sxs-lookup"><span data-stu-id="2d62d-130">String</span></span>                     |
| <span data-ttu-id="2d62d-131">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="2d62d-131">Default</span></span>        | <span data-ttu-id="2d62d-132">""</span><span class="sxs-lookup"><span data-stu-id="2d62d-132">""</span></span>                         |
| <span data-ttu-id="2d62d-133">Système minimal</span><span class="sxs-lookup"><span data-stu-id="2d62d-133">Minimum system</span></span> | <span data-ttu-id="2d62d-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d62d-134">Windows Server 2003</span></span>        |



 

### <a name="name"></a><span data-ttu-id="2d62d-135">Nom</span><span class="sxs-lookup"><span data-stu-id="2d62d-135">Name</span></span>



| <span data-ttu-id="2d62d-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="2d62d-136">Entry</span></span> | <span data-ttu-id="2d62d-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d62d-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d62d-138">Description</span><span class="sxs-lookup"><span data-stu-id="2d62d-138">Description</span></span>    | <span data-ttu-id="2d62d-139">Nom du rôle.</span><span class="sxs-lookup"><span data-stu-id="2d62d-139">The role name.</span></span> <span data-ttu-id="2d62d-140">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="2d62d-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="2d62d-141">Accès</span><span class="sxs-lookup"><span data-stu-id="2d62d-141">Access</span></span>         | <span data-ttu-id="2d62d-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d62d-142">ReadOnly</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2d62d-143">Type</span><span class="sxs-lookup"><span data-stu-id="2d62d-143">Type</span></span>           | <span data-ttu-id="2d62d-144">String</span><span class="sxs-lookup"><span data-stu-id="2d62d-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2d62d-145">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="2d62d-145">Default</span></span>        | <span data-ttu-id="2d62d-146">""</span><span class="sxs-lookup"><span data-stu-id="2d62d-146">""</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2d62d-147">Système minimal</span><span class="sxs-lookup"><span data-stu-id="2d62d-147">Minimum system</span></span> | <span data-ttu-id="2d62d-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d62d-148">Windows Server 2003</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="2d62d-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d62d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d62d-150">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="2d62d-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
