---
description: Représente un lecteur de disque physique tel qu’il est vu par un ordinateur exécutant le système d’exploitation Windows.
ms.assetid: c1fc6a1e-e725-484b-aacf-279f777e9b19
ms.tgt_platform: multiple
title: Win32_DiskDrive, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDrive
- Win32_DiskDrive.Reset
- Win32_DiskDrive.SetPowerState
- Win32_DiskDrive.Availability
- Win32_DiskDrive.BytesPerSector
- Win32_DiskDrive.Capabilities
- Win32_DiskDrive.CapabilityDescriptions
- Win32_DiskDrive.Caption
- Win32_DiskDrive.CompressionMethod
- Win32_DiskDrive.ConfigManagerErrorCode
- Win32_DiskDrive.ConfigManagerUserConfig
- Win32_DiskDrive.CreationClassName
- Win32_DiskDrive.DefaultBlockSize
- Win32_DiskDrive.Description
- Win32_DiskDrive.DeviceID
- Win32_DiskDrive.ErrorCleared
- Win32_DiskDrive.ErrorDescription
- Win32_DiskDrive.ErrorMethodology
- Win32_DiskDrive.FirmwareRevision
- Win32_DiskDrive.Index
- Win32_DiskDrive.InstallDate
- Win32_DiskDrive.InterfaceType
- Win32_DiskDrive.LastErrorCode
- Win32_DiskDrive.Manufacturer
- Win32_DiskDrive.MaxBlockSize
- Win32_DiskDrive.MaxMediaSize
- Win32_DiskDrive.MediaLoaded
- Win32_DiskDrive.MediaType
- Win32_DiskDrive.MinBlockSize
- Win32_DiskDrive.Model
- Win32_DiskDrive.Name
- Win32_DiskDrive.NeedsCleaning
- Win32_DiskDrive.NumberOfMediaSupported
- Win32_DiskDrive.Partitions
- Win32_DiskDrive.PNPDeviceID
- Win32_DiskDrive.PowerManagementCapabilities
- Win32_DiskDrive.PowerManagementSupported
- Win32_DiskDrive.SCSIBus
- Win32_DiskDrive.SCSILogicalUnit
- Win32_DiskDrive.SCSIPort
- Win32_DiskDrive.SCSITargetId
- Win32_DiskDrive.SectorsPerTrack
- Win32_DiskDrive.SerialNumber
- Win32_DiskDrive.Signature
- Win32_DiskDrive.Size
- Win32_DiskDrive.Status
- Win32_DiskDrive.StatusInfo
- Win32_DiskDrive.SystemCreationClassName
- Win32_DiskDrive.SystemName
- Win32_DiskDrive.TotalCylinders
- Win32_DiskDrive.TotalHeads
- Win32_DiskDrive.TotalSectors
- Win32_DiskDrive.TotalTracks
- Win32_DiskDrive.TracksPerCylinder
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 751dee053574be417cb312f6b046ae6b7703d543
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523983"
---
# <a name="win32_diskdrive-class"></a><span data-ttu-id="46a6f-103">\_Classe DiskDrive Win32</span><span class="sxs-lookup"><span data-stu-id="46a6f-103">Win32\_DiskDrive class</span></span>

<span data-ttu-id="46a6f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskDrive** WMI représente un lecteur de disque physique tel qu’il est vu par un ordinateur exécutant le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="46a6f-104">The **Win32\_DiskDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical disk drive as seen by a computer running the Windows operating system.</span></span>

<span data-ttu-id="46a6f-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="46a6f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="46a6f-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="46a6f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="46a6f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46a6f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDrive : CIM_DiskDrive
{
  uint16   Availability;
  uint32   BytesPerSector;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FirmwareRevision;
  uint32   Index;
  datetime InstallDate;
  string   InterfaceType;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  uint64   MinBlockSize;
  string   Model;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Partitions;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  uint32   SectorsPerTrack;
  string   SerialNumber;
  uint32   Signature;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   TotalCylinders;
  uint32   TotalHeads;
  uint64   TotalSectors;
  uint64   TotalTracks;
  uint32   TracksPerCylinder;
};
```

## <a name="members"></a><span data-ttu-id="46a6f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="46a6f-108">Members</span></span>

<span data-ttu-id="46a6f-109">La classe **Win32 \_ DiskDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46a6f-109">The **Win32\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="46a6f-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46a6f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="46a6f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46a6f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="46a6f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46a6f-112">Methods</span></span>

<span data-ttu-id="46a6f-113">La classe **Win32 \_ DiskDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="46a6f-113">The **Win32\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="46a6f-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="46a6f-114">Method</span></span>            | <span data-ttu-id="46a6f-115">Description</span><span class="sxs-lookup"><span data-stu-id="46a6f-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a6f-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="46a6f-116">**Reset**</span></span>         | <span data-ttu-id="46a6f-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="46a6f-117">Not implemented.</span></span> <span data-ttu-id="46a6f-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ DiskDrive**](cim-diskdrive.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="46a6f-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="46a6f-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="46a6f-119">**SetPowerState**</span></span> | <span data-ttu-id="46a6f-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="46a6f-120">Not implemented.</span></span> <span data-ttu-id="46a6f-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ DiskDrive**](cim-diskdrive.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="46a6f-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="46a6f-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46a6f-122">Properties</span></span>

<span data-ttu-id="46a6f-123">La classe **Win32 \_ DiskDrive** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="46a6f-123">The **Win32\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46a6f-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="46a6f-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46a6f-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-127">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="46a6f-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-128">Availability and status of the device.</span></span>

<span data-ttu-id="46a6f-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46a6f-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="46a6f-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46a6f-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="46a6f-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="46a6f-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="46a6f-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="46a6f-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="46a6f-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="46a6f-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="46a6f-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="46a6f-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="46a6f-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="46a6f-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="46a6f-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="46a6f-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="46a6f-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="46a6f-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="46a6f-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="46a6f-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="46a6f-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="46a6f-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="46a6f-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="46a6f-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="46a6f-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="46a6f-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="46a6f-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="46a6f-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="46a6f-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="46a6f-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="46a6f-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="46a6f-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="46a6f-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="46a6f-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="46a6f-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="46a6f-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="46a6f-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="46a6f-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="46a6f-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="46a6f-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="46a6f-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="46a6f-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="46a6f-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="46a6f-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="46a6f-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="46a6f-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="46a6f-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="46a6f-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-156">Le lecteur de disque n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="46a6f-156">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46a6f-157">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="46a6f-157">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-158">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-160">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api- \| [**\_ géométrie de disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| BytesPerSector"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("octets")</span><span class="sxs-lookup"><span data-stu-id="46a6f-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|BytesPerSector"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-161">Nombre d’octets dans chaque secteur pour le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-161">Number of bytes in each sector for the physical disk drive.</span></span>

<span data-ttu-id="46a6f-162">Exemple : 512</span><span class="sxs-lookup"><span data-stu-id="46a6f-162">Example: 512</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="46a6f-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-164">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46a6f-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-166">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="46a6f-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-167">Tableau de fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="46a6f-167">Array of capabilities of the media access device.</span></span> <span data-ttu-id="46a6f-168">Par exemple, l’appareil peut prendre en charge l’accès aléatoire (3), le support amovible (7) et le nettoyage automatique (9).</span><span class="sxs-lookup"><span data-stu-id="46a6f-168">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="46a6f-169">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46a6f-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="46a6f-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46a6f-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="46a6f-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="46a6f-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="46a6f-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="46a6f-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="46a6f-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="46a6f-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="46a6f-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="46a6f-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="46a6f-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="46a6f-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="46a6f-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="46a6f-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="46a6f-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-178">Prend en charge les supports amovibles</span><span class="sxs-lookup"><span data-stu-id="46a6f-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="46a6f-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="46a6f-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="46a6f-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="46a6f-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="46a6f-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="46a6f-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="46a6f-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="46a6f-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-183">Prend en charge Dual-Sided support</span><span class="sxs-lookup"><span data-stu-id="46a6f-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="46a6f-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="46a6f-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-185">Éjection avant le démontage du lecteur non requise</span><span class="sxs-lookup"><span data-stu-id="46a6f-185">Ejection Prior to Drive Dismount Not Required</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46a6f-186">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="46a6f-186">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-187">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="46a6f-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-189">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="46a6f-189">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-190">Liste d’explications plus détaillées sur les fonctionnalités de l’appareil Access indiquées dans le tableau **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="46a6f-190">List of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="46a6f-191">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="46a6f-191">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="46a6f-192">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-192">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-193">**Caption**</span><span class="sxs-lookup"><span data-stu-id="46a6f-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-196">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-197">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="46a6f-197">Short description of the object.</span></span>

<span data-ttu-id="46a6f-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="46a6f-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-202">Algorithme ou outil utilisé par l’appareil pour prendre en charge la compression.</span><span class="sxs-lookup"><span data-stu-id="46a6f-202">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="46a6f-203">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-203">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="46a6f-204">Nom de l’algorithme de compression ou l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="46a6f-204">The name of the compression algorithm or one of the following values.</span></span>

<dt>



 <span data-ttu-id="46a6f-205">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="46a6f-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-206">Le fait que l’appareil prenne en charge les fonctionnalités de compression ou non n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="46a6f-206">Whether the device supports compression capabilities or not is not known.</span></span>

</dd> <dt>



 <span data-ttu-id="46a6f-207">(« Compressé »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-208">L’appareil prend en charge les fonctionnalités de compression, mais son schéma de compression n’est pas connu ou n’est pas divulgué.</span><span class="sxs-lookup"><span data-stu-id="46a6f-208">The device supports compression capabilities but its compression scheme is not known or not disclosed.</span></span>

</dd> <dt>



 <span data-ttu-id="46a6f-209">(« Non compressé »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-210">L’appareil ne prend pas en charge la compression.</span><span class="sxs-lookup"><span data-stu-id="46a6f-210">The device does not support compression.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46a6f-211">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="46a6f-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-212">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-214">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="46a6f-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-215">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="46a6f-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="46a6f-216">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="46a6f-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="46a6f-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="46a6f-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-219">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="46a6f-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="46a6f-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="46a6f-221">(1)</span><span class="sxs-lookup"><span data-stu-id="46a6f-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-222">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="46a6f-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="46a6f-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="46a6f-224">(2)</span><span class="sxs-lookup"><span data-stu-id="46a6f-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="46a6f-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="46a6f-226">(3)</span><span class="sxs-lookup"><span data-stu-id="46a6f-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-227">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="46a6f-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="46a6f-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="46a6f-229">(4)</span><span class="sxs-lookup"><span data-stu-id="46a6f-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-230">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="46a6f-230">Device is not working properly.</span></span> <span data-ttu-id="46a6f-231">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="46a6f-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="46a6f-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="46a6f-233">(5)</span><span class="sxs-lookup"><span data-stu-id="46a6f-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-234">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="46a6f-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="46a6f-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="46a6f-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="46a6f-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-237">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="46a6f-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="46a6f-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="46a6f-239">(7)</span><span class="sxs-lookup"><span data-stu-id="46a6f-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="46a6f-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="46a6f-241">(8)</span><span class="sxs-lookup"><span data-stu-id="46a6f-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-242">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="46a6f-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="46a6f-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="46a6f-244">(9)</span><span class="sxs-lookup"><span data-stu-id="46a6f-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-245">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="46a6f-245">Device is not working properly.</span></span> <span data-ttu-id="46a6f-246">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="46a6f-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="46a6f-248">(10)</span><span class="sxs-lookup"><span data-stu-id="46a6f-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-249">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="46a6f-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="46a6f-251">(11)</span><span class="sxs-lookup"><span data-stu-id="46a6f-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-252">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="46a6f-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="46a6f-254">douze</span><span class="sxs-lookup"><span data-stu-id="46a6f-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-255">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="46a6f-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="46a6f-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="46a6f-257">(13)</span><span class="sxs-lookup"><span data-stu-id="46a6f-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-258">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="46a6f-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="46a6f-260">(14)</span><span class="sxs-lookup"><span data-stu-id="46a6f-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-261">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="46a6f-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="46a6f-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="46a6f-263">(15)</span><span class="sxs-lookup"><span data-stu-id="46a6f-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-264">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="46a6f-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="46a6f-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="46a6f-266">(16)</span><span class="sxs-lookup"><span data-stu-id="46a6f-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-267">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="46a6f-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="46a6f-269">(17)</span><span class="sxs-lookup"><span data-stu-id="46a6f-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-270">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="46a6f-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="46a6f-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="46a6f-272">(18)</span><span class="sxs-lookup"><span data-stu-id="46a6f-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-273">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="46a6f-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="46a6f-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="46a6f-275">(19)</span><span class="sxs-lookup"><span data-stu-id="46a6f-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="46a6f-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="46a6f-277">(20)</span><span class="sxs-lookup"><span data-stu-id="46a6f-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-278">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="46a6f-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="46a6f-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="46a6f-280">(21)</span><span class="sxs-lookup"><span data-stu-id="46a6f-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-281">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="46a6f-281">System failure.</span></span> <span data-ttu-id="46a6f-282">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="46a6f-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="46a6f-283">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="46a6f-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="46a6f-285">(22)</span><span class="sxs-lookup"><span data-stu-id="46a6f-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-286">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="46a6f-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="46a6f-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="46a6f-288">(23)</span><span class="sxs-lookup"><span data-stu-id="46a6f-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-289">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="46a6f-289">System failure.</span></span> <span data-ttu-id="46a6f-290">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="46a6f-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="46a6f-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="46a6f-292">(24)</span><span class="sxs-lookup"><span data-stu-id="46a6f-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-293">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="46a6f-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="46a6f-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="46a6f-295">(25)</span><span class="sxs-lookup"><span data-stu-id="46a6f-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-296">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="46a6f-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="46a6f-298">(26)</span><span class="sxs-lookup"><span data-stu-id="46a6f-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-299">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="46a6f-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="46a6f-301">(27)</span><span class="sxs-lookup"><span data-stu-id="46a6f-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-302">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="46a6f-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="46a6f-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="46a6f-304">(28)</span><span class="sxs-lookup"><span data-stu-id="46a6f-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-305">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="46a6f-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="46a6f-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="46a6f-307">(29)</span><span class="sxs-lookup"><span data-stu-id="46a6f-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-308">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="46a6f-308">Device is disabled.</span></span> <span data-ttu-id="46a6f-309">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="46a6f-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="46a6f-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="46a6f-311">(30)</span><span class="sxs-lookup"><span data-stu-id="46a6f-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-312">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="46a6f-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="46a6f-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="46a6f-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="46a6f-314">31</span><span class="sxs-lookup"><span data-stu-id="46a6f-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-315">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="46a6f-315">Device is not working properly.</span></span> <span data-ttu-id="46a6f-316">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="46a6f-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46a6f-317">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="46a6f-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-318">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="46a6f-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-320">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="46a6f-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-321">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="46a6f-321">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="46a6f-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="46a6f-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-326">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="46a6f-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-327">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="46a6f-327">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="46a6f-328">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="46a6f-328">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="46a6f-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-330">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="46a6f-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-331">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46a6f-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-333">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="46a6f-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-334">Taille de bloc par défaut, en octets, pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-334">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="46a6f-335">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="46a6f-336">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="46a6f-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-337">**Description**</span><span class="sxs-lookup"><span data-stu-id="46a6f-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-340">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="46a6f-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-341">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="46a6f-341">Description of the object.</span></span>

<span data-ttu-id="46a6f-342">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="46a6f-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-344">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-346">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-347">Identificateur unique du lecteur de disque avec les autres périphériques du système.</span><span class="sxs-lookup"><span data-stu-id="46a6f-347">Unique identifier of the disk drive with other devices on the system.</span></span>

<span data-ttu-id="46a6f-348">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-349">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="46a6f-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-350">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="46a6f-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-352">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="46a6f-352">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="46a6f-353">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="46a6f-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-357">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="46a6f-357">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="46a6f-358">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-359">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="46a6f-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-362">Type de détection d’erreurs et de correction pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-362">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="46a6f-363">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-364">**FirmwareRevision**</span><span class="sxs-lookup"><span data-stu-id="46a6f-364">**FirmwareRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-365">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-367">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api \| [**\_ \_ descripteur de périphérique de stockage**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| ProductRevisionOffset")</span><span class="sxs-lookup"><span data-stu-id="46a6f-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-368">Révision du microprogramme de lecteur de disque attribué par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="46a6f-368">Revision for the disk drive firmware that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-369">**Index**</span><span class="sxs-lookup"><span data-stu-id="46a6f-369">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-370">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-372">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows 95/98 Functions de la \| carte de lecteurs \_ \_ \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="46a6f-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows 95/98 Functions\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-373">Numéro de lecteur physique du lecteur donné.</span><span class="sxs-lookup"><span data-stu-id="46a6f-373">Physical drive number of the given drive.</span></span> <span data-ttu-id="46a6f-374">Cette propriété est remplie par la structure du [**\_ \_ numéro du périphérique de stockage**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) renvoyée par le code de contrôle du numéro de l' [**\_ \_ \_ \_ appareil de stockage IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .</span><span class="sxs-lookup"><span data-stu-id="46a6f-374">This property is filled by the [**STORAGE\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) structure returned from the [**IOCTL\_STORAGE\_GET\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) control code.</span></span> <span data-ttu-id="46a6f-375">La valeur 0xFFFFFFFF indique que le lecteur donné n’est pas mappé à un lecteur physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-375">A value of 0xffffffff indicates that the given drive does not map to a physical drive.</span></span>

<span data-ttu-id="46a6f-376">Exemple : 1</span><span class="sxs-lookup"><span data-stu-id="46a6f-376">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-377">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46a6f-377">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-378">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="46a6f-378">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-379">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-380">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="46a6f-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-381">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="46a6f-381">Date and time the object was installed.</span></span> <span data-ttu-id="46a6f-382">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="46a6f-382">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="46a6f-383">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-383">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-384">**InterfaceType**</span><span class="sxs-lookup"><span data-stu-id="46a6f-384">**InterfaceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-385">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-386">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-387">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)»)</span><span class="sxs-lookup"><span data-stu-id="46a6f-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-388">Type d’interface du lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-388">Interface type of physical disk drive.</span></span>

<span data-ttu-id="46a6f-389">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="46a6f-389">The values are:</span></span>

<span data-ttu-id="46a6f-390">SCSI</span><span class="sxs-lookup"><span data-stu-id="46a6f-390">SCSI</span></span>

<span data-ttu-id="46a6f-391">HDC</span><span class="sxs-lookup"><span data-stu-id="46a6f-391">HDC</span></span>

<span data-ttu-id="46a6f-392">IDE</span><span class="sxs-lookup"><span data-stu-id="46a6f-392">IDE</span></span>

<span data-ttu-id="46a6f-393">USB</span><span class="sxs-lookup"><span data-stu-id="46a6f-393">USB</span></span>

<span data-ttu-id="46a6f-394">1394</span><span class="sxs-lookup"><span data-stu-id="46a6f-394">1394</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-395">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="46a6f-395">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-396">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-398">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-398">Last error code reported by the logical device.</span></span>

<span data-ttu-id="46a6f-399">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-400">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="46a6f-400">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-403">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Hardware \\ \\ DEVICEMAP \\ \\ SCSI \\ \\ Port SCSI \\ \\ bus SCSI bus \\ \\ cible ID d' \\ \\ unité logique ID \\ \\ », « \| fabricant Win32Registry »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-404">Nom du fabricant du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="46a6f-404">Name of the disk drive manufacturer.</span></span>

<span data-ttu-id="46a6f-405">Exemple : « Seagate »</span><span class="sxs-lookup"><span data-stu-id="46a6f-405">Example: "Seagate"</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-406">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="46a6f-406">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-407">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46a6f-407">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-409">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="46a6f-409">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-410">Taille maximale de bloc, en octets, pour les médias auxquels ce périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="46a6f-410">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="46a6f-411">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="46a6f-412">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="46a6f-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-413">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="46a6f-413">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-414">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46a6f-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-416">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="46a6f-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-417">Taille de support maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-417">Maximum media size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="46a6f-418">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="46a6f-419">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="46a6f-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-420">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="46a6f-420">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-421">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="46a6f-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-423">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api, \| [**\_**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| MediaType \| FixedMedia")</span><span class="sxs-lookup"><span data-stu-id="46a6f-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType\|FixedMedia")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-424">Si la **valeur est true**, le média d’un lecteur de disque est chargé, ce qui signifie que l’appareil dispose d’un système de fichiers lisible et qu’il est accessible.</span><span class="sxs-lookup"><span data-stu-id="46a6f-424">If **True**, the media for a disk drive is loaded, which means that the device has a readable file system and is accessible.</span></span> <span data-ttu-id="46a6f-425">Pour les lecteurs de disque fixes, cette propriété aura toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="46a6f-425">For fixed disk drives, this property will always be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-426">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="46a6f-426">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-429">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api, MediaType de la \| [**\_ géométrie du disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| ")</span><span class="sxs-lookup"><span data-stu-id="46a6f-429">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-430">Type de média utilisé ou accessible par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-430">Type of media used or accessed by this device.</span></span>

<span data-ttu-id="46a6f-431">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="46a6f-431">Possible values are:</span></span>

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

<span data-ttu-id="46a6f-432">**Support de disque dur externe**</span><span class="sxs-lookup"><span data-stu-id="46a6f-432">**External hard disk media**</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="46a6f-433">**Support amovible** (« support amovible autre qu’une disquette »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-433">**Removable media** ("Removable media other than floppy")</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

<span data-ttu-id="46a6f-434">**Disque dur fixe** (« support de disque dur fixe »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-434">**Fixed hard disk** ("Fixed hard disk media")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46a6f-435">**Inconnu** ("format inconnu")</span><span class="sxs-lookup"><span data-stu-id="46a6f-435">**Unknown** ("Format is unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46a6f-436">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="46a6f-436">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-437">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46a6f-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-438">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-439">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="46a6f-439">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-440">Taille de bloc minimale, en octets, pour les médias auxquels ce périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="46a6f-440">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="46a6f-441">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-441">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="46a6f-442">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="46a6f-442">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-443">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="46a6f-443">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-444">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-446">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Hardware \\ \\ DEVICEMAP \\ \\ SCSI \\ \\ Port SCSI \\ \\ bus SCSI bus \\ \\ cible ID \\ \\ de l’unité logique ID \\ \\ », « Win32Registry \| ProductID »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-447">Numéro de modèle du lecteur de disque du fabricant.</span><span class="sxs-lookup"><span data-stu-id="46a6f-447">Manufacturer's model number of the disk drive.</span></span>

<span data-ttu-id="46a6f-448">Exemple : « ST32171W »</span><span class="sxs-lookup"><span data-stu-id="46a6f-448">Example: "ST32171W"</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-449">**Nom**</span><span class="sxs-lookup"><span data-stu-id="46a6f-449">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-450">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-452">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="46a6f-452">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-453">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="46a6f-453">Label by which the object is known.</span></span> <span data-ttu-id="46a6f-454">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="46a6f-454">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="46a6f-455">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-455">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-456">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="46a6f-456">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-457">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="46a6f-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-459">Si la **valeur est true**, l’appareil d’accès aux médias doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="46a6f-459">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="46a6f-460">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété **capacités** .</span><span class="sxs-lookup"><span data-stu-id="46a6f-460">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="46a6f-461">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-461">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-462">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="46a6f-462">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-463">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-464">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-465">Nombre maximal de médias pouvant être pris en charge ou insérés (lorsque l’appareil d’accès aux médias prend en charge plusieurs médias individuels).</span><span class="sxs-lookup"><span data-stu-id="46a6f-465">Maximum number of media which can be supported or inserted (when the media access device supports multiple individual media).</span></span>

<span data-ttu-id="46a6f-466">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-466">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-467">**Partitions**</span><span class="sxs-lookup"><span data-stu-id="46a6f-467">**Partitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-468">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-470">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api \| [**\_**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RecognizedPartition")</span><span class="sxs-lookup"><span data-stu-id="46a6f-470">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RecognizedPartition")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-471">Nombre de partitions sur ce lecteur de disque physique qui sont reconnues par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="46a6f-471">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

<span data-ttu-id="46a6f-472">Exemple : 2</span><span class="sxs-lookup"><span data-stu-id="46a6f-472">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-473">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="46a6f-473">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-474">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-476">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="46a6f-476">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-477">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-477">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="46a6f-478">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="46a6f-479">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="46a6f-479">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-480">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="46a6f-480">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-481">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46a6f-481">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-483">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-483">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="46a6f-484">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="46a6f-484">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46a6f-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="46a6f-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="46a6f-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="46a6f-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-487">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-487">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="46a6f-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="46a6f-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="46a6f-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="46a6f-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-490">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="46a6f-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="46a6f-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="46a6f-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-492">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="46a6f-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="46a6f-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="46a6f-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-494">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="46a6f-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="46a6f-495">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="46a6f-495">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="46a6f-496">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="46a6f-496">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="46a6f-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="46a6f-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-498">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="46a6f-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="46a6f-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="46a6f-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="46a6f-500">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="46a6f-500">Timed Power-On Supported</span></span>

<span data-ttu-id="46a6f-501">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="46a6f-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46a6f-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="46a6f-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-503">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="46a6f-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-504">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-505">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="46a6f-505">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="46a6f-506">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="46a6f-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="46a6f-507">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-508">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="46a6f-508">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-509">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-509">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-510">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-510">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-511">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| des structures d’entrée et de sortie de l’appareil \| [**\_**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PathID")</span><span class="sxs-lookup"><span data-stu-id="46a6f-511">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-512">Numéro de bus SCSI du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="46a6f-512">SCSI bus number of the disk drive.</span></span>

<span data-ttu-id="46a6f-513">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="46a6f-513">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-514">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="46a6f-514">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-515">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46a6f-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-516">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-517">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| structures d’entrée et de sortie de l’appareil win32api LUN d' \| [**\_ adresse SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-517">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-518">Numéro d’unité logique (LUN) SCSI du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="46a6f-518">SCSI logical unit number (LUN) of the disk drive.</span></span>

<span data-ttu-id="46a6f-519">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="46a6f-519">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-520">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="46a6f-520">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-521">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46a6f-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-522">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-523">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api, \| [**\_ adresse SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| numéro_port")</span><span class="sxs-lookup"><span data-stu-id="46a6f-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PortNumber")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-524">Numéro de Port SCSI du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="46a6f-524">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="46a6f-525">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="46a6f-525">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-526">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="46a6f-526">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-527">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46a6f-527">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-528">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-529">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| des structures d’entrée et de sortie de l’appareil \| [**\_**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| targetID")</span><span class="sxs-lookup"><span data-stu-id="46a6f-529">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|TargetId")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-530">Numéro de l’identificateur SCSI du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="46a6f-530">SCSI identifier number of the disk drive.</span></span>

<span data-ttu-id="46a6f-531">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="46a6f-531">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-532">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="46a6f-532">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-533">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-533">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-534">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-535">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| structures d’entrée et de sortie de l’appareil win32api, \| [**\_ géométrie de disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-535">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-536">Nombre de secteurs dans chaque piste pour ce lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-536">Number of sectors in each track for this physical disk drive.</span></span>

<span data-ttu-id="46a6f-537">Exemple : 63</span><span class="sxs-lookup"><span data-stu-id="46a6f-537">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-538">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="46a6f-538">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-539">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-540">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-541">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api \| [**\_ \_ descripteur de périphérique de stockage**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| SerialNumberOffset")</span><span class="sxs-lookup"><span data-stu-id="46a6f-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-542">Nombre alloué par le fabricant pour identifier le support physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-542">Number allocated by the manufacturer to identify the physical media.</span></span>

<span data-ttu-id="46a6f-543">Exemple : WD-WM3493798728</span><span class="sxs-lookup"><span data-stu-id="46a6f-543">Example: WD-WM3493798728</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-544">**Signature**</span><span class="sxs-lookup"><span data-stu-id="46a6f-544">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-545">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-545">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-546">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-547">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api signature des \| [**\_ \_ informations sur la disposition du lecteur**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information) \| ")</span><span class="sxs-lookup"><span data-stu-id="46a6f-547">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DRIVE\_LAYOUT\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information)\|Signature")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-548">Identification du disque.</span><span class="sxs-lookup"><span data-stu-id="46a6f-548">Disk identification.</span></span> <span data-ttu-id="46a6f-549">Cette propriété peut être utilisée pour identifier une ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="46a6f-549">This property can be used to identify a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-550">**Taille**</span><span class="sxs-lookup"><span data-stu-id="46a6f-550">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-551">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46a6f-551">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-552">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-553">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structure d’entrée et de sortie de l’appareil win32api \| [**\_ géométrie du disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("octets")</span><span class="sxs-lookup"><span data-stu-id="46a6f-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-554">Taille du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="46a6f-554">Size of the disk drive.</span></span> <span data-ttu-id="46a6f-555">Elle est calculée en multipliant le nombre total de cylindres, les pistes de chaque cylindre, les secteurs de chaque piste et les octets de chaque secteur.</span><span class="sxs-lookup"><span data-stu-id="46a6f-555">It is calculated by multiplying the total number of cylinders, tracks in each cylinder, sectors in each track, and bytes in each sector.</span></span>

<span data-ttu-id="46a6f-556">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="46a6f-556">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-557">**État**</span><span class="sxs-lookup"><span data-stu-id="46a6f-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-558">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-559">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-560">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="46a6f-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-561">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="46a6f-561">Current status of the object.</span></span> <span data-ttu-id="46a6f-562">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="46a6f-562">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="46a6f-563">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="46a6f-563">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="46a6f-564">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="46a6f-564">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="46a6f-565">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="46a6f-565">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="46a6f-566">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="46a6f-566">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="46a6f-567">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-567">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="46a6f-568">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="46a6f-568">Values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="46a6f-569">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-569">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="46a6f-570">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-570">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="46a6f-571">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-571">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46a6f-572">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="46a6f-572">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="46a6f-573">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-573">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="46a6f-574">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-574">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="46a6f-575">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-575">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="46a6f-576">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-576">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="46a6f-577">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-577">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="46a6f-578">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-578">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="46a6f-579">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-579">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="46a6f-580">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-580">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46a6f-581">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="46a6f-581">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-582">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46a6f-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-583">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-583">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-584">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="46a6f-584">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-585">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-585">State of the logical device.</span></span> <span data-ttu-id="46a6f-586">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="46a6f-586">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="46a6f-587">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46a6f-588">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="46a6f-588">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46a6f-589">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="46a6f-589">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="46a6f-590">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="46a6f-590">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="46a6f-591">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="46a6f-591">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="46a6f-592">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="46a6f-592">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46a6f-593">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="46a6f-593">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-594">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-594">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-595">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-596">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="46a6f-596">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-597">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="46a6f-597">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="46a6f-598">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-598">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-599">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="46a6f-599">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-600">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46a6f-600">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-601">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-602">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="46a6f-602">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-603">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="46a6f-603">Name of the scoping system.</span></span>

<span data-ttu-id="46a6f-604">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-604">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-605">**TotalCylinders**</span><span class="sxs-lookup"><span data-stu-id="46a6f-605">**TotalCylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-606">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46a6f-606">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-607">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-608">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api les cylindres de la \| [**\_ géométrie du disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| ")</span><span class="sxs-lookup"><span data-stu-id="46a6f-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|Cylinders")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-609">Nombre total de cylindres sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-609">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="46a6f-610">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="46a6f-610">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="46a6f-611">La valeur peut être inexacte si le lecteur utilise un schéma de traduction pour prendre en charge les tailles de disques de grande capacité.</span><span class="sxs-lookup"><span data-stu-id="46a6f-611">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="46a6f-612">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="46a6f-612">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="46a6f-613">Exemple : 657</span><span class="sxs-lookup"><span data-stu-id="46a6f-613">Example: 657</span></span>

<span data-ttu-id="46a6f-614">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="46a6f-614">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-615">**TotalHeads**</span><span class="sxs-lookup"><span data-stu-id="46a6f-615">**TotalHeads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-616">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-616">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-617">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-618">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| structures d’entrée et de sortie de l’appareil win32api, \| [**\_ géométrie de disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-618">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-619">Nombre total de têtes sur le lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="46a6f-619">Total number of heads on the disk drive.</span></span> <span data-ttu-id="46a6f-620">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="46a6f-620">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="46a6f-621">La valeur peut être inexacte si le lecteur utilise un schéma de traduction pour prendre en charge les tailles de disques de grande capacité.</span><span class="sxs-lookup"><span data-stu-id="46a6f-621">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="46a6f-622">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="46a6f-622">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-623">**TotalSectors**</span><span class="sxs-lookup"><span data-stu-id="46a6f-623">**TotalSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-624">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46a6f-624">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-625">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-626">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| structures d’entrée et de sortie de l’appareil win32api, \| [**\_ géométrie de disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-626">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-627">Nombre total de secteurs sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-627">Total number of sectors on the physical disk drive.</span></span> <span data-ttu-id="46a6f-628">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="46a6f-628">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="46a6f-629">La valeur peut être inexacte si le lecteur utilise un schéma de traduction pour prendre en charge les tailles de disques de grande capacité.</span><span class="sxs-lookup"><span data-stu-id="46a6f-629">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="46a6f-630">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="46a6f-630">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="46a6f-631">Exemple : 2649024</span><span class="sxs-lookup"><span data-stu-id="46a6f-631">Example: 2649024</span></span>

<span data-ttu-id="46a6f-632">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="46a6f-632">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-633">**TotalTracks**</span><span class="sxs-lookup"><span data-stu-id="46a6f-633">**TotalTracks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-634">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46a6f-634">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-635">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-636">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| structures d’entrée et de sortie de l’appareil win32api, \| [**\_ géométrie de disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-637">Nombre total de pistes sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-637">Total number of tracks on the physical disk drive.</span></span> <span data-ttu-id="46a6f-638">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="46a6f-638">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="46a6f-639">La valeur peut être inexacte si le lecteur utilise un schéma de traduction pour prendre en charge les tailles de disques de grande capacité.</span><span class="sxs-lookup"><span data-stu-id="46a6f-639">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="46a6f-640">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="46a6f-640">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="46a6f-641">Exemple : 42048</span><span class="sxs-lookup"><span data-stu-id="46a6f-641">Example: 42048</span></span>

<span data-ttu-id="46a6f-642">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="46a6f-642">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="46a6f-643">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="46a6f-643">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46a6f-644">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46a6f-644">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-645">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46a6f-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46a6f-646">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| structures d’entrée et de sortie de l’appareil win32api, \| [**\_ géométrie de disque**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder »)</span><span class="sxs-lookup"><span data-stu-id="46a6f-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="46a6f-647">Nombre de pistes dans chaque cylindre sur le lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-647">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="46a6f-648">Remarque : la valeur de cette propriété est obtenue via des fonctions étendues de l’interruption du BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="46a6f-648">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="46a6f-649">La valeur peut être inexacte si le lecteur utilise un schéma de traduction pour prendre en charge les tailles de disques de grande capacité.</span><span class="sxs-lookup"><span data-stu-id="46a6f-649">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="46a6f-650">Consultez le fabricant pour obtenir des spécifications précises sur les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="46a6f-650">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="46a6f-651">Exemple : 64</span><span class="sxs-lookup"><span data-stu-id="46a6f-651">Example: 64</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46a6f-652">Notes</span><span class="sxs-lookup"><span data-stu-id="46a6f-652">Remarks</span></span>

<span data-ttu-id="46a6f-653">Les lecteurs de disque dur physique sont le support de stockage principal pour les informations dans n’importe quel environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="46a6f-653">Physical hard disk drives are the primary storage medium for information in any computing environment.</span></span> <span data-ttu-id="46a6f-654">Bien que les organisations utilisent souvent des appareils tels que des lecteurs de bande et des lecteurs de disque compact pour l’archivage des données, ces appareils ne sont pas adaptés au stockage quotidien des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="46a6f-654">Although organizations often use devices such as tape drives and compact disc drives for archiving data, these devices are not suited for day-to-day storage of user data.</span></span> <span data-ttu-id="46a6f-655">Seuls les disques durs physiques offrent la vitesse et la facilité d’utilisation nécessaires au stockage des données et à l’exécution des applications et du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="46a6f-655">Only physical hard disks offer the speed and ease of use required for storing data and for running applications and the operating system.</span></span>

<span data-ttu-id="46a6f-656">Pour gérer efficacement les données, il est important de disposer d’un inventaire détaillé de tous vos disques physiques, de leurs fonctionnalités et de leurs capacités.</span><span class="sxs-lookup"><span data-stu-id="46a6f-656">To efficiently manage data, it is important to have a detailed inventory of all your physical disks, their capabilities, and their capacities.</span></span> <span data-ttu-id="46a6f-657">Vous pouvez utiliser la classe **Win32 \_ DiskDrive** pour dériver ce type d’inventaire.</span><span class="sxs-lookup"><span data-stu-id="46a6f-657">You can use the **Win32\_DiskDrive** class to derive this type of inventory.</span></span>

<span data-ttu-id="46a6f-658">Toute interface à un lecteur de disque physique Windows est un descendant (ou membre) de cette classe.</span><span class="sxs-lookup"><span data-stu-id="46a6f-658">Any interface to a Windows physical disk drive is a descendant (or member) of this class.</span></span> <span data-ttu-id="46a6f-659">Les fonctionnalités du lecteur de disque vu par cet objet correspondent aux caractéristiques logiques et de gestion du lecteur.</span><span class="sxs-lookup"><span data-stu-id="46a6f-659">The features of the disk drive seen through this object correspond to the logical and management characteristics of the drive.</span></span> <span data-ttu-id="46a6f-660">Dans certains cas, cela peut ne pas refléter les caractéristiques physiques réelles de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46a6f-660">In some cases, this may not reflect the actual physical characteristics of the device.</span></span> <span data-ttu-id="46a6f-661">Tout objet basé sur un autre périphérique logique ne sera pas membre de cette classe.</span><span class="sxs-lookup"><span data-stu-id="46a6f-661">Any object based on another logical device would not be a member of this class.</span></span>

<span data-ttu-id="46a6f-662">Pour des raisons de sécurité, un utilisateur qui se connecte à partir d’un ordinateur distant doit disposer du privilège de **\_ \_ connexion du gestionnaire SC** pour pouvoir énumérer cette classe.</span><span class="sxs-lookup"><span data-stu-id="46a6f-662">For security reasons, a user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="46a6f-663">Pour plus d’informations, consultez [sécurité des services et droits d’accès](/windows/desktop/Services/service-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="46a6f-663">For more information, see [Service Security and Access Rights](/windows/desktop/Services/service-security-and-access-rights).</span></span>

<span data-ttu-id="46a6f-664">La classe **Win32 \_ DiskDrive** est dérivée de [**CIM \_ DiskDrive**](cim-diskdrive.md) qui dérive de [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-664">The **Win32\_DiskDrive** class is derived from [**CIM\_DiskDrive**](cim-diskdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="46a6f-665">La classe **CIM \_ MediaAccessDevice** dérive de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="46a6f-665">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="46a6f-666">Exemples</span><span class="sxs-lookup"><span data-stu-id="46a6f-666">Examples</span></span>

<span data-ttu-id="46a6f-667">Le [rapport d’inventaire des serveurs-exemple de code WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell sur la Galerie TechNet utilise un certain nombre de classes, notamment **Win32 \_ DiskDrive**, pour renvoyer des informations sur l’état du serveur.</span><span class="sxs-lookup"><span data-stu-id="46a6f-667">The [Servers Inventory report-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell code example on TechNet Gallery uses a number of classes, including **Win32\_DiskDrive**, to return information about server status.</span></span>

<span data-ttu-id="46a6f-668">La [carte de lecteur à lettre de lecteur utilisant l’exemple de code PowerShell de \_ propriété de type interface Win32 DiskDrive](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) mappe un lecteur à une lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="46a6f-668">The [Map Drive to Drive Letter Using the Win32\_DiskDrive Interface Type Property](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) PowerShell code sample maps a drive to a drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="46a6f-669">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46a6f-669">Requirements</span></span>



| <span data-ttu-id="46a6f-670">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46a6f-670">Requirement</span></span> | <span data-ttu-id="46a6f-671">Valeur</span><span class="sxs-lookup"><span data-stu-id="46a6f-671">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46a6f-672">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46a6f-672">Minimum supported client</span></span><br/> | <span data-ttu-id="46a6f-673">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46a6f-673">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46a6f-674">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46a6f-674">Minimum supported server</span></span><br/> | <span data-ttu-id="46a6f-675">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46a6f-675">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46a6f-676">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="46a6f-676">Namespace</span></span><br/>                | <span data-ttu-id="46a6f-677">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="46a6f-677">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46a6f-678">MOF</span><span class="sxs-lookup"><span data-stu-id="46a6f-678">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46a6f-679"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46a6f-679"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46a6f-680">DLL</span><span class="sxs-lookup"><span data-stu-id="46a6f-680">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46a6f-681"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46a6f-681"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46a6f-682">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46a6f-682">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a6f-683">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="46a6f-683">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="46a6f-684">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="46a6f-684">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="46a6f-685">Tâches WMI : disques et systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="46a6f-685">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

