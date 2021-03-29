---
description: Cette classe est la classe de type d’événement pour les événements de configuration de disque logique.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: Classe SystemConfig_V0_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: dbc1ee189bae1fe71f42267f38bd40763764dea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973646"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="b4d84-103">\_Classe SystemConfig v0 \_ LogDisk</span><span class="sxs-lookup"><span data-stu-id="b4d84-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="b4d84-104">Cette classe est la classe de type d’événement pour les événements de configuration de disque logique.</span><span class="sxs-lookup"><span data-stu-id="b4d84-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="b4d84-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="b4d84-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4d84-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4d84-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a><span data-ttu-id="b4d84-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b4d84-107">Members</span></span>

<span data-ttu-id="b4d84-108">La classe **SystemConfig \_ v0 \_ LogDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b4d84-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="b4d84-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4d84-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4d84-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4d84-110">Properties</span></span>

<span data-ttu-id="b4d84-111">La classe **SystemConfig \_ v0 \_ LogDisk** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b4d84-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4d84-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="b4d84-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d84-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-115">Qualificateurs : **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="b4d84-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-116">Nombre d’octets dans chaque secteur pour le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="b4d84-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="b4d84-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d84-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-120">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="b4d84-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-121">Numéro d’index du disque contenant cette partition.</span><span class="sxs-lookup"><span data-stu-id="b4d84-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="b4d84-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-123">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="b4d84-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-125">Qualificateurs : **WmiDataId** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="b4d84-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-126">Lettre de lecteur du disque, sous la forme « <letter> : ».</span><span class="sxs-lookup"><span data-stu-id="b4d84-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="b4d84-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d84-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-130">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="b4d84-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-131">Type de lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="b4d84-131">Type of disk drive.</span></span> <span data-ttu-id="b4d84-132">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4d84-132">Possible values are:</span></span>



| <span data-ttu-id="b4d84-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4d84-133">Value</span></span>                                                                        | <span data-ttu-id="b4d84-134">Signification</span><span class="sxs-lookup"><span data-stu-id="b4d84-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="b4d84-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b4d84-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b4d84-136">Partition</span><span class="sxs-lookup"><span data-stu-id="b4d84-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="b4d84-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b4d84-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b4d84-138">Volume</span><span class="sxs-lookup"><span data-stu-id="b4d84-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="b4d84-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b4d84-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b4d84-140">Partition étendue sur plusieurs disques</span><span class="sxs-lookup"><span data-stu-id="b4d84-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b4d84-141">**FileSystem**</span><span class="sxs-lookup"><span data-stu-id="b4d84-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-142">Type de données : **char16**</span><span class="sxs-lookup"><span data-stu-id="b4d84-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-144">Qualificateurs : **WmiDataId** (13), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="b4d84-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-145">Système de fichiers sur le disque logique, par exemple, NTFS.</span><span class="sxs-lookup"><span data-stu-id="b4d84-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="b4d84-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-147">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="b4d84-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-149">Qualificateurs : **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="b4d84-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-150">Nombre de clusters libres dans le volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4d84-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-151">**Remplir**</span><span class="sxs-lookup"><span data-stu-id="b4d84-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d84-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-154">Qualificateurs : **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="b4d84-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-155">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b4d84-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="b4d84-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d84-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-159">Qualificateurs : **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="b4d84-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-160">Numéro d’index de la partition.</span><span class="sxs-lookup"><span data-stu-id="b4d84-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="b4d84-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-162">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4d84-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-164">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="b4d84-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-165">Taille totale de la partition, en octets.</span><span class="sxs-lookup"><span data-stu-id="b4d84-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-166">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="b4d84-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d84-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-169">Qualificateurs : **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="b4d84-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-170">Nombre de secteurs dans le volume.</span><span class="sxs-lookup"><span data-stu-id="b4d84-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-171">**Taille**</span><span class="sxs-lookup"><span data-stu-id="b4d84-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d84-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-174">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="b4d84-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-175">Taille du lecteur de disque, en octets.</span><span class="sxs-lookup"><span data-stu-id="b4d84-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-176">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="b4d84-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-177">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b4d84-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-179">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="b4d84-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-180">Décalage de départ (en octets) de la partition à partir du début du disque.</span><span class="sxs-lookup"><span data-stu-id="b4d84-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-181">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="b4d84-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-182">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="b4d84-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-184">Qualificateurs : **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="b4d84-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-185">Nombre de clusters utilisés et libres dans le volume.</span><span class="sxs-lookup"><span data-stu-id="b4d84-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="b4d84-186">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="b4d84-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d84-187">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d84-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4d84-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4d84-189">Qualificateurs : **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="b4d84-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="b4d84-190">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b4d84-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4d84-191">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b4d84-191">Requirements</span></span>



| <span data-ttu-id="b4d84-192">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4d84-192">Requirement</span></span> | <span data-ttu-id="b4d84-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4d84-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4d84-194">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4d84-194">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d84-195">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4d84-195">None supported</span></span><br/>                            |
| <span data-ttu-id="b4d84-196">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4d84-196">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d84-197">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4d84-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4d84-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4d84-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d84-199">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="b4d84-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




