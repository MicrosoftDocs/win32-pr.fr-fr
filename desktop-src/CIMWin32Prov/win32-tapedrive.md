---
description: La \_ classe WMI de l’ordinateur Win32 représente un lecteur de bande sur un système informatique exécutant Windows. Les lecteurs de bande sont principalement distingués par le fait qu’ils ne peuvent être accessibles que de manière séquentielle.
ms.assetid: ceefec7b-a904-4b2f-a6b6-b84917a33023
ms.tgt_platform: multiple
title: Classe Win32_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TapeDrive
- Win32_TapeDrive.Reset
- Win32_TapeDrive.SetPowerState
- Win32_TapeDrive.Availability
- Win32_TapeDrive.Capabilities
- Win32_TapeDrive.CapabilityDescriptions
- Win32_TapeDrive.Caption
- Win32_TapeDrive.Compression
- Win32_TapeDrive.CompressionMethod
- Win32_TapeDrive.ConfigManagerErrorCode
- Win32_TapeDrive.ConfigManagerUserConfig
- Win32_TapeDrive.CreationClassName
- Win32_TapeDrive.DefaultBlockSize
- Win32_TapeDrive.Description
- Win32_TapeDrive.DeviceID
- Win32_TapeDrive.ECC
- Win32_TapeDrive.EOTWarningZoneSize
- Win32_TapeDrive.ErrorCleared
- Win32_TapeDrive.ErrorDescription
- Win32_TapeDrive.ErrorMethodology
- Win32_TapeDrive.FeaturesHigh
- Win32_TapeDrive.FeaturesLow
- Win32_TapeDrive.Id
- Win32_TapeDrive.InstallDate
- Win32_TapeDrive.LastErrorCode
- Win32_TapeDrive.Manufacturer
- Win32_TapeDrive.MaxBlockSize
- Win32_TapeDrive.MaxMediaSize
- Win32_TapeDrive.MaxPartitionCount
- Win32_TapeDrive.MediaType
- Win32_TapeDrive.MinBlockSize
- Win32_TapeDrive.Name
- Win32_TapeDrive.NeedsCleaning
- Win32_TapeDrive.NumberOfMediaSupported
- Win32_TapeDrive.Padding
- Win32_TapeDrive.PNPDeviceID
- Win32_TapeDrive.PowerManagementCapabilities
- Win32_TapeDrive.PowerManagementSupported
- Win32_TapeDrive.ReportSetMarks
- Win32_TapeDrive.Status
- Win32_TapeDrive.StatusInfo
- Win32_TapeDrive.SystemCreationClassName
- Win32_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c7e7d3b754a0399acb152dba043da269f67a06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517404"
---
# <a name="win32_tapedrive-class"></a><span data-ttu-id="c3a10-104">Classe Win32 de la \_ classe</span><span class="sxs-lookup"><span data-stu-id="c3a10-104">Win32\_TapeDrive class</span></span>

<span data-ttu-id="c3a10-105">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’ordinateur **Win32 \_** représente un lecteur de bande sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="c3a10-105">The **Win32\_TapeDrive** [WMI class](../wmisdk/retrieving-a-class.md) represents a tape drive on a computer system running Windows.</span></span> <span data-ttu-id="c3a10-106">Les lecteurs de bande sont principalement distingués par le fait qu’ils ne peuvent être accessibles que de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="c3a10-106">Tape drives are primarily distinguished by the fact that they can only be accessed sequentially.</span></span>

<span data-ttu-id="c3a10-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c3a10-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c3a10-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c3a10-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a10-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3a10-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TapeDrive : CIM_TapeDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   Compression;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   ECC;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   FeaturesHigh;
  uint32   FeaturesLow;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  string   MediaType;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ReportSetMarks;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="c3a10-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c3a10-110">Members</span></span>

<span data-ttu-id="c3a10-111">La **classe \_ Win32** de la classe a ces types de membres :</span><span class="sxs-lookup"><span data-stu-id="c3a10-111">The **Win32\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="c3a10-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c3a10-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c3a10-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3a10-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c3a10-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c3a10-114">Methods</span></span>

<span data-ttu-id="c3a10-115">La **classe \_ Win32** de la classe a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c3a10-115">The **Win32\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="c3a10-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="c3a10-116">Method</span></span>            | <span data-ttu-id="c3a10-117">Description</span><span class="sxs-lookup"><span data-stu-id="c3a10-117">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a10-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="c3a10-118">**Reset**</span></span>         | <span data-ttu-id="c3a10-119">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="c3a10-119">Not implemented.</span></span> <span data-ttu-id="c3a10-120">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/>                 |
| <span data-ttu-id="c3a10-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c3a10-121">**SetPowerState**</span></span> | <span data-ttu-id="c3a10-122">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="c3a10-122">Not implemented.</span></span> <span data-ttu-id="c3a10-123">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c3a10-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3a10-124">Properties</span></span>

<span data-ttu-id="c3a10-125">La **classe \_ Win32** de la classe a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c3a10-125">The **Win32\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3a10-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="c3a10-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3a10-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-129">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c3a10-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-130">Availability and status of the device.</span></span>

<span data-ttu-id="c3a10-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c3a10-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c3a10-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3a10-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="c3a10-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c3a10-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="c3a10-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-135">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="c3a10-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c3a10-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="c3a10-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c3a10-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="c3a10-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c3a10-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="c3a10-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c3a10-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="c3a10-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c3a10-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="c3a10-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c3a10-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="c3a10-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c3a10-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="c3a10-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c3a10-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="c3a10-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c3a10-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="c3a10-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c3a10-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="c3a10-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-146">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="c3a10-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c3a10-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="c3a10-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-148">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="c3a10-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c3a10-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="c3a10-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-150">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="c3a10-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c3a10-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="c3a10-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c3a10-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="c3a10-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-153">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="c3a10-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c3a10-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="c3a10-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-155">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="c3a10-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c3a10-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="c3a10-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-157">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="c3a10-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c3a10-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="c3a10-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-159">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="c3a10-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c3a10-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="c3a10-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-161">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="c3a10-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c3a10-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-163">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3a10-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-165">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="c3a10-165">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-166">Tableau de fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="c3a10-166">Array of capabilities of the media access device.</span></span> <span data-ttu-id="c3a10-167">Par exemple, l’appareil peut prendre en charge l’accès aléatoire, le support amovible et le nettoyage automatique.</span><span class="sxs-lookup"><span data-stu-id="c3a10-167">For example, the device may support Random Access, removable media and Automatic Cleaning.</span></span> <span data-ttu-id="c3a10-168">Dans ce cas, les valeurs 3, 7 et 9 sont écrites dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="c3a10-168">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="c3a10-169">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3a10-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3a10-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c3a10-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c3a10-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="c3a10-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="c3a10-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="c3a10-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="c3a10-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="c3a10-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="c3a10-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="c3a10-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="c3a10-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="c3a10-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="c3a10-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="c3a10-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="c3a10-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-178">Prend en charge les supports amovibles</span><span class="sxs-lookup"><span data-stu-id="c3a10-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="c3a10-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="c3a10-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="c3a10-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="c3a10-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="c3a10-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="c3a10-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="c3a10-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="c3a10-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-183">Prend en charge Dual-Sided support</span><span class="sxs-lookup"><span data-stu-id="c3a10-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="c3a10-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="c3a10-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c3a10-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-186">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c3a10-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-188">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="c3a10-188">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-189">Tableau de chaînes de forme libre fournissant des explications plus détaillées sur les fonctionnalités de l’appareil Access indiquées dans le tableau **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="c3a10-189">Array of free-form strings providing more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="c3a10-190">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="c3a10-190">Note that each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="c3a10-191">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-191">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c3a10-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-195">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-195">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-196">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3a10-196">Short description of the object.</span></span>

<span data-ttu-id="c3a10-197">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-198">**Compression**</span><span class="sxs-lookup"><span data-stu-id="c3a10-198">**Compression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-199">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-201">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("structures de sauvegarde sur bande win32api structure de la bande d’accès aux \| \| [**\_ \_ \_ paramètres de lecteur**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| compression")</span><span class="sxs-lookup"><span data-stu-id="c3a10-201">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|Compression")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-202">Si la **valeur est true**, la compression des données matérielles est activée.</span><span class="sxs-lookup"><span data-stu-id="c3a10-202">If **TRUE**, hardware data compression is enabled.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c3a10-203"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="c3a10-203"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-204">FALSE</span><span class="sxs-lookup"><span data-stu-id="c3a10-204">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c3a10-205"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c3a10-205"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-206">TRUE</span><span class="sxs-lookup"><span data-stu-id="c3a10-206">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="c3a10-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-210">Chaîne de forme libre indiquant l’algorithme ou l’outil utilisé par l’appareil pour prendre en charge la compression.</span><span class="sxs-lookup"><span data-stu-id="c3a10-210">Free-form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="c3a10-211">S’il n’est pas possible de décrire le schéma de compression (peut-être parce qu’il n’est pas connu), utilisez les mots suivants : « inconnu » pour indiquer qu’il n’est pas connu que l’appareil prend en charge les fonctionnalités de compression. « Compressed » pour représenter que l’appareil prend en charge les fonctionnalités de compression, mais que son schéma de compression n’est pas connu ou n’est pas divulgué ; et « non compressés » pour représenter que l’appareil ne prend pas en charge les fonctionnalités de compression.</span><span class="sxs-lookup"><span data-stu-id="c3a10-211">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="c3a10-212">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-212">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="c3a10-213">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="c3a10-213">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-214">Le schéma de compression est inconnu ou non décrit.</span><span class="sxs-lookup"><span data-stu-id="c3a10-214">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="c3a10-215">(« Compressé »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-215">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-216">Le fichier logique est compressé, mais le schéma de compression est inconnu ou n’est pas décrit.</span><span class="sxs-lookup"><span data-stu-id="c3a10-216">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="c3a10-217">(« Non compressé »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-217">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-218">Si le fichier logique n’est pas compressé</span><span class="sxs-lookup"><span data-stu-id="c3a10-218">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c3a10-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-220">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-222">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c3a10-222">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-223">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="c3a10-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c3a10-224">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c3a10-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c3a10-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="c3a10-226">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-227">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="c3a10-227">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c3a10-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c3a10-229">(1)</span><span class="sxs-lookup"><span data-stu-id="c3a10-229">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-230">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="c3a10-230">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c3a10-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c3a10-232">(2)</span><span class="sxs-lookup"><span data-stu-id="c3a10-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c3a10-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c3a10-234">(3)</span><span class="sxs-lookup"><span data-stu-id="c3a10-234">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-235">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="c3a10-235">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c3a10-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c3a10-237">(4)</span><span class="sxs-lookup"><span data-stu-id="c3a10-237">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-238">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="c3a10-238">Device is not working properly.</span></span> <span data-ttu-id="c3a10-239">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="c3a10-239">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c3a10-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c3a10-241">(5)</span><span class="sxs-lookup"><span data-stu-id="c3a10-241">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-242">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="c3a10-242">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c3a10-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c3a10-244"> (6)</span><span class="sxs-lookup"><span data-stu-id="c3a10-244">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-245">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="c3a10-245">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c3a10-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c3a10-247">(7)</span><span class="sxs-lookup"><span data-stu-id="c3a10-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c3a10-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c3a10-249">(8)</span><span class="sxs-lookup"><span data-stu-id="c3a10-249">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-250">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="c3a10-250">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c3a10-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c3a10-252">(9)</span><span class="sxs-lookup"><span data-stu-id="c3a10-252">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-253">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="c3a10-253">Device is not working properly.</span></span> <span data-ttu-id="c3a10-254">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-254">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c3a10-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c3a10-256">(10)</span><span class="sxs-lookup"><span data-stu-id="c3a10-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-257">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c3a10-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c3a10-259">(11)</span><span class="sxs-lookup"><span data-stu-id="c3a10-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-260">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c3a10-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c3a10-262">douze</span><span class="sxs-lookup"><span data-stu-id="c3a10-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-263">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c3a10-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c3a10-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c3a10-265">(13)</span><span class="sxs-lookup"><span data-stu-id="c3a10-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-266">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c3a10-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c3a10-268">(14)</span><span class="sxs-lookup"><span data-stu-id="c3a10-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-269">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="c3a10-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c3a10-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c3a10-271">(15)</span><span class="sxs-lookup"><span data-stu-id="c3a10-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-272">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="c3a10-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c3a10-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c3a10-274">(16)</span><span class="sxs-lookup"><span data-stu-id="c3a10-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-275">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c3a10-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c3a10-277">(17)</span><span class="sxs-lookup"><span data-stu-id="c3a10-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-278">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="c3a10-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c3a10-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c3a10-280">(18)</span><span class="sxs-lookup"><span data-stu-id="c3a10-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-281">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="c3a10-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c3a10-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c3a10-283">(19)</span><span class="sxs-lookup"><span data-stu-id="c3a10-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c3a10-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c3a10-285">(20)</span><span class="sxs-lookup"><span data-stu-id="c3a10-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-286">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="c3a10-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c3a10-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c3a10-288">(21)</span><span class="sxs-lookup"><span data-stu-id="c3a10-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-289">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="c3a10-289">System failure.</span></span> <span data-ttu-id="c3a10-290">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="c3a10-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c3a10-291">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c3a10-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c3a10-293">(22)</span><span class="sxs-lookup"><span data-stu-id="c3a10-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-294">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c3a10-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c3a10-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c3a10-296">(23)</span><span class="sxs-lookup"><span data-stu-id="c3a10-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-297">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="c3a10-297">System failure.</span></span> <span data-ttu-id="c3a10-298">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="c3a10-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c3a10-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c3a10-300">(24)</span><span class="sxs-lookup"><span data-stu-id="c3a10-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-301">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="c3a10-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c3a10-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c3a10-303">(25)</span><span class="sxs-lookup"><span data-stu-id="c3a10-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-304">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c3a10-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c3a10-306">(26)</span><span class="sxs-lookup"><span data-stu-id="c3a10-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-307">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c3a10-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c3a10-309">(27)</span><span class="sxs-lookup"><span data-stu-id="c3a10-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-310">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="c3a10-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c3a10-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c3a10-312">(28)</span><span class="sxs-lookup"><span data-stu-id="c3a10-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-313">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="c3a10-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c3a10-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c3a10-315">(29)</span><span class="sxs-lookup"><span data-stu-id="c3a10-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-316">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c3a10-316">Device is disabled.</span></span> <span data-ttu-id="c3a10-317">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="c3a10-317">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c3a10-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c3a10-319">(30)</span><span class="sxs-lookup"><span data-stu-id="c3a10-319">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-320">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="c3a10-320">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c3a10-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c3a10-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c3a10-322">31</span><span class="sxs-lookup"><span data-stu-id="c3a10-322">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-323">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="c3a10-323">Device is not working properly.</span></span> <span data-ttu-id="c3a10-324">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="c3a10-324">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-325">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c3a10-325">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-326">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c3a10-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-328">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c3a10-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-329">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3a10-329">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c3a10-330">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-331">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c3a10-331">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-332">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-334">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c3a10-334">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-335">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="c3a10-335">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c3a10-336">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="c3a10-336">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c3a10-337">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-338">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="c3a10-338">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-339">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3a10-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-341">Qualificateurs : [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c3a10-341">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-342">Taille de bloc par défaut, en octets, pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-342">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="c3a10-343">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-343">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="c3a10-344">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-345">**Description**</span><span class="sxs-lookup"><span data-stu-id="c3a10-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-348">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c3a10-348">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-349">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3a10-349">Description of the object.</span></span>

<span data-ttu-id="c3a10-350">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c3a10-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-354">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("fonctions de \| fichier win32api \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="c3a10-354">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-355">Identificateur unique du lecteur de bande avec les autres périphériques du système.</span><span class="sxs-lookup"><span data-stu-id="c3a10-355">Unique identifier of the tape drive with other devices on the system.</span></span>

<span data-ttu-id="c3a10-356">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-357">**ECC**</span><span class="sxs-lookup"><span data-stu-id="c3a10-357">**ECC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-358">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-360">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de sauvegarde sur bande win32api les \| [**\_ \_ \_ paramètres de lecteur bande**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)d’accès \| ECC")</span><span class="sxs-lookup"><span data-stu-id="c3a10-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ECC")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-361">Si la **valeur est true**, l’appareil prend en charge la correction des erreurs matérielles.</span><span class="sxs-lookup"><span data-stu-id="c3a10-361">If **TRUE**, the device supports hardware error correction.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="c3a10-362">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c3a10-362">**False** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="c3a10-363">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c3a10-363">**True** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-364">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="c3a10-364">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-365">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-367">Qualificateurs : [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c3a10-367">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-368">Taille de zone pour l’avertissement de fin de bande (EOT).</span><span class="sxs-lookup"><span data-stu-id="c3a10-368">Zone size for the end of tape (EOT) warning.</span></span>

<span data-ttu-id="c3a10-369">Cette propriété est héritée de la propriété [**CIM \_**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-369">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-370">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c3a10-370">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-371">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c3a10-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-373">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="c3a10-373">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="c3a10-374">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-375">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c3a10-375">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-378">Chaîne de forme libre fournissant plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="c3a10-378">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="c3a10-379">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-380">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="c3a10-380">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-383">Chaîne de forme libre décrivant le type de détection d’erreurs et de correction pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-383">Free-form string describing the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="c3a10-384">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-385">**FeaturesHigh**</span><span class="sxs-lookup"><span data-stu-id="c3a10-385">**FeaturesHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-386">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-388">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de sauvegarde sur bande win32api \| ,[**\_ \_ \_ paramètres de lecteur de bande**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesHigh")</span><span class="sxs-lookup"><span data-stu-id="c3a10-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesHigh")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-389">Poids élevé 32 bits de l’indicateur de fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-389">High-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-390">**FeaturesLow**</span><span class="sxs-lookup"><span data-stu-id="c3a10-390">**FeaturesLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-391">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-391">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-393">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de sauvegarde sur bande win32api \| ,[**\_ \_ \_ paramètres de lecteur de bande**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesLow")</span><span class="sxs-lookup"><span data-stu-id="c3a10-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesLow")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-394">Poids faible 32 bits de l’indicateur de fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-394">Low-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-395">**Id**</span><span class="sxs-lookup"><span data-stu-id="c3a10-395">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-396">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-398">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions de fichier win32api »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-399">Nom identifiant le lecteur de CD-ROM Windows au fabricant.</span><span class="sxs-lookup"><span data-stu-id="c3a10-399">Manufacturer's identifying name of the Windows CD ROM drive.</span></span>

<span data-ttu-id="c3a10-400">Exemple : « PLEXTOR CD-ROM PX-12CS 1,01 »</span><span class="sxs-lookup"><span data-stu-id="c3a10-400">Example: "PLEXTOR CD-ROM PX-12CS 1.01"</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-401">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c3a10-401">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-402">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3a10-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-404">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="c3a10-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-405">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3a10-405">Date and time the object was installed.</span></span> <span data-ttu-id="c3a10-406">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="c3a10-406">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c3a10-407">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-408">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c3a10-408">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-409">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-411">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c3a10-411">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c3a10-412">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-413">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="c3a10-413">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-414">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-416">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="c3a10-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-417">Fabricant du lecteur de CD-ROM Windows.</span><span class="sxs-lookup"><span data-stu-id="c3a10-417">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="c3a10-418">Exemple : « PLEXTOR »</span><span class="sxs-lookup"><span data-stu-id="c3a10-418">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-419">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="c3a10-419">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-420">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3a10-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-422">Qualificateurs : [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c3a10-422">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-423">Taille maximale de bloc, en octets, pour les médias auxquels ce périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="c3a10-423">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="c3a10-424">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-424">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="c3a10-425">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-426">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="c3a10-426">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-427">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3a10-427">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-429">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](../wmisdk/standard-qualifiers.md) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="c3a10-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-430">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-430">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="c3a10-431">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="c3a10-432">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-432">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-433">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="c3a10-433">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-434">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-436">Nombre maximal de partitions pour le lecteur de bande.</span><span class="sxs-lookup"><span data-stu-id="c3a10-436">Maximum partition count for the tape drive.</span></span>

<span data-ttu-id="c3a10-437">Cette propriété est héritée de la propriété [**CIM \_**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-437">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-438">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="c3a10-438">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-441">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ \| MediaType \| Tape Drive)</span><span class="sxs-lookup"><span data-stu-id="c3a10-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_TapeDrive\|MediaType\|Tape Drive")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-442">Type de média utilisé par cet appareil (ou auquel il est accessible).</span><span class="sxs-lookup"><span data-stu-id="c3a10-442">Media type used by (or accessed by) this device.</span></span> <span data-ttu-id="c3a10-443">Dans ce cas, il est défini sur « lecteur de bande ».</span><span class="sxs-lookup"><span data-stu-id="c3a10-443">In this case, it is set to "Tape Drive".</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-444">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="c3a10-444">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-445">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3a10-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-447">Qualificateurs : [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c3a10-447">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-448">Taille de bloc minimale, en octets, pour les médias auxquels ce périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="c3a10-448">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="c3a10-449">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-449">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="c3a10-450">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-451">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c3a10-451">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-452">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-454">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c3a10-454">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-455">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="c3a10-455">Label by which the object is known.</span></span> <span data-ttu-id="c3a10-456">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="c3a10-456">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c3a10-457">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-458">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="c3a10-458">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-459">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c3a10-459">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-461">Si la **valeur est true**, l’appareil d’accès aux médias doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="c3a10-461">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="c3a10-462">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété **capacités** .</span><span class="sxs-lookup"><span data-stu-id="c3a10-462">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="c3a10-463">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-464">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="c3a10-464">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-465">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-465">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-467">Nombre maximal de médias individuels qui peuvent être pris en charge ou insérés dans l’appareil d’accès aux médias (en cas de prise en charge).</span><span class="sxs-lookup"><span data-stu-id="c3a10-467">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="c3a10-468">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-468">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-469">**Remplissage**</span><span class="sxs-lookup"><span data-stu-id="c3a10-469">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-470">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-470">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-471">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-472">Qualificateurs : [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c3a10-472">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-473">Nombre d’octets insérés entre les blocs sur un support de bande.</span><span class="sxs-lookup"><span data-stu-id="c3a10-473">Number of bytes inserted between blocks on a tape media.</span></span>

<span data-ttu-id="c3a10-474">Cette propriété est héritée de la propriété [**CIM \_**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-474">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-475">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c3a10-475">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-476">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-478">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c3a10-478">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-479">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c3a10-479">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c3a10-480">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c3a10-481">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="c3a10-481">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-482">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c3a10-482">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-483">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3a10-483">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-484">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-485">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="c3a10-485">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c3a10-486">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="c3a10-486">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3a10-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c3a10-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c3a10-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="c3a10-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-489">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="c3a10-489">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c3a10-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="c3a10-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c3a10-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="c3a10-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-492">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="c3a10-492">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c3a10-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="c3a10-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-494">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="c3a10-494">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c3a10-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="c3a10-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-496">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c3a10-496">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c3a10-497">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="c3a10-497">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c3a10-498">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-498">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c3a10-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="c3a10-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-500">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="c3a10-500">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c3a10-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="c3a10-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-502">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3a10-502">Timed Power-On Supported</span></span>

<span data-ttu-id="c3a10-503">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="c3a10-503">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-504">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c3a10-504">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-505">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c3a10-505">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-506">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-507">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="c3a10-507">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c3a10-508">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="c3a10-508">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c3a10-509">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-510">**ReportSetMarks**</span><span class="sxs-lookup"><span data-stu-id="c3a10-510">**ReportSetMarks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-511">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3a10-511">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-512">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-513">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de sauvegarde sur bande win32api \| ,[**\_ \_ \_ paramètres de lecteur de bande**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ReportSetmarks")</span><span class="sxs-lookup"><span data-stu-id="c3a10-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ReportSetmarks")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-514">Si la **valeur est true**, SETMARK Reporting est activé.</span><span class="sxs-lookup"><span data-stu-id="c3a10-514">If **TRUE**, setmark reporting is enabled.</span></span> <span data-ttu-id="c3a10-515">SETMARK Reporting utilise un élément enregistré spécialisé qui ne contient pas de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3a10-515">Setmark reporting makes use of a specialized recorded element that does not contain user data.</span></span> <span data-ttu-id="c3a10-516">Cet élément enregistré est utilisé pour fournir un schéma de segmentation qui est hiérarchiquement supérieur aux marques de programme.</span><span class="sxs-lookup"><span data-stu-id="c3a10-516">This recorded element is used to provide a segmentation scheme that is hierarchically superior to filemarks.</span></span> <span data-ttu-id="c3a10-517">Les Setmarks permettent de positionner plus rapidement les bandes de grande capacité.</span><span class="sxs-lookup"><span data-stu-id="c3a10-517">Setmarks provide faster positioning on high-capacity tapes.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c3a10-518"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="c3a10-518"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-519">FALSE</span><span class="sxs-lookup"><span data-stu-id="c3a10-519">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c3a10-520"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c3a10-520"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c3a10-521">TRUE</span><span class="sxs-lookup"><span data-stu-id="c3a10-521">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-522">**État**</span><span class="sxs-lookup"><span data-stu-id="c3a10-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-525">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c3a10-525">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-526">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3a10-526">Current status of the object.</span></span> <span data-ttu-id="c3a10-527">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="c3a10-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c3a10-528">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="c3a10-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c3a10-529">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="c3a10-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c3a10-530">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="c3a10-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c3a10-531">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="c3a10-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c3a10-532">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c3a10-533">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3a10-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c3a10-534">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c3a10-535">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c3a10-536">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3a10-537">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="c3a10-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c3a10-538">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c3a10-539">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c3a10-540">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c3a10-541">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c3a10-542">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c3a10-543">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c3a10-544">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c3a10-545">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="c3a10-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c3a10-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-547">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3a10-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-548">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-549">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c3a10-549">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-550">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c3a10-550">State of the logical device.</span></span> <span data-ttu-id="c3a10-551">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3a10-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c3a10-552">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c3a10-553">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c3a10-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3a10-554">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="c3a10-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c3a10-555">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="c3a10-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c3a10-556">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="c3a10-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c3a10-557">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="c3a10-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3a10-558">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c3a10-558">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-559">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-560">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-560">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-561">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c3a10-561">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-562">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="c3a10-562">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c3a10-563">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-563">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3a10-564">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c3a10-564">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3a10-565">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c3a10-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-566">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3a10-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3a10-567">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c3a10-567">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c3a10-568">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="c3a10-568">Name of the scoping system.</span></span>

<span data-ttu-id="c3a10-569">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-569">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3a10-570">Notes</span><span class="sxs-lookup"><span data-stu-id="c3a10-570">Remarks</span></span>

<span data-ttu-id="c3a10-571">La **classe \_ Win32** de la part est dérivée de [**CIM \_**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="c3a10-571">The **Win32\_TapeDrive** class is derived from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a10-572">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3a10-572">Requirements</span></span>



| <span data-ttu-id="c3a10-573">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3a10-573">Requirement</span></span> | <span data-ttu-id="c3a10-574">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3a10-574">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a10-575">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3a10-575">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a10-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3a10-576">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3a10-577">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3a10-577">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a10-578">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3a10-578">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3a10-579">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c3a10-579">Namespace</span></span><br/>                | <span data-ttu-id="c3a10-580">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c3a10-580">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c3a10-581">MOF</span><span class="sxs-lookup"><span data-stu-id="c3a10-581">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3a10-582"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3a10-582"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3a10-583">DLL</span><span class="sxs-lookup"><span data-stu-id="c3a10-583">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3a10-584"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3a10-584"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a10-585">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3a10-585">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a10-586">**CIM \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="c3a10-586">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="c3a10-587">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="c3a10-587">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
