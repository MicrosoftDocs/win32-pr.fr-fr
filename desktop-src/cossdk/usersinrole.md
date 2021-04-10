---
description: Contient un objet pour chaque utilisateur du rôle auquel la collection est associée.
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: Collection UsersInRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5bf36937d08efd377b48ef251ffb7219c05504f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201040"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="4a918-103">Collection UsersInRole</span><span class="sxs-lookup"><span data-stu-id="4a918-103">UsersInRole collection</span></span>

<span data-ttu-id="4a918-104">Contient un objet pour chaque utilisateur du rôle auquel la collection est associée.</span><span class="sxs-lookup"><span data-stu-id="4a918-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="4a918-105">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="4a918-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4a918-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4a918-106">Members</span></span>

<span data-ttu-id="4a918-107">La collection **UsersInRole** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4a918-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4a918-108">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="4a918-108">Related Collections</span></span>

<span data-ttu-id="4a918-109">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="4a918-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4a918-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4a918-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4a918-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4a918-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4a918-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4a918-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="4a918-113">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="4a918-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4a918-114">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="4a918-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="4a918-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4a918-115">Properties</span></span>

<span data-ttu-id="4a918-116">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="4a918-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4a918-117">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="4a918-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="4a918-118">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="4a918-118">User</span></span>



| <span data-ttu-id="4a918-119">Entrée</span><span class="sxs-lookup"><span data-stu-id="4a918-119">Entry</span></span> | <span data-ttu-id="4a918-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a918-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a918-121">Description</span><span class="sxs-lookup"><span data-stu-id="4a918-121">Description</span></span>    | <span data-ttu-id="4a918-122">Nom d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a918-122">The user name.</span></span> <span data-ttu-id="4a918-123">Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="4a918-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4a918-124">Accès</span><span class="sxs-lookup"><span data-stu-id="4a918-124">Access</span></span>         | <span data-ttu-id="4a918-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="4a918-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="4a918-126">Type</span><span class="sxs-lookup"><span data-stu-id="4a918-126">Type</span></span>           | <span data-ttu-id="4a918-127">String</span><span class="sxs-lookup"><span data-stu-id="4a918-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="4a918-128">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4a918-128">Default</span></span>        | <span data-ttu-id="4a918-129">« Nouvel utilisateur »</span><span class="sxs-lookup"><span data-stu-id="4a918-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="4a918-130">Système minimal</span><span class="sxs-lookup"><span data-stu-id="4a918-130">Minimum system</span></span> | <span data-ttu-id="4a918-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4a918-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="4a918-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a918-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a918-133">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="4a918-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
