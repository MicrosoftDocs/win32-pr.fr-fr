---
description: Contient une liste des ordinateurs serveurs dans le cluster d’applications. Il contient un objet pour chaque serveur.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: Collection ApplicationCluster
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110566"
---
# <a name="applicationcluster-collection"></a><span data-ttu-id="3d530-104">Collection ApplicationCluster</span><span class="sxs-lookup"><span data-stu-id="3d530-104">ApplicationCluster collection</span></span>

<span data-ttu-id="3d530-105">Contient une liste des ordinateurs serveurs dans le cluster d’applications.</span><span class="sxs-lookup"><span data-stu-id="3d530-105">Contains a list of the server computers in the application cluster.</span></span> <span data-ttu-id="3d530-106">Il contient un objet pour chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="3d530-106">It contains an object for each server.</span></span> <span data-ttu-id="3d530-107">Il s’agit d’une collection de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="3d530-107">This is a top-level collection.</span></span>

<span data-ttu-id="3d530-108">Le cluster d’applications est défini dans le cadre du service d’équilibrage de charge des composants (CLB).</span><span class="sxs-lookup"><span data-stu-id="3d530-108">The application cluster is defined for purposes of the component load balancing (CLB) service.</span></span> <span data-ttu-id="3d530-109">Pour l’utilisation de la collection de clusters d’applications, le service CLB doit être installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3d530-109">For the application cluster collection to be used, the CLB service must be installed on the computer.</span></span>

<span data-ttu-id="3d530-110">Vous désignez un routeur dans le cluster d’applications à l’aide de la propriété IsRouter sur l’objet de collection [**LocalComputer**](localcomputer.md) , et vous désignez qu’un composant donné doit faire l’objet d’un équilibrage de charge avec la propriété LoadBalancingSupported sur un objet de collection de [**composants**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="3d530-110">You designate a router in the application cluster with the IsRouter property on the [**LocalComputer**](localcomputer.md) collection object, and you designate that a given component should be load balanced with the LoadBalancingSupported property on a [**Components**](components.md) collection object.</span></span>

<span data-ttu-id="3d530-111">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="3d530-111">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="3d530-112">Membres</span><span class="sxs-lookup"><span data-stu-id="3d530-112">Members</span></span>

<span data-ttu-id="3d530-113">La collection **ApplicationCluster** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3d530-113">The **ApplicationCluster** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="3d530-114">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="3d530-114">Related Collections</span></span>

<span data-ttu-id="3d530-115">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="3d530-115">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="3d530-116">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="3d530-116">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="3d530-117">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="3d530-117">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="3d530-118">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="3d530-118">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="3d530-119">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="3d530-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="3d530-120">**Causes**</span><span class="sxs-lookup"><span data-stu-id="3d530-120">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="3d530-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d530-121">Properties</span></span>

<span data-ttu-id="3d530-122">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="3d530-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="3d530-123">Nom</span><span class="sxs-lookup"><span data-stu-id="3d530-123">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="3d530-124">Nom</span><span class="sxs-lookup"><span data-stu-id="3d530-124">Name</span></span>



| <span data-ttu-id="3d530-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="3d530-125">Entry</span></span> | <span data-ttu-id="3d530-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d530-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d530-127">Description</span><span class="sxs-lookup"><span data-stu-id="3d530-127">Description</span></span>    | <span data-ttu-id="3d530-128">Nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="3d530-128">The name of the server.</span></span> <span data-ttu-id="3d530-129">Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="3d530-129">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3d530-130">Accès</span><span class="sxs-lookup"><span data-stu-id="3d530-130">Access</span></span>         | <span data-ttu-id="3d530-131">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="3d530-131">WriteOnce</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3d530-132">Type</span><span class="sxs-lookup"><span data-stu-id="3d530-132">Type</span></span>           | <span data-ttu-id="3d530-133">String</span><span class="sxs-lookup"><span data-stu-id="3d530-133">String</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3d530-134">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="3d530-134">Default</span></span>        | <span data-ttu-id="3d530-135">« Nouvel ordinateur »</span><span class="sxs-lookup"><span data-stu-id="3d530-135">"New Computer"</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3d530-136">Système minimal</span><span class="sxs-lookup"><span data-stu-id="3d530-136">Minimum system</span></span> | <span data-ttu-id="3d530-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3d530-137">Windows 2000</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="3d530-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d530-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d530-139">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="3d530-139">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
