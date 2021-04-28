---
description: 'Classe SystemConfig_LogDisk : cette classe est la classe de type d’événement pour les événements de configuration de disque logique.'
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: Classe SystemConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1d7ca8dc3f632e88c250715292a27e18ff36e3af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106107"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="26813-103">SystemConfig \_ LogDisk, classe</span><span class="sxs-lookup"><span data-stu-id="26813-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="26813-104">Cette classe est la classe de type d’événement pour les événements de configuration de disque logique.</span><span class="sxs-lookup"><span data-stu-id="26813-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="26813-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="26813-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="26813-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26813-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="26813-107">Membres</span><span class="sxs-lookup"><span data-stu-id="26813-107">Members</span></span>

<span data-ttu-id="26813-108">La classe **SystemConfig \_ LogDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26813-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="26813-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26813-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26813-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26813-110">Properties</span></span>

<span data-ttu-id="26813-111">La classe **SystemConfig \_ LogDisk** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="26813-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26813-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="26813-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-115">Qualificateurs : **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="26813-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="26813-116">Nombre d’octets dans chaque secteur pour le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="26813-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="26813-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="26813-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-120">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="26813-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="26813-121">Numéro d’index du disque contenant cette partition.</span><span class="sxs-lookup"><span data-stu-id="26813-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="26813-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="26813-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-123">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="26813-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="26813-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-125">Qualificateurs : **WmiDataId** (6), **Max** (4), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="26813-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="26813-126">Lettre de lecteur du disque, sous la forme « <letter> : ».</span><span class="sxs-lookup"><span data-stu-id="26813-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="26813-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="26813-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-130">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="26813-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="26813-131">Type de lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="26813-131">Type of disk drive.</span></span> <span data-ttu-id="26813-132">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="26813-132">Possible values are:</span></span>



| <span data-ttu-id="26813-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="26813-133">Value</span></span>                                                                        | <span data-ttu-id="26813-134">Signification</span><span class="sxs-lookup"><span data-stu-id="26813-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="26813-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="26813-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="26813-136">Partition</span><span class="sxs-lookup"><span data-stu-id="26813-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="26813-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="26813-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="26813-138">Volume</span><span class="sxs-lookup"><span data-stu-id="26813-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="26813-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="26813-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="26813-140">Partition étendue sur plusieurs disques</span><span class="sxs-lookup"><span data-stu-id="26813-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="26813-141">**FileSystem**</span><span class="sxs-lookup"><span data-stu-id="26813-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-142">Type de données : **char16**</span><span class="sxs-lookup"><span data-stu-id="26813-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="26813-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-144">Qualificateurs : **WmiDataId** (14), **Max** (16), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="26813-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="26813-145">Système de fichiers sur le disque logique, par exemple, NTFS.</span><span class="sxs-lookup"><span data-stu-id="26813-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="26813-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="26813-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-147">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="26813-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="26813-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-149">Qualificateurs : **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="26813-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="26813-150">Nombre de clusters libres dans le volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="26813-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="26813-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="26813-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-154">Qualificateurs : **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="26813-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="26813-155">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="26813-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="26813-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="26813-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-159">Qualificateurs : **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="26813-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="26813-160">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="26813-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="26813-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="26813-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-164">Qualificateurs : **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="26813-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="26813-165">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="26813-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="26813-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="26813-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-169">Qualificateurs : **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="26813-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="26813-170">Numéro d’index de la partition.</span><span class="sxs-lookup"><span data-stu-id="26813-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="26813-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="26813-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-172">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26813-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26813-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-174">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="26813-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="26813-175">Taille totale de la partition, en octets.</span><span class="sxs-lookup"><span data-stu-id="26813-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="26813-176">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="26813-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-179">Qualificateurs : **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="26813-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="26813-180">Nombre de secteurs dans le volume.</span><span class="sxs-lookup"><span data-stu-id="26813-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="26813-181">**Taille**</span><span class="sxs-lookup"><span data-stu-id="26813-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-182">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-184">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="26813-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="26813-185">Taille du lecteur de disque, en octets.</span><span class="sxs-lookup"><span data-stu-id="26813-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="26813-186">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="26813-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-187">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26813-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26813-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-189">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="26813-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="26813-190">Décalage de départ (en octets) de la partition à partir du début du disque.</span><span class="sxs-lookup"><span data-stu-id="26813-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="26813-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="26813-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-192">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="26813-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="26813-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-194">Qualificateurs : **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="26813-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="26813-195">Nombre de clusters utilisés et libres dans le volume.</span><span class="sxs-lookup"><span data-stu-id="26813-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="26813-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="26813-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26813-197">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26813-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26813-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26813-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26813-199">Qualificateurs : **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="26813-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="26813-200">Réservé.</span><span class="sxs-lookup"><span data-stu-id="26813-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26813-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26813-201">Requirements</span></span>



| <span data-ttu-id="26813-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26813-202">Requirement</span></span> | <span data-ttu-id="26813-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="26813-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26813-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26813-204">Minimum supported client</span></span><br/> | <span data-ttu-id="26813-205">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26813-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26813-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26813-206">Minimum supported server</span></span><br/> | <span data-ttu-id="26813-207">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26813-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26813-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26813-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26813-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="26813-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




