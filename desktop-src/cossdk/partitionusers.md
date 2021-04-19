---
description: Contient un objet pour chaque utilisateur de la partition.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Collection PartitionUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516581"
---
# <a name="partitionusers-collection"></a><span data-ttu-id="d0efa-103">Collection PartitionUsers</span><span class="sxs-lookup"><span data-stu-id="d0efa-103">PartitionUsers collection</span></span>

<span data-ttu-id="d0efa-104">Contient un objet pour chaque utilisateur de la partition.</span><span class="sxs-lookup"><span data-stu-id="d0efa-104">Contains an object for each partition user.</span></span>

<span data-ttu-id="d0efa-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d0efa-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="d0efa-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d0efa-106">Members</span></span>

<span data-ttu-id="d0efa-107">La collection **PartitionUsers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d0efa-107">The **PartitionUsers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="d0efa-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="d0efa-108">Related Collections</span></span>

<span data-ttu-id="d0efa-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="d0efa-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="d0efa-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="d0efa-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="d0efa-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="d0efa-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="d0efa-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="d0efa-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="d0efa-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="d0efa-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="d0efa-114">**Causes**</span><span class="sxs-lookup"><span data-stu-id="d0efa-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="d0efa-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d0efa-115">Properties</span></span>

<span data-ttu-id="d0efa-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="d0efa-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="d0efa-117">AccountName</span><span class="sxs-lookup"><span data-stu-id="d0efa-117">AccountName</span></span>](#accountname)
-   [<span data-ttu-id="d0efa-118">DefaultPartitionID</span><span class="sxs-lookup"><span data-stu-id="d0efa-118">DefaultPartitionID</span></span>](#defaultpartitionid)

### <a name="accountname"></a><span data-ttu-id="d0efa-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="d0efa-119">AccountName</span></span>



| <span data-ttu-id="d0efa-120">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0efa-120">Entry</span></span> | <span data-ttu-id="d0efa-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0efa-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0efa-122">Description</span><span class="sxs-lookup"><span data-stu-id="d0efa-122">Description</span></span>    | <span data-ttu-id="d0efa-123">Nom du compte de l’utilisateur de la partition.</span><span class="sxs-lookup"><span data-stu-id="d0efa-123">Name of the partition user's account.</span></span> <span data-ttu-id="d0efa-124">Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="d0efa-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="d0efa-125">Accès</span><span class="sxs-lookup"><span data-stu-id="d0efa-125">Access</span></span>         | <span data-ttu-id="d0efa-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="d0efa-126">WriteOnce</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="d0efa-127">Type</span><span class="sxs-lookup"><span data-stu-id="d0efa-127">Type</span></span>           | <span data-ttu-id="d0efa-128">String</span><span class="sxs-lookup"><span data-stu-id="d0efa-128">String</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="d0efa-129">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d0efa-129">Default</span></span>        | <span data-ttu-id="d0efa-130">« Nouvel utilisateur »</span><span class="sxs-lookup"><span data-stu-id="d0efa-130">"New User"</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="d0efa-131">Système minimal</span><span class="sxs-lookup"><span data-stu-id="d0efa-131">Minimum system</span></span> | <span data-ttu-id="d0efa-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0efa-132">Windows Server 2003</span></span>                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a><span data-ttu-id="d0efa-133">DefaultPartitionID</span><span class="sxs-lookup"><span data-stu-id="d0efa-133">DefaultPartitionID</span></span>



| <span data-ttu-id="d0efa-134">Entrée</span><span class="sxs-lookup"><span data-stu-id="d0efa-134">Entry</span></span> | <span data-ttu-id="d0efa-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0efa-135">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="d0efa-136">Description</span><span class="sxs-lookup"><span data-stu-id="d0efa-136">Description</span></span>    | <span data-ttu-id="d0efa-137">Identificateur global unique de la partition d’application de base.</span><span class="sxs-lookup"><span data-stu-id="d0efa-137">The globally unique identifier for the base application partition.</span></span> |
| <span data-ttu-id="d0efa-138">Accès</span><span class="sxs-lookup"><span data-stu-id="d0efa-138">Access</span></span>         | <span data-ttu-id="d0efa-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d0efa-139">ReadWrite</span></span>                                                          |
| <span data-ttu-id="d0efa-140">Type</span><span class="sxs-lookup"><span data-stu-id="d0efa-140">Type</span></span>           | <span data-ttu-id="d0efa-141">String</span><span class="sxs-lookup"><span data-stu-id="d0efa-141">String</span></span>                                                             |
| <span data-ttu-id="d0efa-142">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d0efa-142">Default</span></span>        | <span data-ttu-id="d0efa-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span><span class="sxs-lookup"><span data-stu-id="d0efa-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span></span>                             |
| <span data-ttu-id="d0efa-144">Système minimal</span><span class="sxs-lookup"><span data-stu-id="d0efa-144">Minimum system</span></span> | <span data-ttu-id="d0efa-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0efa-145">Windows Server 2003</span></span>                                                |



 

## <a name="see-also"></a><span data-ttu-id="d0efa-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0efa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0efa-147">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="d0efa-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
