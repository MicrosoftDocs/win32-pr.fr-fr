---
description: La \_ classe CIM AggregatePSExtent définit le nombre de blocs logiques adressables sur un dispositif de stockage unique, à l’exception des blocs logiques mappés en tant que données de vérification.
ms.assetid: 6c188955-a963-414d-94f9-b7e1cb5960ed
ms.tgt_platform: multiple
title: Classe CIM_AggregatePSExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent
- CIM_AggregatePSExtent.Caption
- CIM_AggregatePSExtent.Description
- CIM_AggregatePSExtent.InstallDate
- CIM_AggregatePSExtent.Name
- CIM_AggregatePSExtent.Status
- CIM_AggregatePSExtent.Availability
- CIM_AggregatePSExtent.ConfigManagerErrorCode
- CIM_AggregatePSExtent.ConfigManagerUserConfig
- CIM_AggregatePSExtent.CreationClassName
- CIM_AggregatePSExtent.DeviceID
- CIM_AggregatePSExtent.PowerManagementCapabilities
- CIM_AggregatePSExtent.ErrorCleared
- CIM_AggregatePSExtent.ErrorDescription
- CIM_AggregatePSExtent.LastErrorCode
- CIM_AggregatePSExtent.PNPDeviceID
- CIM_AggregatePSExtent.PowerManagementSupported
- CIM_AggregatePSExtent.StatusInfo
- CIM_AggregatePSExtent.SystemCreationClassName
- CIM_AggregatePSExtent.SystemName
- CIM_AggregatePSExtent.Access
- CIM_AggregatePSExtent.BlockSize
- CIM_AggregatePSExtent.ErrorMethodology
- CIM_AggregatePSExtent.NumberOfBlocks
- CIM_AggregatePSExtent.Purpose
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: edc3f5b91bc39e18321778dbfdbc53446c6c27d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748717"
---
# <a name="cim_aggregatepsextent-class"></a><span data-ttu-id="39f62-103">\_Classe CIM AggregatePSExtent</span><span class="sxs-lookup"><span data-stu-id="39f62-103">CIM\_AggregatePSExtent class</span></span>

<span data-ttu-id="39f62-104">La classe **CIM \_ AggregatePSExtent** définit le nombre de blocs logiques adressables sur un dispositif de stockage unique, à l’exception des blocs logiques mappés en tant que données de vérification.</span><span class="sxs-lookup"><span data-stu-id="39f62-104">The **CIM\_AggregatePSExtent** class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="39f62-105">Si des jeux de volumes sont définis, les blocs logiques sont contenus dans un seul ensemble de volumes.</span><span class="sxs-lookup"><span data-stu-id="39f62-105">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="39f62-106">Il s’agit d’un autre regroupement pour les [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md), lorsque seules les informations de résumé sont nécessaires ou lorsque la configuration automatique est utilisée.</span><span class="sxs-lookup"><span data-stu-id="39f62-106">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

<span data-ttu-id="39f62-107">La configuration automatique peut entraîner la définition de milliers de classes [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md) .</span><span class="sxs-lookup"><span data-stu-id="39f62-107">Automatic configuration can result in thousands of [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) classes being defined.</span></span> <span data-ttu-id="39f62-108">La classe **CIM \_ AggregatePSExtent** a été définie de sorte que les extensions individuelles n’aient pas besoin d’être modélisées.</span><span class="sxs-lookup"><span data-stu-id="39f62-108">The **CIM\_AggregatePSExtent** class was defined so that individual extents would not have to be modeled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39f62-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="39f62-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39f62-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39f62-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39f62-111">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="39f62-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="39f62-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="39f62-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f62-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39f62-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D0E255C-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AggregatePSExtent : CIM_StorageExtent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  string   ErrorMethodology;
  uint64   NumberOfBlocks;
  string   Purpose;
};
```

## <a name="members"></a><span data-ttu-id="39f62-114">Membres</span><span class="sxs-lookup"><span data-stu-id="39f62-114">Members</span></span>

<span data-ttu-id="39f62-115">La classe **CIM \_ AggregatePSExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="39f62-115">The **CIM\_AggregatePSExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="39f62-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="39f62-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="39f62-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="39f62-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="39f62-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="39f62-118">Methods</span></span>

<span data-ttu-id="39f62-119">La classe **CIM \_ AggregatePSExtent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="39f62-119">The **CIM\_AggregatePSExtent** class has these methods.</span></span>



| <span data-ttu-id="39f62-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="39f62-120">Method</span></span>                                                                       | <span data-ttu-id="39f62-121">Description</span><span class="sxs-lookup"><span data-stu-id="39f62-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39f62-122">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="39f62-122">**Reset**</span></span>](reset-method-in-class-cim-aggregatepsextent.md)                 | <span data-ttu-id="39f62-123">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="39f62-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="39f62-124">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="39f62-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="39f62-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="39f62-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepsextent.md) | <span data-ttu-id="39f62-126">Définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="39f62-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="39f62-127">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="39f62-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="39f62-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="39f62-128">Properties</span></span>

<span data-ttu-id="39f62-129">La classe **CIM \_ AggregatePSExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="39f62-129">The **CIM\_AggregatePSExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39f62-130">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="39f62-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39f62-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39f62-133">Décrit les propriétés en lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="39f62-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="39f62-134">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39f62-135">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="39f62-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="39f62-136">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="39f62-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="39f62-137">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="39f62-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="39f62-138">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="39f62-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="39f62-139">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="39f62-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39f62-140">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="39f62-140">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-141">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39f62-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-143">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="39f62-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-144">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="39f62-144">Availability and status of the device.</span></span>

<span data-ttu-id="39f62-145">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-145">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39f62-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="39f62-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39f62-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="39f62-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="39f62-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="39f62-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="39f62-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="39f62-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="39f62-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="39f62-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="39f62-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="39f62-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="39f62-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="39f62-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="39f62-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="39f62-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="39f62-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="39f62-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="39f62-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="39f62-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="39f62-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="39f62-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="39f62-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="39f62-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="39f62-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="39f62-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-159">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="39f62-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="39f62-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="39f62-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-161">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="39f62-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="39f62-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="39f62-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-163">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="39f62-163">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="39f62-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="39f62-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="39f62-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="39f62-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-166">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="39f62-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="39f62-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="39f62-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-168">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="39f62-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="39f62-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="39f62-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-170">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="39f62-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="39f62-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="39f62-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-172">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="39f62-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="39f62-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="39f62-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-174">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="39f62-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39f62-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="39f62-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-176">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="39f62-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-178">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="39f62-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-179">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="39f62-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="39f62-180">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="39f62-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="39f62-181">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="39f62-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="39f62-182">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="39f62-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="39f62-183">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-183">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="39f62-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-187">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="39f62-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-188">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="39f62-188">A short textual description of the object.</span></span>

<span data-ttu-id="39f62-189">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="39f62-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-191">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39f62-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-193">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="39f62-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-194">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="39f62-194">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="39f62-195">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="39f62-196">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="39f62-196">**This device is working properly.**</span></span> <span data-ttu-id="39f62-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="39f62-197">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="39f62-198">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="39f62-198">**This device is not configured correctly.**</span></span> <span data-ttu-id="39f62-199">(1)</span><span class="sxs-lookup"><span data-stu-id="39f62-199">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39f62-200">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-200">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="39f62-201">(2)</span><span class="sxs-lookup"><span data-stu-id="39f62-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="39f62-202">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="39f62-202">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="39f62-203">(3)</span><span class="sxs-lookup"><span data-stu-id="39f62-203">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="39f62-204">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="39f62-204">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="39f62-205">(4)</span><span class="sxs-lookup"><span data-stu-id="39f62-205">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="39f62-206">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="39f62-206">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="39f62-207">(5)</span><span class="sxs-lookup"><span data-stu-id="39f62-207">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="39f62-208">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="39f62-208">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="39f62-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="39f62-209">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="39f62-210">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="39f62-210">**Cannot filter.**</span></span> <span data-ttu-id="39f62-211">(7)</span><span class="sxs-lookup"><span data-stu-id="39f62-211">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="39f62-212">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="39f62-212">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="39f62-213">(8)</span><span class="sxs-lookup"><span data-stu-id="39f62-213">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="39f62-214">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-214">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="39f62-215">(9)</span><span class="sxs-lookup"><span data-stu-id="39f62-215">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="39f62-216">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-216">**This device cannot start.**</span></span> <span data-ttu-id="39f62-217">(10)</span><span class="sxs-lookup"><span data-stu-id="39f62-217">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="39f62-218">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-218">**This device failed.**</span></span> <span data-ttu-id="39f62-219">(11)</span><span class="sxs-lookup"><span data-stu-id="39f62-219">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="39f62-220">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="39f62-220">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="39f62-221">douze</span><span class="sxs-lookup"><span data-stu-id="39f62-221">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="39f62-222">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-222">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="39f62-223">(13)</span><span class="sxs-lookup"><span data-stu-id="39f62-223">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="39f62-224">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="39f62-224">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="39f62-225">(14)</span><span class="sxs-lookup"><span data-stu-id="39f62-225">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="39f62-226">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="39f62-226">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="39f62-227">(15)</span><span class="sxs-lookup"><span data-stu-id="39f62-227">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="39f62-228">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-228">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="39f62-229">(16)</span><span class="sxs-lookup"><span data-stu-id="39f62-229">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="39f62-230">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="39f62-230">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="39f62-231">(17)</span><span class="sxs-lookup"><span data-stu-id="39f62-231">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39f62-232">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-232">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="39f62-233">(18)</span><span class="sxs-lookup"><span data-stu-id="39f62-233">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="39f62-234">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="39f62-234">**Failure using the VxD loader.**</span></span> <span data-ttu-id="39f62-235">(19)</span><span class="sxs-lookup"><span data-stu-id="39f62-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="39f62-236">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="39f62-236">**Your registry might be corrupted.**</span></span> <span data-ttu-id="39f62-237">(20)</span><span class="sxs-lookup"><span data-stu-id="39f62-237">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="39f62-238">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-238">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="39f62-239">(21)</span><span class="sxs-lookup"><span data-stu-id="39f62-239">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="39f62-240">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="39f62-240">**This device is disabled.**</span></span> <span data-ttu-id="39f62-241">(22)</span><span class="sxs-lookup"><span data-stu-id="39f62-241">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="39f62-242">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="39f62-242">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="39f62-243">(23)</span><span class="sxs-lookup"><span data-stu-id="39f62-243">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="39f62-244">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="39f62-244">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="39f62-245">(24)</span><span class="sxs-lookup"><span data-stu-id="39f62-245">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="39f62-246">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="39f62-247">(25)</span><span class="sxs-lookup"><span data-stu-id="39f62-247">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="39f62-248">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-248">**Windows is still setting up this device.**</span></span> <span data-ttu-id="39f62-249">(26)</span><span class="sxs-lookup"><span data-stu-id="39f62-249">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="39f62-250">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="39f62-250">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="39f62-251">(27)</span><span class="sxs-lookup"><span data-stu-id="39f62-251">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="39f62-252">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="39f62-252">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="39f62-253">(28)</span><span class="sxs-lookup"><span data-stu-id="39f62-253">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="39f62-254">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="39f62-254">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="39f62-255">(29)</span><span class="sxs-lookup"><span data-stu-id="39f62-255">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="39f62-256">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="39f62-256">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="39f62-257">(30)</span><span class="sxs-lookup"><span data-stu-id="39f62-257">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39f62-258">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="39f62-258">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="39f62-259">31</span><span class="sxs-lookup"><span data-stu-id="39f62-259">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39f62-260">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="39f62-260">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-261">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="39f62-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-263">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="39f62-263">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-264">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39f62-264">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="39f62-265">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-266">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39f62-266">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-269">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39f62-269">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39f62-270">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="39f62-270">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="39f62-271">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="39f62-271">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="39f62-272">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-273">**Description**</span><span class="sxs-lookup"><span data-stu-id="39f62-273">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-276">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="39f62-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-277">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="39f62-277">A textual description of the object.</span></span>

<span data-ttu-id="39f62-278">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-278">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-279">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="39f62-279">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-282">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39f62-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39f62-283">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="39f62-283">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="39f62-284">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-285">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="39f62-285">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-286">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="39f62-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39f62-288">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="39f62-288">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="39f62-289">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-290">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="39f62-290">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-291">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39f62-293">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="39f62-293">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="39f62-294">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-295">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="39f62-295">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39f62-298">Chaîne de forme libre qui décrit le type de détection d’erreurs et de correction pris en charge par l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="39f62-298">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="39f62-299">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-299">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="39f62-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-301">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="39f62-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-303">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="39f62-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-304">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="39f62-304">Indicates when the object was installed.</span></span> <span data-ttu-id="39f62-305">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="39f62-305">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="39f62-306">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-307">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="39f62-307">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-308">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39f62-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39f62-310">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="39f62-310">Last error code reported by the logical device.</span></span>

<span data-ttu-id="39f62-311">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-312">**Nom**</span><span class="sxs-lookup"><span data-stu-id="39f62-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-315">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="39f62-315">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-316">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="39f62-316">Label by which the object is known.</span></span> <span data-ttu-id="39f62-317">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="39f62-317">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="39f62-318">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-319">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="39f62-319">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-320">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="39f62-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-322">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="39f62-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-323">Nombre de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="39f62-323">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="39f62-324">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="39f62-324">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="39f62-325">Si la valeur de **BlockSize** est 1 (un), cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="39f62-325">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="39f62-326">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="39f62-326">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="39f62-327">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-327">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-328">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="39f62-328">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-331">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="39f62-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-332">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="39f62-332">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="39f62-333">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="39f62-333">Example: "\*PNP030b"</span></span>

<span data-ttu-id="39f62-334">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="39f62-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-336">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39f62-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39f62-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39f62-338">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="39f62-338">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="39f62-339">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39f62-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="39f62-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-341">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="39f62-341">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="39f62-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="39f62-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-343">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="39f62-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="39f62-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="39f62-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-345">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="39f62-345">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="39f62-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="39f62-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-347">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="39f62-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="39f62-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="39f62-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-349">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="39f62-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="39f62-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="39f62-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-351">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="39f62-351">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="39f62-352">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="39f62-352">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="39f62-353">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="39f62-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="39f62-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="39f62-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-355">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="39f62-355">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="39f62-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="39f62-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="39f62-357">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="39f62-357">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39f62-358">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="39f62-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-359">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="39f62-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39f62-361">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="39f62-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="39f62-362">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="39f62-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="39f62-363">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="39f62-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="39f62-364">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="39f62-364">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="39f62-365">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-366">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="39f62-366">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39f62-369">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="39f62-369">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="39f62-370">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-370">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-371">**État**</span><span class="sxs-lookup"><span data-stu-id="39f62-371">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-372">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-374">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="39f62-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-375">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="39f62-375">String that indicates the current status of the object.</span></span> <span data-ttu-id="39f62-376">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="39f62-376">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="39f62-377">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="39f62-377">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="39f62-378">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="39f62-378">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="39f62-379">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="39f62-379">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="39f62-380">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="39f62-380">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="39f62-381">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="39f62-381">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="39f62-382">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-382">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="39f62-383">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="39f62-383">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="39f62-384">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="39f62-384">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="39f62-385">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="39f62-385">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="39f62-386">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="39f62-386">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39f62-387">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="39f62-387">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="39f62-388">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="39f62-388">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="39f62-389">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="39f62-389">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="39f62-390">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="39f62-390">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="39f62-391">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="39f62-391">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="39f62-392">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="39f62-392">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="39f62-393">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="39f62-393">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="39f62-394">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="39f62-394">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="39f62-395">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="39f62-395">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39f62-396">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="39f62-396">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-397">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39f62-397">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-399">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="39f62-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="39f62-400">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="39f62-400">State of the logical device.</span></span> <span data-ttu-id="39f62-401">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="39f62-401">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="39f62-402">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39f62-403">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="39f62-403">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39f62-404">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="39f62-404">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="39f62-405">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="39f62-405">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="39f62-406">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="39f62-406">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="39f62-407">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="39f62-407">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39f62-408">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39f62-408">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-409">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-411">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39f62-411">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39f62-412">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="39f62-412">The scoping system's creation class name.</span></span>

<span data-ttu-id="39f62-413">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39f62-414">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="39f62-414">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f62-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39f62-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39f62-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39f62-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f62-417">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39f62-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39f62-418">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="39f62-418">The scoping system's name.</span></span>

<span data-ttu-id="39f62-419">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39f62-420">Notes</span><span class="sxs-lookup"><span data-stu-id="39f62-420">Remarks</span></span>

<span data-ttu-id="39f62-421">La classe **CIM \_ AggregatePSExtent** est dérivée de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="39f62-421">The **CIM\_AggregatePSExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="39f62-422">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="39f62-422">WMI does not implement this class.</span></span>

<span data-ttu-id="39f62-423">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="39f62-423">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39f62-424">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="39f62-424">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f62-425">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39f62-425">Requirements</span></span>



| <span data-ttu-id="39f62-426">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39f62-426">Requirement</span></span> | <span data-ttu-id="39f62-427">Valeur</span><span class="sxs-lookup"><span data-stu-id="39f62-427">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39f62-428">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39f62-428">Minimum supported client</span></span><br/> | <span data-ttu-id="39f62-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39f62-429">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39f62-430">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39f62-430">Minimum supported server</span></span><br/> | <span data-ttu-id="39f62-431">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39f62-431">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39f62-432">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="39f62-432">Namespace</span></span><br/>                | <span data-ttu-id="39f62-433">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="39f62-433">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39f62-434">MOF</span><span class="sxs-lookup"><span data-stu-id="39f62-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39f62-435"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39f62-435"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39f62-436">DLL</span><span class="sxs-lookup"><span data-stu-id="39f62-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39f62-437"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39f62-437"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f62-438">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39f62-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f62-439">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="39f62-439">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="39f62-440">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="39f62-440">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

