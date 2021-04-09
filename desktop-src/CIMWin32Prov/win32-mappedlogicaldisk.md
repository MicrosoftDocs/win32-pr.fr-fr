---
description: Le \_ MappedLogicalDisk Win32 &\# 32 ; La classe WMI représente les périphériques de stockage réseau mappés en tant que disques logiques sur le système informatique.
ms.assetid: 5dd4b0eb-7872-4f2d-9c8b-ea03f7e2c16d
ms.tgt_platform: multiple
title: Classe Win32_MappedLogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MappedLogicalDisk
- Win32_MappedLogicalDisk.Reset
- Win32_MappedLogicalDisk.SetPowerState
- Win32_MappedLogicalDisk.Access
- Win32_MappedLogicalDisk.Availability
- Win32_MappedLogicalDisk.BlockSize
- Win32_MappedLogicalDisk.Caption
- Win32_MappedLogicalDisk.Compressed
- Win32_MappedLogicalDisk.ConfigManagerErrorCode
- Win32_MappedLogicalDisk.ConfigManagerUserConfig
- Win32_MappedLogicalDisk.CreationClassName
- Win32_MappedLogicalDisk.Description
- Win32_MappedLogicalDisk.DeviceID
- Win32_MappedLogicalDisk.ErrorCleared
- Win32_MappedLogicalDisk.ErrorDescription
- Win32_MappedLogicalDisk.ErrorMethodology
- Win32_MappedLogicalDisk.FileSystem
- Win32_MappedLogicalDisk.FreeSpace
- Win32_MappedLogicalDisk.InstallDate
- Win32_MappedLogicalDisk.LastErrorCode
- Win32_MappedLogicalDisk.MaximumComponentLength
- Win32_MappedLogicalDisk.Name
- Win32_MappedLogicalDisk.NumberOfBlocks
- Win32_MappedLogicalDisk.PNPDeviceID
- Win32_MappedLogicalDisk.PowerManagementCapabilities
- Win32_MappedLogicalDisk.PowerManagementSupported
- Win32_MappedLogicalDisk.ProviderName
- Win32_MappedLogicalDisk.Purpose
- Win32_MappedLogicalDisk.QuotasDisabled
- Win32_MappedLogicalDisk.QuotasIncomplete
- Win32_MappedLogicalDisk.QuotasRebuilding
- Win32_MappedLogicalDisk.SessionID
- Win32_MappedLogicalDisk.Size
- Win32_MappedLogicalDisk.Status
- Win32_MappedLogicalDisk.StatusInfo
- Win32_MappedLogicalDisk.SupportsDiskQuotas
- Win32_MappedLogicalDisk.SupportsFileBasedCompression
- Win32_MappedLogicalDisk.SystemCreationClassName
- Win32_MappedLogicalDisk.SystemName
- Win32_MappedLogicalDisk.VolumeName
- Win32_MappedLogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c3dfee876c34f36fd0b4cf0b59d3a61afcd75c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111487"
---
# <a name="win32_mappedlogicaldisk-class"></a><span data-ttu-id="b1126-103">\_Classe MappedLogicalDisk Win32</span><span class="sxs-lookup"><span data-stu-id="b1126-103">Win32\_MappedLogicalDisk class</span></span>

<span data-ttu-id="b1126-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MappedLogicalDisk** WMI représente les périphériques de stockage réseau mappés en tant que disques logiques sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="b1126-104">The **Win32\_MappedLogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents network storage devices that are mapped as logical disks on the computer system.</span></span>

<span data-ttu-id="b1126-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b1126-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b1126-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b1126-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1126-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1126-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{BCF02FFE-5560-4de2-B419-272918693426}"), AMENDMENT]
class Win32_MappedLogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   SessionID;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="b1126-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b1126-108">Members</span></span>

<span data-ttu-id="b1126-109">La classe **Win32 \_ MappedLogicalDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b1126-109">The **Win32\_MappedLogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="b1126-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b1126-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1126-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b1126-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1126-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b1126-112">Methods</span></span>

<span data-ttu-id="b1126-113">La classe **Win32 \_ MappedLogicalDisk** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b1126-113">The **Win32\_MappedLogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="b1126-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="b1126-114">Method</span></span>            | <span data-ttu-id="b1126-115">Description</span><span class="sxs-lookup"><span data-stu-id="b1126-115">Description</span></span>                                                                                                                                                                                |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1126-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="b1126-116">**Reset**</span></span>         | <span data-ttu-id="b1126-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b1126-117">Not implemented.</span></span> <span data-ttu-id="b1126-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans le [**\_ disque logique CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>                 |
| <span data-ttu-id="b1126-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b1126-119">**SetPowerState**</span></span> | <span data-ttu-id="b1126-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b1126-120">Not implemented.</span></span> <span data-ttu-id="b1126-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans le [**\_ disque logique CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b1126-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b1126-122">Properties</span></span>

<span data-ttu-id="b1126-123">La classe **Win32 \_ MappedLogicalDisk** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b1126-123">The **Win32\_MappedLogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1126-124">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="b1126-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1126-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-127">État de l’accès au périphérique.</span><span class="sxs-lookup"><span data-stu-id="b1126-127">Device access state.</span></span>

<span data-ttu-id="b1126-128">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1126-129">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="b1126-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="b1126-130">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="b1126-130">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="b1126-131">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="b1126-131">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="b1126-132">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="b1126-132">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="b1126-133">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="b1126-133">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1126-134">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="b1126-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1126-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-137">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b1126-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-138">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-138">Availability and status of the device.</span></span>

<span data-ttu-id="b1126-139">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1126-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b1126-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1126-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="b1126-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b1126-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="b1126-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-143">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="b1126-143">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b1126-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="b1126-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b1126-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="b1126-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1126-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="b1126-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b1126-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="b1126-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b1126-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="b1126-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-149">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="b1126-149">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b1126-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="b1126-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1126-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="b1126-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b1126-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="b1126-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b1126-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="b1126-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b1126-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="b1126-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-155">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="b1126-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b1126-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="b1126-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-157">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="b1126-157">The device is in a power save state but still functioning and can exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b1126-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="b1126-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-159">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="b1126-159">The device is not functioning, but can be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b1126-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="b1126-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b1126-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="b1126-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-162">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="b1126-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b1126-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="b1126-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-164">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="b1126-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b1126-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="b1126-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-166">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="b1126-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b1126-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="b1126-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-168">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="b1126-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b1126-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="b1126-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-170">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="b1126-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1126-171">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="b1126-171">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-172">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1126-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-174">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="b1126-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-175">Taille, en octets, des blocs qui forment cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="b1126-175">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="b1126-176">Si ce concept n’est pas valide pour le type d’appareil, la valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="b1126-176">If this concept is not valid for the device type, the value is 1.</span></span>

<span data-ttu-id="b1126-177">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-177">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b1126-178">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1126-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-179">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b1126-179">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-182">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="b1126-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-183">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1126-183">Short description of the object.</span></span>

<span data-ttu-id="b1126-184">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-185">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="b1126-185">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-186">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-188">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions du système de fichiers win32api \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ vol \_ est \_ compressé »)</span><span class="sxs-lookup"><span data-stu-id="b1126-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-189">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="b1126-189">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b1126-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-191">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1126-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-193">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1126-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-194">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b1126-194">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b1126-195">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b1126-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="b1126-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b1126-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="b1126-197">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-198">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="b1126-198">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b1126-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="b1126-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b1126-200">(1)</span><span class="sxs-lookup"><span data-stu-id="b1126-200">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-201">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="b1126-201">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1126-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b1126-203">(2)</span><span class="sxs-lookup"><span data-stu-id="b1126-203">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b1126-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="b1126-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b1126-205">(3)</span><span class="sxs-lookup"><span data-stu-id="b1126-205">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-206">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="b1126-206">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b1126-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="b1126-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b1126-208">(4)</span><span class="sxs-lookup"><span data-stu-id="b1126-208">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-209">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="b1126-209">Device is not working properly.</span></span> <span data-ttu-id="b1126-210">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="b1126-210">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b1126-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="b1126-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b1126-212">(5)</span><span class="sxs-lookup"><span data-stu-id="b1126-212">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-213">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="b1126-213">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b1126-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="b1126-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b1126-215"> (6)</span><span class="sxs-lookup"><span data-stu-id="b1126-215">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-216">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="b1126-216">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b1126-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="b1126-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b1126-218">(7)</span><span class="sxs-lookup"><span data-stu-id="b1126-218">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b1126-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="b1126-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b1126-220">(8)</span><span class="sxs-lookup"><span data-stu-id="b1126-220">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-221">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="b1126-221">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b1126-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b1126-223">(9)</span><span class="sxs-lookup"><span data-stu-id="b1126-223">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-224">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="b1126-224">Device is not working properly.</span></span> <span data-ttu-id="b1126-225">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-225">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b1126-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b1126-227">(10)</span><span class="sxs-lookup"><span data-stu-id="b1126-227">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-228">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-228">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b1126-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b1126-230">(11)</span><span class="sxs-lookup"><span data-stu-id="b1126-230">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-231">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-231">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b1126-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="b1126-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b1126-233">douze</span><span class="sxs-lookup"><span data-stu-id="b1126-233">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-234">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b1126-234">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b1126-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b1126-236">(13)</span><span class="sxs-lookup"><span data-stu-id="b1126-236">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-237">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-237">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b1126-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="b1126-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b1126-239">(14)</span><span class="sxs-lookup"><span data-stu-id="b1126-239">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-240">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="b1126-240">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b1126-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="b1126-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b1126-242">(15)</span><span class="sxs-lookup"><span data-stu-id="b1126-242">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-243">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="b1126-243">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b1126-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b1126-245">(16)</span><span class="sxs-lookup"><span data-stu-id="b1126-245">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-246">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-246">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b1126-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="b1126-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b1126-248">(17)</span><span class="sxs-lookup"><span data-stu-id="b1126-248">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-249">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="b1126-249">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1126-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b1126-251">(18)</span><span class="sxs-lookup"><span data-stu-id="b1126-251">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-252">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="b1126-252">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b1126-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="b1126-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b1126-254">(19)</span><span class="sxs-lookup"><span data-stu-id="b1126-254">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b1126-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="b1126-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b1126-256">(20)</span><span class="sxs-lookup"><span data-stu-id="b1126-256">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-257">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="b1126-257">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b1126-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b1126-259">(21)</span><span class="sxs-lookup"><span data-stu-id="b1126-259">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-260">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="b1126-260">System failure.</span></span> <span data-ttu-id="b1126-261">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="b1126-261">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b1126-262">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-262">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b1126-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="b1126-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b1126-264">(22)</span><span class="sxs-lookup"><span data-stu-id="b1126-264">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-265">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b1126-265">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b1126-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="b1126-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b1126-267">(23)</span><span class="sxs-lookup"><span data-stu-id="b1126-267">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-268">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="b1126-268">System failure.</span></span> <span data-ttu-id="b1126-269">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="b1126-269">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b1126-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="b1126-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b1126-271">(24)</span><span class="sxs-lookup"><span data-stu-id="b1126-271">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-272">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="b1126-272">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b1126-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b1126-274">(25)</span><span class="sxs-lookup"><span data-stu-id="b1126-274">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-275">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b1126-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b1126-277">(26)</span><span class="sxs-lookup"><span data-stu-id="b1126-277">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-278">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1126-278">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b1126-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="b1126-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b1126-280">(27)</span><span class="sxs-lookup"><span data-stu-id="b1126-280">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-281">L’appareil n’a pas de configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="b1126-281">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b1126-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="b1126-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b1126-283">(28)</span><span class="sxs-lookup"><span data-stu-id="b1126-283">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-284">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="b1126-284">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b1126-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="b1126-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b1126-286">(29)</span><span class="sxs-lookup"><span data-stu-id="b1126-286">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-287">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b1126-287">Device is disabled.</span></span> <span data-ttu-id="b1126-288">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="b1126-288">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b1126-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="b1126-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b1126-290">(30)</span><span class="sxs-lookup"><span data-stu-id="b1126-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-291">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="b1126-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1126-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b1126-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b1126-293">31</span><span class="sxs-lookup"><span data-stu-id="b1126-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-294">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="b1126-294">Device is not working properly.</span></span> <span data-ttu-id="b1126-295">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="b1126-295">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1126-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b1126-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-297">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-299">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1126-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-300">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b1126-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b1126-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1126-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-305">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1126-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1126-306">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="b1126-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b1126-307">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="b1126-307">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b1126-308">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-309">**Description**</span><span class="sxs-lookup"><span data-stu-id="b1126-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-312">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b1126-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-313">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1126-313">Description of the object.</span></span>

<span data-ttu-id="b1126-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b1126-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-318">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="b1126-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-319">Identificateur unique du tableau de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b1126-319">Unique identifier of the memory array.</span></span>

<span data-ttu-id="b1126-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b1126-321">Exemple : « Memory Array 1 »</span><span class="sxs-lookup"><span data-stu-id="b1126-321">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="b1126-322">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b1126-322">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-323">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-325">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="b1126-325">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b1126-326">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-327">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b1126-327">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-330">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="b1126-330">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span>

<span data-ttu-id="b1126-331">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-332">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="b1126-332">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-335">Types de contrôle d’erreur utilisés par le matériel.</span><span class="sxs-lookup"><span data-stu-id="b1126-335">Types of error checking used by the hardware.</span></span>

<span data-ttu-id="b1126-336">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-336">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-337">**FileSystem**</span><span class="sxs-lookup"><span data-stu-id="b1126-337">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-340">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions du système de fichiers [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="b1126-340">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="b1126-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-341">Access type: Read-only</span></span>

<span data-ttu-id="b1126-342">Système de fichiers sur le disque logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-342">File system on the logical disk.</span></span>

<span data-ttu-id="b1126-343">Exemple : "NTFS"</span><span class="sxs-lookup"><span data-stu-id="b1126-343">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="b1126-344">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="b1126-344">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-345">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1126-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-347">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b1126-347">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-348">Espace disponible sur le disque logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-348">Space available on the logical disk.</span></span>

<span data-ttu-id="b1126-349">Cette propriété est héritée [**du \_ disque logique CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-349">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="b1126-350">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1126-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-351">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1126-351">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-352">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1126-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-354">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="b1126-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-355">Access type: Read-only</span></span>

<span data-ttu-id="b1126-356">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1126-356">Date and time the object was installed.</span></span> <span data-ttu-id="b1126-357">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="b1126-357">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b1126-358">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-359">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b1126-359">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-360">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1126-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-362">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-362">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b1126-363">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-364">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="b1126-364">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-365">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1126-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-367">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions du système de fichiers [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="b1126-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="b1126-368">Contient la longueur maximale d’un composant de nom de fichier pris en charge par le lecteur Windows.</span><span class="sxs-lookup"><span data-stu-id="b1126-368">Contains the maximum length of a file-name component supported by the Windows drive.</span></span>

<span data-ttu-id="b1126-369">Exemple : 255</span><span class="sxs-lookup"><span data-stu-id="b1126-369">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="b1126-370">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b1126-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-371">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-373">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b1126-373">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-374">Étiquette de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1126-374">Object label.</span></span>

<span data-ttu-id="b1126-375">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-376">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="b1126-376">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-377">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1126-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-379">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="b1126-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-380">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="b1126-380">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="b1126-381">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="b1126-381">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="b1126-382">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="b1126-382">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="b1126-383">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-383">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b1126-384">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1126-384">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-385">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b1126-385">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-386">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-388">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1126-388">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-389">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-389">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b1126-390">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b1126-391">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="b1126-391">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b1126-392">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b1126-392">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-393">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1126-393">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1126-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-395">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-395">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b1126-396">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="b1126-396">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1126-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="b1126-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b1126-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="b1126-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1126-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="b1126-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b1126-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="b1126-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-401">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="b1126-401">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b1126-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="b1126-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-403">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="b1126-403">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b1126-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="b1126-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-405">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b1126-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b1126-406">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="b1126-406">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b1126-407">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b1126-407">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b1126-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="b1126-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-409">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="b1126-409">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b1126-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="b1126-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b1126-411">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1126-411">Timed Power-On Supported</span></span>

<span data-ttu-id="b1126-412">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="b1126-412">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1126-413">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b1126-413">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-414">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-414">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-416">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="b1126-416">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b1126-417">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="b1126-417">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b1126-418">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-418">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-419">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b1126-419">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-420">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-422">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| Windows Networking Functions \| WNetGetConnection »)</span><span class="sxs-lookup"><span data-stu-id="b1126-422">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-423">Nom du chemin d’accès réseau à l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-423">Network path name to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-424">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="b1126-424">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-425">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-427">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="b1126-427">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="b1126-428">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-429">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="b1126-429">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-430">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-430">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-432">Si la **valeur est true**, la gestion de quota n’est pas activée pour ce volume.</span><span class="sxs-lookup"><span data-stu-id="b1126-432">If **True**, quota management is not enabled for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-433">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="b1126-433">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-434">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-434">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-436">Si la **valeur est true**, la gestion de quota a été utilisée mais a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="b1126-436">If **True**, quota management was used but has been disabled.</span></span> <span data-ttu-id="b1126-437">Incomplet fait référence aux informations laissées dans le système de fichiers après la désactivation de la gestion de quota.</span><span class="sxs-lookup"><span data-stu-id="b1126-437">Incomplete refers to the information left in the file system after quota management has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-438">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="b1126-438">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-439">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-441">Si la **valeur est true**, le système de fichiers est configuré pour la gestion de quota.</span><span class="sxs-lookup"><span data-stu-id="b1126-441">If **True**, the file system is setting up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-442">**IDsession**</span><span class="sxs-lookup"><span data-stu-id="b1126-442">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-443">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-445">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b1126-445">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b1126-446">ID de la session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b1126-446">ID of the user's session.</span></span> <span data-ttu-id="b1126-447">L’utilisateur peut être connecté à l’aide d’une connexion locale ou d’une session de terminal.</span><span class="sxs-lookup"><span data-stu-id="b1126-447">The user may be connected using a local login or a terminal session.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-448">**Taille**</span><span class="sxs-lookup"><span data-stu-id="b1126-448">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-449">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1126-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-451">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b1126-451">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-452">Taille du disque logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-452">Size of the logical disk.</span></span>

<span data-ttu-id="b1126-453">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1126-453">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="b1126-454">Cette propriété est héritée [**du \_ disque logique CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-454">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-455">**État**</span><span class="sxs-lookup"><span data-stu-id="b1126-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-456">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-458">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b1126-458">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-459">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1126-459">Current status of the object.</span></span> <span data-ttu-id="b1126-460">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="b1126-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b1126-461">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent peut fonctionner correctement, mais prédit une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="b1126-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="b1126-462">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="b1126-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b1126-463">L’état du service s’applique aux tâches administratives, telles que la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="b1126-463">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b1126-464">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="b1126-464">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b1126-465">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b1126-466">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="b1126-466">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b1126-467">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="b1126-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b1126-468">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="b1126-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1126-469">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="b1126-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1126-470">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="b1126-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b1126-471">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="b1126-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b1126-472">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="b1126-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b1126-473">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="b1126-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b1126-474">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="b1126-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b1126-475">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="b1126-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b1126-476">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="b1126-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b1126-477">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="b1126-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b1126-478">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="b1126-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1126-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b1126-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-480">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1126-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-482">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b1126-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-483">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-483">State of the logical device.</span></span> <span data-ttu-id="b1126-484">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="b1126-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b1126-485">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1126-486">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b1126-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1126-487">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="b1126-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b1126-488">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="b1126-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1126-489">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="b1126-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1126-490">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="b1126-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1126-491">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="b1126-491">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-492">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-492">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-493">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1126-494">Si la **valeur est true**, le système de fichiers sur lequel ce lecteur réseau est mappé prend en charge les quotas de disque.</span><span class="sxs-lookup"><span data-stu-id="b1126-494">If **True**, then the file system on which this network drive is mapped supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-495">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="b1126-495">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-496">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b1126-496">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-497">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-498">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Functions du système de fichiers \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ compression de fichier \_ ")</span><span class="sxs-lookup"><span data-stu-id="b1126-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="b1126-499">Si la **valeur est true**, la partition de disque logique prend en charge la compression basée sur les fichiers, comme c’est le cas avec NTFS.</span><span class="sxs-lookup"><span data-stu-id="b1126-499">If **True**, the logical disk partition supports file-based compression, such as is the case with NTFS.</span></span> <span data-ttu-id="b1126-500">Cette propriété a la **valeur false**, lorsque la propriété **Compressed** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="b1126-500">This property is **False**, when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-501">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1126-501">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-502">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-503">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-504">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1126-504">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1126-505">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b1126-505">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b1126-506">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-506">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-507">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b1126-507">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-508">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-509">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-510">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1126-510">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1126-511">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="b1126-511">Name of the scoping system.</span></span>

<span data-ttu-id="b1126-512">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-512">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1126-513">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="b1126-513">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-514">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-515">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b1126-515">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b1126-516">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions du système de fichiers [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="b1126-516">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="b1126-517">Nom du volume du disque logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-517">Volume name of the logical disk.</span></span> <span data-ttu-id="b1126-518">Cette valeur de propriété peut comporter jusqu’à 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="b1126-518">This property value can have a maximum of 32 characters.</span></span>

</dd> <dt>

<span data-ttu-id="b1126-519">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b1126-519">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1126-520">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b1126-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1126-521">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b1126-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1126-522">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions du système de fichiers [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="b1126-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="b1126-523">Numéro de série du volume du disque logique.</span><span class="sxs-lookup"><span data-stu-id="b1126-523">Volume serial number of the logical disk.</span></span> <span data-ttu-id="b1126-524">Cette valeur de propriété peut avoir un maximum de 11 caractères.</span><span class="sxs-lookup"><span data-stu-id="b1126-524">This property value can have a maximum of 11 characters.</span></span>

<span data-ttu-id="b1126-525">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1126-525">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b1126-526">Exemple : « A8C3-D032 »</span><span class="sxs-lookup"><span data-stu-id="b1126-526">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1126-527">Notes</span><span class="sxs-lookup"><span data-stu-id="b1126-527">Remarks</span></span>

<span data-ttu-id="b1126-528">Les instances retournées pour cette classe sont les suivantes, en supposant que l’utilisateur A énumère les instances :</span><span class="sxs-lookup"><span data-stu-id="b1126-528">The instances returned for this class are as follows, supposing that user A is enumerating the instances:</span></span>

-   <span data-ttu-id="b1126-529">Le fournisseur recherche une session d’ouverture de session de l’utilisateur A sur cet ordinateur :</span><span class="sxs-lookup"><span data-stu-id="b1126-529">The provider looks for a logon session of user A on that machine:</span></span>

    -   <span data-ttu-id="b1126-530">S’il y en a une (et une seule) de cette ouverture de session, le fournisseur retourne les lecteurs mappés de cette session.</span><span class="sxs-lookup"><span data-stu-id="b1126-530">If there is one (and only one) such logon session, then the provider returns the mapped drives of that session.</span></span>
    -   <span data-ttu-id="b1126-531">S’il existe plusieurs sessions pour l’utilisateur A sur l’ordinateur, aucune instance de lecteur mappée n’est retournée (car le fournisseur n’a pas de moyen raisonnable de choisir la session à utiliser).</span><span class="sxs-lookup"><span data-stu-id="b1126-531">If there is more than one session for user A on the machine, then no mapped drive instances are returned (because the provider has no reasonable way of deciding which session to use).</span></span>

-   <span data-ttu-id="b1126-532">Si aucune session de l’utilisateur A n’est en cours d’exécution et qu’il existe un utilisateur connecté localement B :</span><span class="sxs-lookup"><span data-stu-id="b1126-532">If there are no sessions of user A running, and there is a locally logged on user B:</span></span>

    -   <span data-ttu-id="b1126-533">S’il existe une seule session pour l’utilisateur B, le fournisseur emprunte l’identité d’un et retourne les lecteurs mappés de l’utilisateur B. Ce cas de figure prend en charge le scénario de support technique qui souhaite voir les instances d’un utilisateur connecté localement.</span><span class="sxs-lookup"><span data-stu-id="b1126-533">If there is a single session for user B, then the provider impersonates A and returns the mapped drives of user B. This case supports the scenario of Helpdesk wanting to see the instances of a locally logged on user.</span></span> <span data-ttu-id="b1126-534">Toutefois, le fait que les instances soient retournées dépend des paramètres de stratégie de sécurité locale dans les outils d’administration du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b1126-534">However, whether instances are returned depends on the Local Security Policy settings in the Control Panel Administrative Tools.</span></span> <span data-ttu-id="b1126-535">Si la stratégie suivante est définie sur « créateur d’objet », aucune instance de lecteur mappée n’est retournée, même si un est membre du groupe administrateurs :</span><span class="sxs-lookup"><span data-stu-id="b1126-535">If the following policy is set to "Object Creator", then no mapped drive instances are returned, even if A is a member of the Administrators group:</span></span>

        <span data-ttu-id="b1126-536">« Objet système : propriétaire par défaut pour les objets créés par les membres du groupe administrateurs ».</span><span class="sxs-lookup"><span data-stu-id="b1126-536">"System object: default owner for objects created by members of the administrators group."</span></span>

    -   <span data-ttu-id="b1126-537">Là encore, si plusieurs sessions de l’utilisateur B sont en cours d’exécution sur l’ordinateur, le fournisseur n’a aucun moyen de décider de ce qu’il faut utiliser.</span><span class="sxs-lookup"><span data-stu-id="b1126-537">Again, if there is more than one session of user B running on the machine, then the provider has no way of deciding which to use.</span></span> <span data-ttu-id="b1126-538">Dans ce cas, aucune instance de lecteur mappée n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="b1126-538">In this case, no mapped drive instances are returned.</span></span>

<span data-ttu-id="b1126-539">Pour plus d’informations sur l’utilisation de **Win32 \_ MappedLogicalDisk**, consultez [Comment puis-je déterminer quels lecteurs sont mappés à des partages réseau ?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1126-539">For more information on using **Win32\_MappedLogicalDisk**, see [How Can I Determine Which Drives are Mapped to Network Shares?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="b1126-540">Exemples</span><span class="sxs-lookup"><span data-stu-id="b1126-540">Examples</span></span>

<span data-ttu-id="b1126-541">L’extrait de code PowerShell suivant montre les lecteurs mappés.</span><span class="sxs-lookup"><span data-stu-id="b1126-541">The following PowerShell snippet shows mapped drives.</span></span>


```PowerShell
Get-WmiObject Win32_MappedLogicalDisk | Select Name, ProviderName, FileSystem, Size, FreeSpace | Format-Table
```



## <a name="requirements"></a><span data-ttu-id="b1126-542">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1126-542">Requirements</span></span>



| <span data-ttu-id="b1126-543">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1126-543">Requirement</span></span> | <span data-ttu-id="b1126-544">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1126-544">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1126-545">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1126-545">Minimum supported client</span></span><br/> | <span data-ttu-id="b1126-546">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1126-546">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1126-547">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1126-547">Minimum supported server</span></span><br/> | <span data-ttu-id="b1126-548">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1126-548">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1126-549">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b1126-549">Namespace</span></span><br/>                | <span data-ttu-id="b1126-550">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b1126-550">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1126-551">MOF</span><span class="sxs-lookup"><span data-stu-id="b1126-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1126-552"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1126-552"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1126-553">DLL</span><span class="sxs-lookup"><span data-stu-id="b1126-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1126-554"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1126-554"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1126-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1126-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1126-556">**\_Disque logique CIM**</span><span class="sxs-lookup"><span data-stu-id="b1126-556">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="b1126-557">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="b1126-557">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b1126-558">Tâches WMI : disques et systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="b1126-558">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

