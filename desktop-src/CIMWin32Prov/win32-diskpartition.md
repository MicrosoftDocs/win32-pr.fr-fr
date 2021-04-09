---
description: Représente les capacités et la capacité de gestion d’une zone partitionnée d’un disque physique sur un système informatique exécutant Windows.
ms.assetid: 7e78be3f-bae4-4374-abbf-7c4e63ba7593
ms.tgt_platform: multiple
title: Classe Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition
- Win32_DiskPartition.AdditionalAvailability
- Win32_DiskPartition.Availability
- Win32_DiskPartition.PowerManagementCapabilities
- Win32_DiskPartition.IdentifyingDescriptions
- Win32_DiskPartition.MaxQuiesceTime
- Win32_DiskPartition.OtherIdentifyingInfo
- Win32_DiskPartition.StatusInfo
- Win32_DiskPartition.PowerOnHours
- Win32_DiskPartition.TotalPowerOnHours
- Win32_DiskPartition.Access
- Win32_DiskPartition.BlockSize
- Win32_DiskPartition.Bootable
- Win32_DiskPartition.BootPartition
- Win32_DiskPartition.Caption
- Win32_DiskPartition.ConfigManagerErrorCode
- Win32_DiskPartition.ConfigManagerUserConfig
- Win32_DiskPartition.CreationClassName
- Win32_DiskPartition.Description
- Win32_DiskPartition.DeviceID
- Win32_DiskPartition.DiskIndex
- Win32_DiskPartition.ErrorCleared
- Win32_DiskPartition.ErrorDescription
- Win32_DiskPartition.ErrorMethodology
- Win32_DiskPartition.HiddenSectors
- Win32_DiskPartition.Index
- Win32_DiskPartition.InstallDate
- Win32_DiskPartition.LastErrorCode
- Win32_DiskPartition.Name
- Win32_DiskPartition.NumberOfBlocks
- Win32_DiskPartition.PNPDeviceID
- Win32_DiskPartition.PowerManagementSupported
- Win32_DiskPartition.PrimaryPartition
- Win32_DiskPartition.Purpose
- Win32_DiskPartition.RewritePartition
- Win32_DiskPartition.Size
- Win32_DiskPartition.StartingOffset
- Win32_DiskPartition.Status
- Win32_DiskPartition.SystemCreationClassName
- Win32_DiskPartition.SystemName
- Win32_DiskPartition.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4f9a9c16f58d0119c8027848c481479985e7505e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861509"
---
# <a name="win32_diskpartition-class"></a><span data-ttu-id="12836-103">\_Classe DiskPartition Win32</span><span class="sxs-lookup"><span data-stu-id="12836-103">Win32\_DiskPartition class</span></span>

<span data-ttu-id="12836-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ DiskPartition Win32** représente les capacités et la capacité de gestion d’une zone partitionnée d’un disque physique sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="12836-104">The **Win32\_DiskPartition** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a partitioned area of a physical disk on a computer system running Windows.</span></span> <span data-ttu-id="12836-105">Exemple : disque \# 0, partition \# 1.</span><span class="sxs-lookup"><span data-stu-id="12836-105">Example: Disk \#0, Partition \#1.</span></span>

<span data-ttu-id="12836-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="12836-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="12836-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="12836-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12836-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12836-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskPartition : CIM_DiskPartition
{
  unit16   AdditionalAvailability;
  uint16   Availability;
  uint16   PowerManagementCapabilities[];
  string   IdentifyingDescriptions[1];
  uint64   MaxQuiesceTime;
  uint64   OtherIdentifyingInfo;
  uint16   StatusInfo;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  uint16   Access;
  uint64   BlockSize;
  boolean  Bootable;
  boolean  BootPartition;
  string.  Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string.  CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DiskIndex;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   HiddenSectors;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  boolean  RewritePartition;
  uint64   Size;
  uint64   StartingOffset;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   Type;
};
```

## <a name="members"></a><span data-ttu-id="12836-109">Membres</span><span class="sxs-lookup"><span data-stu-id="12836-109">Members</span></span>

<span data-ttu-id="12836-110">La classe **Win32 \_ DiskPartition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="12836-110">The **Win32\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="12836-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="12836-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="12836-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="12836-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12836-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="12836-113">Methods</span></span>

<span data-ttu-id="12836-114">La classe **Win32 \_ DiskPartition** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="12836-114">The **Win32\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="12836-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="12836-115">Method</span></span>                                                     | <span data-ttu-id="12836-116">Description</span><span class="sxs-lookup"><span data-stu-id="12836-116">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12836-117">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="12836-117">**Reset**</span></span>](win32-diskpartition-reset.md)                 | <span data-ttu-id="12836-118">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="12836-118">Requests a reset of the logical device.</span></span><br/>                                                            |
| [<span data-ttu-id="12836-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="12836-119">**SetPowerState**</span></span>](win32-diskpartition-setpowerstate.md) | <span data-ttu-id="12836-120">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="12836-120">Sets the desired power state for a logical device and when a device should be put into that state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="12836-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="12836-121">Properties</span></span>

<span data-ttu-id="12836-122">La classe **Win32 \_ DiskPartition** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="12836-122">The **Win32\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12836-123">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="12836-123">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-124">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12836-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12836-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-126">Accès au média disponible.</span><span class="sxs-lookup"><span data-stu-id="12836-126">Media access available.</span></span>

<span data-ttu-id="12836-127">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12836-127">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12836-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="12836-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="12836-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="12836-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="12836-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="12836-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="12836-131">Accessible en écriture</span><span class="sxs-lookup"><span data-stu-id="12836-131">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="12836-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="12836-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="12836-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="12836-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12836-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="12836-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-135">Type de données : **unit16**</span><span class="sxs-lookup"><span data-stu-id="12836-135">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="12836-136">Type d’accès : écriture seule</span><span class="sxs-lookup"><span data-stu-id="12836-136">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-137">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété Availability.</span><span class="sxs-lookup"><span data-stu-id="12836-137">Additional availability and status of the Device, beyond that specified in the Availability property.</span></span> <span data-ttu-id="12836-138">La propriété de **disponibilité** indique l’état principal et la disponibilité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="12836-138">The **Availability** property denotes the primary status and availability of the Device.</span></span> <span data-ttu-id="12836-139">Dans certains cas, cela ne suffit pas à indiquer l’état complet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="12836-139">In some cases, this will not be sufficient to denote the complete status of the Device.</span></span> <span data-ttu-id="12836-140">Dans ce cas, la propriété **AdditionalAvailability** peut être utilisée pour fournir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="12836-140">In those cases, the **AdditionalAvailability** property can be used to provide further information.</span></span> <span data-ttu-id="12836-141">Par exemple, la **disponibilité** principale d’un appareil peut être hors ligne (valeur = 8), mais il peut également se trouver dans un état d’alimentation faible (valeur **AdditonalAvailability** = 14) ou l’appareil peut exécuter des diagnostics (valeur **AdditionalAvailability** = 5, en test).</span><span class="sxs-lookup"><span data-stu-id="12836-141">For example, a Device's primary **Availability** may be Off line (value=8), but it may also be in a low power state (**AdditonalAvailability** value=14), or the Device could be running Diagnostics (**AdditionalAvailability** value=5, In Test)."</span></span>

<span data-ttu-id="12836-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12836-143">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="12836-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12836-144">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="12836-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="12836-145">**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="12836-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="12836-146">**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="12836-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="12836-147">**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="12836-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12836-148">**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="12836-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="12836-149">**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="12836-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="12836-150">**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="12836-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="12836-151">**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="12836-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12836-152">**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="12836-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="12836-153">**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="12836-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="12836-154">**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="12836-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="12836-155">Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="12836-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="12836-156">Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="12836-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="12836-157">Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="12836-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="12836-158">**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="12836-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="12836-159">Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="12836-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="12836-160">En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="12836-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="12836-161">**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="12836-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="12836-162">**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="12836-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="12836-163">**Suspension** (21)</span><span class="sxs-lookup"><span data-stu-id="12836-163">**Quiesce** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12836-164">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="12836-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12836-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12836-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-167">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="12836-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="12836-168">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="12836-168">Availability and status of the device.</span></span>

<span data-ttu-id="12836-169">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-169">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12836-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="12836-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12836-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="12836-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="12836-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="12836-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="12836-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="12836-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="12836-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="12836-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12836-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="12836-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="12836-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="12836-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="12836-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="12836-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="12836-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="12836-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12836-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="12836-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="12836-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="12836-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="12836-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="12836-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="12836-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="12836-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="12836-183">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="12836-183">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="12836-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="12836-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="12836-185">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="12836-185">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="12836-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="12836-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="12836-187">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="12836-187">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="12836-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="12836-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="12836-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="12836-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="12836-190">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="12836-190">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="12836-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="12836-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="12836-192">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="12836-192">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="12836-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="12836-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="12836-194">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="12836-194">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="12836-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="12836-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="12836-196">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="12836-196">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="12836-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="12836-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="12836-198">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="12836-198">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12836-199">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="12836-199">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-200">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12836-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12836-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-202">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="12836-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="12836-203">Taille en octets des blocs qui forment cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="12836-203">Size in bytes of the blocks which form this storage extent.</span></span> <span data-ttu-id="12836-204">S’il est inconnu ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1.</span><span class="sxs-lookup"><span data-stu-id="12836-204">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="12836-205">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12836-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="12836-206">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12836-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-207">**Démarrable**</span><span class="sxs-lookup"><span data-stu-id="12836-207">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-208">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12836-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12836-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-210">Indique si l’ordinateur peut être démarré à partir de cette partition.</span><span class="sxs-lookup"><span data-stu-id="12836-210">Indicates whether the computer can be booted from this partition.</span></span>

<span data-ttu-id="12836-211">Cette propriété est héritée de la [**\_ DiskPartition CIM**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="12836-211">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-212">**BootPartition**</span><span class="sxs-lookup"><span data-stu-id="12836-212">**BootPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-213">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12836-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12836-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-215">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Functions de fichier \| ReadFile")</span><span class="sxs-lookup"><span data-stu-id="12836-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="12836-216">La partition est la partition active.</span><span class="sxs-lookup"><span data-stu-id="12836-216">Partition is the active partition.</span></span> <span data-ttu-id="12836-217">Le système d’exploitation utilise la partition active lors du démarrage à partir d’un disque dur.</span><span class="sxs-lookup"><span data-stu-id="12836-217">The operating system uses the active partition when booting from a hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="12836-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="12836-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-219">Type de données : **chaîne.**</span><span class="sxs-lookup"><span data-stu-id="12836-219">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="12836-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-221">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="12836-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="12836-222">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12836-222">Short description of the object.</span></span>

<span data-ttu-id="12836-223">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12836-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="12836-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-225">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12836-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12836-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-227">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12836-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12836-228">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="12836-228">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="12836-229">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="12836-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="12836-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="12836-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="12836-231">(0)</span></span>


</dt> <dd>

<span data-ttu-id="12836-232">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="12836-232">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="12836-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="12836-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="12836-234">(1)</span><span class="sxs-lookup"><span data-stu-id="12836-234">(1)</span></span>


</dt> <dd>

<span data-ttu-id="12836-235">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="12836-235">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12836-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="12836-237">(2)</span><span class="sxs-lookup"><span data-stu-id="12836-237">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="12836-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="12836-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="12836-239">(3)</span><span class="sxs-lookup"><span data-stu-id="12836-239">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="12836-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="12836-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="12836-241">(4)</span><span class="sxs-lookup"><span data-stu-id="12836-241">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="12836-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="12836-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="12836-243">(5)</span><span class="sxs-lookup"><span data-stu-id="12836-243">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="12836-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="12836-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="12836-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="12836-245">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="12836-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="12836-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="12836-247">(7)</span><span class="sxs-lookup"><span data-stu-id="12836-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="12836-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="12836-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="12836-249">(8)</span><span class="sxs-lookup"><span data-stu-id="12836-249">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="12836-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="12836-251">(9)</span><span class="sxs-lookup"><span data-stu-id="12836-251">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="12836-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="12836-253">(10)</span><span class="sxs-lookup"><span data-stu-id="12836-253">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="12836-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="12836-255">(11)</span><span class="sxs-lookup"><span data-stu-id="12836-255">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="12836-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="12836-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="12836-257">douze</span><span class="sxs-lookup"><span data-stu-id="12836-257">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="12836-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="12836-259">(13)</span><span class="sxs-lookup"><span data-stu-id="12836-259">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="12836-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="12836-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="12836-261">(14)</span><span class="sxs-lookup"><span data-stu-id="12836-261">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="12836-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="12836-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="12836-263">(15)</span><span class="sxs-lookup"><span data-stu-id="12836-263">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="12836-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="12836-265">(16)</span><span class="sxs-lookup"><span data-stu-id="12836-265">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="12836-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="12836-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="12836-267">(17)</span><span class="sxs-lookup"><span data-stu-id="12836-267">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12836-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="12836-269">(18)</span><span class="sxs-lookup"><span data-stu-id="12836-269">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="12836-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="12836-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="12836-271">(19)</span><span class="sxs-lookup"><span data-stu-id="12836-271">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="12836-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="12836-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="12836-273">(20)</span><span class="sxs-lookup"><span data-stu-id="12836-273">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="12836-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="12836-275">(21)</span><span class="sxs-lookup"><span data-stu-id="12836-275">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="12836-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="12836-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="12836-277">(22)</span><span class="sxs-lookup"><span data-stu-id="12836-277">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="12836-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="12836-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="12836-279">(23)</span><span class="sxs-lookup"><span data-stu-id="12836-279">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="12836-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="12836-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="12836-281">(24)</span><span class="sxs-lookup"><span data-stu-id="12836-281">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="12836-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="12836-283">(25)</span><span class="sxs-lookup"><span data-stu-id="12836-283">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="12836-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="12836-285">(26)</span><span class="sxs-lookup"><span data-stu-id="12836-285">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="12836-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="12836-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="12836-287">(27)</span><span class="sxs-lookup"><span data-stu-id="12836-287">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="12836-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="12836-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="12836-289">(28)</span><span class="sxs-lookup"><span data-stu-id="12836-289">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="12836-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="12836-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="12836-291">(29)</span><span class="sxs-lookup"><span data-stu-id="12836-291">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="12836-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="12836-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="12836-293">(30)</span><span class="sxs-lookup"><span data-stu-id="12836-293">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12836-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="12836-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="12836-295">31</span><span class="sxs-lookup"><span data-stu-id="12836-295">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12836-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="12836-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-297">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12836-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12836-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-299">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12836-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12836-300">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12836-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="12836-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12836-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-303">Type de données : **chaîne.**</span><span class="sxs-lookup"><span data-stu-id="12836-303">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="12836-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-305">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12836-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12836-306">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="12836-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="12836-307">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="12836-307">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="12836-308">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-309">**Description**</span><span class="sxs-lookup"><span data-stu-id="12836-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-312">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="12836-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="12836-313">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12836-313">Description of the object.</span></span>

<span data-ttu-id="12836-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12836-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="12836-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-318">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="12836-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="12836-319">Identificateur unique du lecteur de disque et de la partition, du reste du système.</span><span class="sxs-lookup"><span data-stu-id="12836-319">Unique identifier of the disk drive and partition, from the rest of the system.</span></span>

</dd> <dt>

<span data-ttu-id="12836-320">**DiskIndex**</span><span class="sxs-lookup"><span data-stu-id="12836-320">**DiskIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-321">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12836-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12836-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-323">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Functions de fichier \| ReadFile")</span><span class="sxs-lookup"><span data-stu-id="12836-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="12836-324">Numéro d’index du disque contenant cette partition.</span><span class="sxs-lookup"><span data-stu-id="12836-324">Index number of the disk containing this partition.</span></span>

<span data-ttu-id="12836-325">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="12836-325">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="12836-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="12836-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-327">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12836-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12836-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-329">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="12836-329">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="12836-330">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="12836-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-332">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-334">Informations sur l’erreur enregistrée dans **LastErrorCode**, et informations sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="12836-334">Information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="12836-335">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-336">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="12836-336">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-339">Type de détection d’erreur et de correction pris en charge par cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="12836-339">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="12836-340">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12836-340">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-341">**HiddenSectors**</span><span class="sxs-lookup"><span data-stu-id="12836-341">**HiddenSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-342">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12836-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12836-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-344">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api")</span><span class="sxs-lookup"><span data-stu-id="12836-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span></span>
</dt> </dl>

<span data-ttu-id="12836-345">Nombre de secteurs masqués dans la partition.</span><span class="sxs-lookup"><span data-stu-id="12836-345">Number of hidden sectors in the partition.</span></span>

<span data-ttu-id="12836-346">Exemple : 63</span><span class="sxs-lookup"><span data-stu-id="12836-346">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="12836-347">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="12836-347">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-348">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="12836-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="12836-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-350">Tableau de chaînes de forme libre fournissant des explications et des détails sur les entrées du tableau OtherIdentifyingInfo.</span><span class="sxs-lookup"><span data-stu-id="12836-350">An array of free-form strings providing explanations and details behind the entries in the OtherIdentifyingInfo array.</span></span> <span data-ttu-id="12836-351">Notez que chaque entrée de ce tableau est liée à l’entrée dans OtherIdentifyingInfo qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="12836-351">Note, each entry of this array is related to the entry in OtherIdentifyingInfo that is located at the same index.</span></span>

<span data-ttu-id="12836-352">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-353">**Index**</span><span class="sxs-lookup"><span data-stu-id="12836-353">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-354">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12836-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12836-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-356">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="12836-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="12836-357">Numéro d’index de la partition.</span><span class="sxs-lookup"><span data-stu-id="12836-357">Index number of the partition.</span></span>

<span data-ttu-id="12836-358">Exemple : 1</span><span class="sxs-lookup"><span data-stu-id="12836-358">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="12836-359">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="12836-359">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-360">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="12836-360">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="12836-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-362">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="12836-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="12836-363">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="12836-363">Date the object was installed.</span></span> <span data-ttu-id="12836-364">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="12836-364">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="12836-365">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12836-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-366">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="12836-366">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-367">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12836-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12836-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-369">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="12836-369">Last error code reported by the logical device.</span></span>

<span data-ttu-id="12836-370">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-371">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="12836-371">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-372">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12836-372">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12836-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-374">Qualificateurs : **déconseillée**</span><span class="sxs-lookup"><span data-stu-id="12836-374">Qualifiers: **Depricated**</span></span>
</dt> </dl>

<span data-ttu-id="12836-375">Durée maximale, en millisecondes, pendant laquelle un appareil peut s’exécuter dans un état de veille.</span><span class="sxs-lookup"><span data-stu-id="12836-375">Maximum time in milliseconds, that a Device can run in a Quiesced state.</span></span> <span data-ttu-id="12836-376">L’état d’un appareil est défini dans ses propriétés Availability et AdditionalAvailability, où le ralentissement est transmis par la valeur 21.</span><span class="sxs-lookup"><span data-stu-id="12836-376">A Device's state is defined in its Availability and AdditionalAvailability properties, where Quiesced is conveyed by the value 21.</span></span> <span data-ttu-id="12836-377">Ce qui se produit à la fin de la limite de temps est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="12836-377">What occurs at the end of the time limit is device-specific.</span></span> <span data-ttu-id="12836-378">L’appareil peut être devrez démarrer, peut être hors connexion ou prendre d’autres mesures.</span><span class="sxs-lookup"><span data-stu-id="12836-378">The Device may unquiesce, may offline or take other action.</span></span> <span data-ttu-id="12836-379">La valeur 0 indique qu’un appareil peut rester indéfiniment suspendu.</span><span class="sxs-lookup"><span data-stu-id="12836-379">A value of 0 indicates that a Device can remain quiesced indefinitely.</span></span>

> [!Note]
>
> <span data-ttu-id="12836-380">«La propriété MaxQuiesceTime a été dépréciée.</span><span class="sxs-lookup"><span data-stu-id="12836-380">"The MaxQuiesceTime property has been deprecated.</span></span> <span data-ttu-id="12836-381">Lors de l’évaluation de l’utilisation de la suspension, il a été déterminé que cette propriété unique ne permet pas de décrire le moment où un appareil quitte automatiquement un état de repos.</span><span class="sxs-lookup"><span data-stu-id="12836-381">When evaluating the use of Quiesce, it was determine that this single property is not adequate for describing when a device will automatically exit a quiescent state.</span></span> <span data-ttu-id="12836-382">En fait, le scénario le plus probable pour un appareil pour quitter un état de repos a été déterminé comme étant basé sur le nombre de demandes en attente, plutôt que sur une durée maximale.</span><span class="sxs-lookup"><span data-stu-id="12836-382">In fact, the most likely scenario for a device to exit a quiescent state was determined to be based on the number of outstanding requests queued rather than on a maximum time.</span></span> <span data-ttu-id="12836-383">Elle sera réévaluée et repositionnée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="12836-383">This will be re-evaluated and repositioned later.</span></span> <span data-ttu-id="12836-384">\\n</span><span class="sxs-lookup"><span data-stu-id="12836-384">\\n</span></span>

 

<span data-ttu-id="12836-385">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-386">**Nom**</span><span class="sxs-lookup"><span data-stu-id="12836-386">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-389">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="12836-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="12836-390">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="12836-390">Label by which the object is known.</span></span> <span data-ttu-id="12836-391">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="12836-391">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="12836-392">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12836-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-393">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="12836-393">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-394">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12836-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12836-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-396">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="12836-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="12836-397">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="12836-397">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="12836-398">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="12836-398">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="12836-399">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="12836-399">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="12836-400">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12836-400">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="12836-401">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12836-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="12836-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-403">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12836-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12836-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-405">Tableau qui capture des données supplémentaires, au-delà des informations DeviceID, qui peuvent être utilisées pour identifier un LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="12836-405">Array that captures additional data, beyond DeviceID information, that could be used to identify a LogicalDevice.</span></span> <span data-ttu-id="12836-406">Par exemple, vous pouvez conserver le nom convivial du système d’exploitation de l’appareil dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="12836-406">One example would be to hold the Operating System's user friendly name for the Device in this property.</span></span> <span data-ttu-id="12836-407">La longueur maximale est de 256.</span><span class="sxs-lookup"><span data-stu-id="12836-407">Maximum length is 256.</span></span>

<span data-ttu-id="12836-408">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-409">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="12836-409">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-410">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-412">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12836-412">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12836-413">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="12836-413">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="12836-414">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="12836-414">Example: "\*PNP030b"</span></span>

<span data-ttu-id="12836-415">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-416">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="12836-416">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-417">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12836-417">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="12836-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-419">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="12836-419">Indicates the specific power-related capabilities of the logical device.</span></span> <span data-ttu-id="12836-420">Les valeurs de tableau, 0 = « inconnu », 1 = « non pris en charge » et 2 = « désactivé » sont explicites.</span><span class="sxs-lookup"><span data-stu-id="12836-420">The array values, 0="Unknown", 1="Not Supported" and 2="Disabled" are self-explanatory.</span></span> <span data-ttu-id="12836-421">La valeur 3 = « activé » indique que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais que le jeu de caractéristiques exact est inconnu ou que les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="12836-421">The value, 3="Enabled" indicates that the power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span> <span data-ttu-id="12836-422">« Modes d’économie d’énergie entrés automatiquement » (4) indique qu’un appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="12836-422">"Power Saving Modes Entered Automatically" (4) describes that a device can change its power state based on usage or other criteria.</span></span> <span data-ttu-id="12836-423">« Power State définissable » (5) indique que la méthode SetPowerState est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="12836-423">"Power State Settable" (5) indicates that the SetPowerState method is supported.</span></span> <span data-ttu-id="12836-424">« Cycle d’alimentation pris en charge » (6) indique que la méthode SetPowerState peut être appelée avec la variable d’entrée PowerState définie sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="12836-424">"Power Cycling Supported" (6) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle").</span></span> <span data-ttu-id="12836-425">« Mise sous tension minutée prise en charge » (7) indique que la méthode SetPowerState peut être appelée avec la variable d’entrée PowerState définie sur 5 (« Power cycle ») et le paramètre Time défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="12836-425">"Timed Power On Supported" (7) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle") and the Time parameter set to a specific date and time, or interval, for power-on.</span></span>

<span data-ttu-id="12836-426">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12836-427">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="12836-427">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="12836-428">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="12836-428">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12836-429">**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="12836-429">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12836-430">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="12836-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="12836-431">**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="12836-431">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="12836-432">**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="12836-432">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="12836-433">**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="12836-433">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="12836-434">**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="12836-434">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12836-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="12836-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-436">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12836-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12836-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-438">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="12836-438">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="12836-439">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="12836-439">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="12836-440">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-441">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="12836-441">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-442">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12836-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12836-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-444">Nombre d’heures consécutives pendant lesquelles ce périphérique a été alimenté depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="12836-444">The number of consecutive hours that this Device has been powered, since its last power cycle.</span></span>

<span data-ttu-id="12836-445">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-446">**Partition principale**</span><span class="sxs-lookup"><span data-stu-id="12836-446">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-447">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12836-447">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12836-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-449">Si la **valeur est true**, il s’agit de la partition principale.</span><span class="sxs-lookup"><span data-stu-id="12836-449">If **True**, this is the primary partition.</span></span>

<span data-ttu-id="12836-450">Cette propriété est héritée de la [**\_ DiskPartition CIM**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="12836-450">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-451">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="12836-451">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-452">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-454">Description du support et de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="12836-454">Description of the media and its use.</span></span>

<span data-ttu-id="12836-455">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12836-455">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-456">**RewritePartition**</span><span class="sxs-lookup"><span data-stu-id="12836-456">**RewritePartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-457">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="12836-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12836-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-459">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api \| [**\_**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RewritePartition")</span><span class="sxs-lookup"><span data-stu-id="12836-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RewritePartition")</span></span>
</dt> </dl>

<span data-ttu-id="12836-460">Si la **valeur est true**, les informations de partition ont changé.</span><span class="sxs-lookup"><span data-stu-id="12836-460">If **True**, the partition information has changed.</span></span> <span data-ttu-id="12836-461">Lorsque vous modifiez une partition (avec [**la \_ \_ disposition de \_ lecteur \_ du jeu de disques IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), le système utilise cette propriété pour déterminer les partitions qui ont changé et dont les informations doivent être réécrites.</span><span class="sxs-lookup"><span data-stu-id="12836-461">When you change a partition (with [**IOCTL\_DISK\_SET\_DRIVE\_LAYOUT**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), the system uses this property to determine which partitions have changed and need their information rewritten.</span></span> <span data-ttu-id="12836-462">Si la **valeur est true**, la partition doit être réécrite.</span><span class="sxs-lookup"><span data-stu-id="12836-462">If **TRUE**, the partition must be rewritten.</span></span>

</dd> <dt>

<span data-ttu-id="12836-463">**Taille**</span><span class="sxs-lookup"><span data-stu-id="12836-463">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-464">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12836-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12836-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-466">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Functions de fichier \| ReadFile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="12836-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="12836-467">Taille totale de la partition.</span><span class="sxs-lookup"><span data-stu-id="12836-467">Total size of the partition.</span></span>

<span data-ttu-id="12836-468">Exemple : 1059045376</span><span class="sxs-lookup"><span data-stu-id="12836-468">Example: 1059045376</span></span>

<span data-ttu-id="12836-469">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12836-469">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="12836-470">**StartingOffset**</span><span class="sxs-lookup"><span data-stu-id="12836-470">**StartingOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-471">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12836-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12836-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-473">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Functions de fichier \| ReadFile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="12836-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="12836-474">Décalage de départ (en octets) de la partition.</span><span class="sxs-lookup"><span data-stu-id="12836-474">Starting offset (in bytes) of the partition.</span></span>

<span data-ttu-id="12836-475">Exemple : 32256</span><span class="sxs-lookup"><span data-stu-id="12836-475">Example: 32256</span></span>

<span data-ttu-id="12836-476">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12836-476">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="12836-477">**État**</span><span class="sxs-lookup"><span data-stu-id="12836-477">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-478">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-479">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-480">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="12836-480">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="12836-481">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12836-481">Current status of the object.</span></span> <span data-ttu-id="12836-482">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="12836-482">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="12836-483">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="12836-483">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="12836-484">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="12836-484">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="12836-485">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="12836-485">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="12836-486">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="12836-486">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="12836-487">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12836-487">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="12836-488">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="12836-488">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="12836-489">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="12836-489">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="12836-490">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="12836-490">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12836-491">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="12836-491">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12836-492">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="12836-492">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="12836-493">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="12836-493">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="12836-494">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="12836-494">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="12836-495">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="12836-495">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="12836-496">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="12836-496">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="12836-497">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="12836-497">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="12836-498">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="12836-498">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="12836-499">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="12836-499">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="12836-500">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="12836-500">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12836-501">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="12836-501">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-502">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12836-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12836-503">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-504">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="12836-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="12836-505">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="12836-505">State of the logical device.</span></span> <span data-ttu-id="12836-506">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="12836-506">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="12836-507">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12836-508">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="12836-508">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12836-509">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="12836-509">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12836-510">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="12836-510">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12836-511">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="12836-511">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12836-512">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="12836-512">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12836-513">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12836-513">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-514">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-515">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-516">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12836-516">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12836-517">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="12836-517">Creation class name of the scoping system.</span></span>

<span data-ttu-id="12836-518">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-518">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-519">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="12836-519">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-520">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-521">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-522">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12836-522">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12836-523">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="12836-523">Name of the scoping system.</span></span>

<span data-ttu-id="12836-524">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-525">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="12836-525">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-526">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12836-526">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12836-527">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12836-528">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="12836-528">The total number of hours that this device has been powered.</span></span>

<span data-ttu-id="12836-529">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12836-529">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12836-530">**Type**</span><span class="sxs-lookup"><span data-stu-id="12836-530">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12836-531">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12836-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12836-532">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12836-532">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12836-533">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| PartitionRecord \| dwPartitionType")</span><span class="sxs-lookup"><span data-stu-id="12836-533">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|PartitionRecord\|dwPartitionType")</span></span>
</dt> </dl>

<span data-ttu-id="12836-534">Type de la partition.</span><span class="sxs-lookup"><span data-stu-id="12836-534">Type of the partition.</span></span>

<span data-ttu-id="12836-535">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="12836-535">The values are:</span></span>

<dl> <dd><span data-ttu-id="12836-536">Inutilisé</span><span class="sxs-lookup"><span data-stu-id="12836-536">"Unused"</span></span></dd> <dd><span data-ttu-id="12836-537">« FAT 12 bits »</span><span class="sxs-lookup"><span data-stu-id="12836-537">"12-bit FAT"</span></span></dd> <dd><span data-ttu-id="12836-538">« XENIX type 1 »</span><span class="sxs-lookup"><span data-stu-id="12836-538">"Xenix Type 1"</span></span></dd> <dd><span data-ttu-id="12836-539">« XENIX type 2 »</span><span class="sxs-lookup"><span data-stu-id="12836-539">"Xenix Type 2"</span></span></dd> <dd><span data-ttu-id="12836-540">« FAT 16 bits »</span><span class="sxs-lookup"><span data-stu-id="12836-540">"16-bit FAT"</span></span></dd> <dd><span data-ttu-id="12836-541">« Partition étendue »</span><span class="sxs-lookup"><span data-stu-id="12836-541">"Extended Partition"</span></span></dd> <dd><span data-ttu-id="12836-542">« Énorme de MS-DOS v4 »</span><span class="sxs-lookup"><span data-stu-id="12836-542">"MS-DOS V4 Huge"</span></span></dd> <dd><span data-ttu-id="12836-543">« Système de fichiers installable »</span><span class="sxs-lookup"><span data-stu-id="12836-543">"Installable File System"</span></span></dd> <dd><span data-ttu-id="12836-544">« Plateforme de référence PowerPC »</span><span class="sxs-lookup"><span data-stu-id="12836-544">"PowerPC Reference Platform"</span></span></dd> <dd><span data-ttu-id="12836-545">ENVIRONNEMENTS</span><span class="sxs-lookup"><span data-stu-id="12836-545">"UNIX"</span></span></dd> <dd><span data-ttu-id="12836-546">NTFS</span><span class="sxs-lookup"><span data-stu-id="12836-546">"NTFS"</span></span></dd> <dd><span data-ttu-id="12836-547">« Win95 avec l’extension int 13 »</span><span class="sxs-lookup"><span data-stu-id="12836-547">"Win95 w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="12836-548">"Étendu avec extension int 13"</span><span class="sxs-lookup"><span data-stu-id="12836-548">"Extended w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="12836-549">« Gestionnaire de disque logique »</span><span class="sxs-lookup"><span data-stu-id="12836-549">"Logical Disk Manager"</span></span></dd> <dd><span data-ttu-id="12836-550">Connue</span><span class="sxs-lookup"><span data-stu-id="12836-550">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Unused"></span><span id="unused"></span><span id="UNUSED"></span>

<span data-ttu-id="12836-551">**Inutilisé** ("inutilisé")</span><span class="sxs-lookup"><span data-stu-id="12836-551">**Unused** ("Unused")</span></span>


</dt> <dd></dd> <dt>

<span id="12-bit_FAT"></span><span id="12-bit_fat"></span><span id="12-BIT_FAT"></span>

<span data-ttu-id="12836-552">**FAT 12 bits** (« FAT 12 bits »)</span><span class="sxs-lookup"><span data-stu-id="12836-552">**12-bit FAT** ("12-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_1"></span><span id="xenix_type_1"></span><span id="XENIX_TYPE_1"></span>

<span data-ttu-id="12836-553">**Type XENIX 1** (« XENIX type 1 »)</span><span class="sxs-lookup"><span data-stu-id="12836-553">**Xenix Type 1** ("Xenix Type 1")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_2"></span><span id="xenix_type_2"></span><span id="XENIX_TYPE_2"></span>

<span data-ttu-id="12836-554">**XENIX, type 2** (« XENIX type 2 »)</span><span class="sxs-lookup"><span data-stu-id="12836-554">**Xenix Type 2** ("Xenix Type 2")</span></span>


</dt> <dd></dd> <dt>

<span id="16-bit_FAT"></span><span id="16-bit_fat"></span><span id="16-BIT_FAT"></span>

<span data-ttu-id="12836-555">**FAT 16 bits** ("16 bits Fat")</span><span class="sxs-lookup"><span data-stu-id="12836-555">**16-bit FAT** ("16-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Partition"></span><span id="extended_partition"></span><span id="EXTENDED_PARTITION"></span>

<span data-ttu-id="12836-556">**Partition étendue** (« partition étendue »)</span><span class="sxs-lookup"><span data-stu-id="12836-556">**Extended Partition** ("Extended Partition")</span></span>


</dt> <dd></dd> <dt>

<span id="MS-DOS_V4_Huge"></span><span id="ms-dos_v4_huge"></span><span id="MS-DOS_V4_HUGE"></span>

<span data-ttu-id="12836-557">L' **énorme de MS-DOS v4** (« MS-DOS v4 énorme »)</span><span class="sxs-lookup"><span data-stu-id="12836-557">**MS-DOS V4 Huge** ("MS-DOS V4 Huge")</span></span>


</dt> <dd></dd> <dt>

<span id="Installable_File_System"></span><span id="installable_file_system"></span><span id="INSTALLABLE_FILE_SYSTEM"></span>

<span data-ttu-id="12836-558">**Installation du système de fichiers** (« système de fichiers installable »)</span><span class="sxs-lookup"><span data-stu-id="12836-558">**Installable File System** ("Installable File System")</span></span>


</dt> <dd></dd> <dt>

<span id="PowerPC_Reference_Platform"></span><span id="powerpc_reference_platform"></span><span id="POWERPC_REFERENCE_PLATFORM"></span>

<span data-ttu-id="12836-559">**Plateforme de référence powerpc** (« plateforme de référence PowerPC »)</span><span class="sxs-lookup"><span data-stu-id="12836-559">**PowerPC Reference Platform** ("PowerPC Reference Platform")</span></span>


</dt> <dd></dd> <dt>

<span id="UNIX"></span><span id="unix"></span>

<span data-ttu-id="12836-560">**UNIX** (« UNIX »)</span><span class="sxs-lookup"><span data-stu-id="12836-560">**UNIX** ("UNIX")</span></span>


</dt> <dd></dd> <dt>

<span id="NTFS"></span><span id="ntfs"></span>

<span data-ttu-id="12836-561">**NTFS** (« NTFS »)</span><span class="sxs-lookup"><span data-stu-id="12836-561">**NTFS** ("NTFS")</span></span>


</dt> <dd></dd> <dt>

<span id="Win95_w_Extended_Int_13"></span><span id="win95_w_extended_int_13"></span><span id="WIN95_W_EXTENDED_INT_13"></span>

<span data-ttu-id="12836-562">**Win95 avec l’extension int 13** (« Win95 w/Extended int 13 »)</span><span class="sxs-lookup"><span data-stu-id="12836-562">**Win95 w/Extended Int 13** ("Win95 w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_w_Extended_Int_13"></span><span id="extended_w_extended_int_13"></span><span id="EXTENDED_W_EXTENDED_INT_13"></span>

<span data-ttu-id="12836-563">**Extended avec entier 13 13** (« étendu avec extension int 13 »)</span><span class="sxs-lookup"><span data-stu-id="12836-563">**Extended w/Extended Int 13** ("Extended w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk_Manager"></span><span id="logical_disk_manager"></span><span id="LOGICAL_DISK_MANAGER"></span>

<span data-ttu-id="12836-564">**Gestionnaire de disque logique** (« Logical Disk Manager »)</span><span class="sxs-lookup"><span data-stu-id="12836-564">**Logical Disk Manager** ("Logical Disk Manager")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12836-565">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="12836-565">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="12836-566"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="12836-566"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="12836-567">Notes</span><span class="sxs-lookup"><span data-stu-id="12836-567">Remarks</span></span>

<span data-ttu-id="12836-568">La classe **Win32 \_ DiskPartition** est dérivée de [**CIM \_ DiskPartition**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="12836-568">The **Win32\_DiskPartition** class is derived from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

<span data-ttu-id="12836-569">Une partition est une division structurelle d’un lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="12836-569">A partition is a structural division of a physical disk drive.</span></span> <span data-ttu-id="12836-570">Bien qu’un lecteur puisse contenir une seule partition, les volumes plus grands sont souvent divisés en plusieurs partitions.</span><span class="sxs-lookup"><span data-stu-id="12836-570">Although a drive can contain a single partition, larger volumes are often divided into multiple partitions.</span></span> <span data-ttu-id="12836-571">C’est la raison pour laquelle vous pouvez avoir des lecteurs C, D et E, même si votre ordinateur ne dispose que d’un seul disque dur physique.</span><span class="sxs-lookup"><span data-stu-id="12836-571">This is why you might have drives C, D, and E even though your computer has only a single physical hard disk.</span></span>

<span data-ttu-id="12836-572">Windows prend en charge les types de partition suivants :</span><span class="sxs-lookup"><span data-stu-id="12836-572">Windows supports the following partition types:</span></span>

-   <span data-ttu-id="12836-573">Partition principale.</span><span class="sxs-lookup"><span data-stu-id="12836-573">Primary partition.</span></span> <span data-ttu-id="12836-574">Il s’agit du seul type de partition qui peut avoir un système d’exploitation installé.</span><span class="sxs-lookup"><span data-stu-id="12836-574">This is the only type of partition that can have an operating system installed.</span></span> <span data-ttu-id="12836-575">Chaque lecteur peut avoir jusqu’à quatre partitions principales, chacune ayant une lettre de lecteur différente.</span><span class="sxs-lookup"><span data-stu-id="12836-575">Each drive can have as many as four primary partitions, each assigned a different drive letter.</span></span>
-   <span data-ttu-id="12836-576">Partition étendue.</span><span class="sxs-lookup"><span data-stu-id="12836-576">Extended partition.</span></span> <span data-ttu-id="12836-577">Partition supplémentaire qui peut être divisée en plusieurs lecteurs logiques, chacun affecté une lettre de lecteur unique.</span><span class="sxs-lookup"><span data-stu-id="12836-577">An additional partition that can be subdivided into multiple logical drives, each assigned a unique drive letter.</span></span> <span data-ttu-id="12836-578">Un lecteur ne peut avoir qu’une seule partition étendue ; Toutefois, vous pouvez diviser cette partition en plusieurs lecteurs logiques.</span><span class="sxs-lookup"><span data-stu-id="12836-578">A drive can have only one extended partition; however, you can divide this partition into multiple logical drives.</span></span> <span data-ttu-id="12836-579">Cela permet à un disque d’avoir plus que les quatre partitions principales autorisées.</span><span class="sxs-lookup"><span data-stu-id="12836-579">This enables a disk to have more than just the four allowed primary partitions.</span></span>
-   <span data-ttu-id="12836-580">Partition système.</span><span class="sxs-lookup"><span data-stu-id="12836-580">System partition.</span></span> <span data-ttu-id="12836-581">Toute partition principale contenant un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="12836-581">Any primary partition containing an operating system.</span></span>

<span data-ttu-id="12836-582">Les partitions peuvent vous indiquer comment un lecteur de disque physique est réellement utilisé.</span><span class="sxs-lookup"><span data-stu-id="12836-582">Partitions can tell you how a physical disk drive is actually being used.</span></span> <span data-ttu-id="12836-583">En examinant les partitions physiques sur un disque, vous pouvez déterminer les types d’éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="12836-583">By examining the physical partitions on a disk, you can determine the following types of things:</span></span>

-   <span data-ttu-id="12836-584">Comment le disque a été divisé en lecteurs logiques.</span><span class="sxs-lookup"><span data-stu-id="12836-584">How the disk has been divided into logical drives.</span></span>
-   <span data-ttu-id="12836-585">Si de l’espace non partitionné est disponible sur le disque.</span><span class="sxs-lookup"><span data-stu-id="12836-585">If there is unpartitioned space available on the disk.</span></span> <span data-ttu-id="12836-586">Cela peut être déterminé en soustrayant la taille de toutes les partitions sur un disque de la taille du disque lui-même.</span><span class="sxs-lookup"><span data-stu-id="12836-586">This can be determined by subtracting the size of all the partitions on a disk from the size of the disk itself.</span></span>
-   <span data-ttu-id="12836-587">Si vous pouvez démarrer l’ordinateur à partir de ce disque (c’est-à-dire que le disque contient une partition de démarrage).</span><span class="sxs-lookup"><span data-stu-id="12836-587">If you can boot the computer from that disk (that is, does the disk contain a boot partition).</span></span>

<span data-ttu-id="12836-588">Toutes ces questions peuvent être résolues à l’aide de la classe **Win32 \_ DiskPartition** .</span><span class="sxs-lookup"><span data-stu-id="12836-588">All these questions can be resolved by using the **Win32\_DiskPartition** class.</span></span>

## <a name="examples"></a><span data-ttu-id="12836-589">Exemples</span><span class="sxs-lookup"><span data-stu-id="12836-589">Examples</span></span>

<span data-ttu-id="12836-590">L’exemple de code PowerShell suivant vérifie l’alignement des disques sur un ordinateur : si le décalage est fractionnaire, le disque n’est pas correctement aligné.</span><span class="sxs-lookup"><span data-stu-id="12836-590">The following PowerShell code sample checks the alignment of disks on a computer: if the offset is fractional, the disk is not aligned correctly.</span></span>


```PowerShell
$wql = "SELECT DiskIndex,Index,StartingOffset FROM Win32_DiskPartition"
Get-WmiObject -Query $wql -ComputerName '.' | Select-Object DiskIndex,Index,@{Name='Offset (KB)';Expression={$_.StartingOffset / 1024}} | Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="12836-591">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12836-591">Requirements</span></span>



| <span data-ttu-id="12836-592">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12836-592">Requirement</span></span> | <span data-ttu-id="12836-593">Valeur</span><span class="sxs-lookup"><span data-stu-id="12836-593">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12836-594">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12836-594">Minimum supported client</span></span><br/> | <span data-ttu-id="12836-595">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12836-595">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12836-596">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12836-596">Minimum supported server</span></span><br/> | <span data-ttu-id="12836-597">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12836-597">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12836-598">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="12836-598">Namespace</span></span><br/>                | <span data-ttu-id="12836-599">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="12836-599">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12836-600">MOF</span><span class="sxs-lookup"><span data-stu-id="12836-600">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12836-601"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12836-601"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12836-602">DLL</span><span class="sxs-lookup"><span data-stu-id="12836-602">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12836-603"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12836-603"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12836-604">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12836-604">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12836-605">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="12836-605">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

<span data-ttu-id="12836-606">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12836-606">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="12836-607">Tâches WMI : disques et systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="12836-607">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

