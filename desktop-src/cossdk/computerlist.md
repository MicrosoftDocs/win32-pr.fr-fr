---
description: Contient la liste des ordinateurs figurant dans le dossier ordinateurs de l’outil d’administration Services de composants. Il contient un objet pour chaque ordinateur.
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: Collection ComputerList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483224"
---
# <a name="computerlist-collection"></a><span data-ttu-id="fa030-104">Collection ComputerList</span><span class="sxs-lookup"><span data-stu-id="fa030-104">ComputerList collection</span></span>

<span data-ttu-id="fa030-105">Contient la liste des ordinateurs figurant dans le dossier **ordinateurs** de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="fa030-105">Contains a list of the computers in the **Computers** folder of the Component Services administration tool.</span></span> <span data-ttu-id="fa030-106">Il contient un objet pour chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fa030-106">It contains an object for each computer.</span></span>

<span data-ttu-id="fa030-107">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fa030-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="fa030-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fa030-108">Members</span></span>

<span data-ttu-id="fa030-109">La collection **ComputerList** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fa030-109">The **ComputerList** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="fa030-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="fa030-110">Related Collections</span></span>

<span data-ttu-id="fa030-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="fa030-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="fa030-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fa030-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="fa030-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="fa030-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="fa030-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="fa030-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="fa030-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="fa030-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="fa030-116">**Causes**</span><span class="sxs-lookup"><span data-stu-id="fa030-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="fa030-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa030-117">Properties</span></span>

<span data-ttu-id="fa030-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="fa030-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="fa030-119">Nom</span><span class="sxs-lookup"><span data-stu-id="fa030-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="fa030-120">Nom</span><span class="sxs-lookup"><span data-stu-id="fa030-120">Name</span></span>



| <span data-ttu-id="fa030-121">Entrée</span><span class="sxs-lookup"><span data-stu-id="fa030-121">Entry</span></span> | <span data-ttu-id="fa030-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa030-122">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa030-123">Description</span><span class="sxs-lookup"><span data-stu-id="fa030-123">Description</span></span>    | <span data-ttu-id="fa030-124">Nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fa030-124">The name of the computer.</span></span> <span data-ttu-id="fa030-125">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="fa030-125">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fa030-126">Accès</span><span class="sxs-lookup"><span data-stu-id="fa030-126">Access</span></span>         | <span data-ttu-id="fa030-127">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fa030-127">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fa030-128">Type</span><span class="sxs-lookup"><span data-stu-id="fa030-128">Type</span></span>           | <span data-ttu-id="fa030-129">String</span><span class="sxs-lookup"><span data-stu-id="fa030-129">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fa030-130">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fa030-130">Default</span></span>        | <span data-ttu-id="fa030-131">« Nouvel ordinateur »</span><span class="sxs-lookup"><span data-stu-id="fa030-131">"New Computer"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fa030-132">Système minimal</span><span class="sxs-lookup"><span data-stu-id="fa030-132">Minimum system</span></span> | <span data-ttu-id="fa030-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fa030-133">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="fa030-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa030-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa030-135">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="fa030-135">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
