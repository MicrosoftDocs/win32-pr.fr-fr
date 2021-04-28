---
description: 'Classe SystemConfig_V0_PhyDisk : cette classe est la classe de type d’événement pour les événements de configuration de disque physique.'
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: Classe SystemConfig_V0_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdb12fac8b2b902f21258fd4c7cfe9846d0456eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105957"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="a2734-103">\_Classe SystemConfig v0 \_ PhyDisk</span><span class="sxs-lookup"><span data-stu-id="a2734-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="a2734-104">Cette classe est la classe de type d’événement pour les événements de configuration de disque physique.</span><span class="sxs-lookup"><span data-stu-id="a2734-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="a2734-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a2734-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2734-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2734-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a><span data-ttu-id="a2734-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a2734-107">Members</span></span>

<span data-ttu-id="a2734-108">La classe **SystemConfig \_ v0 \_ PhyDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2734-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="a2734-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2734-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2734-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2734-110">Properties</span></span>

<span data-ttu-id="a2734-111">La classe **SystemConfig \_ v0 \_ PhyDisk** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a2734-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2734-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="a2734-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-113">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="a2734-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="a2734-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-115">Qualificateurs : **WmiDataId** (13), **Max** (3)</span><span class="sxs-lookup"><span data-stu-id="a2734-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-116">Lettre de lecteur du lecteur de démarrage sous la forme « <letter> : ».</span><span class="sxs-lookup"><span data-stu-id="a2734-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="a2734-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="a2734-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-120">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="a2734-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-121">Nombre d’octets dans chaque secteur pour le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="a2734-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-122">**Cylindres**</span><span class="sxs-lookup"><span data-stu-id="a2734-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-123">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2734-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-125">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="a2734-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-126">Nombre total de cylindres sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="a2734-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="a2734-127">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="a2734-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="a2734-128">La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité.</span><span class="sxs-lookup"><span data-stu-id="a2734-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="a2734-129">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="a2734-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="a2734-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-133">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="a2734-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-134">Numéro d’index du disque contenant cette partition.</span><span class="sxs-lookup"><span data-stu-id="a2734-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-135">**Fécule**</span><span class="sxs-lookup"><span data-stu-id="a2734-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-136">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="a2734-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="a2734-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-138">Qualificateurs : **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="a2734-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-139">Nom du fabricant du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="a2734-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="a2734-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-143">Qualificateurs : **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="a2734-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-144">Nombre de partitions sur ce lecteur de disque physique qui sont reconnues par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a2734-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-145">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="a2734-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-148">Qualificateurs : **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="a2734-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-149">Numéro d’unité logique (LUN) SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="a2734-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-150">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="a2734-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-153">Qualificateurs : **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="a2734-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-154">Numéro de bus SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="a2734-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="a2734-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-156">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-158">Qualificateurs : **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="a2734-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-159">Numéro SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="a2734-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-160">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="a2734-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-161">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-163">Qualificateurs : **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="a2734-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-164">Contient le numéro de l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="a2734-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-165">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="a2734-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-166">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-168">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="a2734-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-169">Nombre de secteurs dans chaque piste pour ce lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="a2734-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="a2734-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2734-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-173">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="a2734-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-174">Nombre de pistes dans chaque cylindre sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="a2734-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="a2734-175">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="a2734-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="a2734-176">La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité.</span><span class="sxs-lookup"><span data-stu-id="a2734-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="a2734-177">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="a2734-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="a2734-178">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="a2734-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2734-179">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a2734-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2734-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2734-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2734-181">Qualificateurs : **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="a2734-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="a2734-182">True si le cache d’écriture est activé.</span><span class="sxs-lookup"><span data-stu-id="a2734-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2734-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2734-183">Requirements</span></span>



| <span data-ttu-id="a2734-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2734-184">Requirement</span></span> | <span data-ttu-id="a2734-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2734-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2734-186">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2734-186">Minimum supported client</span></span><br/> | <span data-ttu-id="a2734-187">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2734-187">None supported</span></span><br/>                            |
| <span data-ttu-id="a2734-188">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2734-188">Minimum supported server</span></span><br/> | <span data-ttu-id="a2734-189">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2734-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2734-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2734-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2734-191">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="a2734-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




