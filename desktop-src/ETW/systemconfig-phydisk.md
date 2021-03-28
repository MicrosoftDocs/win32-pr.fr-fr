---
description: Cette classe est la classe de type d’événement pour les événements de configuration de disque physique.
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: Classe SystemConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: d868e3943f22a71b4513f4f77841ddea9204ffea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972111"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="79f53-103">SystemConfig \_ PhyDisk, classe</span><span class="sxs-lookup"><span data-stu-id="79f53-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="79f53-104">Cette classe est la classe de type d’événement pour les événements de configuration de disque physique.</span><span class="sxs-lookup"><span data-stu-id="79f53-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="79f53-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="79f53-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f53-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79f53-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a><span data-ttu-id="79f53-107">Membres</span><span class="sxs-lookup"><span data-stu-id="79f53-107">Members</span></span>

<span data-ttu-id="79f53-108">La classe **SystemConfig \_ PhyDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="79f53-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="79f53-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79f53-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79f53-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79f53-110">Properties</span></span>

<span data-ttu-id="79f53-111">La classe **SystemConfig \_ PhyDisk** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="79f53-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79f53-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="79f53-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-113">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="79f53-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="79f53-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-115">Qualificateurs : **WmiDataId** (14), **Max** (3), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="79f53-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="79f53-116">Lettre de lecteur du lecteur de démarrage sous la forme « <letter> : ».</span><span class="sxs-lookup"><span data-stu-id="79f53-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="79f53-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="79f53-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-120">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="79f53-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-121">Nombre d’octets dans chaque secteur pour le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="79f53-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-122">**Cylindres**</span><span class="sxs-lookup"><span data-stu-id="79f53-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-123">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79f53-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-125">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="79f53-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-126">Nombre total de cylindres sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="79f53-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="79f53-127">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="79f53-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="79f53-128">La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité.</span><span class="sxs-lookup"><span data-stu-id="79f53-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="79f53-129">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="79f53-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="79f53-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-133">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="79f53-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-134">Numéro d’index du disque contenant cette partition.</span><span class="sxs-lookup"><span data-stu-id="79f53-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-135">**Fécule**</span><span class="sxs-lookup"><span data-stu-id="79f53-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-136">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="79f53-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="79f53-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-138">Qualificateurs : **WmiDataId** (10), **Max** (256), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="79f53-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="79f53-139">Nom du fabricant du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="79f53-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-140">**Remplir**</span><span class="sxs-lookup"><span data-stu-id="79f53-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-141">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="79f53-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-143">Qualificateurs : **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="79f53-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-144">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="79f53-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="79f53-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-148">Qualificateurs : **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="79f53-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-149">Nombre de partitions sur ce lecteur de disque physique qui sont reconnues par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="79f53-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="79f53-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-153">Qualificateurs : **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="79f53-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-154">Numéro d’unité logique (LUN) SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="79f53-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="79f53-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-156">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-158">Qualificateurs : **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="79f53-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-159">Numéro de bus SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="79f53-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="79f53-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-161">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-163">Qualificateurs : **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="79f53-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-164">Numéro SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="79f53-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="79f53-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-166">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-168">Qualificateurs : **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="79f53-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-169">Contient le numéro de l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="79f53-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-170">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="79f53-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-173">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="79f53-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-174">Nombre de secteurs dans chaque piste pour ce lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="79f53-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-175">**Chambres**</span><span class="sxs-lookup"><span data-stu-id="79f53-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-176">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="79f53-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="79f53-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-178">Qualificateurs : **WmiDataId** (15), **Max** (2), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="79f53-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="79f53-179">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="79f53-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="79f53-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-181">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79f53-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-183">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="79f53-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-184">Nombre de pistes dans chaque cylindre sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="79f53-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="79f53-185">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="79f53-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="79f53-186">La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité.</span><span class="sxs-lookup"><span data-stu-id="79f53-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="79f53-187">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="79f53-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="79f53-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="79f53-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79f53-189">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="79f53-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="79f53-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79f53-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79f53-191">Qualificateurs : **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="79f53-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="79f53-192">True si le cache d’écriture est activé.</span><span class="sxs-lookup"><span data-stu-id="79f53-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79f53-193">Spécifications</span><span class="sxs-lookup"><span data-stu-id="79f53-193">Requirements</span></span>



| <span data-ttu-id="79f53-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79f53-194">Requirement</span></span> | <span data-ttu-id="79f53-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="79f53-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79f53-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79f53-196">Minimum supported client</span></span><br/> | <span data-ttu-id="79f53-197">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79f53-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="79f53-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79f53-198">Minimum supported server</span></span><br/> | <span data-ttu-id="79f53-199">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79f53-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79f53-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79f53-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f53-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="79f53-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




