---
description: La \_ classe LOGICALDISK CIM représente une plage contiguë de blocs logiques qui est identifiable par un système de fichiers par le biais du champ DeviceID (Key) du disque.
ms.assetid: 1c2fd0bf-a1e3-4706-9f84-5dd4d371a167
ms.tgt_platform: multiple
title: CIM_LogicalDisk, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.Access
- CIM_LogicalDisk.Availability
- CIM_LogicalDisk.BlockSize
- CIM_LogicalDisk.Caption
- CIM_LogicalDisk.ConfigManagerErrorCode
- CIM_LogicalDisk.ConfigManagerUserConfig
- CIM_LogicalDisk.CreationClassName
- CIM_LogicalDisk.Description
- CIM_LogicalDisk.DeviceID
- CIM_LogicalDisk.ErrorCleared
- CIM_LogicalDisk.ErrorDescription
- CIM_LogicalDisk.ErrorMethodology
- CIM_LogicalDisk.FreeSpace
- CIM_LogicalDisk.InstallDate
- CIM_LogicalDisk.LastErrorCode
- CIM_LogicalDisk.Name
- CIM_LogicalDisk.NumberOfBlocks
- CIM_LogicalDisk.PNPDeviceID
- CIM_LogicalDisk.PowerManagementCapabilities
- CIM_LogicalDisk.PowerManagementSupported
- CIM_LogicalDisk.Purpose
- CIM_LogicalDisk.Size
- CIM_LogicalDisk.Status
- CIM_LogicalDisk.StatusInfo
- CIM_LogicalDisk.SystemCreationClassName
- CIM_LogicalDisk.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd28ab0b9982606278e65705273a9965cfb9b396
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747957"
---
# <a name="cim_logicaldisk-class-cimwin32-wmi-providers"></a><span data-ttu-id="562ff-103">CIM_LogicalDisk, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="562ff-103">CIM_LogicalDisk class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="562ff-104">La **classe \_ LogicalDisk CIM** représente une plage contiguë de blocs logiques qui est identifiable par un système de fichiers par le biais du champ **DeviceID** (Key) du disque.</span><span class="sxs-lookup"><span data-stu-id="562ff-104">The **CIM\_LogicalDisk** class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="562ff-105">Par exemple, dans un environnement Windows, le champ **DeviceID** contient une lettre de lecteur. dans un environnement UNIX, elle contient le chemin d’accès ; dans un environnement NetWare, il contient le nom du volume.</span><span class="sxs-lookup"><span data-stu-id="562ff-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="562ff-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="562ff-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="562ff-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="562ff-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="562ff-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="562ff-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="562ff-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="562ff-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="562ff-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="562ff-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C539-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="562ff-111">Membres</span><span class="sxs-lookup"><span data-stu-id="562ff-111">Members</span></span>

<span data-ttu-id="562ff-112">La classe de **\_ disque logique CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="562ff-112">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="562ff-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="562ff-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="562ff-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="562ff-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="562ff-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="562ff-115">Methods</span></span>

<span data-ttu-id="562ff-116">La classe de **\_ disque logique CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="562ff-116">The **CIM\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="562ff-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="562ff-117">Method</span></span>                                                                 | <span data-ttu-id="562ff-118">Description</span><span class="sxs-lookup"><span data-stu-id="562ff-118">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="562ff-119">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="562ff-119">**Reset**</span></span>](reset-method-in-class-cim-logicaldisk.md)                 | <span data-ttu-id="562ff-120">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="562ff-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="562ff-121">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="562ff-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="562ff-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="562ff-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldisk.md) | <span data-ttu-id="562ff-123">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="562ff-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="562ff-124">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="562ff-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="562ff-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="562ff-125">Properties</span></span>

<span data-ttu-id="562ff-126">La classe de **\_ disque logique CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="562ff-126">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="562ff-127">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="562ff-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="562ff-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="562ff-130">Indique si le média est lisible, accessible en écriture, ou les deux à la fois, par exemple.</span><span class="sxs-lookup"><span data-stu-id="562ff-130">Describes whether the media is readable, writable, or both, for example.</span></span> <span data-ttu-id="562ff-131">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="562ff-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="562ff-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-133">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="562ff-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="562ff-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="562ff-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-135">R.a..</span><span class="sxs-lookup"><span data-stu-id="562ff-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="562ff-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="562ff-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-137">Inscriptible.</span><span class="sxs-lookup"><span data-stu-id="562ff-137">Writable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="562ff-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="562ff-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-139">Lecture/écriture prise en charge.</span><span class="sxs-lookup"><span data-stu-id="562ff-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="562ff-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="562ff-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-141">Écriture unique.</span><span class="sxs-lookup"><span data-stu-id="562ff-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="562ff-142">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="562ff-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="562ff-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-145">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="562ff-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-146">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-146">Availability and status of the device.</span></span>

<span data-ttu-id="562ff-147">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="562ff-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="562ff-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="562ff-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="562ff-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="562ff-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="562ff-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="562ff-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="562ff-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="562ff-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="562ff-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="562ff-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="562ff-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="562ff-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="562ff-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="562ff-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="562ff-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="562ff-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="562ff-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="562ff-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="562ff-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="562ff-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="562ff-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="562ff-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="562ff-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="562ff-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="562ff-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-161">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="562ff-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="562ff-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="562ff-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-163">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="562ff-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="562ff-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="562ff-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-165">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="562ff-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="562ff-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="562ff-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="562ff-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="562ff-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-168">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="562ff-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="562ff-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="562ff-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-170">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="562ff-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="562ff-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="562ff-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-172">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="562ff-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="562ff-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="562ff-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-174">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="562ff-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="562ff-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="562ff-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-176">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="562ff-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="562ff-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="562ff-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-178">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="562ff-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-180">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="562ff-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-181">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="562ff-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="562ff-182">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="562ff-182">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="562ff-183">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1.</span><span class="sxs-lookup"><span data-stu-id="562ff-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="562ff-184">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="562ff-185">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="562ff-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-186">**Caption**</span><span class="sxs-lookup"><span data-stu-id="562ff-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-189">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="562ff-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-190">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="562ff-190">Short textual description of the object.</span></span>

<span data-ttu-id="562ff-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-192">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="562ff-192">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-193">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="562ff-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-195">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="562ff-195">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-196">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="562ff-196">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="562ff-197">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-197">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="562ff-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="562ff-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="562ff-199"> (0)</span><span class="sxs-lookup"><span data-stu-id="562ff-199">(0)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-200">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="562ff-200">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="562ff-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="562ff-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="562ff-202">(1)</span><span class="sxs-lookup"><span data-stu-id="562ff-202">(1)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-203">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="562ff-203">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="562ff-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="562ff-205">(2)</span><span class="sxs-lookup"><span data-stu-id="562ff-205">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="562ff-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="562ff-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="562ff-207">(3)</span><span class="sxs-lookup"><span data-stu-id="562ff-207">(3)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-208">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="562ff-208">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="562ff-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="562ff-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="562ff-210">(4)</span><span class="sxs-lookup"><span data-stu-id="562ff-210">(4)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-211">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="562ff-211">Device is not working properly.</span></span> <span data-ttu-id="562ff-212">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="562ff-212">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="562ff-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="562ff-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="562ff-214">(5)</span><span class="sxs-lookup"><span data-stu-id="562ff-214">(5)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-215">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="562ff-215">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="562ff-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="562ff-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="562ff-217"> (6)</span><span class="sxs-lookup"><span data-stu-id="562ff-217">(6)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-218">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="562ff-218">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="562ff-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="562ff-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="562ff-220">(7)</span><span class="sxs-lookup"><span data-stu-id="562ff-220">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="562ff-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="562ff-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="562ff-222">(8)</span><span class="sxs-lookup"><span data-stu-id="562ff-222">(8)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-223">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="562ff-223">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="562ff-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="562ff-225">(9)</span><span class="sxs-lookup"><span data-stu-id="562ff-225">(9)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-226">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-226">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="562ff-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="562ff-228">(10)</span><span class="sxs-lookup"><span data-stu-id="562ff-228">(10)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-229">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-229">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="562ff-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="562ff-231">(11)</span><span class="sxs-lookup"><span data-stu-id="562ff-231">(11)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-232">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-232">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="562ff-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="562ff-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="562ff-234">douze</span><span class="sxs-lookup"><span data-stu-id="562ff-234">(12)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-235">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="562ff-235">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="562ff-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="562ff-237">(13)</span><span class="sxs-lookup"><span data-stu-id="562ff-237">(13)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-238">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-238">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="562ff-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="562ff-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="562ff-240">(14)</span><span class="sxs-lookup"><span data-stu-id="562ff-240">(14)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-241">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="562ff-241">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="562ff-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="562ff-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="562ff-243">(15)</span><span class="sxs-lookup"><span data-stu-id="562ff-243">(15)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-244">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="562ff-244">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="562ff-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="562ff-246">(16)</span><span class="sxs-lookup"><span data-stu-id="562ff-246">(16)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-247">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-247">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="562ff-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="562ff-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="562ff-249">(17)</span><span class="sxs-lookup"><span data-stu-id="562ff-249">(17)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-250">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="562ff-250">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="562ff-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="562ff-252">(18)</span><span class="sxs-lookup"><span data-stu-id="562ff-252">(18)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-253">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="562ff-253">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="562ff-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="562ff-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="562ff-255">(19)</span><span class="sxs-lookup"><span data-stu-id="562ff-255">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="562ff-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="562ff-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="562ff-257">(20)</span><span class="sxs-lookup"><span data-stu-id="562ff-257">(20)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-258">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="562ff-258">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="562ff-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="562ff-260">(21)</span><span class="sxs-lookup"><span data-stu-id="562ff-260">(21)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-261">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="562ff-261">System failure.</span></span> <span data-ttu-id="562ff-262">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="562ff-262">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="562ff-263">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-263">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="562ff-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="562ff-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="562ff-265">(22)</span><span class="sxs-lookup"><span data-stu-id="562ff-265">(22)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-266">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="562ff-266">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="562ff-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="562ff-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="562ff-268">(23)</span><span class="sxs-lookup"><span data-stu-id="562ff-268">(23)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-269">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="562ff-269">System failure.</span></span> <span data-ttu-id="562ff-270">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="562ff-270">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="562ff-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="562ff-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="562ff-272">(24)</span><span class="sxs-lookup"><span data-stu-id="562ff-272">(24)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-273">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="562ff-273">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="562ff-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="562ff-275">(25)</span><span class="sxs-lookup"><span data-stu-id="562ff-275">(25)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-276">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="562ff-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="562ff-278">(26)</span><span class="sxs-lookup"><span data-stu-id="562ff-278">(26)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-279">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="562ff-279">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="562ff-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="562ff-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="562ff-281">(27)</span><span class="sxs-lookup"><span data-stu-id="562ff-281">(27)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-282">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="562ff-282">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="562ff-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="562ff-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="562ff-284">(28)</span><span class="sxs-lookup"><span data-stu-id="562ff-284">(28)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-285">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="562ff-285">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="562ff-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="562ff-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="562ff-287">(29)</span><span class="sxs-lookup"><span data-stu-id="562ff-287">(29)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-288">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="562ff-288">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="562ff-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="562ff-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="562ff-290">(30)</span><span class="sxs-lookup"><span data-stu-id="562ff-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-291">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="562ff-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="562ff-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="562ff-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="562ff-293">31</span><span class="sxs-lookup"><span data-stu-id="562ff-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-294">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="562ff-294">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="562ff-295">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="562ff-295">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-296">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="562ff-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-298">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="562ff-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-299">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="562ff-299">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="562ff-300">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-301">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="562ff-301">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-304">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="562ff-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="562ff-305">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="562ff-305">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="562ff-306">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="562ff-306">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="562ff-307">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-308">**Description**</span><span class="sxs-lookup"><span data-stu-id="562ff-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-311">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="562ff-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-312">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="562ff-312">Textual description of the object.</span></span>

<span data-ttu-id="562ff-313">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="562ff-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-317">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="562ff-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="562ff-318">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="562ff-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="562ff-319">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="562ff-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-321">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="562ff-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="562ff-323">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="562ff-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="562ff-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="562ff-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="562ff-328">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="562ff-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="562ff-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-330">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="562ff-330">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="562ff-333">Chaîne de forme libre qui décrit le type de détection d’erreurs et de correction pris en charge par l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="562ff-333">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="562ff-334">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-334">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-335">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="562ff-335">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-336">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="562ff-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-338">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="562ff-338">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-339">Espace libre disponible, en octets, sur le disque logique.</span><span class="sxs-lookup"><span data-stu-id="562ff-339">Available free space, in bytes, on the logical disk.</span></span>

<span data-ttu-id="562ff-340">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="562ff-340">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-341">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="562ff-341">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-342">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="562ff-342">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-344">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="562ff-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-345">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="562ff-345">Date and time the object was installed.</span></span> <span data-ttu-id="562ff-346">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="562ff-346">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="562ff-347">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-348">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="562ff-348">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-349">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="562ff-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="562ff-351">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="562ff-351">Last error code reported by the logical device.</span></span>

<span data-ttu-id="562ff-352">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-353">**Nom**</span><span class="sxs-lookup"><span data-stu-id="562ff-353">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-354">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-356">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="562ff-356">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-357">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="562ff-357">Label by which the object is known.</span></span> <span data-ttu-id="562ff-358">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="562ff-358">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="562ff-359">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-359">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-360">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="562ff-360">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-361">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="562ff-361">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-363">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="562ff-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-364">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui constitue l’étendue de stockage.</span><span class="sxs-lookup"><span data-stu-id="562ff-364">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form the storage extent.</span></span> <span data-ttu-id="562ff-365">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="562ff-365">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="562ff-366">Si la valeur de la propriété **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="562ff-366">If the value of the **BlockSize** property is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="562ff-367">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-367">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="562ff-368">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="562ff-368">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-369">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="562ff-369">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-370">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-372">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="562ff-372">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-373">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="562ff-373">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="562ff-374">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="562ff-375">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="562ff-375">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="562ff-376">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="562ff-376">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-377">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="562ff-377">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="562ff-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="562ff-379">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="562ff-379">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="562ff-380">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="562ff-380">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="562ff-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="562ff-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="562ff-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="562ff-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="562ff-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="562ff-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="562ff-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="562ff-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-385">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="562ff-385">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="562ff-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="562ff-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-387">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="562ff-387">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="562ff-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="562ff-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-389">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="562ff-389">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="562ff-390">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="562ff-390">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="562ff-391">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="562ff-391">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="562ff-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="562ff-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-393">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="562ff-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="562ff-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="562ff-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="562ff-395">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="562ff-395">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="562ff-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="562ff-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-397">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="562ff-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="562ff-399">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="562ff-399">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="562ff-400">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="562ff-400">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="562ff-401">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="562ff-401">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="562ff-402">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="562ff-402">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="562ff-403">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-404">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="562ff-404">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-405">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="562ff-407">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="562ff-407">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="562ff-408">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-408">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-409">**Taille**</span><span class="sxs-lookup"><span data-stu-id="562ff-409">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-410">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="562ff-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-412">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="562ff-412">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-413">Taille du disque logique, en octets.</span><span class="sxs-lookup"><span data-stu-id="562ff-413">Size of the logical disk, in bytes.</span></span>

<span data-ttu-id="562ff-414">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="562ff-414">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-415">**État**</span><span class="sxs-lookup"><span data-stu-id="562ff-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-416">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-418">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="562ff-418">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-419">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="562ff-419">Current status of the object.</span></span>

<span data-ttu-id="562ff-420">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-420">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="562ff-421">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="562ff-421">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="562ff-422">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="562ff-422">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="562ff-423">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="562ff-423">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="562ff-424">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="562ff-424">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="562ff-425">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="562ff-425">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="562ff-426">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="562ff-426">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="562ff-427">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="562ff-427">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="562ff-428">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="562ff-428">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="562ff-429">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="562ff-429">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="562ff-430">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="562ff-430">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="562ff-431">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="562ff-431">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="562ff-432">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="562ff-432">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="562ff-433">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="562ff-433">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="562ff-434">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="562ff-434">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-435">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="562ff-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-437">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="562ff-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="562ff-438">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="562ff-438">State of the logical device.</span></span> <span data-ttu-id="562ff-439">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="562ff-439">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="562ff-440">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="562ff-441">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="562ff-441">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="562ff-442">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="562ff-442">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="562ff-443">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="562ff-443">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="562ff-444">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="562ff-444">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="562ff-445">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="562ff-445">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="562ff-446">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="562ff-446">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-447">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-449">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="562ff-449">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="562ff-450">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="562ff-450">Scoping system's creation class name.</span></span>

<span data-ttu-id="562ff-451">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="562ff-452">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="562ff-452">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="562ff-453">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="562ff-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="562ff-454">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="562ff-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="562ff-455">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="562ff-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="562ff-456">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="562ff-456">Scoping system's name.</span></span>

<span data-ttu-id="562ff-457">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="562ff-458">Notes</span><span class="sxs-lookup"><span data-stu-id="562ff-458">Remarks</span></span>

<span data-ttu-id="562ff-459">La **classe \_ LogicalDisk CIM** est dérivée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-459">The **CIM\_LogicalDisk** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="562ff-460">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="562ff-460">WMI does not implement this class.</span></span> <span data-ttu-id="562ff-461">Pour les classes dérivées du **\_ disque logique CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-461">For classes derived from **CIM\_LogicalDisk**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="562ff-462">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="562ff-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="562ff-463">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="562ff-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="562ff-464">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="562ff-464">Requirements</span></span>



| <span data-ttu-id="562ff-465">Condition requise</span><span class="sxs-lookup"><span data-stu-id="562ff-465">Requirement</span></span> | <span data-ttu-id="562ff-466">Valeur</span><span class="sxs-lookup"><span data-stu-id="562ff-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="562ff-467">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="562ff-467">Minimum supported client</span></span><br/> | <span data-ttu-id="562ff-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="562ff-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="562ff-469">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="562ff-469">Minimum supported server</span></span><br/> | <span data-ttu-id="562ff-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="562ff-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="562ff-471">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="562ff-471">Namespace</span></span><br/>                | <span data-ttu-id="562ff-472">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="562ff-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="562ff-473">MOF</span><span class="sxs-lookup"><span data-stu-id="562ff-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="562ff-474"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="562ff-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="562ff-475">DLL</span><span class="sxs-lookup"><span data-stu-id="562ff-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="562ff-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="562ff-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562ff-477">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="562ff-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562ff-478">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="562ff-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

