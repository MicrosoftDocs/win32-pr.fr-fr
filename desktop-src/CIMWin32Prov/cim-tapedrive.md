---
description: La classe CIM CIM \_ représente un lecteur de bande sur le système. Les lecteurs de bande sont principalement distingués dans le fait qu’ils sont accessibles uniquement de façon séquentielle.
ms.assetid: 8b7f2277-e37d-4597-81bb-d3c8d4966a81
ms.tgt_platform: multiple
title: CIM_TapeDrive, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.Availability
- CIM_TapeDrive.Capabilities
- CIM_TapeDrive.CapabilityDescriptions
- CIM_TapeDrive.Caption
- CIM_TapeDrive.CompressionMethod
- CIM_TapeDrive.ConfigManagerErrorCode
- CIM_TapeDrive.ConfigManagerUserConfig
- CIM_TapeDrive.CreationClassName
- CIM_TapeDrive.DefaultBlockSize
- CIM_TapeDrive.Description
- CIM_TapeDrive.DeviceID
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.ErrorCleared
- CIM_TapeDrive.ErrorDescription
- CIM_TapeDrive.ErrorMethodology
- CIM_TapeDrive.InstallDate
- CIM_TapeDrive.LastErrorCode
- CIM_TapeDrive.MaxBlockSize
- CIM_TapeDrive.MaxMediaSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.MinBlockSize
- CIM_TapeDrive.Name
- CIM_TapeDrive.NeedsCleaning
- CIM_TapeDrive.NumberOfMediaSupported
- CIM_TapeDrive.Padding
- CIM_TapeDrive.PNPDeviceID
- CIM_TapeDrive.PowerManagementCapabilities
- CIM_TapeDrive.PowerManagementSupported
- CIM_TapeDrive.Status
- CIM_TapeDrive.StatusInfo
- CIM_TapeDrive.SystemCreationClassName
- CIM_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 184b855d5989c77292e51e8b477c5392893deccb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861762"
---
# <a name="cim_tapedrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="9ca8f-104">CIM_TapeDrive, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-104">CIM_TapeDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9ca8f-105">La **classe \_ CIM CIM** représente un lecteur de bande sur le système.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-105">The **CIM\_TapeDrive** class represents a tape drive on the system.</span></span> <span data-ttu-id="9ca8f-106">Les lecteurs de bande sont principalement distingués dans le fait qu’ils sont accessibles uniquement de façon séquentielle.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-106">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ca8f-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9ca8f-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9ca8f-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9ca8f-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca8f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ca8f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_TapeDrive : CIM_MediaAccessDevice
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
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="9ca8f-112">Membres</span><span class="sxs-lookup"><span data-stu-id="9ca8f-112">Members</span></span>

<span data-ttu-id="9ca8f-113">La **classe \_ CIM CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9ca8f-113">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="9ca8f-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9ca8f-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="9ca8f-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ca8f-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9ca8f-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9ca8f-116">Methods</span></span>

<span data-ttu-id="9ca8f-117">La **classe \_ CIM CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-117">The **CIM\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="9ca8f-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="9ca8f-118">Method</span></span>                                                               | <span data-ttu-id="9ca8f-119">Description</span><span class="sxs-lookup"><span data-stu-id="9ca8f-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ca8f-120">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-120">**Reset**</span></span>](reset-method-in-class-cim-tapedrive.md)                 | <span data-ttu-id="9ca8f-121">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="9ca8f-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9ca8f-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-tapedrive.md) | <span data-ttu-id="9ca8f-124">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9ca8f-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9ca8f-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ca8f-126">Properties</span></span>

<span data-ttu-id="9ca8f-127">La **classe \_ CIM CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-127">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ca8f-128">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-131">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-132">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-132">Availability and status of the device.</span></span>

<span data-ttu-id="9ca8f-133">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ca8f-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ca8f-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9ca8f-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9ca8f-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9ca8f-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9ca8f-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9ca8f-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9ca8f-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9ca8f-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ca8f-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9ca8f-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9ca8f-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9ca8f-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-147">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9ca8f-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-149">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9ca8f-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-151">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-151">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9ca8f-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9ca8f-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-154">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9ca8f-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-156">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9ca8f-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-158">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9ca8f-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-160">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9ca8f-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-162">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ca8f-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-164">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-166">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-167">Fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-167">Capabilities of the media access device.</span></span> <span data-ttu-id="9ca8f-168">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-168">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ca8f-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-170">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-170">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ca8f-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-172">Autre.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-172">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="9ca8f-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-174">Accès séquentiel.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-174">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="9ca8f-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-176">Accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-176">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="9ca8f-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-178">Écriture.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-178">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="9ca8f-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-180">Chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-180">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="9ca8f-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-182">Compression.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-182">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="9ca8f-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-184">Support amovible.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-184">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="9ca8f-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-186">Nettoyage manuel.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-186">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="9ca8f-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-188">Nettoyage automatique.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-188">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="9ca8f-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-190">Notification intelligente.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-190">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="9ca8f-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-192">Distingue un appareil qui peut accéder aux deux côtés d’un média à deux faces à partir d’un appareil qui ne lit qu’un seul côté et requiert le basculement du média.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-192">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="9ca8f-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-194">Indique qu’il n’est pas nécessaire d’éjecter explicitement le média de l’appareil avant d’y accéder par un élément sélecteur.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-194">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ca8f-195">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-195">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-196">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-196">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-198">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-198">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-199">Chaînes de forme libre qui fournissent des explications détaillées sur les fonctionnalités de l’appareil Access indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="9ca8f-199">Free-form strings that provide detailed explanations for the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="9ca8f-200">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-200">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="9ca8f-201">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-202">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-202">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-205">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-206">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-206">Short textual description of the object.</span></span>

<span data-ttu-id="9ca8f-207">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-207">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-208">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-208">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-211">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-211">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="9ca8f-212">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="9ca8f-212">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="9ca8f-213">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="9ca8f-213">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="9ca8f-214">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="9ca8f-214">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="9ca8f-215">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-215">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="9ca8f-216">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-216">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-217">Le schéma de compression est inconnu ou non décrit.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-217">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="9ca8f-218">(« Compressé »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-218">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-219">Le fichier logique est compressé, mais le schéma de compression est inconnu ou n’est pas décrit.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-219">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="9ca8f-220">(« Non compressé »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-220">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-221">Si le fichier logique n’est pas compressé</span><span class="sxs-lookup"><span data-stu-id="9ca8f-221">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ca8f-222">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-222">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-223">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-225">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-225">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-226">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-226">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="9ca8f-227">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-227">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9ca8f-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9ca8f-229"> (0)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-229">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-230">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-230">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9ca8f-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9ca8f-232">(1)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-232">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-233">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-233">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ca8f-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9ca8f-235">(2)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9ca8f-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9ca8f-237">(3)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-237">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-238">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-238">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9ca8f-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9ca8f-240">(4)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-240">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-241">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-241">Device is not working properly.</span></span> <span data-ttu-id="9ca8f-242">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-242">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9ca8f-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9ca8f-244">(5)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-244">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-245">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-245">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9ca8f-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9ca8f-247"> (6)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-247">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-248">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-248">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9ca8f-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9ca8f-250">(7)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-250">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9ca8f-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9ca8f-252">(8)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-252">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-253">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-253">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9ca8f-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9ca8f-255">(9)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-255">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-256">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-256">Device is not working properly.</span></span> <span data-ttu-id="9ca8f-257">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-257">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9ca8f-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9ca8f-259">(10)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-259">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-260">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-260">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9ca8f-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9ca8f-262">(11)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-262">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-263">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-263">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9ca8f-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9ca8f-265">douze</span><span class="sxs-lookup"><span data-stu-id="9ca8f-265">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-266">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-266">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9ca8f-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9ca8f-268">(13)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-268">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-269">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-269">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9ca8f-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9ca8f-271">(14)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-271">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-272">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-272">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9ca8f-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9ca8f-274">(15)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-274">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-275">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-275">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9ca8f-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9ca8f-277">(16)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-277">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-278">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-278">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9ca8f-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9ca8f-280">(17)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-280">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-281">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-281">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ca8f-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9ca8f-283">(18)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-283">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-284">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-284">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9ca8f-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9ca8f-286">(19)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-286">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9ca8f-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9ca8f-288">(20)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-288">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-289">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-289">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9ca8f-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9ca8f-291">(21)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-291">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-292">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-292">System failure.</span></span> <span data-ttu-id="9ca8f-293">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-293">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9ca8f-294">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-294">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9ca8f-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9ca8f-296">(22)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-296">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-297">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-297">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9ca8f-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9ca8f-299">(23)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-299">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-300">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-300">System failure.</span></span> <span data-ttu-id="9ca8f-301">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-301">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9ca8f-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9ca8f-303">(24)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-303">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-304">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-304">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9ca8f-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9ca8f-306">(25)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-306">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-307">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9ca8f-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9ca8f-309">(26)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-309">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-310">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-310">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9ca8f-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9ca8f-312">(27)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-312">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-313">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-313">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9ca8f-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9ca8f-315">(28)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-315">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-316">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-316">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9ca8f-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9ca8f-318">(29)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-318">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-319">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-319">Device is disabled.</span></span> <span data-ttu-id="9ca8f-320">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-320">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9ca8f-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9ca8f-322">(30)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-322">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-323">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-323">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ca8f-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9ca8f-325">31</span><span class="sxs-lookup"><span data-stu-id="9ca8f-325">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-326">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-326">Device is not working properly.</span></span> <span data-ttu-id="9ca8f-327">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-327">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ca8f-328">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-328">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-329">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-331">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-332">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-332">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9ca8f-333">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-333">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-334">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-334">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-335">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-337">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-337">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-338">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-338">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9ca8f-339">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-339">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9ca8f-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-341">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-341">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-342">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-344">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-344">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-345">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-345">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="9ca8f-346">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-346">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9ca8f-347">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-348">**Description**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-348">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-351">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-352">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-352">Textual description of the object.</span></span>

<span data-ttu-id="9ca8f-353">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-353">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-354">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-354">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-357">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-358">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-358">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9ca8f-359">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-360">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-360">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-361">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-363">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-363">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-364">Taille, en octets, de la zone désignée comme fin de bande.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-364">Size, in bytes, of the area designated as end-of-tape.</span></span> <span data-ttu-id="9ca8f-365">L’accès dans cette zone génère un avertissement de fin de bande.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-365">Access in this area generates an end-of-tape warning.</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-366">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-366">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-367">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-367">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-369">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-369">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9ca8f-370">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-371">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-371">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-372">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-374">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-374">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9ca8f-375">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-376">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-376">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-377">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-379">Chaîne de forme libre qui décrit les types de détection d’erreurs et de correction pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-379">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="9ca8f-380">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-380">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-381">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-381">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-382">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-382">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-384">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-385">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-385">Date and time the object was installed.</span></span> <span data-ttu-id="9ca8f-386">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-386">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9ca8f-387">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-388">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-388">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-389">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-391">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-391">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9ca8f-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-393">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-393">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-394">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-396">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-397">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-397">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="9ca8f-398">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-398">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9ca8f-399">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-400">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-400">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-401">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-403">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-404">Taille maximale, en kilo-octets, des médias pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-404">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="9ca8f-405">Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-405">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="9ca8f-406">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-406">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9ca8f-407">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-407">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-408">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-408">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-409">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-411">Nombre maximal de partitions pour le lecteur de bande.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-411">Maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-412">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-412">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-413">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-413">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-415">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-416">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-416">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="9ca8f-417">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9ca8f-418">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-418">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-419">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-420">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-422">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-423">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-423">Label by which the object is known.</span></span> <span data-ttu-id="9ca8f-424">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-424">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9ca8f-425">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-426">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-426">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-427">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-429">Si la **valeur est true**, l’appareil d’accès aux médias doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-429">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="9ca8f-430">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété du tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="9ca8f-430">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="9ca8f-431">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-432">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-432">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-433">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-435">Lorsque l’appareil d’accès aux médias prend en charge plusieurs médias individuels, cette propriété définit le nombre maximal qui peut être pris en charge ou inséré.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-435">When the media access device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

<span data-ttu-id="9ca8f-436">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-436">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-437">**Remplissage**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-437">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-438">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-440">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-440">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-441">Nombre d’octets insérés entre les blocs sur un support de bande.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-441">Number of bytes inserted between blocks on a tape media.</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-443">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-445">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-445">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-446">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-446">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="9ca8f-447">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9ca8f-448">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="9ca8f-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-450">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-452">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9ca8f-453">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ca8f-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9ca8f-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-456">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-456">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9ca8f-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9ca8f-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-459">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-459">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9ca8f-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-461">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-461">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9ca8f-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-463">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9ca8f-464">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-464">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9ca8f-465">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-465">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9ca8f-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-467">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-467">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9ca8f-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9ca8f-469">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ca8f-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-471">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-473">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-473">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9ca8f-474">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9ca8f-474">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9ca8f-475">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-475">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9ca8f-476">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9ca8f-476">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="9ca8f-477">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-478">**État**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-478">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-479">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-480">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-481">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-481">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-482">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-482">Current status of the object.</span></span> <span data-ttu-id="9ca8f-483">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-483">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9ca8f-484">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ca8f-484">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9ca8f-485">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-485">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9ca8f-486">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-486">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ca8f-487">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-487">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ca8f-488">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-488">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9ca8f-489">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-489">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9ca8f-490">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-490">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9ca8f-491">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-491">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9ca8f-492">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-492">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9ca8f-493">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-493">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9ca8f-494">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-494">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9ca8f-495">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-495">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9ca8f-496">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-496">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ca8f-497">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-497">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-498">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-498">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-500">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9ca8f-500">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-501">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-501">State of the logical device.</span></span> <span data-ttu-id="9ca8f-502">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-502">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9ca8f-503">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ca8f-504">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-504">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ca8f-505">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-505">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9ca8f-506">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-506">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9ca8f-507">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-507">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9ca8f-508">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-508">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ca8f-509">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-509">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-510">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-511">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-512">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-513">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-513">Scoping system's creation class name.</span></span>

<span data-ttu-id="9ca8f-514">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ca8f-515">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-515">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ca8f-516">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-517">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ca8f-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ca8f-518">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ca8f-518">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ca8f-519">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-519">Scoping system's name.</span></span>

<span data-ttu-id="9ca8f-520">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-520">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ca8f-521">Notes</span><span class="sxs-lookup"><span data-stu-id="9ca8f-521">Remarks</span></span>

<span data-ttu-id="9ca8f-522">La **classe \_ CIM CIM** est dérivée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-522">The **CIM\_TapeDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9ca8f-523">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-523">WMI does not implement this class.</span></span> <span data-ttu-id="9ca8f-524">Pour les classes WMI dérivées de la page **CIM CIM \_**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9ca8f-524">For WMI classes derived from **CIM\_TapeDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9ca8f-525">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-525">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9ca8f-526">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9ca8f-526">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca8f-527">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ca8f-527">Requirements</span></span>



| <span data-ttu-id="9ca8f-528">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ca8f-528">Requirement</span></span> | <span data-ttu-id="9ca8f-529">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ca8f-529">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca8f-530">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ca8f-530">Minimum supported client</span></span><br/> | <span data-ttu-id="9ca8f-531">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ca8f-531">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ca8f-532">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ca8f-532">Minimum supported server</span></span><br/> | <span data-ttu-id="9ca8f-533">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ca8f-533">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ca8f-534">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9ca8f-534">Namespace</span></span><br/>                | <span data-ttu-id="9ca8f-535">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9ca8f-535">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ca8f-536">MOF</span><span class="sxs-lookup"><span data-stu-id="9ca8f-536">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ca8f-537"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ca8f-537"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ca8f-538">DLL</span><span class="sxs-lookup"><span data-stu-id="9ca8f-538">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ca8f-539"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ca8f-539"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca8f-540">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ca8f-540">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca8f-541">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9ca8f-541">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

