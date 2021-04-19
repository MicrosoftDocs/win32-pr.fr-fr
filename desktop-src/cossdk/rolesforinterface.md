---
description: Contient un objet pour chaque rôle assigné à l’interface à laquelle la collection est associée. Les rôles doivent déjà être affectés au niveau de l’application.
ms.assetid: f5c1dc9a-13da-4504-a244-4ce8058240b8
title: Collection RolesForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60c52e3cb48adc0ed52ef10bd9e0a73e716fabfc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513126"
---
# <a name="rolesforinterface-collection"></a><span data-ttu-id="b1622-104">Collection RolesForInterface</span><span class="sxs-lookup"><span data-stu-id="b1622-104">RolesForInterface collection</span></span>

<span data-ttu-id="b1622-105">Contient un objet pour chaque rôle assigné à l’interface à laquelle la collection est associée.</span><span class="sxs-lookup"><span data-stu-id="b1622-105">Contains an object for each role assigned to the interface to which the collection is related.</span></span> <span data-ttu-id="b1622-106">Les rôles doivent déjà être affectés au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="b1622-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="b1622-107">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b1622-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b1622-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b1622-108">Members</span></span>

<span data-ttu-id="b1622-109">La collection **RolesForInterface** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b1622-109">The **RolesForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b1622-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="b1622-110">Related Collections</span></span>

<span data-ttu-id="b1622-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="b1622-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b1622-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b1622-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b1622-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b1622-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b1622-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b1622-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b1622-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="b1622-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b1622-116">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="b1622-116">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="b1622-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b1622-117">Properties</span></span>

<span data-ttu-id="b1622-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="b1622-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b1622-119">Nom</span><span class="sxs-lookup"><span data-stu-id="b1622-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="b1622-120">Nom</span><span class="sxs-lookup"><span data-stu-id="b1622-120">Name</span></span>



| <span data-ttu-id="b1622-121">Entrée</span><span class="sxs-lookup"><span data-stu-id="b1622-121">Entry</span></span> | <span data-ttu-id="b1622-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1622-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1622-123">Description</span><span class="sxs-lookup"><span data-stu-id="b1622-123">Description</span></span>    | <span data-ttu-id="b1622-124">Nom du rôle.</span><span class="sxs-lookup"><span data-stu-id="b1622-124">The role name.</span></span> <span data-ttu-id="b1622-125">Doit déjà être un rôle affecté à l’application (qui apparaît dans la collection de rôles).</span><span class="sxs-lookup"><span data-stu-id="b1622-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="b1622-126">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="b1622-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b1622-127">Accès</span><span class="sxs-lookup"><span data-stu-id="b1622-127">Access</span></span>         | <span data-ttu-id="b1622-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b1622-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b1622-129">Type</span><span class="sxs-lookup"><span data-stu-id="b1622-129">Type</span></span>           | <span data-ttu-id="b1622-130">String</span><span class="sxs-lookup"><span data-stu-id="b1622-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b1622-131">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b1622-131">Default</span></span>        | <span data-ttu-id="b1622-132">« Nouveau rôle »</span><span class="sxs-lookup"><span data-stu-id="b1622-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b1622-133">Système minimal</span><span class="sxs-lookup"><span data-stu-id="b1622-133">Minimum system</span></span> | <span data-ttu-id="b1622-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1622-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="b1622-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1622-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1622-136">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="b1622-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
