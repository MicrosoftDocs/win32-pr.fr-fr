---
description: La \_ classe CIM StorageExtent représente les fonctionnalités et la gestion des différents médias qui existent pour stocker des données et permettre la récupération des données.
ms.assetid: 3895e00e-1a80-4d45-be0a-b159f8f335e8
ms.tgt_platform: multiple
title: CIM_StorageExtent, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.Access
- CIM_StorageExtent.Availability
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.Caption
- CIM_StorageExtent.ConfigManagerErrorCode
- CIM_StorageExtent.ConfigManagerUserConfig
- CIM_StorageExtent.CreationClassName
- CIM_StorageExtent.Description
- CIM_StorageExtent.DeviceID
- CIM_StorageExtent.ErrorCleared
- CIM_StorageExtent.ErrorDescription
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.InstallDate
- CIM_StorageExtent.LastErrorCode
- CIM_StorageExtent.Name
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.PNPDeviceID
- CIM_StorageExtent.PowerManagementCapabilities
- CIM_StorageExtent.PowerManagementSupported
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Status
- CIM_StorageExtent.StatusInfo
- CIM_StorageExtent.SystemCreationClassName
- CIM_StorageExtent.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f2d83386822d0994cc3acf68b97acc2841b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513144"
---
# <a name="cim_storageextent-class-cimwin32-wmi-providers"></a><span data-ttu-id="9f64a-103">CIM_StorageExtent, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9f64a-103">CIM_StorageExtent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9f64a-104">La classe **CIM \_ StorageExtent** représente les fonctionnalités et la gestion des différents médias qui existent pour stocker des données et permettre la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="9f64a-104">The **CIM\_StorageExtent** class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="9f64a-105">Cette classe parente peut représenter les différents composants de RAID (matériel ou logiciel) ou une extension logique brute sur les supports physiques.</span><span class="sxs-lookup"><span data-stu-id="9f64a-105">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f64a-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9f64a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9f64a-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9f64a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9f64a-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9f64a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9f64a-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9f64a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f64a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f64a-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C538-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
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
};
```

## <a name="members"></a><span data-ttu-id="9f64a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="9f64a-111">Members</span></span>

<span data-ttu-id="9f64a-112">La classe **CIM \_ StorageExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9f64a-112">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="9f64a-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9f64a-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f64a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f64a-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f64a-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9f64a-115">Methods</span></span>

<span data-ttu-id="9f64a-116">La classe **CIM \_ StorageExtent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9f64a-116">The **CIM\_StorageExtent** class has these methods.</span></span>



| <span data-ttu-id="9f64a-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="9f64a-117">Method</span></span>                                                                   | <span data-ttu-id="9f64a-118">Description</span><span class="sxs-lookup"><span data-stu-id="9f64a-118">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f64a-119">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="9f64a-119">**Reset**</span></span>](reset-method-in-class-cim-storageextent.md)                 | <span data-ttu-id="9f64a-120">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9f64a-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="9f64a-121">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="9f64a-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9f64a-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9f64a-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-storageextent.md) | <span data-ttu-id="9f64a-123">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="9f64a-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9f64a-124">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="9f64a-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9f64a-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f64a-125">Properties</span></span>

<span data-ttu-id="9f64a-126">La classe **CIM \_ StorageExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f64a-126">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f64a-127">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="9f64a-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f64a-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-130">Décrit les propriétés en lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="9f64a-130">Describes the read/write properties of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f64a-131">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9f64a-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="9f64a-132">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="9f64a-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="9f64a-133">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="9f64a-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="9f64a-134">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="9f64a-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="9f64a-135">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="9f64a-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f64a-136">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="9f64a-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f64a-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9f64a-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-140">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-140">Availability and status of the device.</span></span>

<span data-ttu-id="9f64a-141">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f64a-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9f64a-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f64a-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9f64a-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9f64a-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="9f64a-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9f64a-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="9f64a-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9f64a-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="9f64a-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9f64a-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="9f64a-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9f64a-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="9f64a-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9f64a-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="9f64a-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9f64a-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="9f64a-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9f64a-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="9f64a-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9f64a-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="9f64a-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9f64a-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="9f64a-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9f64a-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="9f64a-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-155">Économie d’énergie-inconnu</span><span class="sxs-lookup"><span data-stu-id="9f64a-155">Power Save - Unknown</span></span>

<span data-ttu-id="9f64a-156">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="9f64a-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9f64a-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="9f64a-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-158">Économie d’énergie-mode faible puissance</span><span class="sxs-lookup"><span data-stu-id="9f64a-158">Power Save - Low Power Mode</span></span>

<span data-ttu-id="9f64a-159">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="9f64a-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9f64a-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="9f64a-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-161">Économie d’énergie-veille</span><span class="sxs-lookup"><span data-stu-id="9f64a-161">Power Save - Standby</span></span>

<span data-ttu-id="9f64a-162">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="9f64a-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9f64a-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="9f64a-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9f64a-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="9f64a-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-165">Économie d’énergie-Avertissement</span><span class="sxs-lookup"><span data-stu-id="9f64a-165">Power Save - Warning</span></span>

<span data-ttu-id="9f64a-166">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="9f64a-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9f64a-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="9f64a-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-168">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="9f64a-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9f64a-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="9f64a-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-170">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="9f64a-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9f64a-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="9f64a-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-172">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="9f64a-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9f64a-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="9f64a-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-174">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="9f64a-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f64a-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="9f64a-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-176">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f64a-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-178">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="9f64a-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-179">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="9f64a-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="9f64a-180">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9f64a-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="9f64a-181">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="9f64a-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="9f64a-182">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9f64a-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-183">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9f64a-183">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-186">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-187">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-187">Short textual description of the object.</span></span>

<span data-ttu-id="9f64a-188">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-189">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9f64a-189">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-190">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f64a-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-192">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f64a-192">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-193">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9f64a-193">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="9f64a-194">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9f64a-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9f64a-196"> (0)</span><span class="sxs-lookup"><span data-stu-id="9f64a-196">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-197">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="9f64a-197">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9f64a-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9f64a-199">(1)</span><span class="sxs-lookup"><span data-stu-id="9f64a-199">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-200">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="9f64a-200">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f64a-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9f64a-202">(2)</span><span class="sxs-lookup"><span data-stu-id="9f64a-202">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9f64a-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9f64a-204">(3)</span><span class="sxs-lookup"><span data-stu-id="9f64a-204">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-205">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="9f64a-205">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9f64a-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9f64a-207">(4)</span><span class="sxs-lookup"><span data-stu-id="9f64a-207">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-208">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9f64a-208">Device is not working properly.</span></span> <span data-ttu-id="9f64a-209">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="9f64a-209">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9f64a-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9f64a-211">(5)</span><span class="sxs-lookup"><span data-stu-id="9f64a-211">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-212">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="9f64a-212">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9f64a-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9f64a-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="9f64a-214">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-215">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="9f64a-215">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9f64a-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9f64a-217">(7)</span><span class="sxs-lookup"><span data-stu-id="9f64a-217">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9f64a-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9f64a-219">(8)</span><span class="sxs-lookup"><span data-stu-id="9f64a-219">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-220">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="9f64a-220">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9f64a-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9f64a-222">(9)</span><span class="sxs-lookup"><span data-stu-id="9f64a-222">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-223">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9f64a-223">Device is not working properly.</span></span> <span data-ttu-id="9f64a-224">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-224">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9f64a-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9f64a-226">(10)</span><span class="sxs-lookup"><span data-stu-id="9f64a-226">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-227">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-227">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9f64a-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9f64a-229">(11)</span><span class="sxs-lookup"><span data-stu-id="9f64a-229">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-230">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-230">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9f64a-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9f64a-232">douze</span><span class="sxs-lookup"><span data-stu-id="9f64a-232">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-233">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9f64a-233">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9f64a-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9f64a-235">(13)</span><span class="sxs-lookup"><span data-stu-id="9f64a-235">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-236">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-236">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9f64a-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9f64a-238">(14)</span><span class="sxs-lookup"><span data-stu-id="9f64a-238">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-239">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="9f64a-239">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9f64a-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9f64a-241">(15)</span><span class="sxs-lookup"><span data-stu-id="9f64a-241">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-242">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="9f64a-242">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9f64a-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9f64a-244">(16)</span><span class="sxs-lookup"><span data-stu-id="9f64a-244">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-245">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-245">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9f64a-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9f64a-247">(17)</span><span class="sxs-lookup"><span data-stu-id="9f64a-247">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-248">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="9f64a-248">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f64a-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9f64a-250">(18)</span><span class="sxs-lookup"><span data-stu-id="9f64a-250">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-251">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="9f64a-251">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9f64a-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9f64a-253">(19)</span><span class="sxs-lookup"><span data-stu-id="9f64a-253">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9f64a-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9f64a-255">(20)</span><span class="sxs-lookup"><span data-stu-id="9f64a-255">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-256">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="9f64a-256">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9f64a-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9f64a-258">(21)</span><span class="sxs-lookup"><span data-stu-id="9f64a-258">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-259">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="9f64a-259">System failure.</span></span> <span data-ttu-id="9f64a-260">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="9f64a-260">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9f64a-261">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-261">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9f64a-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9f64a-263">(22)</span><span class="sxs-lookup"><span data-stu-id="9f64a-263">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-264">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9f64a-264">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9f64a-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9f64a-266">(23)</span><span class="sxs-lookup"><span data-stu-id="9f64a-266">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-267">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="9f64a-267">System failure.</span></span> <span data-ttu-id="9f64a-268">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="9f64a-268">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9f64a-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9f64a-270">(24)</span><span class="sxs-lookup"><span data-stu-id="9f64a-270">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-271">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="9f64a-271">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9f64a-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9f64a-273">(25)</span><span class="sxs-lookup"><span data-stu-id="9f64a-273">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-274">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9f64a-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9f64a-276">(26)</span><span class="sxs-lookup"><span data-stu-id="9f64a-276">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-277">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9f64a-277">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9f64a-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9f64a-279">(27)</span><span class="sxs-lookup"><span data-stu-id="9f64a-279">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-280">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="9f64a-280">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9f64a-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9f64a-282">(28)</span><span class="sxs-lookup"><span data-stu-id="9f64a-282">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-283">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="9f64a-283">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9f64a-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9f64a-285">(29)</span><span class="sxs-lookup"><span data-stu-id="9f64a-285">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-286">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9f64a-286">Device is disabled.</span></span> <span data-ttu-id="9f64a-287">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="9f64a-287">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9f64a-288"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-288"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9f64a-289">(30)</span><span class="sxs-lookup"><span data-stu-id="9f64a-289">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-290">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="9f64a-290">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f64a-291"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9f64a-291"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9f64a-292">31</span><span class="sxs-lookup"><span data-stu-id="9f64a-292">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-293">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9f64a-293">Device is not working properly.</span></span> <span data-ttu-id="9f64a-294">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="9f64a-294">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f64a-295">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9f64a-295">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-296">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9f64a-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-298">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f64a-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-299">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f64a-299">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9f64a-300">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-301">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9f64a-301">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-304">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f64a-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-305">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9f64a-305">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9f64a-306">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="9f64a-306">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9f64a-307">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-308">**Description**</span><span class="sxs-lookup"><span data-stu-id="9f64a-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-311">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9f64a-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-312">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-312">Textual description of the object.</span></span>

<span data-ttu-id="9f64a-313">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f64a-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-317">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f64a-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-318">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9f64a-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9f64a-319">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9f64a-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-321">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9f64a-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-323">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="9f64a-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9f64a-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9f64a-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-328">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="9f64a-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9f64a-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-330">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="9f64a-330">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-333">Chaîne de forme libre qui décrit le type de détection d’erreurs et de correction pris en charge par l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="9f64a-333">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9f64a-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-335">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9f64a-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="9f64a-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-338">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-338">Date and time the object was installed.</span></span> <span data-ttu-id="9f64a-339">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="9f64a-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9f64a-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9f64a-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-342">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f64a-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-344">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9f64a-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9f64a-345">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-346">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9f64a-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-349">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9f64a-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-350">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9f64a-350">Label by which the object is known.</span></span> <span data-ttu-id="9f64a-351">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="9f64a-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9f64a-352">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="9f64a-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-354">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f64a-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-356">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="9f64a-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-357">Nombre de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="9f64a-357">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="9f64a-358">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9f64a-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="9f64a-359">Si la valeur de **BlockSize** est 1 (un), cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="9f64a-359">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="9f64a-360">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9f64a-360">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-361">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f64a-361">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-362">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-364">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f64a-364">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-365">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9f64a-365">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9f64a-366">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9f64a-367">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="9f64a-367">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-368">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9f64a-368">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-369">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f64a-369">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-371">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="9f64a-371">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9f64a-372">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f64a-373"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9f64a-373"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9f64a-374"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="9f64a-374"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9f64a-375"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="9f64a-375"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9f64a-376"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="9f64a-376"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-377">activé</span><span class="sxs-lookup"><span data-stu-id="9f64a-377">Enabled</span></span>

<span data-ttu-id="9f64a-378">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="9f64a-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9f64a-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="9f64a-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-380">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="9f64a-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9f64a-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="9f64a-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-382">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9f64a-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9f64a-383">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="9f64a-383">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9f64a-384">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9f64a-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9f64a-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="9f64a-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-386">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="9f64a-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9f64a-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="9f64a-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9f64a-388">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="9f64a-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f64a-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9f64a-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-390">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9f64a-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-392">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="9f64a-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9f64a-393">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9f64a-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9f64a-394">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9f64a-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9f64a-395">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9f64a-395">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9f64a-396">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-397">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="9f64a-397">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-398">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-400">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="9f64a-400">Free form string that describes the media and its use.</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-401">**État**</span><span class="sxs-lookup"><span data-stu-id="9f64a-401">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-402">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-404">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9f64a-404">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-405">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-405">Current status of the object.</span></span>

<span data-ttu-id="9f64a-406">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9f64a-407">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f64a-407">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9f64a-408">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-408">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9f64a-409">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-409">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9f64a-410">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-410">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f64a-411">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="9f64a-411">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9f64a-412">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-412">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9f64a-413">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-413">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9f64a-414">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-414">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9f64a-415">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-415">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9f64a-416">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-416">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9f64a-417">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-417">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9f64a-418">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-418">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9f64a-419">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="9f64a-419">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f64a-420">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9f64a-420">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-421">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f64a-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-423">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9f64a-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-424">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9f64a-424">State of the logical device.</span></span> <span data-ttu-id="9f64a-425">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="9f64a-425">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9f64a-426">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f64a-427">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9f64a-427">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f64a-428">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9f64a-428">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9f64a-429">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="9f64a-429">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9f64a-430">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="9f64a-430">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9f64a-431">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="9f64a-431">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f64a-432">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9f64a-432">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-433">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-435">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f64a-435">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-436">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9f64a-436">Scoping system's creation class name.</span></span>

<span data-ttu-id="9f64a-437">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f64a-438">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9f64a-438">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f64a-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f64a-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f64a-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f64a-441">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f64a-441">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f64a-442">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9f64a-442">Scoping system's name.</span></span>

<span data-ttu-id="9f64a-443">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f64a-444">Notes</span><span class="sxs-lookup"><span data-stu-id="9f64a-444">Remarks</span></span>

<span data-ttu-id="9f64a-445">La classe **CIM \_ StorageExtent** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-445">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9f64a-446">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="9f64a-446">WMI does not implement this class.</span></span> <span data-ttu-id="9f64a-447">Pour les classes WMI dérivées de **CIM \_ StorageExtent**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-447">For WMI classes derived from **CIM\_StorageExtent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9f64a-448">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9f64a-448">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9f64a-449">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9f64a-449">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f64a-450">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f64a-450">Requirements</span></span>



| <span data-ttu-id="9f64a-451">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f64a-451">Requirement</span></span> | <span data-ttu-id="9f64a-452">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f64a-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f64a-453">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f64a-453">Minimum supported client</span></span><br/> | <span data-ttu-id="9f64a-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f64a-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f64a-455">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f64a-455">Minimum supported server</span></span><br/> | <span data-ttu-id="9f64a-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f64a-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f64a-457">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9f64a-457">Namespace</span></span><br/>                | <span data-ttu-id="9f64a-458">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9f64a-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f64a-459">MOF</span><span class="sxs-lookup"><span data-stu-id="9f64a-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f64a-460"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f64a-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f64a-461">DLL</span><span class="sxs-lookup"><span data-stu-id="9f64a-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f64a-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f64a-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f64a-463">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f64a-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f64a-464">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9f64a-464">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

