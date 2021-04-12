---
description: Les administrateurs peuvent utiliser COM+ pour créer et configurer des partitions COM+ par programmation.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Création et configuration de partitions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523559"
---
# <a name="creating-and-configuring-com-partitions"></a><span data-ttu-id="a19e2-103">Création et configuration de partitions COM+</span><span class="sxs-lookup"><span data-stu-id="a19e2-103">Creating and Configuring COM+ Partitions</span></span>

<span data-ttu-id="a19e2-104">Les administrateurs peuvent utiliser COM+ pour créer et configurer des partitions COM+ par programmation.</span><span class="sxs-lookup"><span data-stu-id="a19e2-104">Administrators can use COM+ to programmatically create and configure COM+ partitions.</span></span> <span data-ttu-id="a19e2-105">En fait, toutes les tâches de création et de configuration qu’un administrateur peut effectuer à partir des services de composants ou les outils d’administration utilisateurs et ordinateurs Active Directory peuvent être effectuées à l’aide de regroupements, d’objets et d’interfaces COM+ ou par le biais de l’interface de système Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="a19e2-105">In fact, all creation and configuration tasks that an administrator can do from the Component Services or the Active Directory Users and Computers administrative tools can be done by using COM+ collections, objects, and interfaces or through the Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="a19e2-106">**Windows XP :** La possibilité de créer, de configurer ou de déléguer des partitions COM+ n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a19e2-106">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="a19e2-107">La partition globale est la seule partition COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="a19e2-107">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="a19e2-108">\* \* Windows 2000 : \* \* le service partitions COM+ n’est pas disponible dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a19e2-108">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

> [!Note]  
> <span data-ttu-id="a19e2-109">Le service partitions COM+ n’est pas activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="a19e2-109">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="a19e2-110">Pour utiliser le service partitions COM+, vous devez l’activer par le biais de l’outil d’administration Services de composants ou en modifiant la propriété PartitionsEnabled de la collection [**LocalComputer**](localcomputer.md) sur true.</span><span class="sxs-lookup"><span data-stu-id="a19e2-110">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="a19e2-111">Pour accomplir des tâches liées aux partitions, COM+ fournit les éléments de programmation suivants :</span><span class="sxs-lookup"><span data-stu-id="a19e2-111">To accomplish partition-related tasks, COM+ provides the following programming elements:</span></span>

-   <span data-ttu-id="a19e2-112">Méthodes et propriétés de l’interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) sur la classe [**COMAdminCatalog**](comadmincatalog.md) :</span><span class="sxs-lookup"><span data-stu-id="a19e2-112">Methods and properties of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface on the [**COMAdminCatalog**](comadmincatalog.md) class:</span></span>
    -   <span data-ttu-id="a19e2-113">Propriété [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-113">[**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) property.</span></span>
    -   <span data-ttu-id="a19e2-114">Propriété [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-114">[**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) property.</span></span>
    -   <span data-ttu-id="a19e2-115">Propriété [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-115">[**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) property.</span></span>
    -   <span data-ttu-id="a19e2-116">Méthode [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-116">[**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>
    -   <span data-ttu-id="a19e2-117">Méthode [**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-117">[**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) method.</span></span>
    -   <span data-ttu-id="a19e2-118">Méthode [**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-118">[**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) method.</span></span>
    -   <span data-ttu-id="a19e2-119">Propriété [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-119">[**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) property.</span></span>
-   <span data-ttu-id="a19e2-120">Ensemble d’objets COM+ pour créer et gérer des partitions dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a19e2-120">A set of COM+ objects for creating and managing partitions in Active Directory.</span></span>
-   <span data-ttu-id="a19e2-121">Une clé de registre COM+, **PartitionCache**, pour la modification de la taille du cache de partition.</span><span class="sxs-lookup"><span data-stu-id="a19e2-121">A COM+ registry key, **PartitionCache**, for changing the partition cache size.</span></span>
-   <span data-ttu-id="a19e2-122">Ensemble de [regroupements d’administration com+](com--administration-collections.md)liés aux partitions :</span><span class="sxs-lookup"><span data-stu-id="a19e2-122">A set of partitions-related [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="a19e2-123">Collection [**partitions**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-123">[**Partitions**](partitions.md) collection.</span></span>
    -   <span data-ttu-id="a19e2-124">Collection [**PartitionUsers**](partitionusers.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-124">[**PartitionUsers**](partitionusers.md) collection.</span></span>
    -   <span data-ttu-id="a19e2-125">Collection [**RolesForPartition**](rolesforpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-125">[**RolesForPartition**](rolesforpartition.md) collection.</span></span>
    -   <span data-ttu-id="a19e2-126">Collection [**UsersInPartitionRole**](usersinpartitionrole.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-126">[**UsersInPartitionRole**](usersinpartitionrole.md) collection.</span></span>
-   <span data-ttu-id="a19e2-127">Propriétés d’autres [regroupements d’administration com+](com--administration-collections.md):</span><span class="sxs-lookup"><span data-stu-id="a19e2-127">Properties of other [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="a19e2-128">Propriété PartitionID sur la collection [**ApplicationInstances**](applicationinstances.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-128">PartitionID property on the [**ApplicationInstances**](applicationinstances.md) collection.</span></span>
    -   <span data-ttu-id="a19e2-129">Propriété AppPartitionID sur la collection d' [**applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-129">AppPartitionID property on the [**Applications**](applications.md) collection.</span></span>
    -   <span data-ttu-id="a19e2-130">Propriétés PartitionDescription, PartitionID et PartitionName sur la collection [**FilesForImport**](filesforimport.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-130">PartitionDescription, PartitionID, and PartitionName properties on the [**FilesForImport**](filesforimport.md) collection.</span></span>
    -   <span data-ttu-id="a19e2-131">Propriétés DSPartitionLookupEnabled, LocalPartitionLookupEnabled et PartitionsEnabled sur la collection [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-131">DSPartitionLookupEnabled, LocalPartitionLookupEnabled, and PartitionsEnabled properties on the [**LocalComputer**](localcomputer.md) collection.</span></span>
    -   <span data-ttu-id="a19e2-132">Propriétés EventClassPartitionID et SubscriberPartitionID sur la collection [**SubscriptionsForComponent**](subscriptionsforcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-132">EventClassPartitionID and SubscriberPartitionID properties on the [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>
    -   <span data-ttu-id="a19e2-133">Propriétés EventClassPartitionID et SubscriberPartitionID sur la collection [**TransientSubscriptions**](transientsubscriptions.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e2-133">EventClassPartitionID and SubscriberPartitionID properties on the [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a19e2-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a19e2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a19e2-135">Collecte des métriques de partition</span><span class="sxs-lookup"><span data-stu-id="a19e2-135">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="a19e2-136">Configuration du cache de partition</span><span class="sxs-lookup"><span data-stu-id="a19e2-136">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="a19e2-137">Regroupement d’applications en partitions</span><span class="sxs-lookup"><span data-stu-id="a19e2-137">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="a19e2-138">Gestion des partitions locales</span><span class="sxs-lookup"><span data-stu-id="a19e2-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="a19e2-139">Gestion des partitions dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="a19e2-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="a19e2-140">Définition des droits d’administration pour une partition</span><span class="sxs-lookup"><span data-stu-id="a19e2-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



