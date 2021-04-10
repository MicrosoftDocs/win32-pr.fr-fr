---
description: Représente un lecteur de CD-ROM sur un système informatique exécutant Windows.
ms.assetid: 08087976-ca88-4ac8-9456-0d8bd799e66c
ms.tgt_platform: multiple
title: Win32_CDROMDrive, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CDROMDrive
- Win32_CDROMDrive.Reset
- Win32_CDROMDrive.SetPowerState
- Win32_CDROMDrive.Availability
- Win32_CDROMDrive.Capabilities
- Win32_CDROMDrive.CapabilityDescriptions
- Win32_CDROMDrive.Caption
- Win32_CDROMDrive.CompressionMethod
- Win32_CDROMDrive.ConfigManagerErrorCode
- Win32_CDROMDrive.ConfigManagerUserConfig
- Win32_CDROMDrive.CreationClassName
- Win32_CDROMDrive.DefaultBlockSize
- Win32_CDROMDrive.Description
- Win32_CDROMDrive.DeviceID
- Win32_CDROMDrive.Drive
- Win32_CDROMDrive.DriveIntegrity
- Win32_CDROMDrive.ErrorCleared
- Win32_CDROMDrive.ErrorDescription
- Win32_CDROMDrive.ErrorMethodology
- Win32_CDROMDrive.FileSystemFlags
- Win32_CDROMDrive.FileSystemFlagsEx
- Win32_CDROMDrive.Id
- Win32_CDROMDrive.InstallDate
- Win32_CDROMDrive.LastErrorCode
- Win32_CDROMDrive.Manufacturer
- Win32_CDROMDrive.MaxBlockSize
- Win32_CDROMDrive.MaximumComponentLength
- Win32_CDROMDrive.MaxMediaSize
- Win32_CDROMDrive.MediaLoaded
- Win32_CDROMDrive.MediaType
- Win32_CDROMDrive.MfrAssignedRevisionLevel
- Win32_CDROMDrive.MinBlockSize
- Win32_CDROMDrive.Name
- Win32_CDROMDrive.NeedsCleaning
- Win32_CDROMDrive.NumberOfMediaSupported
- Win32_CDROMDrive.PNPDeviceID
- Win32_CDROMDrive.PowerManagementCapabilities
- Win32_CDROMDrive.PowerManagementSupported
- Win32_CDROMDrive.RevisionLevel
- Win32_CDROMDrive.SCSIBus
- Win32_CDROMDrive.SCSILogicalUnit
- Win32_CDROMDrive.SCSIPort
- Win32_CDROMDrive.SCSITargetId
- Win32_CDROMDrive.SerialNumber
- Win32_CDROMDrive.Size
- Win32_CDROMDrive.Status
- Win32_CDROMDrive.StatusInfo
- Win32_CDROMDrive.SystemCreationClassName
- Win32_CDROMDrive.SystemName
- Win32_CDROMDrive.TransferRate
- Win32_CDROMDrive.VolumeName
- Win32_CDROMDrive.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c352d2ee717f5eb888b49d6e5e8ff456cc5a85f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950769"
---
# <a name="win32_cdromdrive-class"></a><span data-ttu-id="069d8-103">\_Classe CDROMDrive Win32</span><span class="sxs-lookup"><span data-stu-id="069d8-103">Win32\_CDROMDrive class</span></span>

<span data-ttu-id="069d8-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CDROMDrive** WMI représente un lecteur de CD-ROM sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="069d8-104">The **Win32\_CDROMDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a CD-ROM drive on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="069d8-105">N’oubliez pas que le nom du lecteur ne correspond pas à la lettre de lecteur logique attribuée à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-105">Be aware that the name of the drive does not correspond to the logical drive letter assigned to the device.</span></span>

 

<span data-ttu-id="069d8-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="069d8-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="069d8-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="069d8-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="069d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="069d8-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CDROMDrive : CIM_CDROMDrive
{
  uint16   Availability;
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
  string   Drive;
  boolean  DriveIntegrity;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint16   FileSystemFlags;
  uint32   FileSystemFlagsEx;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint32   MaximumComponentLength;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  string   MfrAssignedRevisionLevel;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   RevisionLevel;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  string   SerialNumber;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  real64   TransferRate;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="069d8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="069d8-109">Members</span></span>

<span data-ttu-id="069d8-110">La classe **Win32 \_ CDROMDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="069d8-110">The **Win32\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="069d8-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="069d8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="069d8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="069d8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="069d8-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="069d8-113">Methods</span></span>

<span data-ttu-id="069d8-114">La classe **Win32 \_ CDROMDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="069d8-114">The **Win32\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="069d8-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="069d8-115">Method</span></span>            | <span data-ttu-id="069d8-116">Description</span><span class="sxs-lookup"><span data-stu-id="069d8-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="069d8-117">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="069d8-117">**Reset**</span></span>         | <span data-ttu-id="069d8-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="069d8-118">Not implemented.</span></span> <span data-ttu-id="069d8-119">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ CDROMDrive**](cim-cdromdrive.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="069d8-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="069d8-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="069d8-120">**SetPowerState**</span></span> | <span data-ttu-id="069d8-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="069d8-121">Not implemented.</span></span> <span data-ttu-id="069d8-122">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ CDROMDrive**](cim-cdromdrive.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="069d8-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="069d8-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="069d8-123">Properties</span></span>

<span data-ttu-id="069d8-124">La classe **Win32 \_ CDROMDrive** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="069d8-124">The **Win32\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="069d8-125">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="069d8-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069d8-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="069d8-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-129">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-129">Availability and status of the device.</span></span>

<span data-ttu-id="069d8-130">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="069d8-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="069d8-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="069d8-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="069d8-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="069d8-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="069d8-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-134">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="069d8-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="069d8-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="069d8-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="069d8-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="069d8-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="069d8-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="069d8-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="069d8-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="069d8-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="069d8-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="069d8-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="069d8-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="069d8-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="069d8-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="069d8-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="069d8-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="069d8-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="069d8-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="069d8-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="069d8-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="069d8-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="069d8-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="069d8-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="069d8-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="069d8-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="069d8-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="069d8-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-149">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="069d8-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="069d8-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="069d8-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="069d8-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="069d8-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="069d8-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="069d8-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="069d8-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="069d8-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="069d8-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="069d8-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="069d8-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="069d8-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="069d8-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="069d8-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="069d8-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="069d8-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="069d8-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="069d8-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="069d8-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-162">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069d8-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="069d8-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-164">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="069d8-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-165">Tableau de fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="069d8-165">Array of capabilities of the media access device.</span></span> <span data-ttu-id="069d8-166">Par exemple, l’appareil peut prendre en charge l’accès aléatoire (3), le support amovible (7) et le nettoyage automatique (9).</span><span class="sxs-lookup"><span data-stu-id="069d8-166">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="069d8-167">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="069d8-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="069d8-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="069d8-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="069d8-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="069d8-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="069d8-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="069d8-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="069d8-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="069d8-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="069d8-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="069d8-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="069d8-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="069d8-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="069d8-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="069d8-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="069d8-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-176">Prend en charge les supports amovibles</span><span class="sxs-lookup"><span data-stu-id="069d8-176">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="069d8-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="069d8-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="069d8-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="069d8-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="069d8-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="069d8-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="069d8-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="069d8-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-181">Prend en charge Dual-Sided support</span><span class="sxs-lookup"><span data-stu-id="069d8-181">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="069d8-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="069d8-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="069d8-183">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="069d8-183">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-184">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="069d8-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="069d8-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-186">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="069d8-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-187">Tableau d’explications plus détaillées sur les fonctionnalités de l’appareil Access indiquées dans le tableau **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="069d8-187">Array of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="069d8-188">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="069d8-188">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="069d8-189">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-189">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="069d8-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-193">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="069d8-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-194">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="069d8-194">Short description of the object a one-line string.</span></span>

<span data-ttu-id="069d8-195">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-196">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="069d8-196">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-199">Algorithme ou outil utilisé par l’appareil pour prendre en charge la compression.</span><span class="sxs-lookup"><span data-stu-id="069d8-199">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="069d8-200">S’il n’est pas possible de décrire le schéma de compression (peut-être parce qu’il n’est pas connu), utilisez les mots suivants : « inconnu » pour indiquer qu’il n’est pas connu que l’appareil prend en charge les fonctionnalités de compression ; « Compressed » pour représenter que l’appareil prend en charge les fonctionnalités de compression, mais que son schéma de compression n’est pas connu ou n’est pas divulgué ; et « non compressés » pour représenter que l’appareil ne prend pas en charge les fonctionnalités de compression.</span><span class="sxs-lookup"><span data-stu-id="069d8-200">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="069d8-201">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="069d8-202">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="069d8-202">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="069d8-203">Le schéma de compression est inconnu ou non décrit.</span><span class="sxs-lookup"><span data-stu-id="069d8-203">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="069d8-204">(« Compressé »)</span><span class="sxs-lookup"><span data-stu-id="069d8-204">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="069d8-205">Le fichier logique est compressé, mais le schéma de compression est inconnu ou n’est pas décrit.</span><span class="sxs-lookup"><span data-stu-id="069d8-205">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="069d8-206">(« Non compressé »)</span><span class="sxs-lookup"><span data-stu-id="069d8-206">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="069d8-207">Si le fichier logique n’est pas compressé</span><span class="sxs-lookup"><span data-stu-id="069d8-207">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="069d8-208">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="069d8-208">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-209">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069d8-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-211">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="069d8-211">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-212">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="069d8-212">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="069d8-213">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-213">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="069d8-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="069d8-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="069d8-215"> (0)</span><span class="sxs-lookup"><span data-stu-id="069d8-215">(0)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-216">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="069d8-216">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="069d8-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="069d8-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="069d8-218">(1)</span><span class="sxs-lookup"><span data-stu-id="069d8-218">(1)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-219">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="069d8-219">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="069d8-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="069d8-221">(2)</span><span class="sxs-lookup"><span data-stu-id="069d8-221">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="069d8-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="069d8-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="069d8-223">(3)</span><span class="sxs-lookup"><span data-stu-id="069d8-223">(3)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-224">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="069d8-224">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="069d8-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="069d8-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="069d8-226">(4)</span><span class="sxs-lookup"><span data-stu-id="069d8-226">(4)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-227">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="069d8-227">Device is not working properly.</span></span> <span data-ttu-id="069d8-228">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="069d8-228">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="069d8-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="069d8-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="069d8-230">(5)</span><span class="sxs-lookup"><span data-stu-id="069d8-230">(5)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-231">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="069d8-231">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="069d8-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="069d8-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="069d8-233"> (6)</span><span class="sxs-lookup"><span data-stu-id="069d8-233">(6)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-234">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="069d8-234">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="069d8-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="069d8-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="069d8-236">(7)</span><span class="sxs-lookup"><span data-stu-id="069d8-236">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="069d8-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="069d8-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="069d8-238">(8)</span><span class="sxs-lookup"><span data-stu-id="069d8-238">(8)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-239">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="069d8-239">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="069d8-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="069d8-241">(9)</span><span class="sxs-lookup"><span data-stu-id="069d8-241">(9)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-242">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="069d8-242">Device is not working properly.</span></span> <span data-ttu-id="069d8-243">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-243">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="069d8-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="069d8-245">(10)</span><span class="sxs-lookup"><span data-stu-id="069d8-245">(10)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-246">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-246">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="069d8-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="069d8-248">(11)</span><span class="sxs-lookup"><span data-stu-id="069d8-248">(11)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-249">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-249">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="069d8-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="069d8-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="069d8-251">douze</span><span class="sxs-lookup"><span data-stu-id="069d8-251">(12)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-252">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="069d8-252">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="069d8-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="069d8-254">(13)</span><span class="sxs-lookup"><span data-stu-id="069d8-254">(13)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-255">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-255">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="069d8-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="069d8-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="069d8-257">(14)</span><span class="sxs-lookup"><span data-stu-id="069d8-257">(14)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-258">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="069d8-258">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="069d8-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="069d8-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="069d8-260">(15)</span><span class="sxs-lookup"><span data-stu-id="069d8-260">(15)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-261">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="069d8-261">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="069d8-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="069d8-263">(16)</span><span class="sxs-lookup"><span data-stu-id="069d8-263">(16)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-264">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-264">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="069d8-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="069d8-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="069d8-266">(17)</span><span class="sxs-lookup"><span data-stu-id="069d8-266">(17)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-267">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="069d8-267">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="069d8-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="069d8-269">(18)</span><span class="sxs-lookup"><span data-stu-id="069d8-269">(18)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-270">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="069d8-270">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="069d8-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="069d8-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="069d8-272">(19)</span><span class="sxs-lookup"><span data-stu-id="069d8-272">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="069d8-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="069d8-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="069d8-274">(20)</span><span class="sxs-lookup"><span data-stu-id="069d8-274">(20)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-275">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="069d8-275">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="069d8-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="069d8-277">(21)</span><span class="sxs-lookup"><span data-stu-id="069d8-277">(21)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-278">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="069d8-278">System failure.</span></span> <span data-ttu-id="069d8-279">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="069d8-279">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="069d8-280">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-280">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="069d8-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="069d8-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="069d8-282">(22)</span><span class="sxs-lookup"><span data-stu-id="069d8-282">(22)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-283">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="069d8-283">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="069d8-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="069d8-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="069d8-285">(23)</span><span class="sxs-lookup"><span data-stu-id="069d8-285">(23)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-286">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="069d8-286">System failure.</span></span> <span data-ttu-id="069d8-287">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="069d8-287">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="069d8-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="069d8-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="069d8-289">(24)</span><span class="sxs-lookup"><span data-stu-id="069d8-289">(24)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-290">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="069d8-290">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="069d8-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="069d8-292">(25)</span><span class="sxs-lookup"><span data-stu-id="069d8-292">(25)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-293">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-293">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="069d8-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="069d8-295">(26)</span><span class="sxs-lookup"><span data-stu-id="069d8-295">(26)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-296">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="069d8-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="069d8-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="069d8-298">(27)</span><span class="sxs-lookup"><span data-stu-id="069d8-298">(27)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-299">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="069d8-299">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="069d8-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="069d8-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="069d8-301">(28)</span><span class="sxs-lookup"><span data-stu-id="069d8-301">(28)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-302">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="069d8-302">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="069d8-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="069d8-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="069d8-304">(29)</span><span class="sxs-lookup"><span data-stu-id="069d8-304">(29)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-305">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="069d8-305">Device is disabled.</span></span> <span data-ttu-id="069d8-306">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="069d8-306">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="069d8-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="069d8-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="069d8-308">(30)</span><span class="sxs-lookup"><span data-stu-id="069d8-308">(30)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-309">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="069d8-309">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="069d8-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="069d8-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="069d8-311">31</span><span class="sxs-lookup"><span data-stu-id="069d8-311">(31)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-312">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="069d8-312">Device is not working properly.</span></span> <span data-ttu-id="069d8-313">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="069d8-313">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="069d8-314">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="069d8-314">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-315">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="069d8-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-317">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="069d8-317">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-318">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="069d8-318">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="069d8-319">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-320">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="069d8-320">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-323">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="069d8-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="069d8-324">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="069d8-324">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="069d8-325">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="069d8-325">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="069d8-326">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-327">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="069d8-327">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-328">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="069d8-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-330">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="069d8-330">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-331">Taille de bloc par défaut, en octets, pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-331">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="069d8-332">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-332">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="069d8-333">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="069d8-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-334">**Description**</span><span class="sxs-lookup"><span data-stu-id="069d8-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-335">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-337">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="069d8-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-338">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="069d8-338">Description of the object.</span></span>

<span data-ttu-id="069d8-339">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-340">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="069d8-340">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-341">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-343">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("fonctions de \| fichier win32api \| GetLogicalDriveStrings")</span><span class="sxs-lookup"><span data-stu-id="069d8-343">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetLogicalDriveStrings")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-344">Identificateur unique d’un lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="069d8-344">Unique identifier for a CD-ROM drive.</span></span>

<span data-ttu-id="069d8-345">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-346">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="069d8-346">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-349">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions de fichier \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="069d8-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-350">Lettre de lecteur du lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="069d8-350">Drive letter of the CD-ROM drive.</span></span>

<span data-ttu-id="069d8-351">Exemple : "d : \\ "</span><span class="sxs-lookup"><span data-stu-id="069d8-351">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="069d8-352">**DriveIntegrity**</span><span class="sxs-lookup"><span data-stu-id="069d8-352">**DriveIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-353">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="069d8-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-355">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="069d8-355">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-356">Si la **valeur est true**, les fichiers peuvent être lus avec précision à partir du périphérique CD.</span><span class="sxs-lookup"><span data-stu-id="069d8-356">If **True**, files can be accurately read from the CD device.</span></span> <span data-ttu-id="069d8-357">Pour ce faire, il suffit de lire un bloc de données à deux reprises et de comparer les données à eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="069d8-357">This is achieved by reading a block of data twice and comparing the data against itself.</span></span>

</dd> <dt>

<span data-ttu-id="069d8-358">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="069d8-358">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-359">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="069d8-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-361">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="069d8-361">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="069d8-362">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-363">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="069d8-363">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-366">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="069d8-366">More information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="069d8-367">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-368">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="069d8-368">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-369">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-371">Type de détection d’erreurs et de correction pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-371">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="069d8-372">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-372">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-373">**FileSystemFlags**</span><span class="sxs-lookup"><span data-stu-id="069d8-373">**FileSystemFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-374">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069d8-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-376">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions du système de fichiers \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="069d8-376">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-377">Cette propriété est obsolète.</span><span class="sxs-lookup"><span data-stu-id="069d8-377">This property is obsolete.</span></span> <span data-ttu-id="069d8-378">À la place de cette propriété, utilisez **FileSystemFlagsEx**.</span><span class="sxs-lookup"><span data-stu-id="069d8-378">In place of this property, use **FileSystemFlagsEx**.</span></span>

</dd> <dt>

<span data-ttu-id="069d8-379">**FileSystemFlagsEx**</span><span class="sxs-lookup"><span data-stu-id="069d8-379">**FileSystemFlagsEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-380">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069d8-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-382">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions du système de fichiers win32api \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)»)</span><span class="sxs-lookup"><span data-stu-id="069d8-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-383">Indicateurs du système de fichiers associés au lecteur de CD-ROM Windows.</span><span class="sxs-lookup"><span data-stu-id="069d8-383">File system flags associated with the Windows CD-ROM drive.</span></span> <span data-ttu-id="069d8-384">Ce paramètre peut être n’importe quelle combinaison d’indicateurs, mais la **\_ \_ compression de fichiers FS** et le **\_ volume FS \_ est \_ compressé** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="069d8-384">This parameter can be any combination of flags, but **FS\_FILE\_COMPRESSION** and **FS\_VOL\_IS\_COMPRESSED** are mutually exclusive.</span></span>

<dt>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>

<span data-ttu-id="069d8-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Recherche respectant la casse** (1)</span><span class="sxs-lookup"><span data-stu-id="069d8-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Case Sensitive Search** (1)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-386">Le système de fichiers prend en charge les noms de fichiers sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="069d8-386">The file system supports case-sensitive file names.</span></span>

</dd> <dt>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>

<span data-ttu-id="069d8-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Noms conservés** de la casse (2)</span><span class="sxs-lookup"><span data-stu-id="069d8-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Case Preserved Names** (2)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-388">Le système de fichiers conserve la casse des noms de fichiers lorsqu’il place un nom sur un disque.</span><span class="sxs-lookup"><span data-stu-id="069d8-388">The file system preserves the case of file names when it places a name on a disk.</span></span>

</dd> <dt>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>

<span data-ttu-id="069d8-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode sur le disque** (4)</span><span class="sxs-lookup"><span data-stu-id="069d8-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode On Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-390">Le système de fichiers prend en charge Unicode dans les noms de fichiers tels qu’ils apparaissent sur le disque.</span><span class="sxs-lookup"><span data-stu-id="069d8-390">The file system supports Unicode in file names as they appear on the disk.</span></span>

</dd> <dt>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>

<span data-ttu-id="069d8-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**ACL persistantes** (8)</span><span class="sxs-lookup"><span data-stu-id="069d8-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Persistent ACLs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-392">Le système de fichiers conserve et applique les listes de contrôle d’accès (ACL).</span><span class="sxs-lookup"><span data-stu-id="069d8-392">The file system preserves and enforces access control lists (ACLs).</span></span> <span data-ttu-id="069d8-393">Par exemple, le système de fichiers NTFS conserve et applique les listes de contrôle d’accès et le système de fichiers FAT ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="069d8-393">For example, the NTFS file system preserves and enforces ACLs and the FAT file system does not.</span></span>

</dd> <dt>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>

<span data-ttu-id="069d8-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**Compression de fichiers** (16)</span><span class="sxs-lookup"><span data-stu-id="069d8-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**File Compression** (16)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-395">Le système de fichiers prend en charge la compression basée sur les fichiers.</span><span class="sxs-lookup"><span data-stu-id="069d8-395">The file system supports file-based compression.</span></span>

</dd> <dt>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>

<span data-ttu-id="069d8-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Quotas de volume** (32)</span><span class="sxs-lookup"><span data-stu-id="069d8-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Volume Quotas** (32)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-397">Le système de fichiers prend en charge les quotas de disque.</span><span class="sxs-lookup"><span data-stu-id="069d8-397">The file system supports disk quotas.</span></span>

</dd> <dt>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>

<span data-ttu-id="069d8-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Prend en charge les fichiers partiellement alloués** (64)</span><span class="sxs-lookup"><span data-stu-id="069d8-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Supports Sparse Files** (64)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-399">Le système de fichiers prend en charge les fichiers de réserve.</span><span class="sxs-lookup"><span data-stu-id="069d8-399">The file system supports spare files.</span></span>

</dd> <dt>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>

<span data-ttu-id="069d8-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Prend en charge les points d’analyse** (128)</span><span class="sxs-lookup"><span data-stu-id="069d8-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Supports Reparse Points** (128)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-401">Le système de fichiers prend en charge les points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="069d8-401">The file system supports reparse points.</span></span>

</dd> <dt>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>

<span data-ttu-id="069d8-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Prend en charge le stockage distant** (256)</span><span class="sxs-lookup"><span data-stu-id="069d8-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Supports Remote Storage** (256)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-403">Le système de fichiers prend en charge le stockage étendu des fichiers.</span><span class="sxs-lookup"><span data-stu-id="069d8-403">The file system supports the remote storage of files.</span></span>

</dd> <dt>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>

<span data-ttu-id="069d8-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Prend en charge les noms longs** (16384)</span><span class="sxs-lookup"><span data-stu-id="069d8-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Supports Long Names** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-405">Le système de fichiers prend en charge les noms de fichiers de plus de huit caractères.</span><span class="sxs-lookup"><span data-stu-id="069d8-405">The file system supports file names that are longer than eight characters.</span></span>

</dd> <dt>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>

<span data-ttu-id="069d8-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>Le **volume est compressé** (32768)</span><span class="sxs-lookup"><span data-stu-id="069d8-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume Is Compressed** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-407">Le volume de disque spécifié est un volume compressé, par exemple, un volume DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="069d8-407">The specified disk volume is a compressed volume, for example, a DoubleSpace volume.</span></span>

</dd> <dt>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>

<span data-ttu-id="069d8-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Volume en lecture seule** (524289)</span><span class="sxs-lookup"><span data-stu-id="069d8-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Read Only Volume** (524289)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-409">Le volume spécifié est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="069d8-409">The specified volume is read-only.</span></span>

</dd> <dt>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>

<span data-ttu-id="069d8-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Prend en charge les ID d’objet** (65536)</span><span class="sxs-lookup"><span data-stu-id="069d8-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Supports Object IDS** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-411">Le système de fichiers prend en charge les identificateurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="069d8-411">The file system supports object identifiers.</span></span>

</dd> <dt>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>

<span data-ttu-id="069d8-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Prend en charge le chiffrement** (131072)</span><span class="sxs-lookup"><span data-stu-id="069d8-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Supports Encryption** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-413">Le système de fichiers prend en charge le système de fichiers EFS (Encrypted File System).</span><span class="sxs-lookup"><span data-stu-id="069d8-413">The file system supports the Encrypted File System (EFS).</span></span>

</dd> <dt>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>

<span data-ttu-id="069d8-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Prend en charge les flux nommés** (262144)</span><span class="sxs-lookup"><span data-stu-id="069d8-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Supports Named Streams** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-415">Le système de fichiers prend en charge les flux nommés.</span><span class="sxs-lookup"><span data-stu-id="069d8-415">The file system supports named streams.</span></span>

</dd> </dl>

<span data-ttu-id="069d8-416">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="069d8-416">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="069d8-417">**Id**</span><span class="sxs-lookup"><span data-stu-id="069d8-417">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-418">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-420">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions de fichier \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="069d8-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-421">Lettre de lecteur qui identifie de façon unique ce lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="069d8-421">Drive letter that uniquely identifies this CD-ROM drive.</span></span>

<span data-ttu-id="069d8-422">Exemple : "d : \\ "</span><span class="sxs-lookup"><span data-stu-id="069d8-422">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="069d8-423">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="069d8-423">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-424">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="069d8-424">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-426">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="069d8-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-427">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="069d8-427">Date and time the object is installed.</span></span> <span data-ttu-id="069d8-428">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="069d8-428">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="069d8-429">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-430">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="069d8-430">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-431">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069d8-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-433">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="069d8-433">Last error code reported by the logical device.</span></span>

<span data-ttu-id="069d8-434">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-434">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-435">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="069d8-435">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-438">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="069d8-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-439">Fabricant du lecteur de CD-ROM Windows.</span><span class="sxs-lookup"><span data-stu-id="069d8-439">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="069d8-440">Exemple : « PLEXTOR »</span><span class="sxs-lookup"><span data-stu-id="069d8-440">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="069d8-441">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="069d8-441">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-442">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="069d8-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-444">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="069d8-444">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-445">Taille maximale de bloc, en octets, pour les médias auxquels ce périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="069d8-445">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="069d8-446">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-446">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="069d8-447">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="069d8-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-448">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="069d8-448">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-449">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069d8-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-451">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions du système de fichiers win32api \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)»)</span><span class="sxs-lookup"><span data-stu-id="069d8-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-452">Longueur maximale d’un composant de nom de fichier pris en charge par le lecteur de CD-ROM Windows.</span><span class="sxs-lookup"><span data-stu-id="069d8-452">Maximum length of a filename component supported by the Windows CD-ROM drive.</span></span> <span data-ttu-id="069d8-453">Composant de nom de fichier qui est la partie d’un nom de fichier entre les barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="069d8-453">A file name component the portion of a file name between backslashes.</span></span> <span data-ttu-id="069d8-454">La valeur peut être utilisée pour indiquer que les noms longs sont pris en charge par le système de fichiers spécifié.</span><span class="sxs-lookup"><span data-stu-id="069d8-454">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="069d8-455">Par exemple, pour un système de fichiers FAT prenant en charge les noms longs, la fonction stocke la valeur 255, plutôt que l’indicateur 8,3 précédent.</span><span class="sxs-lookup"><span data-stu-id="069d8-455">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="069d8-456">Les noms longs peuvent également être pris en charge sur les systèmes qui utilisent le système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="069d8-456">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="069d8-457">Exemple : 255</span><span class="sxs-lookup"><span data-stu-id="069d8-457">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="069d8-458">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="069d8-458">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-459">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="069d8-459">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-461">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="069d8-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-462">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-462">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="069d8-463">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="069d8-464">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="069d8-464">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-465">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="069d8-465">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-466">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="069d8-466">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-467">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-468">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions du système de fichiers win32api \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)»)</span><span class="sxs-lookup"><span data-stu-id="069d8-468">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-469">Si la **valeur est true**, un CD-ROM se trouve dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="069d8-469">If **True**, a CD-ROM is in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="069d8-470">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="069d8-470">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-471">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-473">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="069d8-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-474">Type de média qui peut être utilisé ou accessible par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-474">Type of media that can be used or accessed by this device.</span></span> <span data-ttu-id="069d8-475">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="069d8-475">Possible values are:</span></span>

<dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="069d8-476">**Accès aléatoire** (« accès aléatoire »)</span><span class="sxs-lookup"><span data-stu-id="069d8-476">**Random Access** ("Random Access")</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="069d8-477">**Prend en charge l’écriture** (« prend en charge l’écriture »)</span><span class="sxs-lookup"><span data-stu-id="069d8-477">**Supports Writing** ("Supports Writing")</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="069d8-478">**Support amovible** (« support amovible »)</span><span class="sxs-lookup"><span data-stu-id="069d8-478">**Removable Media** ("Removable Media")</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="069d8-479">**CD-ROM** (« CD-ROM »)</span><span class="sxs-lookup"><span data-stu-id="069d8-479">**CD-ROM** ("CD-ROM")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="069d8-480">**MfrAssignedRevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="069d8-480">**MfrAssignedRevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-483">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win2000DDK \| KernelModeDrivers \| [**Storage \_ Device \_ Description**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| ProductRevisionOffset »)</span><span class="sxs-lookup"><span data-stu-id="069d8-483">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK\|KernelModeDrivers\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-484">Niveau de révision du microprogramme attribué par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="069d8-484">Firmware revision level that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="069d8-485">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="069d8-485">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-486">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="069d8-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-488">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="069d8-488">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-489">Taille de bloc minimale, en octets, pour les médias auxquels ce périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="069d8-489">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="069d8-490">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-490">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="069d8-491">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="069d8-491">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-492">**Nom**</span><span class="sxs-lookup"><span data-stu-id="069d8-492">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-493">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-494">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-495">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="069d8-495">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-496">Étiquette de l’objet.</span><span class="sxs-lookup"><span data-stu-id="069d8-496">Label for the object.</span></span> <span data-ttu-id="069d8-497">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="069d8-497">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="069d8-498">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-498">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-499">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="069d8-499">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-500">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="069d8-500">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-501">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-502">Si la **valeur est true**, l’appareil d’accès aux médias doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="069d8-502">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="069d8-503">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété **capacités** .</span><span class="sxs-lookup"><span data-stu-id="069d8-503">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="069d8-504">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-504">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-505">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="069d8-505">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-506">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069d8-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-508">Nombre maximal de médias pouvant être pris en charge ou insérés lorsque l’appareil d’accès aux médias prend en charge plusieurs médias individuels.</span><span class="sxs-lookup"><span data-stu-id="069d8-508">Maximum number of media that can be supported or inserted, when the media access device supports multiple individual media.</span></span>

<span data-ttu-id="069d8-509">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-509">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-510">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="069d8-510">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-511">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-512">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-513">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="069d8-513">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-514">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="069d8-514">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="069d8-515">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-515">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="069d8-516">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="069d8-516">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="069d8-517">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="069d8-517">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-518">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069d8-518">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="069d8-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-520">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="069d8-520">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="069d8-521">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="069d8-521">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="069d8-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="069d8-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="069d8-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="069d8-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-524">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="069d8-524">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="069d8-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="069d8-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="069d8-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="069d8-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-527">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="069d8-527">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="069d8-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="069d8-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-529">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="069d8-529">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="069d8-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="069d8-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-531">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="069d8-531">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="069d8-532">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="069d8-532">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="069d8-533">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="069d8-533">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="069d8-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="069d8-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-535">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="069d8-535">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="069d8-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="069d8-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="069d8-537">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="069d8-537">Timed Power-On Supported</span></span>

<span data-ttu-id="069d8-538">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="069d8-538">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="069d8-539">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="069d8-539">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-540">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="069d8-540">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-541">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-541">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069d8-542">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, ce qui signifie qu’il peut être mis en mode de suspension, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="069d8-542">If **True**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="069d8-543">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="069d8-543">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="069d8-544">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-544">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-545">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="069d8-545">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-546">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-547">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-548">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| RevisionLevel")</span><span class="sxs-lookup"><span data-stu-id="069d8-548">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|RevisionLevel")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-549">Niveau de révision du microprogramme du lecteur de CD-ROM Windows.</span><span class="sxs-lookup"><span data-stu-id="069d8-549">Firmware revision level of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="069d8-550">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="069d8-550">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-551">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069d8-551">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-552">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-553">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| SCSI structures \| [**SCSI \_ Request \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| PathID »)</span><span class="sxs-lookup"><span data-stu-id="069d8-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-554">Numéro de bus SCSI du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="069d8-554">SCSI bus number for the disk drive.</span></span>

<span data-ttu-id="069d8-555">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="069d8-555">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="069d8-556">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="069d8-556">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-557">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069d8-557">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-558">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-559">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| SCSI structures \| [**SCSI \_ Request \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| LUN »)</span><span class="sxs-lookup"><span data-stu-id="069d8-559">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-560">Numéro d’unité logique (LUN) SCSI du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="069d8-560">SCSI logical unit number (LUN) of the disk drive.</span></span> <span data-ttu-id="069d8-561">Le numéro d’unité logique est utilisé pour désigner le contrôleur SCSI qui fait l’objet d’un accès dans un système où plusieurs contrôleurs sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="069d8-561">The LUN is used to designate which SCSI controller is being accessed in a system with more than one controller being used.</span></span> <span data-ttu-id="069d8-562">L’identificateur du périphérique SCSI est similaire, mais il s’agit de la désignation de plusieurs appareils sur un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="069d8-562">The SCSI device identifier is similar, but is the designation for multiple devices on one controller.</span></span>

<span data-ttu-id="069d8-563">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="069d8-563">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="069d8-564">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="069d8-564">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-565">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069d8-565">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-566">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-567">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| SCSI structures \| [**SCSI \_ Request \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| ScsiStatus »)</span><span class="sxs-lookup"><span data-stu-id="069d8-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|ScsiStatus")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-568">Numéro de Port SCSI du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="069d8-568">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="069d8-569">Exemple : 1</span><span class="sxs-lookup"><span data-stu-id="069d8-569">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="069d8-570">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="069d8-570">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-571">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069d8-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-572">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-573">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| DeviceIoControl \| IOCTL \_ SCSI \_ obten \_ Address")</span><span class="sxs-lookup"><span data-stu-id="069d8-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|DeviceIoControl\|IOCTL\_SCSI\_GET\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-574">Numéro d’identificateur SCSI du lecteur de CD-ROM Windows.</span><span class="sxs-lookup"><span data-stu-id="069d8-574">SCSI identifier number of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="069d8-575">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="069d8-575">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="069d8-576">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="069d8-576">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-577">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-578">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-579">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| structures d’entrée et de sortie de l’appareil win32api \| [**\_ \_ descripteur de périphérique de stockage**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| SerialNumberOffset")</span><span class="sxs-lookup"><span data-stu-id="069d8-579">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-580">Numéro fourni par le fabricant qui identifie le support physique.</span><span class="sxs-lookup"><span data-stu-id="069d8-580">Number supplied by the manufacturer that identifies the physical media.</span></span> <span data-ttu-id="069d8-581">Exemple : WD-WM3493798728.</span><span class="sxs-lookup"><span data-stu-id="069d8-581">Example: WD-WM3493798728.</span></span>

</dd> <dt>

<span data-ttu-id="069d8-582">**Taille**</span><span class="sxs-lookup"><span data-stu-id="069d8-582">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-583">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="069d8-583">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-584">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-585">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Function Functions \| GetDiskFreeSpace"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="069d8-585">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDiskFreeSpace"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-586">Taille du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="069d8-586">Size of the disk drive.</span></span>

<span data-ttu-id="069d8-587">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="069d8-587">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-588">**État**</span><span class="sxs-lookup"><span data-stu-id="069d8-588">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-589">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-590">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-591">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="069d8-591">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-592">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="069d8-592">Current status of the object.</span></span> <span data-ttu-id="069d8-593">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="069d8-593">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="069d8-594">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="069d8-594">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="069d8-595">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="069d8-595">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="069d8-596">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="069d8-596">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="069d8-597">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="069d8-597">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="069d8-598">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-598">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="069d8-599">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="069d8-599">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="069d8-600">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="069d8-600">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="069d8-601">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="069d8-601">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="069d8-602">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="069d8-602">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="069d8-603">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="069d8-603">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="069d8-604">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="069d8-604">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="069d8-605">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="069d8-605">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="069d8-606">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="069d8-606">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="069d8-607">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="069d8-607">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="069d8-608">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="069d8-608">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="069d8-609">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="069d8-609">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="069d8-610">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="069d8-610">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="069d8-611">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="069d8-611">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="069d8-612">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="069d8-612">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-613">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069d8-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-614">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-615">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="069d8-615">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-616">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="069d8-616">State of the logical device.</span></span> <span data-ttu-id="069d8-617">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="069d8-617">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="069d8-618">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-618">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="069d8-619">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="069d8-619">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="069d8-620">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="069d8-620">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="069d8-621">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="069d8-621">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="069d8-622">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="069d8-622">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="069d8-623">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="069d8-623">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="069d8-624">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="069d8-624">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-625">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-626">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-626">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-627">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="069d8-627">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="069d8-628">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="069d8-628">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="069d8-629">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-629">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-630">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="069d8-630">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-631">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-632">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-632">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-633">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="069d8-633">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="069d8-634">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="069d8-634">Name of the scoping system.</span></span>

<span data-ttu-id="069d8-635">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-635">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="069d8-636">**TransferRate**</span><span class="sxs-lookup"><span data-stu-id="069d8-636">**TransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-637">Type de données : **real64**</span><span class="sxs-lookup"><span data-stu-id="069d8-637">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-638">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-638">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-639">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Référence du fichier et heure de référence"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilo-octets par seconde")</span><span class="sxs-lookup"><span data-stu-id="069d8-639">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Reference and Time Reference"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes per second")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-640">Taux de transfert du lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="069d8-640">Transfer rate of the CD-ROM drive.</span></span> <span data-ttu-id="069d8-641">La valeur-1 indique que le taux ne peut pas être déterminé.</span><span class="sxs-lookup"><span data-stu-id="069d8-641">A value of -1 indicates that the rate cannot be determined.</span></span> <span data-ttu-id="069d8-642">Dans ce cas, le CD n’est pas dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="069d8-642">When this happens, the CD is not in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="069d8-643">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="069d8-643">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-644">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-644">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-645">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-646">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions du système de fichiers win32api \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)»)</span><span class="sxs-lookup"><span data-stu-id="069d8-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-647">Nom du volume du lecteur de CD-ROM Windows.</span><span class="sxs-lookup"><span data-stu-id="069d8-647">Volume name of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="069d8-648">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="069d8-648">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069d8-649">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="069d8-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069d8-650">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="069d8-650">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069d8-651">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions du système de fichiers win32api \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)»)</span><span class="sxs-lookup"><span data-stu-id="069d8-651">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="069d8-652">Numéro de série du volume du support dans le lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="069d8-652">Volume serial number of the media in the CD-ROM drive.</span></span>

<span data-ttu-id="069d8-653">Exemple : A8C3-D032</span><span class="sxs-lookup"><span data-stu-id="069d8-653">Example: A8C3-D032</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="069d8-654">Notes</span><span class="sxs-lookup"><span data-stu-id="069d8-654">Remarks</span></span>

<span data-ttu-id="069d8-655">La classe **Win32 \_ CDROMDrive** est dérivée de [**CIM \_ CDROMDrive**](cim-cdromdrive.md) qui dérive de [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-655">The **Win32\_CDROMDrive** class is derived from [**CIM\_CDROMDrive**](cim-cdromdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="069d8-656">La classe **CIM \_ MediaAccessDevice** dérive de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="069d8-656">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="069d8-657">Exemples</span><span class="sxs-lookup"><span data-stu-id="069d8-657">Examples</span></span>

<span data-ttu-id="069d8-658">L’exemple VBScript suivant détermine si un CD se trouve dans un lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="069d8-658">The following VBScript example determines if a CD is in a CDROM drive.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject(_
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery( _
    "Select * from Win32_CDROMDrive")
For Each objItem in colItems
    Wscript.Echo "Device ID: " _
        & objItem.DeviceID
    Wscript.Echo "Media Loaded: " _
        & objItem.MediaLoaded
Next
```



## <a name="requirements"></a><span data-ttu-id="069d8-659">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="069d8-659">Requirements</span></span>



| <span data-ttu-id="069d8-660">Condition requise</span><span class="sxs-lookup"><span data-stu-id="069d8-660">Requirement</span></span> | <span data-ttu-id="069d8-661">Valeur</span><span class="sxs-lookup"><span data-stu-id="069d8-661">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="069d8-662">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="069d8-662">Minimum supported client</span></span><br/> | <span data-ttu-id="069d8-663">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="069d8-663">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="069d8-664">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="069d8-664">Minimum supported server</span></span><br/> | <span data-ttu-id="069d8-665">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="069d8-665">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="069d8-666">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="069d8-666">Namespace</span></span><br/>                | <span data-ttu-id="069d8-667">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="069d8-667">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="069d8-668">MOF</span><span class="sxs-lookup"><span data-stu-id="069d8-668">MOF</span></span><br/>                      | <dl> <span data-ttu-id="069d8-669"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="069d8-669"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="069d8-670">DLL</span><span class="sxs-lookup"><span data-stu-id="069d8-670">DLL</span></span><br/>                      | <dl> <span data-ttu-id="069d8-671"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="069d8-671"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="069d8-672">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="069d8-672">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069d8-673">**\_CDROMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="069d8-673">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="069d8-674">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="069d8-674">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="069d8-675">Tâches WMI : matériel de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="069d8-675">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="069d8-676">Tâches WMI : disques et systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="069d8-676">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

