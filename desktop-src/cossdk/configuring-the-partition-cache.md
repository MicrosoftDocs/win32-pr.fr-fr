---
description: La fonctionnalité partitions COM+ comprend un cache de partition. Ce cache stocke les mappages d’utilisateur à partition et est conçu pour éviter un accès Active Directory répétitif.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configuration du cache de partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543447"
---
# <a name="configuring-the-partition-cache"></a><span data-ttu-id="74dcc-104">Configuration du cache de partition</span><span class="sxs-lookup"><span data-stu-id="74dcc-104">Configuring the Partition Cache</span></span>

<span data-ttu-id="74dcc-105">La fonctionnalité partitions COM+ comprend un cache de partition.</span><span class="sxs-lookup"><span data-stu-id="74dcc-105">The COM+ partitions feature includes a partition cache.</span></span> <span data-ttu-id="74dcc-106">Ce cache stocke les mappages d’utilisateur à partition et est conçu pour éviter un accès Active Directory répétitif.</span><span class="sxs-lookup"><span data-stu-id="74dcc-106">This cache stores user-to-partition mappings and is designed to avoid repetitive Active Directory access.</span></span>

## <a name="changing-cache-size"></a><span data-ttu-id="74dcc-107">Modification de la taille du cache</span><span class="sxs-lookup"><span data-stu-id="74dcc-107">Changing Cache Size</span></span>

<span data-ttu-id="74dcc-108">Le cache de partition est constitué de trois tables, dont la taille peut être modifiée pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="74dcc-108">The partition cache consists of three tables, whose size can be modified to enhance performance.</span></span> <span data-ttu-id="74dcc-109">Ces tables comportent le nombre d’entrées de SID dans le cache, le nombre d’entrées d’UO dans le cache et le nombre d’entrées de partition dans le cache.</span><span class="sxs-lookup"><span data-stu-id="74dcc-109">These tables consist of the number of SID entries in the cache, the number of OU entries in the cache, and the number of partition entries in the cache.</span></span>

<span data-ttu-id="74dcc-110">Pour modifier ces tailles de table, les administrateurs peuvent modifier les valeurs d’une clé de registre.</span><span class="sxs-lookup"><span data-stu-id="74dcc-110">To change these table sizes, administrators can modify the values of a registry key.</span></span> <span data-ttu-id="74dcc-111">La clé de Registre et ses valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="74dcc-111">The registry key and its values are as follows:</span></span>

<span data-ttu-id="74dcc-112">**HKLM \\ Software \\ Microsoft \\ COM3 \\ PartitionCache**</span><span class="sxs-lookup"><span data-stu-id="74dcc-112">**HKLM\\SOFTWARE\\Microsoft\\COM3\\PartitionCache**</span></span>



| <span data-ttu-id="74dcc-113">Valeurs de clé</span><span class="sxs-lookup"><span data-stu-id="74dcc-113">Key values</span></span>                         | <span data-ttu-id="74dcc-114">Description</span><span class="sxs-lookup"><span data-stu-id="74dcc-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74dcc-115">**NumSidEntries**</span><span class="sxs-lookup"><span data-stu-id="74dcc-115">**NumSidEntries**</span></span><br/>       | <span data-ttu-id="74dcc-116">Contient la \_ valeur reg DWORD pour le nombre d’entrées sid dans le cache (valeur par défaut = 512).</span><span class="sxs-lookup"><span data-stu-id="74dcc-116">Contains the REG\_DWORD value for the number of SID entries in the cache (default=512).</span></span> <span data-ttu-id="74dcc-117">Cette valeur doit être définie sur une valeur supérieure au nombre d’identités uniques qu’un ordinateur traitera dans la fenêtre de temps d’invalidation du cache.</span><span class="sxs-lookup"><span data-stu-id="74dcc-117">This value should be set to a value greater than the number of unique identities that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="74dcc-118">**NumNameEntries**</span><span class="sxs-lookup"><span data-stu-id="74dcc-118">**NumNameEntries**</span></span><br/>      | <span data-ttu-id="74dcc-119">Contient la \_ valeur reg DWORD pour le nombre d’entrées de nom d’unité d’organisation dans le cache (valeur par défaut = 64).</span><span class="sxs-lookup"><span data-stu-id="74dcc-119">Contains the REG\_DWORD value for the number of OU name entries in the cache (default=64).</span></span> <span data-ttu-id="74dcc-120">Cette valeur doit être définie sur une valeur supérieure au nombre de noms d’UO uniques qu’un ordinateur traitera dans la fenêtre de temps d’invalidation du cache.</span><span class="sxs-lookup"><span data-stu-id="74dcc-120">This value should be set to a value greater than the number of unique OU names that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="74dcc-121">**NumPartitionEntries**</span><span class="sxs-lookup"><span data-stu-id="74dcc-121">**NumPartitionEntries**</span></span><br/> | <span data-ttu-id="74dcc-122">Contient la \_ valeur reg DWORD pour le nombre d’entrées de partition dans le cache (valeur par défaut = 1 024).</span><span class="sxs-lookup"><span data-stu-id="74dcc-122">Contains the REG\_DWORD value for the number of partition entries in the cache (default=1024).</span></span><br/> <span data-ttu-id="74dcc-123">Dans la fenêtre de temps d’invalidation du cache, la valeur DWORD doit être définie sur un nombre supérieur au nombre de partitions uniques qu’un ordinateur doit traiter.</span><span class="sxs-lookup"><span data-stu-id="74dcc-123">In the cache invalidation time window, the DWORD value should be set to a number greater than the number of unique partitions that a machine will be servicing.</span></span> <span data-ttu-id="74dcc-124">Cela est dû au fait que le contexte d’un composant peut inclure un ID de partition pour une partition qui ne réside pas sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="74dcc-124">This is because a component's context can include a partition ID for a partition that does not reside on that machine.</span></span> <br/> |
| <span data-ttu-id="74dcc-125">**EntryExpiration**</span><span class="sxs-lookup"><span data-stu-id="74dcc-125">**EntryExpiration**</span></span><br/>     | <span data-ttu-id="74dcc-126">Contient la \_ valeur reg DWORD pour le nombre de cycles (chaque graduation = ~ 7 minutes) jusqu’à ce qu’une entrée de cache devienne non valide (valeur par défaut = 4 (environ 28 minutes)).</span><span class="sxs-lookup"><span data-stu-id="74dcc-126">Contains the REG\_DWORD value for the tick count (each tick = ~7 minutes) until a cache entry becomes invalid (default=4 (~28 minutes)).</span></span><br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a><span data-ttu-id="74dcc-127">Vidage du cache</span><span class="sxs-lookup"><span data-stu-id="74dcc-127">Flushing the Cache</span></span>

<span data-ttu-id="74dcc-128">Étant donné que COM+ met en cache la partition par défaut pour les utilisateurs, vous souhaiterez peut-être appeler cette méthode après avoir modifié la partition par défaut d’un utilisateur dans la Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74dcc-128">Because COM+ caches the default partition for users, you might want to call this method after changing the default partition for a user in the Active Directory.</span></span> <span data-ttu-id="74dcc-129">Les administrateurs peuvent effectuer cette opération par programme en appelant la méthode [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="74dcc-129">Administrators can do this programmatically by calling the [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74dcc-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74dcc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74dcc-131">Collecte des métriques de partition</span><span class="sxs-lookup"><span data-stu-id="74dcc-131">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="74dcc-132">Regroupement d’applications en partitions</span><span class="sxs-lookup"><span data-stu-id="74dcc-132">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="74dcc-133">Gestion des partitions locales</span><span class="sxs-lookup"><span data-stu-id="74dcc-133">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="74dcc-134">Gestion des partitions dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="74dcc-134">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="74dcc-135">Définition des droits d’administration pour une partition</span><span class="sxs-lookup"><span data-stu-id="74dcc-135">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




