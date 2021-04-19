---
description: Contient un objet pour chaque rôle assigné à la méthode à laquelle la collection est associée. Les rôles doivent déjà être affectés au niveau de l’application.
ms.assetid: 3a086163-e367-4dd1-996b-821b3e1111b2
title: Collection RolesForMethod
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForMethod
api_type:
- COM
api_location: ''
ms.openlocfilehash: c73ba5f7a14a5efc6711a65f211cd036e1c2a14d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514753"
---
# <a name="rolesformethod-collection"></a><span data-ttu-id="4b780-104">Collection RolesForMethod</span><span class="sxs-lookup"><span data-stu-id="4b780-104">RolesForMethod collection</span></span>

<span data-ttu-id="4b780-105">Contient un objet pour chaque rôle assigné à la méthode à laquelle la collection est associée.</span><span class="sxs-lookup"><span data-stu-id="4b780-105">Contains an object for each role assigned to the method to which the collection is related.</span></span> <span data-ttu-id="4b780-106">Les rôles doivent déjà être affectés au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="4b780-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="4b780-107">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="4b780-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4b780-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4b780-108">Members</span></span>

<span data-ttu-id="4b780-109">La collection **RolesForMethod** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4b780-109">The **RolesForMethod** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4b780-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="4b780-110">Related Collections</span></span>

<span data-ttu-id="4b780-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="4b780-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4b780-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4b780-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4b780-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4b780-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4b780-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4b780-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="4b780-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="4b780-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4b780-116">**MethodsForInterface**</span><span class="sxs-lookup"><span data-stu-id="4b780-116">**MethodsForInterface**</span></span>](methodsforinterface.md)

## <a name="properties"></a><span data-ttu-id="4b780-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b780-117">Properties</span></span>

<span data-ttu-id="4b780-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="4b780-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4b780-119">Nom</span><span class="sxs-lookup"><span data-stu-id="4b780-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="4b780-120">Nom</span><span class="sxs-lookup"><span data-stu-id="4b780-120">Name</span></span>



| <span data-ttu-id="4b780-121">Entrée</span><span class="sxs-lookup"><span data-stu-id="4b780-121">Entry</span></span> | <span data-ttu-id="4b780-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b780-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b780-123">Description</span><span class="sxs-lookup"><span data-stu-id="4b780-123">Description</span></span>    | <span data-ttu-id="4b780-124">Nom du rôle.</span><span class="sxs-lookup"><span data-stu-id="4b780-124">The role name.</span></span> <span data-ttu-id="4b780-125">Doit déjà être un rôle affecté à l’application (qui apparaît dans la collection de rôles).</span><span class="sxs-lookup"><span data-stu-id="4b780-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="4b780-126">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="4b780-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4b780-127">Accès</span><span class="sxs-lookup"><span data-stu-id="4b780-127">Access</span></span>         | <span data-ttu-id="4b780-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="4b780-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="4b780-129">Type</span><span class="sxs-lookup"><span data-stu-id="4b780-129">Type</span></span>           | <span data-ttu-id="4b780-130">String</span><span class="sxs-lookup"><span data-stu-id="4b780-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4b780-131">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4b780-131">Default</span></span>        | <span data-ttu-id="4b780-132">« Nouveau rôle »</span><span class="sxs-lookup"><span data-stu-id="4b780-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="4b780-133">Système minimal</span><span class="sxs-lookup"><span data-stu-id="4b780-133">Minimum system</span></span> | <span data-ttu-id="4b780-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4b780-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="4b780-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b780-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b780-136">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="4b780-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
