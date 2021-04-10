---
description: Récupère des informations sur d’autres collections relatives à la collection à partir de laquelle elle est appelée.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Collection RelatedCollectionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200979"
---
# <a name="relatedcollectioninfo-collection"></a><span data-ttu-id="378e8-103">Collection RelatedCollectionInfo</span><span class="sxs-lookup"><span data-stu-id="378e8-103">RelatedCollectionInfo collection</span></span>

<span data-ttu-id="378e8-104">Récupère des informations sur d’autres collections relatives à la collection à partir de laquelle elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="378e8-104">Retrieves information about other collections related to the collection from which it is called.</span></span> <span data-ttu-id="378e8-105">La collection **RelatedCollectionInfo** est accessible à partir de n’importe quel objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="378e8-105">The **RelatedCollectionInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="378e8-106">La collection **RelatedCollectionInfo** contient un objet pour chaque collection qui est accessible à partir de la collection d’origine.</span><span class="sxs-lookup"><span data-stu-id="378e8-106">The **RelatedCollectionInfo** collection contains one object for each collection that is accessible from the original collection.</span></span> <span data-ttu-id="378e8-107">Les regroupements connexes suivent la hiérarchie de regroupement de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="378e8-107">Related collections follow the Component Services administration tool collection hierarchy.</span></span>

<span data-ttu-id="378e8-108">Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="378e8-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="378e8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="378e8-109">Members</span></span>

<span data-ttu-id="378e8-110">La collection **RelatedCollectionInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="378e8-110">The **RelatedCollectionInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="378e8-111">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="378e8-111">Related Collections</span></span>

<span data-ttu-id="378e8-112">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="378e8-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="378e8-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="378e8-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   <span data-ttu-id="378e8-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="378e8-114">**RelatedCollectionInfo**</span></span>

<span data-ttu-id="378e8-115">Vous pouvez accéder à cette collection à partir de chaque collection.</span><span class="sxs-lookup"><span data-stu-id="378e8-115">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="378e8-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="378e8-116">Properties</span></span>

<span data-ttu-id="378e8-117">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="378e8-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="378e8-118">Nom</span><span class="sxs-lookup"><span data-stu-id="378e8-118">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="378e8-119">Nom</span><span class="sxs-lookup"><span data-stu-id="378e8-119">Name</span></span>



| <span data-ttu-id="378e8-120">Entrée</span><span class="sxs-lookup"><span data-stu-id="378e8-120">Entry</span></span> | <span data-ttu-id="378e8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="378e8-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="378e8-122">Description</span><span class="sxs-lookup"><span data-stu-id="378e8-122">Description</span></span>    | <span data-ttu-id="378e8-123">Nom de la collection associée.</span><span class="sxs-lookup"><span data-stu-id="378e8-123">The name of the related collection.</span></span> <span data-ttu-id="378e8-124">Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="378e8-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="378e8-125">Accès</span><span class="sxs-lookup"><span data-stu-id="378e8-125">Access</span></span>         | <span data-ttu-id="378e8-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="378e8-126">ReadOnly</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="378e8-127">Type</span><span class="sxs-lookup"><span data-stu-id="378e8-127">Type</span></span>           | <span data-ttu-id="378e8-128">String</span><span class="sxs-lookup"><span data-stu-id="378e8-128">String</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="378e8-129">Default</span><span class="sxs-lookup"><span data-stu-id="378e8-129">Default</span></span>        | <span data-ttu-id="378e8-130">None</span><span class="sxs-lookup"><span data-stu-id="378e8-130">None</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="378e8-131">Système minimal</span><span class="sxs-lookup"><span data-stu-id="378e8-131">Minimum system</span></span> | <span data-ttu-id="378e8-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="378e8-132">Windows 2000</span></span>                                                                                                                                                                                               |



 

## <a name="see-also"></a><span data-ttu-id="378e8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="378e8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378e8-134">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="378e8-134">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
