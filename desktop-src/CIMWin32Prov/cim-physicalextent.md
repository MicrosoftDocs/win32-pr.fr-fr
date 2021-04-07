---
description: La \_ classe CIM PhysicalExtent représente une implémentation RAID SCC.
ms.assetid: d1950464-e17a-4651-aa53-6385659994ff
ms.tgt_platform: multiple
title: Classe CIM_PhysicalExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalExtent
- CIM_PhysicalExtent.Access
- CIM_PhysicalExtent.Availability
- CIM_PhysicalExtent.BlockSize
- CIM_PhysicalExtent.Caption
- CIM_PhysicalExtent.ConfigManagerErrorCode
- CIM_PhysicalExtent.ConfigManagerUserConfig
- CIM_PhysicalExtent.CreationClassName
- CIM_PhysicalExtent.Description
- CIM_PhysicalExtent.DeviceID
- CIM_PhysicalExtent.ErrorCleared
- CIM_PhysicalExtent.ErrorDescription
- CIM_PhysicalExtent.ErrorMethodology
- CIM_PhysicalExtent.InstallDate
- CIM_PhysicalExtent.LastErrorCode
- CIM_PhysicalExtent.Name
- CIM_PhysicalExtent.NumberOfBlocks
- CIM_PhysicalExtent.PNPDeviceID
- CIM_PhysicalExtent.PowerManagementCapabilities
- CIM_PhysicalExtent.PowerManagementSupported
- CIM_PhysicalExtent.Purpose
- CIM_PhysicalExtent.Status
- CIM_PhysicalExtent.StatusInfo
- CIM_PhysicalExtent.SystemCreationClassName
- CIM_PhysicalExtent.SystemName
- CIM_PhysicalExtent.UnitsBeforeCheckDataInterleave
- CIM_PhysicalExtent.UnitsOfCheckData
- CIM_PhysicalExtent.UnitsOfUserData
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 31e05d3b339d64fd640460716376c3d8b538fa95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747845"
---
# <a name="cim_physicalextent-class"></a><span data-ttu-id="0e6f4-103">\_Classe CIM PhysicalExtent</span><span class="sxs-lookup"><span data-stu-id="0e6f4-103">CIM\_PhysicalExtent class</span></span>

<span data-ttu-id="0e6f4-104">La classe **CIM \_ PhysicalExtent** représente une implémentation RAID SCC.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-104">The **CIM\_PhysicalExtent** class represents an SCC RAID implementation.</span></span> <span data-ttu-id="0e6f4-105">Il définit les adresses de bloc adressables consécutives sur un dispositif de stockage unique qui sont traitées comme une extension de stockage unique dans la même classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="0e6f4-105">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="0e6f4-106">Une alternative, lorsque la configuration automatique est utilisée, consiste à instancier ou étendre la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .</span><span class="sxs-lookup"><span data-stu-id="0e6f4-106">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e6f4-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0e6f4-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0e6f4-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0e6f4-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e6f4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e6f4-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979E-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalExtent : CIM_StorageExtent
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
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   UnitsBeforeCheckDataInterleave;
  uint64   UnitsOfCheckData;
  uint64   UnitsOfUserData;
};
```

## <a name="members"></a><span data-ttu-id="0e6f4-112">Membres</span><span class="sxs-lookup"><span data-stu-id="0e6f4-112">Members</span></span>

<span data-ttu-id="0e6f4-113">La classe **CIM \_ PhysicalExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e6f4-113">The **CIM\_PhysicalExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="0e6f4-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e6f4-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e6f4-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e6f4-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e6f4-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e6f4-116">Methods</span></span>

<span data-ttu-id="0e6f4-117">La classe **CIM \_ PhysicalExtent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-117">The **CIM\_PhysicalExtent** class has these methods.</span></span>



| <span data-ttu-id="0e6f4-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="0e6f4-118">Method</span></span>                                                                    | <span data-ttu-id="0e6f4-119">Description</span><span class="sxs-lookup"><span data-stu-id="0e6f4-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e6f4-120">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-120">**Reset**</span></span>](reset-method-in-class-cim-physicalextent.md)                 | <span data-ttu-id="0e6f4-121">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="0e6f4-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0e6f4-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-physicalextent.md) | <span data-ttu-id="0e6f4-124">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0e6f4-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0e6f4-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e6f4-126">Properties</span></span>

<span data-ttu-id="0e6f4-127">La classe **CIM \_ PhysicalExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-127">The **CIM\_PhysicalExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e6f4-128">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-131">Propriétés de lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-131">Read/write properties of the media.</span></span>

<span data-ttu-id="0e6f4-132">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e6f4-133">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="0e6f4-134">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="0e6f4-135">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="0e6f4-136">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="0e6f4-137">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e6f4-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-141">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-142">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-142">Availability and status of the device.</span></span>

<span data-ttu-id="0e6f4-143">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e6f4-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e6f4-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0e6f4-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-147">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="0e6f4-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0e6f4-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0e6f4-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0e6f4-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0e6f4-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0e6f4-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0e6f4-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e6f4-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0e6f4-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0e6f4-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0e6f4-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-158">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0e6f4-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-160">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0e6f4-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-162">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0e6f4-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0e6f4-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-165">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0e6f4-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-167">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0e6f4-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-169">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0e6f4-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-171">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0e6f4-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-173">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e6f4-174">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-174">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-175">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-177">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BlockSize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extension physique DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-177">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BlockSize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-178">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-178">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="0e6f4-179">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-179">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="0e6f4-180">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-180">If the block size is unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one) .</span></span>

<span data-ttu-id="0e6f4-181">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0e6f4-182">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-183">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-183">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-186">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-187">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-187">Short textual description of the object.</span></span>

<span data-ttu-id="0e6f4-188">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-189">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-189">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-190">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-192">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-192">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-193">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-193">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="0e6f4-194">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0e6f4-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0e6f4-196"> (0)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-196">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-197">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-197">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0e6f4-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0e6f4-199">(1)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-199">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-200">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-200">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e6f4-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0e6f4-202">(2)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-202">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0e6f4-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0e6f4-204">(3)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-204">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-205">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-205">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0e6f4-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0e6f4-207">(4)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-207">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-208">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-208">Device is not working properly.</span></span> <span data-ttu-id="0e6f4-209">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-209">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0e6f4-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0e6f4-211">(5)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-211">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-212">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-212">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0e6f4-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0e6f4-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-214">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-215">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-215">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0e6f4-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0e6f4-217">(7)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-217">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0e6f4-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0e6f4-219">(8)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-219">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-220">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-220">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0e6f4-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0e6f4-222">(9)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-222">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-223">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-223">Device is not working properly.</span></span> <span data-ttu-id="0e6f4-224">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-224">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0e6f4-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0e6f4-226">(10)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-226">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-227">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-227">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0e6f4-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0e6f4-229">(11)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-229">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-230">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-230">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0e6f4-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0e6f4-232">douze</span><span class="sxs-lookup"><span data-stu-id="0e6f4-232">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-233">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-233">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0e6f4-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0e6f4-235">(13)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-235">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-236">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-236">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0e6f4-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0e6f4-238">(14)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-238">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-239">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-239">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0e6f4-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0e6f4-241">(15)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-241">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-242">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-242">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0e6f4-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0e6f4-244">(16)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-244">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-245">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-245">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0e6f4-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0e6f4-247">(17)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-247">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-248">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-248">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e6f4-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0e6f4-250">(18)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-250">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-251">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-251">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0e6f4-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0e6f4-253">(19)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-253">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0e6f4-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0e6f4-255">(20)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-255">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-256">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-256">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0e6f4-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0e6f4-258">(21)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-258">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-259">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-259">System failure.</span></span> <span data-ttu-id="0e6f4-260">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-260">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0e6f4-261">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-261">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0e6f4-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0e6f4-263">(22)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-263">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-264">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-264">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0e6f4-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0e6f4-266">(23)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-266">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-267">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-267">System failure.</span></span> <span data-ttu-id="0e6f4-268">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-268">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0e6f4-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0e6f4-270">(24)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-270">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-271">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-271">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0e6f4-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0e6f4-273">(25)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-273">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-274">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0e6f4-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0e6f4-276">(26)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-276">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-277">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-277">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0e6f4-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0e6f4-279">(27)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-279">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-280">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-280">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0e6f4-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0e6f4-282">(28)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-282">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-283">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-283">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0e6f4-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0e6f4-285">(29)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-285">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-286">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-286">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0e6f4-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0e6f4-288">(30)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-289">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0e6f4-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0e6f4-291">31</span><span class="sxs-lookup"><span data-stu-id="0e6f4-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-292">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-292">Device is not working properly.</span></span> <span data-ttu-id="0e6f4-293">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e6f4-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-295">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-297">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-298">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0e6f4-299">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-303">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-304">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0e6f4-305">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0e6f4-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-307">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-310">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-311">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-311">Textual description of the object.</span></span>

<span data-ttu-id="0e6f4-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-314">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-316">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-317">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0e6f4-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-320">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-322">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0e6f4-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-327">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0e6f4-328">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-332">Chaîne de forme libre qui décrit le type de détection d’erreurs et de correction pris en charge par l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="0e6f4-333">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-335">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-338">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-338">Date and time the object was installed.</span></span> <span data-ttu-id="0e6f4-339">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0e6f4-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-342">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-344">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0e6f4-345">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-346">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-349">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-350">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-350">Label by which the object is known.</span></span> <span data-ttu-id="0e6f4-351">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0e6f4-352">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-354">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-356">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extension physique DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-356">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-357">Nombre total de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forme cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="0e6f4-358">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="0e6f4-359">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="0e6f4-360">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0e6f4-361">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-363">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-365">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-366">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="0e6f4-367">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0e6f4-368">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="0e6f4-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-370">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-372">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0e6f4-373">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e6f4-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0e6f4-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0e6f4-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0e6f4-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-378">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0e6f4-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-380">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0e6f4-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-382">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0e6f4-383">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-383">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0e6f4-384">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0e6f4-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-386">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0e6f4-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0e6f4-388">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e6f4-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-390">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-392">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0e6f4-393">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0e6f4-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0e6f4-394">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0e6f4-395">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0e6f4-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="0e6f4-396">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-397">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-397">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-398">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-400">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-400">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="0e6f4-401">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-402">**État**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-402">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-405">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-406">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-406">Current status of the object.</span></span>

<span data-ttu-id="0e6f4-407">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0e6f4-408">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e6f4-408">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0e6f4-409">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-409">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0e6f4-410">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-410">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e6f4-411">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-411">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e6f4-412">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-412">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0e6f4-413">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-413">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0e6f4-414">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-414">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0e6f4-415">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-415">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0e6f4-416">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-416">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0e6f4-417">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-417">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0e6f4-418">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-418">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0e6f4-419">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-419">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0e6f4-420">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-420">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e6f4-421">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-421">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-422">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-423">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-424">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-425">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-425">State of the logical device.</span></span> <span data-ttu-id="0e6f4-426">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-426">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0e6f4-427">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e6f4-428">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-428">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e6f4-429">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-429">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0e6f4-430">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0e6f4-431">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-431">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0e6f4-432">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-432">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e6f4-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-436">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-437">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-437">Scoping system's creation class name.</span></span>

<span data-ttu-id="0e6f4-438">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-440">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-442">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e6f4-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-443">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-443">Scoping system's name.</span></span>

<span data-ttu-id="0e6f4-444">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-445">**UnitsBeforeCheckDataInterleave**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-445">**UnitsBeforeCheckDataInterleave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-446">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-446">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-448">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extension physique DMTF \| 001,6 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-449">Nombre d’octets de données utilisateur à ignorer avant de démarrer l’entrelacement des données de vérification.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-449">Number of user data bytes to skip before starting the check-data interleave.</span></span>

<span data-ttu-id="0e6f4-450">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-451">**UnitsOfCheckData**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-451">**UnitsOfCheckData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-452">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-452">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-454">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extension physique DMTF \| 001,7 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-455">Nombre d’octets à réserver pour les données de vérification.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-455">Number of bytes to be reserved for check data.</span></span>

<span data-ttu-id="0e6f4-456">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-456">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0e6f4-457">**UnitsOfUserData**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-457">**UnitsOfUserData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6f4-458">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-458">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-459">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e6f4-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e6f4-460">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extension physique DMTF \| 001,8 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="0e6f4-460">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0e6f4-461">Nombre d’octets à réserver pour les données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-461">Number of bytes to be reserved for user data.</span></span>

<span data-ttu-id="0e6f4-462">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-462">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e6f4-463">Notes</span><span class="sxs-lookup"><span data-stu-id="0e6f4-463">Remarks</span></span>

<span data-ttu-id="0e6f4-464">La classe **CIM \_ PhysicalExtent** est dérivée de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="0e6f4-464">The **CIM\_PhysicalExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="0e6f4-465">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-465">WMI does not implement this class.</span></span>

<span data-ttu-id="0e6f4-466">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-466">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0e6f4-467">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0e6f4-467">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e6f4-468">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e6f4-468">Requirements</span></span>



| <span data-ttu-id="0e6f4-469">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e6f4-469">Requirement</span></span> | <span data-ttu-id="0e6f4-470">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e6f4-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6f4-471">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e6f4-471">Minimum supported client</span></span><br/> | <span data-ttu-id="0e6f4-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e6f4-472">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e6f4-473">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e6f4-473">Minimum supported server</span></span><br/> | <span data-ttu-id="0e6f4-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e6f4-474">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e6f4-475">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e6f4-475">Namespace</span></span><br/>                | <span data-ttu-id="0e6f4-476">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0e6f4-476">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e6f4-477">MOF</span><span class="sxs-lookup"><span data-stu-id="0e6f4-477">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e6f4-478"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e6f4-478"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e6f4-479">DLL</span><span class="sxs-lookup"><span data-stu-id="0e6f4-479">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e6f4-480"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e6f4-480"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e6f4-481">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e6f4-481">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6f4-482">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0e6f4-482">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

