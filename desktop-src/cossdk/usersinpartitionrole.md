---
description: Contient un objet pour chaque utilisateur du rôle auquel la collection est associée.
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Collection UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: fce1577636a7b2e678bdade9c32f706c7ccbf158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110891"
---
# <a name="usersinpartitionrole-collection"></a><span data-ttu-id="76784-103">Collection UsersInPartitionRole</span><span class="sxs-lookup"><span data-stu-id="76784-103">UsersInPartitionRole collection</span></span>

<span data-ttu-id="76784-104">Contient un objet pour chaque utilisateur du rôle auquel la collection est associée.</span><span class="sxs-lookup"><span data-stu-id="76784-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="76784-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="76784-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="76784-106">Membres</span><span class="sxs-lookup"><span data-stu-id="76784-106">Members</span></span>

<span data-ttu-id="76784-107">La collection **UsersInPartitionRole** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="76784-107">The **UsersInPartitionRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="76784-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="76784-108">Related Collections</span></span>

<span data-ttu-id="76784-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="76784-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="76784-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="76784-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="76784-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="76784-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="76784-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="76784-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="76784-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="76784-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="76784-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="76784-114">**RolesForPartition**</span></span>](rolesforpartition.md)

## <a name="properties"></a><span data-ttu-id="76784-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76784-115">Properties</span></span>

<span data-ttu-id="76784-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="76784-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="76784-117">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="76784-117">User</span></span>](#usersinpartitionrole-collection)

### <a name="user"></a><span data-ttu-id="76784-118">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="76784-118">User</span></span>



| <span data-ttu-id="76784-119">Entrée</span><span class="sxs-lookup"><span data-stu-id="76784-119">Entry</span></span> | <span data-ttu-id="76784-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="76784-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76784-121">Description</span><span class="sxs-lookup"><span data-stu-id="76784-121">Description</span></span>    | <span data-ttu-id="76784-122">Nom d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76784-122">The user name.</span></span> <span data-ttu-id="76784-123">Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="76784-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="76784-124">Accès</span><span class="sxs-lookup"><span data-stu-id="76784-124">Access</span></span>         | <span data-ttu-id="76784-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="76784-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="76784-126">Type</span><span class="sxs-lookup"><span data-stu-id="76784-126">Type</span></span>           | <span data-ttu-id="76784-127">String</span><span class="sxs-lookup"><span data-stu-id="76784-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="76784-128">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="76784-128">Default</span></span>        | <span data-ttu-id="76784-129">« Nouvel utilisateur »</span><span class="sxs-lookup"><span data-stu-id="76784-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="76784-130">Système minimal</span><span class="sxs-lookup"><span data-stu-id="76784-130">Minimum system</span></span> | <span data-ttu-id="76784-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76784-131">Windows Server 2003</span></span>                                                                                                                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="76784-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76784-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76784-133">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="76784-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
