---
description: Cette section fournit un glossaire des termes techniques utilisés dans la documentation du service de disque virtuel (VDS).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossaire du service de disque virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc8804f1aea832f59fcbcab65423e92e134939f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952093"
---
# <a name="virtual-disk-service-glossary"></a><span data-ttu-id="66111-103">Glossaire du service de disque virtuel</span><span class="sxs-lookup"><span data-stu-id="66111-103">Virtual Disk Service Glossary</span></span>

<span data-ttu-id="66111-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66111-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="66111-105">Cette section fournit un glossaire des termes techniques utilisés dans la documentation du service de disque virtuel (VDS).</span><span class="sxs-lookup"><span data-stu-id="66111-105">This section provides a glossary of technical terms used in the Virtual Disk Service (VDS) documentation.</span></span>

<dl> <dt>

<span data-ttu-id="66111-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configuration automatique**</span><span class="sxs-lookup"><span data-stu-id="66111-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic configuration**</span></span>
</dt> <dd>

<span data-ttu-id="66111-107">Fournisseur RAID matériel fournissant un ensemble de règles pour le choix du remappage de bloc logique LUN basé sur des attributs simples.</span><span class="sxs-lookup"><span data-stu-id="66111-107">Hardware RAID provider that supplies a set of rules for choosing LUN logical block remapping based on simple attributes.</span></span> <span data-ttu-id="66111-108">Les fournisseurs automagic peuvent également modifier dynamiquement le mappage pour la gestion des erreurs ou des performances.</span><span class="sxs-lookup"><span data-stu-id="66111-108">Automagic providers can also dynamically alter the mapping for performance or fault management.</span></span>

</dd> <dt>

<span data-ttu-id="66111-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**indicateurs automagic**</span><span class="sxs-lookup"><span data-stu-id="66111-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic hints**</span></span>
</dt> <dd>

<span data-ttu-id="66111-110">Informations fournies à un fournisseur automagic pour guider la configuration du bloc logique LUN.</span><span class="sxs-lookup"><span data-stu-id="66111-110">Information supplied to an automagic provider to guide the LUN logical block configuration.</span></span> <span data-ttu-id="66111-111">Les indicateurs incluent des informations sur la tolérance de panne, l’atomicité physique et le modèle d’accès aux e/s prévus.</span><span class="sxs-lookup"><span data-stu-id="66111-111">Hints include information as to the desired fault tolerance, physical atomicity, and intended I/O access pattern.</span></span>

</dd> <dt>

<span data-ttu-id="66111-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disque de base**</span><span class="sxs-lookup"><span data-stu-id="66111-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**basic disk**</span></span>
</dt> <dd>

<span data-ttu-id="66111-113">Un disque géré par le fournisseur de logiciels le plus simple possible.</span><span class="sxs-lookup"><span data-stu-id="66111-113">A disk managed by the simplest possible software provider.</span></span> <span data-ttu-id="66111-114">Le fournisseur de disque de base prend en charge uniquement les volumes qui sont directement mappés aux structures de données de configuration de partition.</span><span class="sxs-lookup"><span data-stu-id="66111-114">The basic disk provider supports only volumes that directly map to partition configuration data structures.</span></span>

</dd> <dt>

<span data-ttu-id="66111-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**liant**</span><span class="sxs-lookup"><span data-stu-id="66111-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="66111-116">Sélection pour un ensemble de mappages aux ressources physiques.</span><span class="sxs-lookup"><span data-stu-id="66111-116">Selecting for a set of mappings to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="66111-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**passer**</span><span class="sxs-lookup"><span data-stu-id="66111-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**convert**</span></span>
</dt> <dd>

<span data-ttu-id="66111-118">Processus de conversion d’un disque de base en disque dynamique.</span><span class="sxs-lookup"><span data-stu-id="66111-118">The process of converting a basic disk to a dynamic disk.</span></span>

</dd> <dt>

<span data-ttu-id="66111-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuré**</span><span class="sxs-lookup"><span data-stu-id="66111-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuration**</span></span>
</dt> <dd>

<span data-ttu-id="66111-120">Collection des paramètres de fonctionnement qui fournissent le mappage d’un volume ou d’un numéro d’unité logique aux ressources physiques.</span><span class="sxs-lookup"><span data-stu-id="66111-120">A collection of the operating parameters that supply the mapping from a volume, or LUN, to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="66111-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**SideWinder**</span><span class="sxs-lookup"><span data-stu-id="66111-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**</span></span>
</dt> <dd>

<span data-ttu-id="66111-122">Programme logiciel qui contient l’intelligence du runtime pour un fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="66111-122">A software program that contains the runtime intelligence for a hardware provider.</span></span>

</dd> <dt>

<span data-ttu-id="66111-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**libérer**</span><span class="sxs-lookup"><span data-stu-id="66111-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disk**</span></span>
</dt> <dd>

<span data-ttu-id="66111-124">Un disque physique ou un LUN RAID matériel.</span><span class="sxs-lookup"><span data-stu-id="66111-124">A physical disk or hardware RAID LUN.</span></span> <span data-ttu-id="66111-125">Les disques sont des cibles pour la charge d’e/s de stockage d’exécution ; Plug-and-Play (PNP) ne fait pas la distinction entre JBOD et les LUN.</span><span class="sxs-lookup"><span data-stu-id="66111-125">Disks are targets for runtime storage I/O load; Plug and Play (PNP) does not distinguish between JBOD and LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="66111-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disque plateau**</span><span class="sxs-lookup"><span data-stu-id="66111-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disk platter**</span></span>
</dt> <dd>

<span data-ttu-id="66111-127">Sous-ensemble d’un Pack utilisé pour exporter ou importer des volumes à partir d’un Pack.</span><span class="sxs-lookup"><span data-stu-id="66111-127">A subset of a pack used for exporting or importing volumes from a pack.</span></span>

</dd> <dt>

<span data-ttu-id="66111-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**Pack de disques**</span><span class="sxs-lookup"><span data-stu-id="66111-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**disk pack**</span></span>
</dt> <dd>

<span data-ttu-id="66111-129">Consultez *Pack*.</span><span class="sxs-lookup"><span data-stu-id="66111-129">See *pack*.</span></span>

</dd> <dt>

<span data-ttu-id="66111-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**unités**</span><span class="sxs-lookup"><span data-stu-id="66111-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**drive**</span></span>
</dt> <dd>

<span data-ttu-id="66111-131">Une pile de disques physiques au sein d’un sous-système RAID matériel.</span><span class="sxs-lookup"><span data-stu-id="66111-131">A physical disk spindle within a hardware RAID subsystem.</span></span> <span data-ttu-id="66111-132">Les lecteurs sont liés aux numéros d’unités logiques par le sous-système.</span><span class="sxs-lookup"><span data-stu-id="66111-132">Drives are bound into LUNs by the subsystem.</span></span>

</dd> <dt>

<span data-ttu-id="66111-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disque dynamique**</span><span class="sxs-lookup"><span data-stu-id="66111-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamic disk**</span></span>
</dt> <dd>

<span data-ttu-id="66111-134">Un disque géré par un fournisseur RAID logiciel avec prise en charge de la reconfiguration de volume flexible.</span><span class="sxs-lookup"><span data-stu-id="66111-134">A disk managed by a software RAID provider with support for flexible volume reconfiguration.</span></span> <span data-ttu-id="66111-135">Un disque dynamique utilise une partition comme conteneur pour les volumes ; Il n’existe aucun mappage garanti.</span><span class="sxs-lookup"><span data-stu-id="66111-135">A dynamic disk uses a partition as a container for volumes; there is no guaranteed mapping.</span></span>

</dd> <dt>

<span data-ttu-id="66111-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configuration explicite**</span><span class="sxs-lookup"><span data-stu-id="66111-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explicit configuration**</span></span>
</dt> <dd>

<span data-ttu-id="66111-137">Configuration avec les paramètres, y compris le type de volume et la disposition exacte, pour une collection de volumes cibles.</span><span class="sxs-lookup"><span data-stu-id="66111-137">A configuration with the parameters, including the volume type and the exact layout, for a collection of target volumes.</span></span>

</dd> <dt>

<span data-ttu-id="66111-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**exporter**</span><span class="sxs-lookup"><span data-stu-id="66111-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**export**</span></span>
</dt> <dd>

<span data-ttu-id="66111-139">Action consistant à déplacer un plateau de disque et tous les volumes qu’il contient à l’extérieur d’un Pack.</span><span class="sxs-lookup"><span data-stu-id="66111-139">The act of moving a disk platter and all volumes contained on that platter out of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="66111-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**étendue**</span><span class="sxs-lookup"><span data-stu-id="66111-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**</span></span>
</dt> <dd>

<span data-ttu-id="66111-141">Plage contiguë de secteurs logiques contribuant à un volume ou à un disque unique.</span><span class="sxs-lookup"><span data-stu-id="66111-141">A contiguous range of logical sectors contributing to a single volume or disk.</span></span> <span data-ttu-id="66111-142">Une étendue peut également être une plage de secteurs non alloués.</span><span class="sxs-lookup"><span data-stu-id="66111-142">An extent can also be range of unallocated sectors.</span></span> <span data-ttu-id="66111-143">En règle générale, un système de fichiers affiche les détails de l’étendue à un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="66111-143">Commonly, a file system displays the extent details to an end-user.</span></span>

</dd> <dt>

<span data-ttu-id="66111-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Table de partition GUID (GPT)**</span><span class="sxs-lookup"><span data-stu-id="66111-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID Partition Table (GPT)**</span></span>
</dt> <dd>

<span data-ttu-id="66111-145">Structures utilisées par le microprogramme EFI.</span><span class="sxs-lookup"><span data-stu-id="66111-145">Structures used by EFI firmware.</span></span> <span data-ttu-id="66111-146">GPT est l’un des deux formats de données de configuration de logiciel de niveau le plus bas utilisés par le microprogramme de la plateforme pour localiser un système d’exploitation de démarrage ou une autre image exécutable.</span><span class="sxs-lookup"><span data-stu-id="66111-146">GPT is one of two lowest level software configuration data formats used by platform firmware to locate a bootable operating system or other executable image.</span></span>

</dd> <dt>

<span data-ttu-id="66111-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**fournisseur de matériel**</span><span class="sxs-lookup"><span data-stu-id="66111-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**hardware provider**</span></span>
</dt> <dd>

<span data-ttu-id="66111-148">Ensemble de logiciels qui s’exécutent sur l’ordinateur hôte, un adaptateur de bus et éventuellement un sous-système de stockage externe qui fonctionne ensemble pour faire surface et gérer les LUN RAID.</span><span class="sxs-lookup"><span data-stu-id="66111-148">A collection of software that executes on the host, a bus adapter, and possibly an external storage subsystem that works together to surface and manage RAID LUNs.</span></span> <span data-ttu-id="66111-149">Les fournisseurs de matériel pour la plupart des sous-systèmes de stockage externes contiennent uniquement des logiciels basés sur l’hôte et en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66111-149">Hardware providers for most external storage subsystems contain only user-mode, host-based software.</span></span>

</dd> <dt>

<span data-ttu-id="66111-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**assurance**</span><span class="sxs-lookup"><span data-stu-id="66111-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**health**</span></span>
</dt> <dd>

<span data-ttu-id="66111-151">État actuel de la gestion des erreurs d’un volume ou d’un numéro d’unité logique.</span><span class="sxs-lookup"><span data-stu-id="66111-151">The current fault-management status of a volume or a LUN.</span></span>

</dd> <dt>

<span data-ttu-id="66111-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**remplacement à chaud**</span><span class="sxs-lookup"><span data-stu-id="66111-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**</span></span>
</dt> <dd>

<span data-ttu-id="66111-153">Ajout temporaire d’un plex de volume à un volume.</span><span class="sxs-lookup"><span data-stu-id="66111-153">Temporarily adding a volume plex to a volume.</span></span>

</dd> <dt>

<span data-ttu-id="66111-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**port**</span><span class="sxs-lookup"><span data-stu-id="66111-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**import**</span></span>
</dt> <dd>

<span data-ttu-id="66111-155">Action consistant à déplacer un plateau de disque et tous ses volumes dans un pack existant.</span><span class="sxs-lookup"><span data-stu-id="66111-155">The act of moving a disk platter and all its volumes into an existing pack.</span></span>

</dd> <dt>

<span data-ttu-id="66111-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**juste une série de disques (JBOD)**</span><span class="sxs-lookup"><span data-stu-id="66111-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**just a bunch of disks (JBOD)**</span></span>
</dt> <dd>

<span data-ttu-id="66111-157">Collection de piles physiques sans le contrôle coordonné fourni par un périphérique RAID matériel.</span><span class="sxs-lookup"><span data-stu-id="66111-157">A collection of physical spindles without the coordinated control provided by a hardware RAID device.</span></span>

</dd> <dt>

<span data-ttu-id="66111-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**Numéro de bloc logique (LBN)**</span><span class="sxs-lookup"><span data-stu-id="66111-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logical block number (LBN)**</span></span>
</dt> <dd>

<span data-ttu-id="66111-159">Plus petite unité adressable de données de stockage.</span><span class="sxs-lookup"><span data-stu-id="66111-159">The smallest addressable unit of storage data.</span></span> <span data-ttu-id="66111-160">LBN est utilisé avec les protocoles de commande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="66111-160">LBN is used with I/O command protocols.</span></span>

</dd> <dt>

<span data-ttu-id="66111-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**mappage de bloc logique**</span><span class="sxs-lookup"><span data-stu-id="66111-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logical block mapping**</span></span>
</dt> <dd>

<span data-ttu-id="66111-162">Transformation des blocs logiques présentés à un fournisseur à ceux exposés par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="66111-162">The transformation of the logical blocks presented to a provider to those exposed by the provider.</span></span>

</dd> <dt>

<span data-ttu-id="66111-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**Numéro d’unité logique (LUN)**</span><span class="sxs-lookup"><span data-stu-id="66111-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logical unit number (LUN)**</span></span>
</dt> <dd>

<span data-ttu-id="66111-164">Unité de stockage physiquement adressable, telle qu’elle est exposée par un sous-système RAID matériel.</span><span class="sxs-lookup"><span data-stu-id="66111-164">A physically addressable storage unit as surfaced by a hardware RAID subsystem.</span></span> <span data-ttu-id="66111-165">Ce terme peut également faire référence à l’identificateur SCSI pour l’unité de stockage.</span><span class="sxs-lookup"><span data-stu-id="66111-165">This term can also refer to the SCSI identifier for the storage unit.</span></span>

</dd> <dt>

<span data-ttu-id="66111-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Numéro de LUN**</span><span class="sxs-lookup"><span data-stu-id="66111-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN number**</span></span>
</dt> <dd>

<span data-ttu-id="66111-167">Nombre qu’un fournisseur de matériel VDS attribue à un numéro d’unité logique (LUN) dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="66111-167">A number that a VDS hardware provider assigns to a LUN in an array.</span></span> <span data-ttu-id="66111-168">Ce n’est pas le même que le « numéro d’unité logique » dans l’adresse SCSI du disque.</span><span class="sxs-lookup"><span data-stu-id="66111-168">This is not the same as the "logical unit number" in the disk's SCSI address.</span></span>

</dd> <dt>

<span data-ttu-id="66111-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**service de gestion**</span><span class="sxs-lookup"><span data-stu-id="66111-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**management service**</span></span>
</dt> <dd>

<span data-ttu-id="66111-170">Programme logiciel qui s’exécute en fonction des besoins pour effectuer la configuration du volume, l’analyse ou la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="66111-170">A software program that executes as needed to perform volume configuration, monitoring, or fault handling.</span></span>

</dd> <dt>

<span data-ttu-id="66111-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mappage**</span><span class="sxs-lookup"><span data-stu-id="66111-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**</span></span>
</dt> <dd>

<span data-ttu-id="66111-172">Un volume exposé au système d’exploitation et ayant un nom de volume associé (une lettre de lecteur).</span><span class="sxs-lookup"><span data-stu-id="66111-172">A volume that is exposed to the operating system and has an associated volume name (a drive letter).</span></span> <span data-ttu-id="66111-173">Un volume est accessible par un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="66111-173">A volume is accessible by a file system.</span></span>

</dd> <dt>

<span data-ttu-id="66111-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**masquage**</span><span class="sxs-lookup"><span data-stu-id="66111-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**masking**</span></span>
</dt> <dd>

<span data-ttu-id="66111-175">Un disque non reconnu par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="66111-175">A disk not recognized by the operating system.</span></span> <span data-ttu-id="66111-176">Un disque peut être masqué par le sous-système RAID matériel, le commutateur, la réserve SCSI par un autre ordinateur hôte ou le logiciel dans la pile de disques.</span><span class="sxs-lookup"><span data-stu-id="66111-176">A disk can be masked by the hardware RAID subsystem, switch, SCSI RESERVE by another computer host, or software in the disk stack.</span></span>

</dd> <dt>

<span data-ttu-id="66111-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**partitionnement d’enregistrement de démarrage principal (MBR)**</span><span class="sxs-lookup"><span data-stu-id="66111-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**master boot record partitioning (MBR)**</span></span>
</dt> <dd>

<span data-ttu-id="66111-178">MBR est l’un des deux formats de données de configuration de logiciel de niveau le plus bas et est utilisé par le microprogramme BIOS pour localiser une image de système d’exploitation amorçable.</span><span class="sxs-lookup"><span data-stu-id="66111-178">MBR is one of two lowest level software configuration data formats, and is used by BIOS firmware to locate a bootable operating system image.</span></span>

</dd> <dt>

<span data-ttu-id="66111-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**membre**</span><span class="sxs-lookup"><span data-stu-id="66111-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**member**</span></span>
</dt> <dd>

<span data-ttu-id="66111-180">Collection d’étendues de disque concaténées contenues sur un ou plusieurs disques.</span><span class="sxs-lookup"><span data-stu-id="66111-180">A collection of concatenated disk extents contained on one more disks.</span></span> <span data-ttu-id="66111-181">Un disque ne peut contribuer qu’à un seul membre d’un volume.</span><span class="sxs-lookup"><span data-stu-id="66111-181">A disk can contribute to only one member of a volume.</span></span>

</dd> <dt>

<span data-ttu-id="66111-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mémoire**</span><span class="sxs-lookup"><span data-stu-id="66111-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mirror**</span></span>
</dt> <dd>

<span data-ttu-id="66111-183">Un mappage de volume ou de disque qui gère au moins deux copies de données identiques.</span><span class="sxs-lookup"><span data-stu-id="66111-183">A volume or disk mapping that maintains two or more identical data copies.</span></span> <span data-ttu-id="66111-184">Le type de mappage est également appelé RAID niveau 1.</span><span class="sxs-lookup"><span data-stu-id="66111-184">The type of mapping is also called RAID Level 1.</span></span>

</dd> <dt>

<span data-ttu-id="66111-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**presse**</span><span class="sxs-lookup"><span data-stu-id="66111-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**pack**</span></span>
</dt> <dd>

<span data-ttu-id="66111-186">Collection de volumes logiques et de disques sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="66111-186">A collection of logical volumes and underlying disks.</span></span> <span data-ttu-id="66111-187">Un Pack est l’unité de fermeture transitive pour un volume.</span><span class="sxs-lookup"><span data-stu-id="66111-187">A pack is the unit of transitive closure for a volume.</span></span> <span data-ttu-id="66111-188">Les Disk packs et les groupes de disques dynamiques sont des termes pour le même élément.</span><span class="sxs-lookup"><span data-stu-id="66111-188">Dynamic disk packs and disk groups are terms for the same item.</span></span>

</dd> <dt>

<span data-ttu-id="66111-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**entrelacement de parité**</span><span class="sxs-lookup"><span data-stu-id="66111-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**parity stripe**</span></span>
</dt> <dd>

<span data-ttu-id="66111-190">Un mappage de volume ou de disque qui gère les informations de contrôle de parité ainsi que les données.</span><span class="sxs-lookup"><span data-stu-id="66111-190">A volume or disk mapping that maintains parity check information as well as data.</span></span> <span data-ttu-id="66111-191">Chaque fournisseur fournit le schéma de protection et de mappage exacts.</span><span class="sxs-lookup"><span data-stu-id="66111-191">Each vendor supplies the exact mapping and protection scheme.</span></span> <span data-ttu-id="66111-192">Comprend les configurations RAID 3, 4, 5 et 6.</span><span class="sxs-lookup"><span data-stu-id="66111-192">Includes RAID 3, 4, 5, and 6.</span></span>

</dd> <dt>

<span data-ttu-id="66111-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configuration partiellement dirigée**</span><span class="sxs-lookup"><span data-stu-id="66111-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**partially directed configuration**</span></span>
</dt> <dd>

<span data-ttu-id="66111-194">Configuration de volume ou de disque qui n’est pas entièrement explicite.</span><span class="sxs-lookup"><span data-stu-id="66111-194">A volume or disk configuration that is not fully explicit.</span></span> <span data-ttu-id="66111-195">Le type de liaison et une collection de ressources cibles sont spécifiés ; la disposition réelle n’est pas.</span><span class="sxs-lookup"><span data-stu-id="66111-195">The binding type and a collection of target resources are specified; the actual layout is not.</span></span> <span data-ttu-id="66111-196">La configuration partiellement dirigée est la configuration de volume la plus courante.</span><span class="sxs-lookup"><span data-stu-id="66111-196">Partially directed configuration is the most common volume configuration.</span></span>

</dd> <dt>

<span data-ttu-id="66111-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**non**</span><span class="sxs-lookup"><span data-stu-id="66111-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**partition**</span></span>
</dt> <dd>

<span data-ttu-id="66111-198">Plage contiguë de secteurs logiques décrite par une seule entrée dans la structure MBR ou GPT.</span><span class="sxs-lookup"><span data-stu-id="66111-198">A contiguous range of logical sectors described by a single entry in the MBR or GPT structure.</span></span> <span data-ttu-id="66111-199">Sur les disques de base, les partitions correspondent directement aux volumes simples.</span><span class="sxs-lookup"><span data-stu-id="66111-199">On basic disks, partitions directly correspond to simple volumes.</span></span> <span data-ttu-id="66111-200">Les structures de partition sont partagées entre le microprogramme du BIOS ou de la plateforme EFI et un système d’exploitation ou une autre image de démarrage.</span><span class="sxs-lookup"><span data-stu-id="66111-200">Partition structures are shared between the BIOS or EFI platform firmware and an operating system or other bootable image.</span></span>

</dd> <dt>

<span data-ttu-id="66111-201"><span id="base.path"></span><span id="BASE.PATH"></span>**d**</span><span class="sxs-lookup"><span data-stu-id="66111-201"><span id="base.path"></span><span id="BASE.PATH"></span>**path**</span></span>
</dt> <dd>

<span data-ttu-id="66111-202">Le chemin d’accès entre un ordinateur et un disque ou un numéro d’unité logique matériel externe.</span><span class="sxs-lookup"><span data-stu-id="66111-202">The access path from a computer to a disk or external hardware LUN.</span></span>

</dd> <dt>

<span data-ttu-id="66111-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**duplex**</span><span class="sxs-lookup"><span data-stu-id="66111-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plex**</span></span>
</dt> <dd>

<span data-ttu-id="66111-204">Un membre d’un volume ou d’un numéro d’unité logique mis en miroir.</span><span class="sxs-lookup"><span data-stu-id="66111-204">One member of a mirrored volume or LUN.</span></span>

</dd> <dt>

<span data-ttu-id="66111-205"><span id="base.port"></span><span id="BASE.PORT"></span>**importer**</span><span class="sxs-lookup"><span data-stu-id="66111-205"><span id="base.port"></span><span id="BASE.PORT"></span>**port**</span></span>
</dt> <dd>

<span data-ttu-id="66111-206">Point de terminaison d’un chemin d’accès sur un disque.</span><span class="sxs-lookup"><span data-stu-id="66111-206">The endpoint of a path at a disk.</span></span>

</dd> <dt>

<span data-ttu-id="66111-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**baie redondante de disques indépendants (RAID)**</span><span class="sxs-lookup"><span data-stu-id="66111-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundant array of independent disks (RAID)**</span></span>
</dt> <dd>

<span data-ttu-id="66111-208">Ensemble de techniques pour la gestion de plusieurs disques.</span><span class="sxs-lookup"><span data-stu-id="66111-208">A collection of techniques for managing multiple disks.</span></span>

</dd> <dt>

<span data-ttu-id="66111-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**service Runtime**</span><span class="sxs-lookup"><span data-stu-id="66111-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**runtime service**</span></span>
</dt> <dd>

<span data-ttu-id="66111-210">Programme logiciel qui s’exécute sur la base d’une demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="66111-210">A software program that executes on an I/O-request basis.</span></span>

</dd> <dt>

<span data-ttu-id="66111-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disque simple**</span><span class="sxs-lookup"><span data-stu-id="66111-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**simple disk**</span></span>
</dt> <dd>

<span data-ttu-id="66111-212">Une broche qui n’est pas connectée à un contrôleur RAID matériel.</span><span class="sxs-lookup"><span data-stu-id="66111-212">A spindle that is not connected to a hardware RAID controller.</span></span> <span data-ttu-id="66111-213">Voir aussi simplement une série de disques (JBOD).</span><span class="sxs-lookup"><span data-stu-id="66111-213">See also Just a Bunch Of Disks (JBOD).</span></span>

</dd> <dt>

<span data-ttu-id="66111-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**fournisseur de logiciels**</span><span class="sxs-lookup"><span data-stu-id="66111-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="66111-215">Logiciel basé sur l’hôte qui expose des volumes logiques et s’exécute sur des disques.</span><span class="sxs-lookup"><span data-stu-id="66111-215">Host-based software that exposes logical volumes and operates on disks.</span></span> <span data-ttu-id="66111-216">Un fournisseur de logiciels comprend des services d’exécution en mode noyau, des données de configuration et des services de gestion en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66111-216">A software provider includes kernel-mode runtime services, configuration data, and user-mode management services.</span></span>

</dd> <dt>

<span data-ttu-id="66111-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**répartis**</span><span class="sxs-lookup"><span data-stu-id="66111-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**span**</span></span>
</dt> <dd>

<span data-ttu-id="66111-218">Un mappage linéaire de volume ou de disque de plusieurs extensions de disque ou de lecteur discontinues.</span><span class="sxs-lookup"><span data-stu-id="66111-218">A volume or disk linear mapping of multiple discontinuous disk or drive extents.</span></span> <span data-ttu-id="66111-219">Les étendues peuvent se trouver sur un ou plusieurs axes ou numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="66111-219">The extents can be on one or more spindles or LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="66111-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**pivot**</span><span class="sxs-lookup"><span data-stu-id="66111-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**spindle**</span></span>
</dt> <dd>

<span data-ttu-id="66111-221">Unité physique de stockage sur disque.</span><span class="sxs-lookup"><span data-stu-id="66111-221">A physical unit of disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="66111-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**empilement**</span><span class="sxs-lookup"><span data-stu-id="66111-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**stacking**</span></span>
</dt> <dd>

<span data-ttu-id="66111-223">Opération de construction d’un volume ou d’un numéro d’unité logique en effectuant plusieurs opérations de mappage de bloc logique.</span><span class="sxs-lookup"><span data-stu-id="66111-223">The act of constructing a volume or LUN by performing more than one logical block mapping operation.</span></span> <span data-ttu-id="66111-224">Un volume agrégé par bandes en miroir en est un exemple.</span><span class="sxs-lookup"><span data-stu-id="66111-224">An example is a mirrored striped volume.</span></span> <span data-ttu-id="66111-225">L’empilement le plus courant se produit lorsque le RAID logiciel est utilisé sur des numéros d’unités logiques créés par RAID matériel.</span><span class="sxs-lookup"><span data-stu-id="66111-225">The most common stacking occurs when software RAID is used across LUNs constructed by hardware RAID.</span></span>

</dd> <dt>

<span data-ttu-id="66111-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Stripe**</span><span class="sxs-lookup"><span data-stu-id="66111-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**</span></span>
</dt> <dd>

<span data-ttu-id="66111-227">Un mappage de volume ou de disque qui entrelace les extensions contiguës sur plusieurs volumes, disques ou lecteurs.</span><span class="sxs-lookup"><span data-stu-id="66111-227">A volume or disk mapping that interleaves contiguous extents across multiple volumes, disks, or drives.</span></span> <span data-ttu-id="66111-228">Ce mappage est également appelé RAID 0.</span><span class="sxs-lookup"><span data-stu-id="66111-228">This mapping is also called RAID 0.</span></span>

</dd> <dt>

<span data-ttu-id="66111-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**statu**</span><span class="sxs-lookup"><span data-stu-id="66111-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**status**</span></span>
</dt> <dd>

<span data-ttu-id="66111-230">Disponibilité actuelle d’un volume, d’un disque ou d’un lecteur.</span><span class="sxs-lookup"><span data-stu-id="66111-230">The current availability of a volume, disk, or drive.</span></span>

</dd> <dt>

<span data-ttu-id="66111-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**sous-système**</span><span class="sxs-lookup"><span data-stu-id="66111-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsystem**</span></span>
</dt> <dd>

<span data-ttu-id="66111-232">Instanciation du logiciel du fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="66111-232">The instantiation of hardware-provider software.</span></span> <span data-ttu-id="66111-233">Un sous-système contient au moins un contrôleur et un lecteur.</span><span class="sxs-lookup"><span data-stu-id="66111-233">A subsystem contains at least one controller and one drive.</span></span> <span data-ttu-id="66111-234">Si le sous-système est externe à l’ordinateur, un ou plusieurs chemins d’accès réseau connectent le sous-système à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="66111-234">If the subsystem is external to the computer, one or more network paths connect the subsystem to the computer.</span></span>

</dd> <dt>

<span data-ttu-id="66111-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**État de transition**</span><span class="sxs-lookup"><span data-stu-id="66111-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**transition state**</span></span>
</dt> <dd>

<span data-ttu-id="66111-236">État du mappage logique à physique qui est en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="66111-236">Status of the logical to physical mapping that is undergoing change.</span></span>

</dd> <dt>

<span data-ttu-id="66111-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disque non initialisé**</span><span class="sxs-lookup"><span data-stu-id="66111-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**uninitialized disk**</span></span>
</dt> <dd>

<span data-ttu-id="66111-238">Disque qui n’est pas membre d’un Pack.</span><span class="sxs-lookup"><span data-stu-id="66111-238">A disk that is not a member of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="66111-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disque non masqué**</span><span class="sxs-lookup"><span data-stu-id="66111-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmasked disk**</span></span>
</dt> <dd>

<span data-ttu-id="66111-240">Disque visible par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="66111-240">A disk that is visible to the operating system.</span></span> <span data-ttu-id="66111-241">Le contenu d’un disque non masqué est visible pour les gestionnaires de volume logiciel, les systèmes de fichiers, etc.</span><span class="sxs-lookup"><span data-stu-id="66111-241">The contents of an unmasked disk are visible to software volume managers, file systems, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="66111-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**agrégat**</span><span class="sxs-lookup"><span data-stu-id="66111-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="66111-243">Un certain nombre d’étendues de disque liées à une plage pratiquement contiguë de blocs logiques.</span><span class="sxs-lookup"><span data-stu-id="66111-243">A number of disk extents bound into a virtually contiguous range of logical blocks.</span></span> <span data-ttu-id="66111-244">Un volume est accessible par le biais d’une lettre de lecteur, d’un dossier monté ou d’un chemin d’accès de GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="66111-244">A volume can be accessed through a drive letter, a mounted folder, or a volume GUID path.</span></span>

</dd> </dl>

 

 
