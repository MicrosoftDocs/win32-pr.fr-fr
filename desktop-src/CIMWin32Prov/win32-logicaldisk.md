---
description: Représente une source de données qui correspond à un périphérique de stockage local réel sur un système informatique exécutant Windows.
ms.assetid: 134a90cc-b2c3-4ade-a317-b96c4aabe63d
ms.tgt_platform: multiple
title: Classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk
- Win32_LogicalDisk.Reset
- Win32_LogicalDisk.SetPowerState
- Win32_LogicalDisk.Access
- Win32_LogicalDisk.Availability
- Win32_LogicalDisk.BlockSize
- Win32_LogicalDisk.Caption
- Win32_LogicalDisk.Compressed
- Win32_LogicalDisk.ConfigManagerErrorCode
- Win32_LogicalDisk.ConfigManagerUserConfig
- Win32_LogicalDisk.CreationClassName
- Win32_LogicalDisk.Description
- Win32_LogicalDisk.DeviceID
- Win32_LogicalDisk.DriveType
- Win32_LogicalDisk.ErrorCleared
- Win32_LogicalDisk.ErrorDescription
- Win32_LogicalDisk.ErrorMethodology
- Win32_LogicalDisk.FileSystem
- Win32_LogicalDisk.FreeSpace
- Win32_LogicalDisk.InstallDate
- Win32_LogicalDisk.LastErrorCode
- Win32_LogicalDisk.MaximumComponentLength
- Win32_LogicalDisk.MediaType
- Win32_LogicalDisk.Name
- Win32_LogicalDisk.NumberOfBlocks
- Win32_LogicalDisk.PNPDeviceID
- Win32_LogicalDisk.PowerManagementCapabilities
- Win32_LogicalDisk.PowerManagementSupported
- Win32_LogicalDisk.ProviderName
- Win32_LogicalDisk.Purpose
- Win32_LogicalDisk.QuotasDisabled
- Win32_LogicalDisk.QuotasIncomplete
- Win32_LogicalDisk.QuotasRebuilding
- Win32_LogicalDisk.Size
- Win32_LogicalDisk.Status
- Win32_LogicalDisk.StatusInfo
- Win32_LogicalDisk.SupportsDiskQuotas
- Win32_LogicalDisk.SupportsFileBasedCompression
- Win32_LogicalDisk.SystemCreationClassName
- Win32_LogicalDisk.SystemName
- Win32_LogicalDisk.VolumeDirty
- Win32_LogicalDisk.VolumeName
- Win32_LogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad1472f14e73d06c19ccc0808794a47f7588cf9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516563"
---
# <a name="win32_logicaldisk-class"></a><span data-ttu-id="05af7-103">\_Classe disque logique Win32</span><span class="sxs-lookup"><span data-stu-id="05af7-103">Win32\_LogicalDisk class</span></span>

<span data-ttu-id="05af7-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ disque logique Win32** représente une source de données qui correspond à un périphérique de stockage local réel sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="05af7-104">The **Win32\_LogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a data source that resolves to an actual local storage device on a computer system running Windows.</span></span>

<span data-ttu-id="05af7-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="05af7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="05af7-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="05af7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="05af7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05af7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDisk : CIM_LogicalDisk
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
  uint32   DriveType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  uint32   MediaType;
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
  string   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VolumeDirty;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="05af7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="05af7-108">Members</span></span>

<span data-ttu-id="05af7-109">La **classe \_ disque logique Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="05af7-109">The **Win32\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="05af7-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="05af7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="05af7-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="05af7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="05af7-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="05af7-112">Methods</span></span>

<span data-ttu-id="05af7-113">La **classe \_ disque logique Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="05af7-113">The **Win32\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="05af7-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="05af7-114">Method</span></span>                                                                             | <span data-ttu-id="05af7-115">Description</span><span class="sxs-lookup"><span data-stu-id="05af7-115">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05af7-116">**Chkdsk**</span><span class="sxs-lookup"><span data-stu-id="05af7-116">**Chkdsk**</span></span>](chkdsk-method-in-class-win32-logicaldisk.md)                         | <span data-ttu-id="05af7-117">Appelle l’opération [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) sur le disque.</span><span class="sxs-lookup"><span data-stu-id="05af7-117">Invokes the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation on the disk.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="05af7-118">**ExcludeFromAutochk**</span><span class="sxs-lookup"><span data-stu-id="05af7-118">**ExcludeFromAutochk**</span></span>](excludefromautochk-method-in-class-win32-logicaldisk.md) | <span data-ttu-id="05af7-119">Exclut les disques de l’opération [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) à exécuter au redémarrage suivant.</span><span class="sxs-lookup"><span data-stu-id="05af7-119">Excludes disks from the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation to be run at the next restart.</span></span><br/>                                                                                      |
| <span data-ttu-id="05af7-120">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="05af7-120">**Reset**</span></span>                                                                          | <span data-ttu-id="05af7-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="05af7-121">Not implemented.</span></span> <span data-ttu-id="05af7-122">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans le [**\_ disque logique CIM**](cim-logicaldisk.md) pour la documentation.</span><span class="sxs-lookup"><span data-stu-id="05af7-122">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md) for documentation.</span></span><br/> |
| [<span data-ttu-id="05af7-123">**ScheduleAutoChk**</span><span class="sxs-lookup"><span data-stu-id="05af7-123">**ScheduleAutoChk**</span></span>](scheduleautochk-method-in-class-win32-logicaldisk.md)       | <span data-ttu-id="05af7-124">Planifie l’exécution de [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) au prochain redémarrage si le bit d’intégrité a été défini.</span><span class="sxs-lookup"><span data-stu-id="05af7-124">Schedules [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart if the dirty bit has been set.</span></span><br/>                                                                                |
| <span data-ttu-id="05af7-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="05af7-125">**SetPowerState**</span></span>                                                                  | <span data-ttu-id="05af7-126">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="05af7-126">Not implemented.</span></span> <span data-ttu-id="05af7-127">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans le [**\_ disque logique CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-127">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="05af7-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="05af7-128">Properties</span></span>

<span data-ttu-id="05af7-129">La **classe \_ disque logique Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="05af7-129">The **Win32\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05af7-130">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="05af7-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05af7-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-133">Type d’accès aux médias disponible.</span><span class="sxs-lookup"><span data-stu-id="05af7-133">Type of media access available.</span></span>

<span data-ttu-id="05af7-134">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05af7-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="05af7-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="05af7-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="05af7-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="05af7-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="05af7-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-138">Accessible en écriture</span><span class="sxs-lookup"><span data-stu-id="05af7-138">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="05af7-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="05af7-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="05af7-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="05af7-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05af7-141">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="05af7-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05af7-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-144">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="05af7-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-145">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-145">Availability and status of the device.</span></span>

<span data-ttu-id="05af7-146">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="05af7-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="05af7-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05af7-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="05af7-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="05af7-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="05af7-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-150">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="05af7-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="05af7-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="05af7-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="05af7-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="05af7-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="05af7-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="05af7-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="05af7-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="05af7-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="05af7-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="05af7-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-156">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="05af7-156">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="05af7-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="05af7-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="05af7-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="05af7-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="05af7-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="05af7-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="05af7-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="05af7-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="05af7-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="05af7-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-162">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="05af7-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="05af7-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="05af7-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-164">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="05af7-164">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="05af7-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="05af7-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-166">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="05af7-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="05af7-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="05af7-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="05af7-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="05af7-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-169">L’appareil est dans un état d’avertissement, mais également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="05af7-169">The device is in a warning state, but also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="05af7-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="05af7-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-171">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="05af7-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="05af7-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="05af7-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-173">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="05af7-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="05af7-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="05af7-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-175">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="05af7-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="05af7-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="05af7-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-177">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="05af7-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05af7-178">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="05af7-178">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-179">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="05af7-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-181">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="05af7-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-182">Taille, en octets, des blocs qui forment cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="05af7-182">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="05af7-183">S’il est inconnu ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1.</span><span class="sxs-lookup"><span data-stu-id="05af7-183">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter 1.</span></span>

<span data-ttu-id="05af7-184">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="05af7-185">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="05af7-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-186">**Caption**</span><span class="sxs-lookup"><span data-stu-id="05af7-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-189">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="05af7-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-190">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="05af7-190">Short description of the object a one-line string.</span></span>

<span data-ttu-id="05af7-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-192">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="05af7-192">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-193">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-195">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions du système de fichiers win32api \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ vol \_ est \_ compressé »)</span><span class="sxs-lookup"><span data-stu-id="05af7-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-196">Si la **valeur est true**, le volume logique existe en tant qu’entité compressée unique, par exemple un volume DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="05af7-196">If **True**, the logical volume exists as a single compressed entity, such as a DoubleSpace volume.</span></span> <span data-ttu-id="05af7-197">Si la compression basée sur les fichiers est prise en charge, par exemple sur NTFS, cette propriété a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="05af7-197">If file based compression is supported, such as on NTFS, this property is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-198">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="05af7-198">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-199">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05af7-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-201">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="05af7-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-202">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="05af7-202">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="05af7-203">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-203">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="05af7-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="05af7-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="05af7-205"> (0)</span><span class="sxs-lookup"><span data-stu-id="05af7-205">(0)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-206">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="05af7-206">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="05af7-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="05af7-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="05af7-208">(1)</span><span class="sxs-lookup"><span data-stu-id="05af7-208">(1)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-209">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="05af7-209">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="05af7-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="05af7-211">(2)</span><span class="sxs-lookup"><span data-stu-id="05af7-211">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="05af7-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="05af7-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="05af7-213">(3)</span><span class="sxs-lookup"><span data-stu-id="05af7-213">(3)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-214">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="05af7-214">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="05af7-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="05af7-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="05af7-216">(4)</span><span class="sxs-lookup"><span data-stu-id="05af7-216">(4)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-217">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="05af7-217">Device is not working properly.</span></span> <span data-ttu-id="05af7-218">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="05af7-218">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="05af7-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="05af7-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="05af7-220">(5)</span><span class="sxs-lookup"><span data-stu-id="05af7-220">(5)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-221">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="05af7-221">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="05af7-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="05af7-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="05af7-223"> (6)</span><span class="sxs-lookup"><span data-stu-id="05af7-223">(6)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-224">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="05af7-224">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="05af7-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="05af7-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="05af7-226">(7)</span><span class="sxs-lookup"><span data-stu-id="05af7-226">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="05af7-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="05af7-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="05af7-228">(8)</span><span class="sxs-lookup"><span data-stu-id="05af7-228">(8)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-229">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="05af7-229">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="05af7-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="05af7-231">(9)</span><span class="sxs-lookup"><span data-stu-id="05af7-231">(9)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-232">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="05af7-232">Device is not working properly.</span></span> <span data-ttu-id="05af7-233">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-233">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="05af7-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="05af7-235">(10)</span><span class="sxs-lookup"><span data-stu-id="05af7-235">(10)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-236">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-236">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="05af7-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="05af7-238">(11)</span><span class="sxs-lookup"><span data-stu-id="05af7-238">(11)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-239">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-239">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="05af7-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="05af7-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="05af7-241">douze</span><span class="sxs-lookup"><span data-stu-id="05af7-241">(12)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-242">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="05af7-242">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="05af7-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="05af7-244">(13)</span><span class="sxs-lookup"><span data-stu-id="05af7-244">(13)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-245">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-245">Windows cannot verify the device resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="05af7-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="05af7-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="05af7-247">(14)</span><span class="sxs-lookup"><span data-stu-id="05af7-247">(14)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-248">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="05af7-248">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="05af7-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="05af7-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="05af7-250">(15)</span><span class="sxs-lookup"><span data-stu-id="05af7-250">(15)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-251">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="05af7-251">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="05af7-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="05af7-253">(16)</span><span class="sxs-lookup"><span data-stu-id="05af7-253">(16)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-254">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-254">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="05af7-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="05af7-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="05af7-256">(17)</span><span class="sxs-lookup"><span data-stu-id="05af7-256">(17)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-257">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="05af7-257">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="05af7-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="05af7-259">(18)</span><span class="sxs-lookup"><span data-stu-id="05af7-259">(18)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-260">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="05af7-260">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="05af7-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="05af7-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="05af7-262">(19)</span><span class="sxs-lookup"><span data-stu-id="05af7-262">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="05af7-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="05af7-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="05af7-264">(20)</span><span class="sxs-lookup"><span data-stu-id="05af7-264">(20)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-265">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="05af7-265">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="05af7-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="05af7-267">(21)</span><span class="sxs-lookup"><span data-stu-id="05af7-267">(21)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-268">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="05af7-268">System failure.</span></span> <span data-ttu-id="05af7-269">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="05af7-269">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="05af7-270">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-270">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="05af7-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="05af7-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="05af7-272">(22)</span><span class="sxs-lookup"><span data-stu-id="05af7-272">(22)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-273">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="05af7-273">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="05af7-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="05af7-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="05af7-275">(23)</span><span class="sxs-lookup"><span data-stu-id="05af7-275">(23)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-276">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="05af7-276">System failure.</span></span> <span data-ttu-id="05af7-277">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="05af7-277">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="05af7-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="05af7-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="05af7-279">(24)</span><span class="sxs-lookup"><span data-stu-id="05af7-279">(24)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-280">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="05af7-280">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="05af7-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="05af7-282">(25)</span><span class="sxs-lookup"><span data-stu-id="05af7-282">(25)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-283">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="05af7-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="05af7-285">(26)</span><span class="sxs-lookup"><span data-stu-id="05af7-285">(26)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-286">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05af7-286">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="05af7-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="05af7-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="05af7-288">(27)</span><span class="sxs-lookup"><span data-stu-id="05af7-288">(27)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-289">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="05af7-289">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="05af7-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="05af7-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="05af7-291">(28)</span><span class="sxs-lookup"><span data-stu-id="05af7-291">(28)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-292">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="05af7-292">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="05af7-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="05af7-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="05af7-294">(29)</span><span class="sxs-lookup"><span data-stu-id="05af7-294">(29)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-295">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="05af7-295">Device is disabled.</span></span> <span data-ttu-id="05af7-296">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="05af7-296">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="05af7-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="05af7-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="05af7-298">(30)</span><span class="sxs-lookup"><span data-stu-id="05af7-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-299">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="05af7-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="05af7-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="05af7-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="05af7-301">31</span><span class="sxs-lookup"><span data-stu-id="05af7-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-302">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="05af7-302">Device is not working properly.</span></span> <span data-ttu-id="05af7-303">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="05af7-303">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05af7-304">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="05af7-304">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-305">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-307">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="05af7-307">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-308">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05af7-308">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="05af7-309">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-310">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="05af7-310">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-311">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-313">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="05af7-313">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="05af7-314">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="05af7-314">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="05af7-315">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="05af7-315">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="05af7-316">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-317">**Description**</span><span class="sxs-lookup"><span data-stu-id="05af7-317">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-318">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-320">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="05af7-320">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-321">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="05af7-321">Description of the object.</span></span>

<span data-ttu-id="05af7-322">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-323">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="05af7-323">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-326">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="05af7-326">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-327">Identificateur unique du disque logique à partir d’autres périphériques sur le système.</span><span class="sxs-lookup"><span data-stu-id="05af7-327">Unique identifier of the logical disk from other devices on the system.</span></span>

<span data-ttu-id="05af7-328">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="05af7-329">Pour obtenir un exemple de code qui récupère cette propriété, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="05af7-329">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-330">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="05af7-330">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-331">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05af7-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-333">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| FileFunctions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="05af7-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|FileFunctions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-334">Valeur numérique qui correspond au type de lecteur de disque représenté par ce disque logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-334">Numeric value that corresponds to the type of disk drive this logical disk represents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05af7-335">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="05af7-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Root_Directory"></span><span id="no_root_directory"></span><span id="NO_ROOT_DIRECTORY"></span>

<span data-ttu-id="05af7-336">**Aucun répertoire racine** (1)</span><span class="sxs-lookup"><span data-stu-id="05af7-336">**No Root Directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Disk"></span><span id="removable_disk"></span><span id="REMOVABLE_DISK"></span>

<span data-ttu-id="05af7-337">**Disque amovible** (2)</span><span class="sxs-lookup"><span data-stu-id="05af7-337">**Removable Disk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Disk"></span><span id="local_disk"></span><span id="LOCAL_DISK"></span>

<span data-ttu-id="05af7-338">**Disque local** (3)</span><span class="sxs-lookup"><span data-stu-id="05af7-338">**Local Disk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Drive"></span><span id="network_drive"></span><span id="NETWORK_DRIVE"></span>

<span data-ttu-id="05af7-339">**Lecteur réseau** (4)</span><span class="sxs-lookup"><span data-stu-id="05af7-339">**Network Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Compact_Disc"></span><span id="compact_disc"></span><span id="COMPACT_DISC"></span>

<span data-ttu-id="05af7-340">**Disque compact** (5)</span><span class="sxs-lookup"><span data-stu-id="05af7-340">**Compact Disc** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM_Disk"></span><span id="ram_disk"></span><span id="RAM_DISK"></span>

<span data-ttu-id="05af7-341">**Disque RAM** (6)</span><span class="sxs-lookup"><span data-stu-id="05af7-341">**RAM Disk** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05af7-342">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="05af7-342">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-343">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-345">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="05af7-345">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="05af7-346">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-347">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="05af7-347">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-348">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-350">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="05af7-350">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="05af7-351">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-352">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="05af7-352">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-355">Type de détection d’erreur et de correction pris en charge par cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="05af7-355">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="05af7-356">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-356">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-357">**FileSystem**</span><span class="sxs-lookup"><span data-stu-id="05af7-357">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-360">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions du système de fichiers [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="05af7-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="05af7-361">Système de fichiers sur le disque logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-361">File system on the logical disk.</span></span>

<span data-ttu-id="05af7-362">Exemple : "NTFS"</span><span class="sxs-lookup"><span data-stu-id="05af7-362">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="05af7-363">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="05af7-363">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-364">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="05af7-364">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-366">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="05af7-366">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-367">Espace, en octets, disponible sur le disque logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-367">Space, in bytes, available on the logical disk.</span></span>

<span data-ttu-id="05af7-368">Cette propriété est héritée [**du \_ disque logique CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-368">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="05af7-369">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="05af7-369">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="05af7-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-371">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="05af7-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-373">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="05af7-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-374">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="05af7-374">Date and time the object was installed.</span></span> <span data-ttu-id="05af7-375">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="05af7-375">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="05af7-376">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="05af7-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-378">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05af7-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-379">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-380">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="05af7-381">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-382">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="05af7-382">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-383">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05af7-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-385">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions du système de fichiers [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="05af7-385">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="05af7-386">Longueur maximale d’un composant de nom de fichier pris en charge par le lecteur Windows.</span><span class="sxs-lookup"><span data-stu-id="05af7-386">Maximum length of a filename component supported by the Windows drive.</span></span> <span data-ttu-id="05af7-387">Un composant de nom de fichier est cette partie d’un nom de fichier entre barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="05af7-387">A filename component is that portion of a filename between backslashes.</span></span> <span data-ttu-id="05af7-388">La valeur peut être utilisée pour indiquer que les noms longs sont pris en charge par le système de fichiers spécifié.</span><span class="sxs-lookup"><span data-stu-id="05af7-388">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="05af7-389">Par exemple, pour un système de fichiers FAT prenant en charge les noms longs, la fonction stocke la valeur 255, plutôt que l’indicateur 8,3 précédent.</span><span class="sxs-lookup"><span data-stu-id="05af7-389">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="05af7-390">Les noms longs peuvent également être pris en charge sur les systèmes qui utilisent le système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="05af7-390">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="05af7-391">Exemple : 255</span><span class="sxs-lookup"><span data-stu-id="05af7-391">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="05af7-392">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="05af7-392">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-393">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05af7-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-395">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| DeviceIoControl »)</span><span class="sxs-lookup"><span data-stu-id="05af7-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-396">Type de support actuellement présent dans le lecteur logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-396">Type of media currently present in the logical drive.</span></span> <span data-ttu-id="05af7-397">Cette valeur sera l’une des valeurs de l' \_ énumération de type de média définie dans winioctl. h.</span><span class="sxs-lookup"><span data-stu-id="05af7-397">This value will be one of the values of the MEDIA\_TYPE enumeration defined in Winioctl.h.</span></span> <span data-ttu-id="05af7-398">La valeur peut ne pas être exacte pour les lecteurs amovibles s’il n’y a actuellement aucun média dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="05af7-398">The value may not be exact for removable drives if currently there is no media in the drive.</span></span>

<dt>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>

<span data-ttu-id="05af7-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>Le **format est inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="05af7-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Format is unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (1)</span><span class="sxs-lookup"><span data-stu-id="05af7-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (1)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-401">Disquette 5 1/4 pouces-1,2 Mo-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-401">5 1/4-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (2)</span><span class="sxs-lookup"><span data-stu-id="05af7-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (2)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-403">Disquette 3 1/2 pouces – 1,44 Mo-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-403">3 1/2-Inch Floppy Disk - 1.44 MB -512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (3)</span><span class="sxs-lookup"><span data-stu-id="05af7-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (3)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-405">Disquette 3 1/2 pouces – 2,88 Mo-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-405">3 1/2-Inch Floppy Disk - 2.88 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (4)</span><span class="sxs-lookup"><span data-stu-id="05af7-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-407">Disquette 3 1/2 pouces – 20,8 Mo-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-407">3 1/2-Inch Floppy Disk - 20.8 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (5)</span><span class="sxs-lookup"><span data-stu-id="05af7-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (5)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-409">Disquette 3 1/2 pouces-720 Ko-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-409">3 1/2-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (6)</span><span class="sxs-lookup"><span data-stu-id="05af7-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (6)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-411">Disquette 5 1/4 pouces-360 Ko-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-411">5 1/4-Inch Floppy Disk - 360 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (7)</span><span class="sxs-lookup"><span data-stu-id="05af7-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (7)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-413">Disquette 5 1/4 pouces-320 Ko-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-413">5 1/4-Inch Floppy Disk - 320 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (8)</span><span class="sxs-lookup"><span data-stu-id="05af7-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (8)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-415">Disquette 5 1/4 pouces-320 ko-1024 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-415">5 1/4-Inch Floppy Disk - 320 KB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (9)</span><span class="sxs-lookup"><span data-stu-id="05af7-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (9)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-417">Disquette 5 1/4 pouces-180 Ko-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-417">5 1/4-Inch Floppy Disk - 180 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (10)</span><span class="sxs-lookup"><span data-stu-id="05af7-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (10)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-419">Disquette 5 1/4 pouces-160 Ko-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-419">5 1/4-Inch Floppy Disk - 160 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>

<span data-ttu-id="05af7-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Support amovible autre que disquette** (11)</span><span class="sxs-lookup"><span data-stu-id="05af7-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Removable media other than floppy** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>

<span data-ttu-id="05af7-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Disque dur fixe** (12)</span><span class="sxs-lookup"><span data-stu-id="05af7-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Fixed hard disk media** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (13)</span><span class="sxs-lookup"><span data-stu-id="05af7-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (13)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-423">Disquette 3 1/2 pouces – 120 Mo-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-423">3 1/2-Inch Floppy Disk - 120 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (14)</span><span class="sxs-lookup"><span data-stu-id="05af7-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (14)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-425">Disquette 3 1/2 pouces-640 Ko-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-425">3 1/2-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (15)</span><span class="sxs-lookup"><span data-stu-id="05af7-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (15)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-427">Disquette 5 1/4 pouces-640 Ko-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-427">5 1/4-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (16)</span><span class="sxs-lookup"><span data-stu-id="05af7-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (16)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-429">Disquette 5 1/4 pouces-720 Ko-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-429">5 1/4-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (17)</span><span class="sxs-lookup"><span data-stu-id="05af7-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (17)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-431">Disquette 3 1/2 pouces – 1,2 Mo-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-431">3 1/2-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (18)</span><span class="sxs-lookup"><span data-stu-id="05af7-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (18)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-433">Disquette 3 1/2 pouces – 1,23 Mo-1024 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-433">3 1/2-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquette 5 pouces** (19)</span><span class="sxs-lookup"><span data-stu-id="05af7-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (19)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-435">Disquette 5 1/4 pouces-1,23 Mo-1024 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-435">5 1/4-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (20)</span><span class="sxs-lookup"><span data-stu-id="05af7-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (20)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-437">Disquette 3 1/2 pouces – 128 Mo-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-437">3 1/2-Inch Floppy Disk - 128 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquette 3 pouces** (21)</span><span class="sxs-lookup"><span data-stu-id="05af7-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (21)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-439">Disquette 3 1/2 pouces – 230 Mo-512 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-439">3 1/2-Inch Floppy Disk - 230 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="05af7-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**disquette 8 pouces** (22)</span><span class="sxs-lookup"><span data-stu-id="05af7-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-Inch Floppy Disk** (22)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-441">Disquette 8 pouces-256 Ko-128 octets/secteur</span><span class="sxs-lookup"><span data-stu-id="05af7-441">8-Inch Floppy Disk - 256 KB - 128 bytes/sector</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05af7-442">**Nom**</span><span class="sxs-lookup"><span data-stu-id="05af7-442">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-443">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-445">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="05af7-445">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-446">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="05af7-446">Label by which the object is known.</span></span> <span data-ttu-id="05af7-447">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="05af7-447">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="05af7-448">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-448">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-449">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="05af7-449">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-450">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="05af7-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-452">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="05af7-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-453">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="05af7-453">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="05af7-454">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="05af7-454">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="05af7-455">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="05af7-455">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="05af7-456">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-456">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="05af7-457">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="05af7-457">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-458">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="05af7-458">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-459">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-461">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="05af7-461">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-462">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-462">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="05af7-463">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="05af7-464">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="05af7-464">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="05af7-465">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="05af7-465">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-466">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05af7-466">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="05af7-467">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-468">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-468">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="05af7-469">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="05af7-469">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05af7-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="05af7-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="05af7-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="05af7-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="05af7-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="05af7-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="05af7-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="05af7-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-474">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="05af7-474">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="05af7-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="05af7-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-476">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="05af7-476">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="05af7-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="05af7-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-478">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="05af7-478">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="05af7-479">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="05af7-479">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="05af7-480">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="05af7-480">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="05af7-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="05af7-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-482">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="05af7-482">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="05af7-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="05af7-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="05af7-484">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="05af7-484">Timed Power-On Supported</span></span>

<span data-ttu-id="05af7-485">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="05af7-485">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="05af7-486">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="05af7-486">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-487">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-487">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-488">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-489">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="05af7-489">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="05af7-490">Cette propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable d’effectuer la gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="05af7-490">This property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="05af7-491">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-492">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="05af7-492">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-493">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-494">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-495">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| Windows Networking Functions \| WNetGetConnection »)</span><span class="sxs-lookup"><span data-stu-id="05af7-495">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-496">Chemin d’accès réseau à l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-496">Network path to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-497">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="05af7-497">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-498">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-500">Chaîne de forme libre décrivant le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="05af7-500">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="05af7-501">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-501">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-502">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="05af7-502">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-503">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-504">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-505">Indique que la gestion de quota n’est pas activée (TRUE) sur ce système.</span><span class="sxs-lookup"><span data-stu-id="05af7-505">Indicates that quota management is not enabled (TRUE) on this system.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-506">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="05af7-506">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-507">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-507">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-508">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-509">Indique que la gestion de quota a été utilisée mais a été désactivée (**true**).</span><span class="sxs-lookup"><span data-stu-id="05af7-509">Indicates that the quota management was used but has been disabled (**True**).</span></span> <span data-ttu-id="05af7-510">Incomplet fait référence aux informations laissées dans le système de fichiers après la désactivation de la gestion de quota.</span><span class="sxs-lookup"><span data-stu-id="05af7-510">Incomplete refers to the information left in the file system after quota management was disabled.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-511">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="05af7-511">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-512">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-512">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-514">Si la **valeur est true**, indique que le système de fichiers est dans le processus actif de compilation des informations et de configuration du disque pour la gestion des quotas.</span><span class="sxs-lookup"><span data-stu-id="05af7-514">If **True**, indicates that the file system is in the active process of compiling information and setting the disk up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-515">**Taille**</span><span class="sxs-lookup"><span data-stu-id="05af7-515">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-516">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-517">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-518">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="05af7-518">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-519">Taille du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="05af7-519">Size of the disk drive.</span></span>

<span data-ttu-id="05af7-520">Cette propriété est héritée [**du \_ disque logique CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-520">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="05af7-521">Pour obtenir un exemple de code qui récupère cette propriété, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="05af7-521">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-522">**État**</span><span class="sxs-lookup"><span data-stu-id="05af7-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-525">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="05af7-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-526">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="05af7-526">Current status of the object.</span></span> <span data-ttu-id="05af7-527">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="05af7-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="05af7-528">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="05af7-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="05af7-529">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="05af7-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="05af7-530">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="05af7-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="05af7-531">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="05af7-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="05af7-532">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="05af7-533">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="05af7-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="05af7-534">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="05af7-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="05af7-535">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="05af7-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="05af7-536">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="05af7-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05af7-537">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="05af7-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="05af7-538">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="05af7-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="05af7-539">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="05af7-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="05af7-540">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="05af7-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="05af7-541">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="05af7-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="05af7-542">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="05af7-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="05af7-543">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="05af7-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="05af7-544">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="05af7-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="05af7-545">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="05af7-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05af7-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="05af7-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-547">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05af7-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-548">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-549">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="05af7-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-550">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-550">State of the logical device.</span></span> <span data-ttu-id="05af7-551">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="05af7-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="05af7-552">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="05af7-553">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="05af7-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="05af7-554">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="05af7-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="05af7-555">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="05af7-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="05af7-556">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="05af7-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="05af7-557">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="05af7-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="05af7-558">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="05af7-558">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-559">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-559">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-560">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-560">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05af7-561">Si la **valeur est true**, ce volume prend en charge les quotas de disque.</span><span class="sxs-lookup"><span data-stu-id="05af7-561">If **True**, this volume supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-562">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="05af7-562">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-563">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-564">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-565">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Functions du système de fichiers \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ compression de fichier \_ ")</span><span class="sxs-lookup"><span data-stu-id="05af7-565">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-566">Si la **valeur est true**, la partition de disque logique prend en charge la compression basée sur les fichiers, comme c’est le cas avec le système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="05af7-566">If **True**, the logical disk partition supports file-based compression, such as is the case with the NTFS file system.</span></span> <span data-ttu-id="05af7-567">Cette propriété a la **valeur false** lorsque la propriété **Compressed** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="05af7-567">This property is **False** when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-568">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="05af7-568">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-569">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-569">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-570">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-570">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-571">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="05af7-571">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="05af7-572">Valeur de la propriété de l’étendue **CreationClassName** de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="05af7-572">Value of the scoping computer **CreationClassName** property.</span></span>

<span data-ttu-id="05af7-573">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-574">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="05af7-574">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-575">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-575">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-576">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-577">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="05af7-577">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="05af7-578">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="05af7-578">Name of the scoping system.</span></span>

<span data-ttu-id="05af7-579">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-579">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="05af7-580">**VolumeDirty**</span><span class="sxs-lookup"><span data-stu-id="05af7-580">**VolumeDirty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-581">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="05af7-581">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-582">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-582">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-583">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« FSCTL \_ est un \_ volume \_ sale »)</span><span class="sxs-lookup"><span data-stu-id="05af7-583">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL\_IS\_VOLUME\_DIRTY")</span></span>
</dt> </dl>

<span data-ttu-id="05af7-584">Si la **valeur est true**, le disque nécessite l’exécution de [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) lors du prochain redémarrage.</span><span class="sxs-lookup"><span data-stu-id="05af7-584">If **True**, the disk requires [**ChkDsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart.</span></span> <span data-ttu-id="05af7-585">Cette propriété s’applique uniquement aux instances de disque logique qui représentent un disque physique de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="05af7-585">This property is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="05af7-586">Elle ne s’applique pas aux lecteurs logiques mappés.</span><span class="sxs-lookup"><span data-stu-id="05af7-586">It is not applicable to mapped logical drives.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-587">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="05af7-587">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-588">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-589">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="05af7-589">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="05af7-590">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions du système de fichiers [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="05af7-590">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="05af7-591">Nom du volume du disque logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-591">Volume name of the logical disk.</span></span>

<span data-ttu-id="05af7-592">Contraintes : maximum 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="05af7-592">Constraints: Maximum 32 characters.</span></span>

<span data-ttu-id="05af7-593">Pour obtenir un exemple de code qui récupère cette propriété, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="05af7-593">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="05af7-594">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="05af7-594">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05af7-595">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="05af7-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05af7-596">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05af7-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05af7-597">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions du système de fichiers [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="05af7-597">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="05af7-598">Numéro de série du volume du disque logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-598">Volume serial number of the logical disk.</span></span>

<span data-ttu-id="05af7-599">Contraintes : 11 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="05af7-599">Constraints: Maximum 11 characters.</span></span>

<span data-ttu-id="05af7-600">Exemple : « A8C3-D032 »</span><span class="sxs-lookup"><span data-stu-id="05af7-600">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05af7-601">Notes</span><span class="sxs-lookup"><span data-stu-id="05af7-601">Remarks</span></span>

<span data-ttu-id="05af7-602">La **classe \_ disque logique Win32** est dérivée du [**\_ disque logique CIM**](cim-logicaldisk.md) qui dérive de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-602">The **Win32\_LogicalDisk** class is derived from [**CIM\_LogicalDisk**](cim-logicaldisk.md) which derives from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="05af7-603">La classe **CIM \_ StorageExtent** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="05af7-603">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="05af7-604">Un lecteur de disque physique est la pierre angulaire de tout système de gestion de stockage.</span><span class="sxs-lookup"><span data-stu-id="05af7-604">A physical disk drive is the cornerstone of any storage management system.</span></span> <span data-ttu-id="05af7-605">Toutefois, après l’installation d’un lecteur de disque physique, ni les utilisateurs ni les administrateurs système ne traitent généralement le matériel directement.</span><span class="sxs-lookup"><span data-stu-id="05af7-605">However, after a physical disk drive has been installed, neither users nor system administrators typically deal with the hardware directly.</span></span> <span data-ttu-id="05af7-606">Au lieu de cela, les utilisateurs et les administrateurs système interagissent avec les lecteurs logiques qui ont été créés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="05af7-606">Instead, both users and system administrators interact with the logical drives that have been created on the disk.</span></span>

<span data-ttu-id="05af7-607">Un lecteur logique est une sous-division d’une partition à laquelle a été affectée sa propre lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="05af7-607">A logical drive is a subdivision of a partition that has been assigned its own drive letter.</span></span> <span data-ttu-id="05af7-608">(Il est possible d’avoir une partition à laquelle aucune lettre de lecteur n’a été affectée.) Lorsque vous communiquez avec le lecteur C ou le lecteur D, vous faites référence à un lecteur logique plutôt qu’à un lecteur de disque physique.</span><span class="sxs-lookup"><span data-stu-id="05af7-608">(It is possible to have a partition that has not been assigned a drive letter.) When you talk about drive C or drive D, you are referring to a logical drive rather than to a physical disk drive.</span></span> <span data-ttu-id="05af7-609">De même, lorsque vous enregistrez un document sur le lecteur E, vous l’enregistrez sur le lecteur logique.</span><span class="sxs-lookup"><span data-stu-id="05af7-609">Likewise, when you save a document to drive E, you are saving it to the logical drive.</span></span> <span data-ttu-id="05af7-610">Les disques physiques composent le matériel qui compose un lecteur, y compris des composants tels que les têtes, les secteurs et les cylindres.</span><span class="sxs-lookup"><span data-stu-id="05af7-610">Physical disks compose the hardware that makes up a drive, including such components as heads, sectors, and cylinders.</span></span> <span data-ttu-id="05af7-611">En revanche, les lecteurs logiques ont des propriétés telles que l’espace disque, l’espace disque disponible et les lettres de lecteur.</span><span class="sxs-lookup"><span data-stu-id="05af7-611">Logical drives, by contrast, have properties such as disk space, available disk space, and drive letters.</span></span>

> [!Note]  
> <span data-ttu-id="05af7-612">La classe disque **\_ logique Win32** peut être utilisée uniquement pour énumérer les propriétés de lecteurs de disque locaux.</span><span class="sxs-lookup"><span data-stu-id="05af7-612">The **Win32\_LogicalDisk** class can be used only to enumerate the properties of local disk drives.</span></span> <span data-ttu-id="05af7-613">Toutefois, vous pouvez utiliser la classe [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md) pour énumérer les propriétés des lecteurs réseau mappés.</span><span class="sxs-lookup"><span data-stu-id="05af7-613">However, you can use the [**Win32\_MappedLogicalDisk**](win32-mappedlogicaldisk.md) class to enumerate the properties of mapped network drives.</span></span>

 

## <a name="examples"></a><span data-ttu-id="05af7-614">Exemples</span><span class="sxs-lookup"><span data-stu-id="05af7-614">Examples</span></span>

<span data-ttu-id="05af7-615">Vous trouverez d’autres exemples à l’aide de disque **\_ logique Win32** pour obtenir des données de disque ou de volume dans la rubrique [tâches WMI : disques et systèmes de fichiers](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) .</span><span class="sxs-lookup"><span data-stu-id="05af7-615">You can find other examples using **Win32\_LogicalDisk** to obtain disk or volume data in the [WMI Tasks: Disks and File Systems](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) topic.</span></span>

<span data-ttu-id="05af7-616">L’exemple de code VBScript de l' [extracteur d’informations WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) sur la Galerie TechNet utilise la classe **\_ disque logique Win32** pour récupérer des informations matérielles à partir de plusieurs ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="05af7-616">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_LogicalDisk** class to retrieve hardware information from a number of remote computers.</span></span>

<span data-ttu-id="05af7-617">La [récupération d’informations sur le disque à l’aide de WMI/CIM...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) L’exemple de code PowerShell sur la Galerie TechNet utilise le **\_ disque logique Win32** pour récupérer **DeviceID**, **nom_volume** et la **taille** d’un appareil cible.</span><span class="sxs-lookup"><span data-stu-id="05af7-617">The [Get Disk info using wmi/cim...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) PowerShell code example on the TechNet Gallery uses **Win32\_LogicalDisk** to retrieve **DeviceID**, **VolumeName**, and **Size** from a target device.</span></span> <span data-ttu-id="05af7-618">En particulier, cet exemple comprend une gestion rigoureuse des exceptions et retourne un seul objet par ordinateur, plutôt que par disque.</span><span class="sxs-lookup"><span data-stu-id="05af7-618">In particular, this sample includes rigorous exception handling, and returns a single object per computer, rather than per disk.</span></span>

<span data-ttu-id="05af7-619">Les scripts d’entreprise impliquent souvent la configuration du matériel et des logiciels sur des ordinateurs distants. à son tour, vous devez savoir, à l’avance, le type de lecteur de disque installé sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="05af7-619">Enterprise scripting often involves configuring hardware and software on remote computers; in turn, this requires you to know, in advance, the type of disk drives installed on a computer.</span></span> <span data-ttu-id="05af7-620">Par exemple, un script qui installe une application sur le lecteur E fonctionne uniquement si le lecteur E est un disque dur.</span><span class="sxs-lookup"><span data-stu-id="05af7-620">For example, a script that installs an application on drive E works only if drive E is a hard disk.</span></span> <span data-ttu-id="05af7-621">Si le lecteur E représente une disquette ou un lecteur de CD-ROM, le script échoue.</span><span class="sxs-lookup"><span data-stu-id="05af7-621">If drive E happens to represent a floppy disk or a CD-ROM drive, the script fails.</span></span> <span data-ttu-id="05af7-622">Le code suivant identifie les lecteurs et les types de lecteurs installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="05af7-622">The following code identifies the drives and drive types installed on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk")
For Each objDisk in colDisks
 Wscript.Echo "DeviceID: "& objDisk.DeviceID 
 Select Case objDisk.DriveType
 Case 1
 Wscript.Echo "No root directory."
 Case 2
 Wscript.Echo "DriveType: Removable drive."
 Case 3
 Wscript.Echo "DriveType: Local hard disk."
 Case 4
 Wscript.Echo "DriveType: Network disk." 
 Case 5
 Wscript.Echo "DriveType: Compact disk." 
 Case 6
 Wscript.Echo "DriveType: RAM disk." 
 Case Else
 Wscript.Echo "Drive type could not be determined."
 End Select
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...
{
   string strComputer = &quot;.&quot;;
            
   ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
   ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk&quot;);
   ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
   ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

   foreach (ManagementObject objDisk in colDisks)
   {
      Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
                
      switch ((uint)(objDisk[&quot;DriveType&quot;]))
      {
         case 1: {   Console.WriteLine(&quot;No root directory.&quot;);
                     break;}
         case 2: {   Console.WriteLine(&quot;DriveType: Removable drive.&quot;); 
                     break;}
         case 3: {   Console.WriteLine(&quot;DriveType: Local hard disk.&quot;);
                     break;}
         case 4: {   Console.WriteLine(&quot;DriveType: Network disk.&quot;);
                     break;}
         case 5: {   Console.WriteLine(&quot;DriveType: Compact disk.&quot;);
                     break;}
         case 6: {   Console.WriteLine(&quot;DriveType: RAM disk.&quot;);
                     break;}
         default: {  Console.WriteLine(&quot;Drive type could not be determined.&quot;);
                     break;}
      }
      //Readline is in here so the user can see the result before the code exists
      Console.ReadLine();
   }
}
```





<span data-ttu-id="05af7-623">Les exemples suivants énumèrent l’espace libre sur tous les lecteurs de disque dur d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="05af7-623">The following samples enumerate the free space on all the hard disk drives on a computer.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk WHERE DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
 Wscript.Echo "Device ID: " & objDisk.DeviceID 
 Wscript.Echo "Free Disk Space: " & objDisk.FreeSpace
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...

const int HARD_DISK = 3;
string strComputer = &quot;.&quot;;

ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk WHERE DriveType = &quot; + HARD_DISK + &quot;&quot;);
ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

foreach (ManagementObject objDisk in colDisks)
{
    Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
    Console.WriteLine(&quot;Free Disk Space : {0}&quot;, objDisk[&quot;FreeSpace&quot;]);
    Console.ReadLine();
}
```





<span data-ttu-id="05af7-624">L’exemple de code suivant retourne le type de système de fichiers (FAT, NTFS, FAT32, etc.) utilisé sur chaque lecteur d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="05af7-624">The following code example returns the type of file system (FAT, NTFS, FAT32, and so on) used on each drive in a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
    Wscript.Echo "DeviceID: "& vbTab &  objDisk.DeviceID  
    Wscript.Echo "File System: "& vbTab & objDisk.FileSystem
Next
```


```PowerShell

Get-WMIObject Win32_LogicalDisk | Select DeviceID, FileSystem | Format=Table -AutoSize
```





<span data-ttu-id="05af7-625">L’exemple de code PowerShell suivant récupère des informations supplémentaires sur les disques locaux logiques.</span><span class="sxs-lookup"><span data-stu-id="05af7-625">The following PowerShell code sample retrieves additional information about the logical local disks.</span></span>


```PowerShell
Write-Host "Drive information for $env:ComputerName"

Get-WmiObject -Class Win32_LogicalDisk |
    Where-Object {$_.DriveType -ne 5} |
    Sort-Object -Property Name | 
    Select-Object Name, VolumeName, FileSystem, Description, VolumeDirty, `
        @{"Label"="DiskSize(GB)";"Expression"={"{0:N}" -f ($_.Size/1GB) -as [float]}}, `
        @{"Label"="FreeSpace(GB)";"Expression"={"{0:N}" -f ($_.FreeSpace/1GB) -as [float]}}, `
        @{"Label"="%Free";"Expression"={"{0:N}" -f ($_.FreeSpace/$_.Size*100) -as [float]}} |
    Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="05af7-626">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05af7-626">Requirements</span></span>



| <span data-ttu-id="05af7-627">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05af7-627">Requirement</span></span> | <span data-ttu-id="05af7-628">Valeur</span><span class="sxs-lookup"><span data-stu-id="05af7-628">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05af7-629">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05af7-629">Minimum supported client</span></span><br/> | <span data-ttu-id="05af7-630">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05af7-630">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05af7-631">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05af7-631">Minimum supported server</span></span><br/> | <span data-ttu-id="05af7-632">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05af7-632">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05af7-633">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="05af7-633">Namespace</span></span><br/>                | <span data-ttu-id="05af7-634">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="05af7-634">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05af7-635">MOF</span><span class="sxs-lookup"><span data-stu-id="05af7-635">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05af7-636"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05af7-636"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05af7-637">DLL</span><span class="sxs-lookup"><span data-stu-id="05af7-637">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05af7-638"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05af7-638"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05af7-639">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05af7-639">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05af7-640">**\_Disque logique CIM**</span><span class="sxs-lookup"><span data-stu-id="05af7-640">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="05af7-641">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="05af7-641">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="05af7-642">Tâches WMI : disques et systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="05af7-642">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

