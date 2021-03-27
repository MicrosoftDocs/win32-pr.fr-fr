---
description: La \_ classe HWConfig PhyDisk est la classe de type d’événement pour les événements de configuration de disque physique. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: Classe HWConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972199"
---
# <a name="hwconfig_phydisk-class"></a><span data-ttu-id="9b613-104">HWConfig \_ PhyDisk, classe</span><span class="sxs-lookup"><span data-stu-id="9b613-104">HWConfig\_PhyDisk class</span></span>

<span data-ttu-id="9b613-105">La classe **HWConfig \_ PhyDisk** est la classe de type d’événement pour les événements de configuration de disque physique.</span><span class="sxs-lookup"><span data-stu-id="9b613-105">The **HWConfig\_PhyDisk** class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="9b613-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="9b613-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b613-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b613-107">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a><span data-ttu-id="9b613-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9b613-108">Members</span></span>

<span data-ttu-id="9b613-109">La classe **HWConfig \_ PhyDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9b613-109">The **HWConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="9b613-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b613-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b613-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b613-111">Properties</span></span>

<span data-ttu-id="9b613-112">La classe **HWConfig \_ PhyDisk** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9b613-112">The **HWConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b613-113">BytesPerSector</span><span class="sxs-lookup"><span data-stu-id="9b613-113">BytesPerSector</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b613-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-116">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="9b613-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-117">Nombre d’octets dans chaque secteur pour le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="9b613-117">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-118">Cylindres</span><span class="sxs-lookup"><span data-stu-id="9b613-118">Cylinders</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-119">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b613-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-121">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="9b613-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-122">Nombre total de cylindres sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="9b613-122">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="9b613-123">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="9b613-123">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="9b613-124">La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité.</span><span class="sxs-lookup"><span data-stu-id="9b613-124">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="9b613-125">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="9b613-125">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-126">DiskNumber</span><span class="sxs-lookup"><span data-stu-id="9b613-126">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-127">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b613-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-129">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="9b613-129">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-130">Numéro d’index du disque contenant cette partition.</span><span class="sxs-lookup"><span data-stu-id="9b613-130">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-131">Fabricant</span><span class="sxs-lookup"><span data-stu-id="9b613-131">Manufacturer</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9b613-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-134">Qualificateurs : WmiDataId (10), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="9b613-134">Qualifiers: WmiDataId(10), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="9b613-135">Nom du fabricant du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="9b613-135">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-136">SCSILun</span><span class="sxs-lookup"><span data-stu-id="9b613-136">SCSILun</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b613-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-139">Qualificateurs : WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="9b613-139">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-140">Numéro d’unité logique (LUN) SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="9b613-140">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-141">SCSIPath</span><span class="sxs-lookup"><span data-stu-id="9b613-141">SCSIPath</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b613-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-144">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="9b613-144">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-145">Numéro de bus SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="9b613-145">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-146">SCSIPort</span><span class="sxs-lookup"><span data-stu-id="9b613-146">SCSIPort</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b613-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-149">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="9b613-149">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-150">Numéro SCSI de la carte SCSI.</span><span class="sxs-lookup"><span data-stu-id="9b613-150">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-151">SCSITarget</span><span class="sxs-lookup"><span data-stu-id="9b613-151">SCSITarget</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b613-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-154">Qualificateurs : WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="9b613-154">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-155">Contient le numéro de l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="9b613-155">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-156">SectorsPerTrack</span><span class="sxs-lookup"><span data-stu-id="9b613-156">SectorsPerTrack</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b613-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-159">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="9b613-159">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-160">Nombre de secteurs dans chaque piste pour ce lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="9b613-160">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="9b613-161">TracksPerCylinder</span><span class="sxs-lookup"><span data-stu-id="9b613-161">TracksPerCylinder</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b613-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b613-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b613-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b613-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b613-164">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="9b613-164">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="9b613-165">Nombre de pistes dans chaque cylindre sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="9b613-165">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="9b613-166">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="9b613-166">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="9b613-167">La valeur peut être incorrecte si le lecteur utilise un schéma de traduction pour prendre en charge des tailles de disque à grande capacité.</span><span class="sxs-lookup"><span data-stu-id="9b613-167">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="9b613-168">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="9b613-168">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b613-169">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9b613-169">Requirements</span></span>



| <span data-ttu-id="9b613-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b613-170">Requirement</span></span> | <span data-ttu-id="9b613-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b613-171">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="9b613-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b613-172">Minimum supported client</span></span><br/> | <span data-ttu-id="9b613-173">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b613-173">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9b613-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b613-174">Minimum supported server</span></span><br/> | <span data-ttu-id="9b613-175">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b613-175">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="9b613-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b613-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b613-177">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="9b613-177">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




