---
description: Contient les collections de niveau supérieur dans le catalogue.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Collection racine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516368"
---
# <a name="root-collection"></a><span data-ttu-id="0c2e4-103">Collection racine</span><span class="sxs-lookup"><span data-stu-id="0c2e4-103">Root collection</span></span>

<span data-ttu-id="0c2e4-104">Contient les collections de niveau supérieur dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-104">Contains the top-level collections in the catalog.</span></span> <span data-ttu-id="0c2e4-105">Il ne contient pas d’objets [**COMAdminCatalogObject**](comadmincatalogobject.md) ou ne prend en charge aucune propriété.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-105">It does not contain any [**COMAdminCatalogObject**](comadmincatalogobject.md) objects or support any properties.</span></span>

<span data-ttu-id="0c2e4-106">La collection **racine** ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0c2e4-106">The **Root** collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="0c2e4-107">Vous ne pouvez pas accéder à la collection **racine** à partir d’une collection.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-107">You cannot navigate to the **Root** collection from any collection.</span></span>

## <a name="members"></a><span data-ttu-id="0c2e4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0c2e4-108">Members</span></span>

<span data-ttu-id="0c2e4-109">La collection **racine** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-109">The **Root** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="0c2e4-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="0c2e4-110">Related Collections</span></span>

<span data-ttu-id="0c2e4-111">Voici les collections de niveau supérieur dans le catalogue :</span><span class="sxs-lookup"><span data-stu-id="0c2e4-111">The following are the top-level collections in the catalog:</span></span>

-   [<span data-ttu-id="0c2e4-112">**ApplicationCluster**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-112">**ApplicationCluster**</span></span>](applicationcluster.md)
-   [<span data-ttu-id="0c2e4-113">**ApplicationInstances**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-113">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="0c2e4-114">**Applications**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="0c2e4-115">**ComputerList**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-115">**ComputerList**</span></span>](computerlist.md)
-   [<span data-ttu-id="0c2e4-116">**DCOMProtocols**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-116">**DCOMProtocols**</span></span>](dcomprotocols.md)
-   [<span data-ttu-id="0c2e4-117">**EventClassesForIID**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-117">**EventClassesForIID**</span></span>](eventclassesforiid.md)
-   [<span data-ttu-id="0c2e4-118">**FilesForImport**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-118">**FilesForImport**</span></span>](filesforimport.md)
-   [<span data-ttu-id="0c2e4-119">**InprocServers**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-119">**InprocServers**</span></span>](inprocservers.md)
-   [<span data-ttu-id="0c2e4-120">**LegacyServers**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-120">**LegacyServers**</span></span>](legacyservers.md)
-   [<span data-ttu-id="0c2e4-121">**LocalComputer**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-121">**LocalComputer**</span></span>](localcomputer.md)
-   [<span data-ttu-id="0c2e4-122">**Partitions**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-122">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="0c2e4-123">**PartitionUsers**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-123">**PartitionUsers**</span></span>](partitionusers.md)
-   [<span data-ttu-id="0c2e4-124">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-124">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="0c2e4-125">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-125">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="0c2e4-126">**TransientSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-126">**TransientSubscriptions**</span></span>](transientsubscriptions.md)
-   [<span data-ttu-id="0c2e4-127">**WOWInprocServers**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-127">**WOWInprocServers**</span></span>](wowinprocservers.md)
-   [<span data-ttu-id="0c2e4-128">**WOWLegacyServers**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-128">**WOWLegacyServers**</span></span>](wowlegacyservers.md)

## <a name="see-also"></a><span data-ttu-id="0c2e4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c2e4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c2e4-130">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="0c2e4-130">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
