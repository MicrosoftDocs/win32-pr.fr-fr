---
description: La \_ classe CIM AggregatePExtent fournit des informations récapitulatives sur les blocs logiques adressables, qui se trouvent dans le même groupe de redondance de stockage et qui se trouvent sur le même support physique.
ms.assetid: c8def347-e8d7-48d5-94d0-f6e704e7b40e
ms.tgt_platform: multiple
title: Classe CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent
- CIM_AggregatePExtent.Caption
- CIM_AggregatePExtent.Description
- CIM_AggregatePExtent.InstallDate
- CIM_AggregatePExtent.Name
- CIM_AggregatePExtent.Status
- CIM_AggregatePExtent.Availability
- CIM_AggregatePExtent.ConfigManagerErrorCode
- CIM_AggregatePExtent.ConfigManagerUserConfig
- CIM_AggregatePExtent.CreationClassName
- CIM_AggregatePExtent.DeviceID
- CIM_AggregatePExtent.PowerManagementCapabilities
- CIM_AggregatePExtent.ErrorCleared
- CIM_AggregatePExtent.ErrorDescription
- CIM_AggregatePExtent.LastErrorCode
- CIM_AggregatePExtent.PNPDeviceID
- CIM_AggregatePExtent.PowerManagementSupported
- CIM_AggregatePExtent.StatusInfo
- CIM_AggregatePExtent.SystemCreationClassName
- CIM_AggregatePExtent.SystemName
- CIM_AggregatePExtent.Access
- CIM_AggregatePExtent.BlockSize
- CIM_AggregatePExtent.ErrorMethodology
- CIM_AggregatePExtent.Purpose
- CIM_AggregatePExtent.NumberOfBlocks
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2f1b2b5b7e08876317888d02d4830cd72659bc0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523903"
---
# <a name="cim_aggregatepextent-class"></a><span data-ttu-id="d025d-103">\_Classe CIM AggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="d025d-103">CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="d025d-104">La classe **CIM \_ AggregatePExtent** fournit des informations récapitulatives sur les blocs logiques adressables, qui se trouvent dans le même groupe de redondance de stockage et qui se trouvent sur le même support physique.</span><span class="sxs-lookup"><span data-stu-id="d025d-104">The **CIM\_AggregatePExtent** class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

<span data-ttu-id="d025d-105">La **classe \_ AggregatePExtent CIM** est un regroupement alternatif pour les extensions physiques lorsque seules des informations de synthèse sont nécessaires ou lorsque la configuration automatique est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d025d-105">The **CIM\_AggregatePExtent** class is an alternative grouping for physical extents when only summary information is needed, or when automatic configuration is used.</span></span> <span data-ttu-id="d025d-106">La configuration automatique peut entraîner la définition de milliers d’extensions physiques.</span><span class="sxs-lookup"><span data-stu-id="d025d-106">Automatic configuration can result in thousands of physical extents being defined.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d025d-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d025d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d025d-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d025d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d025d-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d025d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d025d-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d025d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d025d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d025d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979F-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AggregatePExtent : CIM_StorageExtent
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
  string   Purpose;
  uint64   NumberOfBlocks;
};
```

## <a name="members"></a><span data-ttu-id="d025d-112">Membres</span><span class="sxs-lookup"><span data-stu-id="d025d-112">Members</span></span>

<span data-ttu-id="d025d-113">La classe **CIM \_ AggregatePExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d025d-113">The **CIM\_AggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="d025d-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d025d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d025d-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d025d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d025d-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d025d-116">Methods</span></span>

<span data-ttu-id="d025d-117">La classe **CIM \_ AggregatePExtent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d025d-117">The **CIM\_AggregatePExtent** class has these methods.</span></span>



| <span data-ttu-id="d025d-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="d025d-118">Method</span></span>                                                                      | <span data-ttu-id="d025d-119">Description</span><span class="sxs-lookup"><span data-stu-id="d025d-119">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d025d-120">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="d025d-120">**Reset**</span></span>](reset-method-in-class-cim-aggregatepextent.md)                 | <span data-ttu-id="d025d-121">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d025d-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="d025d-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="d025d-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="d025d-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d025d-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md) | <span data-ttu-id="d025d-124">Définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="d025d-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="d025d-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="d025d-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d025d-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d025d-126">Properties</span></span>

<span data-ttu-id="d025d-127">La classe **CIM \_ AggregatePExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d025d-127">The **CIM\_AggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d025d-128">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="d025d-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d025d-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d025d-131">Décrit les propriétés en lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="d025d-131">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="d025d-132">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d025d-133">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d025d-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="d025d-134">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="d025d-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="d025d-135">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="d025d-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="d025d-136">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="d025d-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="d025d-137">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="d025d-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d025d-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="d025d-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d025d-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-141">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d025d-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-142">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d025d-142">Availability and status of the device.</span></span>

<span data-ttu-id="d025d-143">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d025d-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d025d-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d025d-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d025d-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d025d-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="d025d-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d025d-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="d025d-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d025d-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="d025d-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d025d-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d025d-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d025d-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="d025d-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d025d-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="d025d-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d025d-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="d025d-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d025d-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="d025d-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d025d-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="d025d-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d025d-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="d025d-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d025d-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="d025d-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-157">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d025d-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d025d-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="d025d-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-159">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="d025d-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d025d-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="d025d-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-161">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="d025d-161">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d025d-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="d025d-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d025d-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="d025d-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-164">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d025d-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d025d-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="d025d-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-166">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="d025d-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d025d-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="d025d-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-168">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="d025d-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d025d-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="d025d-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-170">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="d025d-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d025d-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="d025d-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-172">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="d025d-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d025d-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="d025d-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-174">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d025d-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-176">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="d025d-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-177">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="d025d-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="d025d-178">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d025d-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="d025d-179">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="d025d-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="d025d-180">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d025d-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d025d-181">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d025d-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-185">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d025d-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-186">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d025d-186">A short textual description of the object.</span></span>

<span data-ttu-id="d025d-187">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d025d-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-189">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d025d-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-191">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d025d-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-192">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="d025d-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d025d-193">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d025d-194">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="d025d-194">**This device is working properly.**</span></span> <span data-ttu-id="d025d-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="d025d-195">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d025d-196">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="d025d-196">**This device is not configured correctly.**</span></span> <span data-ttu-id="d025d-197">(1)</span><span class="sxs-lookup"><span data-stu-id="d025d-197">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d025d-198">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-198">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d025d-199">(2)</span><span class="sxs-lookup"><span data-stu-id="d025d-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d025d-200">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="d025d-200">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d025d-201">(3)</span><span class="sxs-lookup"><span data-stu-id="d025d-201">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d025d-202">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="d025d-202">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d025d-203">(4)</span><span class="sxs-lookup"><span data-stu-id="d025d-203">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d025d-204">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="d025d-204">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d025d-205">(5)</span><span class="sxs-lookup"><span data-stu-id="d025d-205">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d025d-206">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="d025d-206">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d025d-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="d025d-207">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d025d-208">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="d025d-208">**Cannot filter.**</span></span> <span data-ttu-id="d025d-209">(7)</span><span class="sxs-lookup"><span data-stu-id="d025d-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d025d-210">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="d025d-210">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d025d-211">(8)</span><span class="sxs-lookup"><span data-stu-id="d025d-211">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d025d-212">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-212">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d025d-213">(9)</span><span class="sxs-lookup"><span data-stu-id="d025d-213">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d025d-214">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-214">**This device cannot start.**</span></span> <span data-ttu-id="d025d-215">(10)</span><span class="sxs-lookup"><span data-stu-id="d025d-215">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d025d-216">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-216">**This device failed.**</span></span> <span data-ttu-id="d025d-217">(11)</span><span class="sxs-lookup"><span data-stu-id="d025d-217">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d025d-218">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="d025d-218">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d025d-219">douze</span><span class="sxs-lookup"><span data-stu-id="d025d-219">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d025d-220">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-220">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d025d-221">(13)</span><span class="sxs-lookup"><span data-stu-id="d025d-221">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d025d-222">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="d025d-222">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d025d-223">(14)</span><span class="sxs-lookup"><span data-stu-id="d025d-223">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d025d-224">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="d025d-224">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d025d-225">(15)</span><span class="sxs-lookup"><span data-stu-id="d025d-225">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d025d-226">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-226">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d025d-227">(16)</span><span class="sxs-lookup"><span data-stu-id="d025d-227">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d025d-228">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="d025d-228">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d025d-229">(17)</span><span class="sxs-lookup"><span data-stu-id="d025d-229">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d025d-230">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-230">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d025d-231">(18)</span><span class="sxs-lookup"><span data-stu-id="d025d-231">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d025d-232">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="d025d-232">**Failure using the VxD loader.**</span></span> <span data-ttu-id="d025d-233">(19)</span><span class="sxs-lookup"><span data-stu-id="d025d-233">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d025d-234">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="d025d-234">**Your registry might be corrupted.**</span></span> <span data-ttu-id="d025d-235">(20)</span><span class="sxs-lookup"><span data-stu-id="d025d-235">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d025d-236">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-236">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d025d-237">(21)</span><span class="sxs-lookup"><span data-stu-id="d025d-237">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d025d-238">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="d025d-238">**This device is disabled.**</span></span> <span data-ttu-id="d025d-239">(22)</span><span class="sxs-lookup"><span data-stu-id="d025d-239">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d025d-240">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="d025d-240">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d025d-241">(23)</span><span class="sxs-lookup"><span data-stu-id="d025d-241">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d025d-242">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="d025d-242">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d025d-243">(24)</span><span class="sxs-lookup"><span data-stu-id="d025d-243">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d025d-244">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-244">**Windows is still setting up this device.**</span></span> <span data-ttu-id="d025d-245">(25)</span><span class="sxs-lookup"><span data-stu-id="d025d-245">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d025d-246">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="d025d-247">(26)</span><span class="sxs-lookup"><span data-stu-id="d025d-247">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d025d-248">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="d025d-248">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d025d-249">(27)</span><span class="sxs-lookup"><span data-stu-id="d025d-249">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d025d-250">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="d025d-250">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d025d-251">(28)</span><span class="sxs-lookup"><span data-stu-id="d025d-251">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d025d-252">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="d025d-252">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d025d-253">(29)</span><span class="sxs-lookup"><span data-stu-id="d025d-253">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d025d-254">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="d025d-254">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d025d-255">(30)</span><span class="sxs-lookup"><span data-stu-id="d025d-255">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d025d-256">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d025d-256">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d025d-257">31</span><span class="sxs-lookup"><span data-stu-id="d025d-257">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d025d-258">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d025d-258">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-259">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d025d-259">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-261">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d025d-261">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-262">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d025d-262">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d025d-263">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-263">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-264">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d025d-264">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-265">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-267">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d025d-267">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d025d-268">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d025d-268">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d025d-269">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="d025d-269">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d025d-270">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-271">**Description**</span><span class="sxs-lookup"><span data-stu-id="d025d-271">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-274">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d025d-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-275">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d025d-275">A textual description of the object.</span></span>

<span data-ttu-id="d025d-276">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-277">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d025d-277">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-280">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d025d-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d025d-281">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d025d-281">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="d025d-282">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-283">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d025d-283">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-284">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d025d-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d025d-286">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="d025d-286">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="d025d-287">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-288">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d025d-288">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d025d-291">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="d025d-291">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="d025d-292">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-293">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="d025d-293">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d025d-296">Chaîne de forme libre qui décrit le type de détection d’erreurs et de correction pris en charge par l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="d025d-296">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="d025d-297">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-297">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d025d-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-299">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d025d-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-301">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d025d-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-302">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="d025d-302">Indicates when the object was installed.</span></span> <span data-ttu-id="d025d-303">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="d025d-303">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d025d-304">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-305">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d025d-305">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-306">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d025d-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d025d-308">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d025d-308">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d025d-309">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-310">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d025d-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-311">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-313">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d025d-313">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-314">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d025d-314">Label by which the object is known.</span></span> <span data-ttu-id="d025d-315">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="d025d-315">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d025d-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-317">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="d025d-317">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-318">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d025d-318">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-320">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Étendue physique cumulée DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="d025d-320">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Aggregate Physical Extent\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-321">Nombre total de blocs (y compris les blocs de données de vérification) contenus dans cette étendue physique d’agrégat.</span><span class="sxs-lookup"><span data-stu-id="d025d-321">Total number of blocks (including the check data blocks) contained in this aggregate physical extent.</span></span> <span data-ttu-id="d025d-322">La taille de bloc (propriété héritée) doit être définie sur la même valeur que pour l’appareil d’accès aux médias associé à cette extension.</span><span class="sxs-lookup"><span data-stu-id="d025d-322">The block size (an inherited property) should be set to the same value as for the media access device associated with this extent.</span></span>

</dd> <dt>

<span data-ttu-id="d025d-323">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d025d-323">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-326">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d025d-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-327">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="d025d-327">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d025d-328">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="d025d-328">Example: "\*PNP030b"</span></span>

<span data-ttu-id="d025d-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-330">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d025d-330">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-331">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d025d-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d025d-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d025d-333">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="d025d-333">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="d025d-334">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d025d-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d025d-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-336">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="d025d-336">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d025d-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="d025d-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-338">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="d025d-338">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d025d-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="d025d-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-340">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="d025d-340">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d025d-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="d025d-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-342">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="d025d-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d025d-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="d025d-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-344">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="d025d-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d025d-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="d025d-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-346">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d025d-346">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="d025d-347">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="d025d-347">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="d025d-348">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d025d-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d025d-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="d025d-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-350">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="d025d-350">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d025d-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="d025d-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d025d-352">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="d025d-352">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d025d-353">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d025d-353">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-354">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d025d-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d025d-356">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d025d-356">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="d025d-357">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d025d-357">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d025d-358">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d025d-358">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="d025d-359">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d025d-359">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d025d-360">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-361">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="d025d-361">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-362">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d025d-364">Chaîne de forme libre qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="d025d-364">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="d025d-365">Cette propriété est héritée de la [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-365">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-366">**État**</span><span class="sxs-lookup"><span data-stu-id="d025d-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-369">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d025d-369">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-370">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d025d-370">String that indicates the current status of the object.</span></span> <span data-ttu-id="d025d-371">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="d025d-371">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d025d-372">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="d025d-372">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d025d-373">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="d025d-373">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d025d-374">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="d025d-374">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d025d-375">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="d025d-375">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d025d-376">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="d025d-376">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d025d-377">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-377">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d025d-378">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d025d-378">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d025d-379">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d025d-379">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d025d-380">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d025d-380">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d025d-381">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d025d-381">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d025d-382">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d025d-382">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d025d-383">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d025d-383">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d025d-384">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d025d-384">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d025d-385">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d025d-385">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d025d-386">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d025d-386">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d025d-387">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d025d-387">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d025d-388">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d025d-388">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d025d-389">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d025d-389">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d025d-390">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d025d-390">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d025d-391">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d025d-391">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-392">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d025d-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-394">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d025d-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d025d-395">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d025d-395">State of the logical device.</span></span> <span data-ttu-id="d025d-396">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d025d-396">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="d025d-397">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d025d-398">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d025d-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d025d-399">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d025d-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d025d-400">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="d025d-400">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d025d-401">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="d025d-401">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d025d-402">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d025d-402">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d025d-403">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d025d-403">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-404">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-406">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d025d-406">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d025d-407">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d025d-407">The scoping system's creation class name.</span></span>

<span data-ttu-id="d025d-408">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d025d-409">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d025d-409">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d025d-410">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d025d-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d025d-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d025d-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d025d-412">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d025d-412">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d025d-413">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d025d-413">The scoping system's name.</span></span>

<span data-ttu-id="d025d-414">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d025d-415">Notes</span><span class="sxs-lookup"><span data-stu-id="d025d-415">Remarks</span></span>

<span data-ttu-id="d025d-416">La classe **CIM \_ AggregatePExtent** est dérivée de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d025d-416">The **CIM\_AggregatePExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d025d-417">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d025d-417">WMI does not implement this class.</span></span>

<span data-ttu-id="d025d-418">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d025d-418">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d025d-419">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d025d-419">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d025d-420">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d025d-420">Requirements</span></span>



| <span data-ttu-id="d025d-421">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d025d-421">Requirement</span></span> | <span data-ttu-id="d025d-422">Valeur</span><span class="sxs-lookup"><span data-stu-id="d025d-422">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d025d-423">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d025d-423">Minimum supported client</span></span><br/> | <span data-ttu-id="d025d-424">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d025d-424">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d025d-425">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d025d-425">Minimum supported server</span></span><br/> | <span data-ttu-id="d025d-426">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d025d-426">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d025d-427">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d025d-427">Namespace</span></span><br/>                | <span data-ttu-id="d025d-428">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d025d-428">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d025d-429">MOF</span><span class="sxs-lookup"><span data-stu-id="d025d-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d025d-430"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d025d-430"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d025d-431">DLL</span><span class="sxs-lookup"><span data-stu-id="d025d-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d025d-432"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d025d-432"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d025d-433">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d025d-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d025d-434">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d025d-434">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="d025d-435">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="d025d-435">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

