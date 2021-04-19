---
description: Contient un objet pour chaque rôle assigné au composant auquel la collection est associée. Les rôles doivent déjà être affectés au niveau de l’application.
ms.assetid: c253c72f-908e-4990-ac1a-27e32c99283c
title: Collection RolesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 701921f8f88656753857707c045da0c8e231e1a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536947"
---
# <a name="rolesforcomponent-collection"></a><span data-ttu-id="2010f-104">Collection RolesForComponent</span><span class="sxs-lookup"><span data-stu-id="2010f-104">RolesForComponent collection</span></span>

<span data-ttu-id="2010f-105">Contient un objet pour chaque rôle assigné au composant auquel la collection est associée.</span><span class="sxs-lookup"><span data-stu-id="2010f-105">Contains an object for each role assigned to the component to which the collection is related.</span></span> <span data-ttu-id="2010f-106">Les rôles doivent déjà être affectés au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="2010f-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="2010f-107">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="2010f-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="2010f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2010f-108">Members</span></span>

<span data-ttu-id="2010f-109">La collection **RolesForComponent** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2010f-109">The **RolesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="2010f-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="2010f-110">Related Collections</span></span>

<span data-ttu-id="2010f-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="2010f-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="2010f-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2010f-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="2010f-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="2010f-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="2010f-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="2010f-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="2010f-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="2010f-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="2010f-116">**Composants**</span><span class="sxs-lookup"><span data-stu-id="2010f-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="2010f-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2010f-117">Properties</span></span>

<span data-ttu-id="2010f-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="2010f-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="2010f-119">Nom</span><span class="sxs-lookup"><span data-stu-id="2010f-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="2010f-120">Nom</span><span class="sxs-lookup"><span data-stu-id="2010f-120">Name</span></span>



| <span data-ttu-id="2010f-121">Entrée</span><span class="sxs-lookup"><span data-stu-id="2010f-121">Entry</span></span> | <span data-ttu-id="2010f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2010f-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2010f-123">Description</span><span class="sxs-lookup"><span data-stu-id="2010f-123">Description</span></span>    | <span data-ttu-id="2010f-124">Nom du rôle.</span><span class="sxs-lookup"><span data-stu-id="2010f-124">The role name.</span></span> <span data-ttu-id="2010f-125">Doit déjà être un rôle affecté à l’application (qui apparaît dans la collection de rôles).</span><span class="sxs-lookup"><span data-stu-id="2010f-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="2010f-126">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="2010f-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="2010f-127">Accès</span><span class="sxs-lookup"><span data-stu-id="2010f-127">Access</span></span>         | <span data-ttu-id="2010f-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="2010f-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2010f-129">Type</span><span class="sxs-lookup"><span data-stu-id="2010f-129">Type</span></span>           | <span data-ttu-id="2010f-130">String</span><span class="sxs-lookup"><span data-stu-id="2010f-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2010f-131">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="2010f-131">Default</span></span>        | <span data-ttu-id="2010f-132">« Nouveau rôle »</span><span class="sxs-lookup"><span data-stu-id="2010f-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2010f-133">Système minimal</span><span class="sxs-lookup"><span data-stu-id="2010f-133">Minimum system</span></span> | <span data-ttu-id="2010f-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2010f-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="2010f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2010f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2010f-136">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="2010f-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
