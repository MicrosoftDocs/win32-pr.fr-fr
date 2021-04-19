---
description: Réénumération et actualisation
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Réénumération et actualisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528157"
---
# <a name="reenumerating-and-refreshing"></a><span data-ttu-id="41a29-103">Réénumération et actualisation</span><span class="sxs-lookup"><span data-stu-id="41a29-103">Reenumerating and Refreshing</span></span>

<span data-ttu-id="41a29-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="41a29-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="41a29-105">L’opération de réénumération Découvre les appareils qui viennent d’être connectés et qui viennent d’être déconnectés.</span><span class="sxs-lookup"><span data-stu-id="41a29-105">The reenumeration operation discovers newly connected and newly disconnected devices.</span></span> <span data-ttu-id="41a29-106">L’opération d’actualisation met à jour les informations de configuration des appareils existants.</span><span class="sxs-lookup"><span data-stu-id="41a29-106">The refresh operation updates the configuration information of existing devices.</span></span>

<span data-ttu-id="41a29-107">**Pour réénumérer les objets du fournisseur de logiciels**</span><span class="sxs-lookup"><span data-stu-id="41a29-107">**To reenumerate software provider objects**</span></span>

-   <span data-ttu-id="41a29-108">Appelez la méthode [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="41a29-108">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method.</span></span> <span data-ttu-id="41a29-109">Cette méthode Découvre tous les disques récemment connectés et déconnectés et les lecteurs de CD-ROM, et garantit que tous les disques possèdent le propriétaire approprié.</span><span class="sxs-lookup"><span data-stu-id="41a29-109">This method discovers all newly connected and disconnected disks and CD-ROM drives, and ensures that all disks have the proper owner.</span></span> <span data-ttu-id="41a29-110">VDS possède des disques bruts ou des disques défaillants ; le fournisseur de base possède des disques de base ; et le fournisseur dynamique possède des disques dynamiques.</span><span class="sxs-lookup"><span data-stu-id="41a29-110">VDS owns raw disks or disks with failures; the basic provider owns basic disks; and the dynamic provider owns dynamic disks.</span></span> <span data-ttu-id="41a29-111">Cette opération peut impliquer l’analyse des bus du sous-système interne et l’attente des délais d’attente.</span><span class="sxs-lookup"><span data-stu-id="41a29-111">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="41a29-112">**Pour réénumérer et actualiser des objets de fournisseur de logiciels**</span><span class="sxs-lookup"><span data-stu-id="41a29-112">**To reenumerate and refresh software provider objects**</span></span>

-   <span data-ttu-id="41a29-113">Appelez la méthode [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) , puis appelez la méthode [**IVdsService :: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) .</span><span class="sxs-lookup"><span data-stu-id="41a29-113">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method and then call the [**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) method.</span></span> <span data-ttu-id="41a29-114">En plus de découvrir les disques récemment connectés et déconnectés et les lecteurs de CD-ROM, cette combinaison de méthodes met à jour toutes les informations sur les disques, les volumes et les plex dans le cache VDS pour les disques qui n’ont pas été récemment connectés ou déconnectés.</span><span class="sxs-lookup"><span data-stu-id="41a29-114">In addition to discovering newly connected and disconnected disks and CD-ROM drives, this combination of methods updates all disk, volume, and plex information in the VDS cache for disks that have not been recently connected or disconnected.</span></span> <span data-ttu-id="41a29-115">Appelez **Refresh** seul pour actualiser les informations sur les propriétés des objets existants dans le cache.</span><span class="sxs-lookup"><span data-stu-id="41a29-115">Call **Refresh** alone to refresh the property information of existing objects in the cache.</span></span> <span data-ttu-id="41a29-116">Cette opération peut impliquer l’analyse des bus du sous-système interne et l’attente des délais d’attente.</span><span class="sxs-lookup"><span data-stu-id="41a29-116">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span> <span data-ttu-id="41a29-117">Notez que VDS met à jour automatiquement le cache chaque fois qu’une modification se produit et déclenche une notification.</span><span class="sxs-lookup"><span data-stu-id="41a29-117">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="41a29-118">En outre, l’appel de l' **actualisation** en réponse à une notification VDS peut entraîner l’envoi d’une boucle infinie de notifications.</span><span class="sxs-lookup"><span data-stu-id="41a29-118">Also, calling **Refresh** in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="41a29-119">Pour ces raisons, l' **actualisation** doit être appelée uniquement lorsqu’il semble que le cache n’est pas mis à jour correctement.</span><span class="sxs-lookup"><span data-stu-id="41a29-119">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

<span data-ttu-id="41a29-120">**Pour réénumérer les sous-systèmes matériels**</span><span class="sxs-lookup"><span data-stu-id="41a29-120">**To reenumerate hardware subsystems**</span></span>

-   <span data-ttu-id="41a29-121">Appelez la méthode [**IVdsHwProvider :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="41a29-121">Call the [**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) method.</span></span> <span data-ttu-id="41a29-122">Selon le fournisseur, cette opération peut impliquer l’envoi de paquets réseau et l’attente de délais d’attente, la nouvelle analyse des bus SCSI et l’attente de délais d’attente, etc.</span><span class="sxs-lookup"><span data-stu-id="41a29-122">Depending on the provider, this operation can involve sending network packets and waiting for time-outs, rescanning SCSI buses and waiting for time-outs, and so on.</span></span>

<span data-ttu-id="41a29-123">**Pour réénumérer les objets du sous-système matériel**</span><span class="sxs-lookup"><span data-stu-id="41a29-123">**To reenumerate hardware subsystem objects**</span></span>

-   <span data-ttu-id="41a29-124">Appelez la méthode [**IVdsSubSystem :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) pour inventorier les objets (généralement des lecteurs) dans le sous-système.</span><span class="sxs-lookup"><span data-stu-id="41a29-124">Call the [**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) method to inventory the objects (typically drives) in the subsystem.</span></span> <span data-ttu-id="41a29-125">Selon le sous-système, cette opération peut impliquer l’analyse des bus du sous-système interne et l’attente des délais d’attente.</span><span class="sxs-lookup"><span data-stu-id="41a29-125">Depending on the subsystem, this operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="41a29-126">**Pour actualiser des sous-systèmes matériels et des objets de sous-système**</span><span class="sxs-lookup"><span data-stu-id="41a29-126">**To refresh hardware subsystems and subsystem objects**</span></span>

-   <span data-ttu-id="41a29-127">Appelez la méthode [**IVdsHwProvider :: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) pour actualiser le cache VDS d’informations sur les sous-systèmes existants qui sont gérés par les fournisseurs de matériel VDS.</span><span class="sxs-lookup"><span data-stu-id="41a29-127">Call the [**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) method to refresh the VDS cache of information about existing subsystems that are managed by VDS hardware providers.</span></span> <span data-ttu-id="41a29-128">Notez que VDS met à jour automatiquement le cache chaque fois qu’une modification se produit et déclenche une notification.</span><span class="sxs-lookup"><span data-stu-id="41a29-128">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="41a29-129">En outre, l’appel de l' [**actualisation**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) en réponse à une notification VDS peut entraîner l’envoi d’une boucle infinie de notifications.</span><span class="sxs-lookup"><span data-stu-id="41a29-129">Also, calling [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="41a29-130">Pour ces raisons, l' **actualisation** doit être appelée uniquement lorsqu’il semble que le cache n’est pas mis à jour correctement.</span><span class="sxs-lookup"><span data-stu-id="41a29-130">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41a29-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41a29-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41a29-132">Utilisation de VDS</span><span class="sxs-lookup"><span data-stu-id="41a29-132">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="41a29-133">**IVdsService :: réénumération**</span><span class="sxs-lookup"><span data-stu-id="41a29-133">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="41a29-134">**IVdsService :: Refresh**</span><span class="sxs-lookup"><span data-stu-id="41a29-134">**IVdsService::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[<span data-ttu-id="41a29-135">**IVdsHwProvider :: réénumération**</span><span class="sxs-lookup"><span data-stu-id="41a29-135">**IVdsHwProvider::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[<span data-ttu-id="41a29-136">**IVdsSubSystem :: réénumération**</span><span class="sxs-lookup"><span data-stu-id="41a29-136">**IVdsSubSystem::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[<span data-ttu-id="41a29-137">**IVdsHwProvider :: Refresh**</span><span class="sxs-lookup"><span data-stu-id="41a29-137">**IVdsHwProvider::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
