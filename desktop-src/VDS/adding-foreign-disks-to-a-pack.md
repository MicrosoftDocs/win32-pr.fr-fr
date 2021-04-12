---
description: Ajout de disques étrangers à un Pack
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Ajout de disques étrangers à un Pack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320689"
---
# <a name="adding-foreign-disks-to-a-pack"></a><span data-ttu-id="1e91c-103">Ajout de disques étrangers à un Pack</span><span class="sxs-lookup"><span data-stu-id="1e91c-103">Adding Foreign Disks to a Pack</span></span>

<span data-ttu-id="1e91c-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e91c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1e91c-105">Le plus souvent, un disque étranger est un disque dynamique qui est alloué sur un ordinateur et physiquement déplacé vers un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1e91c-105">Most commonly, a foreign disk is a dynamic disk that is allocated on one computer and physically moved to another computer.</span></span> <span data-ttu-id="1e91c-106">Toutefois, tout disque appartenant à un autre Pack que le Pack en ligne est considéré comme un disque étranger qui appartient à un pack de disques étrangers.</span><span class="sxs-lookup"><span data-stu-id="1e91c-106">However, any disk that belongs to a pack other than the online pack is considered to be a foreign disk that belongs to a foreign disk pack.</span></span>

<span data-ttu-id="1e91c-107">Un pack étranger a l' **indicateur \_ \_ étranger PKF VDS** défini dans le membre **ulFlags** de la structure de la [**\_ \_ prop Pack VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) .</span><span class="sxs-lookup"><span data-stu-id="1e91c-107">A foreign pack has the **VDS\_PKF\_FOREIGN** flag set in the **ulFlags** member of the [**VDS\_PACK\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) structure.</span></span> <span data-ttu-id="1e91c-108">Les packs étrangers sont toujours hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1e91c-108">Foreign packs are always offline.</span></span>

<span data-ttu-id="1e91c-109">La procédure suivante décrit comment importer un ou plusieurs disques étrangers.</span><span class="sxs-lookup"><span data-stu-id="1e91c-109">The following procedure describes how to import one or more foreign disks.</span></span>

<span data-ttu-id="1e91c-110">**Pour importer un ou plusieurs disques étrangers**</span><span class="sxs-lookup"><span data-stu-id="1e91c-110">**To import one or more foreign disks**</span></span>

1.  <span data-ttu-id="1e91c-111">Déplacez les disques vers le nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1e91c-111">Move disks to the new computer.</span></span>
2.  <span data-ttu-id="1e91c-112">Sur le nouvel ordinateur, utilisez la méthode [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) pour installer les disques étrangers.</span><span class="sxs-lookup"><span data-stu-id="1e91c-112">On the new computer, use the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method to install the foreign disks.</span></span>
3.  <span data-ttu-id="1e91c-113">Sélectionnez le Pack en ligne à utiliser pour le Pack cible qui reçoit les disques étrangers.</span><span class="sxs-lookup"><span data-stu-id="1e91c-113">Select the online pack to be the target pack that receives the foreign disks.</span></span> <span data-ttu-id="1e91c-114">S’il n’existe aucun Pack en ligne, utilisez la méthode [**IVdsSwProvider :: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) pour créer un nouveau Pack vide.</span><span class="sxs-lookup"><span data-stu-id="1e91c-114">If no online pack exists, use the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a new empty pack.</span></span>
4.  <span data-ttu-id="1e91c-115">Utilisez la méthode [**IVdsPack :: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) pour importer les disques dans le nouveau Pack dynamique.</span><span class="sxs-lookup"><span data-stu-id="1e91c-115">Use the [**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) method to import the disks to the new dynamic pack.</span></span>
5.  <span data-ttu-id="1e91c-116">Utilisez la méthode [**IVdsSwProvider :: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) pour énumérer les packs et [**IVdsPack :: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) pour déterminer quel Pack est maintenant le Pack en ligne.</span><span class="sxs-lookup"><span data-stu-id="1e91c-116">Use the [**IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) method to enumerate the packs and [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) to determine which pack is now the online pack.</span></span>

<span data-ttu-id="1e91c-117">Si vous créez un nouveau Pack cible vide, les disques étrangers ne sont pas réellement migrés vers ce Pack.</span><span class="sxs-lookup"><span data-stu-id="1e91c-117">If you create a new empty target pack, the foreign disks are not actually migrated to that pack.</span></span> <span data-ttu-id="1e91c-118">Au lieu de cela, le Pack étranger est marqué en ligne, l’indicateur de l' **\_ \_ étranger PKF VDS** pour le Pack est effacé (par conséquent, le Pack n’est plus étranger) et le Pack cible que vous avez créé est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1e91c-118">Instead, the foreign pack is marked online, the **VDS\_PKF\_FOREIGN** flag for the pack is cleared (so the pack is no longer foreign), and the target pack that you created is discarded.</span></span>

> [!Note]  
> <span data-ttu-id="1e91c-119">Utilisez la méthode [**IVdsPack :: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) pour ajouter des disques non alloués (disques non revendiqués par un fournisseur) à un Pack.</span><span class="sxs-lookup"><span data-stu-id="1e91c-119">Use the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add unallocated disks—disks not claimed by a provider—to a pack.</span></span> <span data-ttu-id="1e91c-120">Un disque non alloué ne peut pas être étranger.</span><span class="sxs-lookup"><span data-stu-id="1e91c-120">An unallocated disk cannot be foreign.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1e91c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e91c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e91c-122">Utilisation de VDS</span><span class="sxs-lookup"><span data-stu-id="1e91c-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="1e91c-123">**IVdsService :: réénumération**</span><span class="sxs-lookup"><span data-stu-id="1e91c-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="1e91c-124">**IVdsSwProvider::CreatePack**</span><span class="sxs-lookup"><span data-stu-id="1e91c-124">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="1e91c-125">**IVdsPack::MigrateDisks**</span><span class="sxs-lookup"><span data-stu-id="1e91c-125">**IVdsPack::MigrateDisks**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[<span data-ttu-id="1e91c-126">**IVdsPack::AddDisk**</span><span class="sxs-lookup"><span data-stu-id="1e91c-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
