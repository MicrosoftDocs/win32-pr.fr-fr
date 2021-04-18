---
description: La \_ classe du processeur CIM représente les fonctionnalités et la gestion du périphérique logique du processeur.
ms.assetid: 7af3208f-f1d5-4911-b6ab-46b54eec0b69
ms.tgt_platform: multiple
title: CIM_Processor, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.AddressWidth
- CIM_Processor.Availability
- CIM_Processor.Caption
- CIM_Processor.ConfigManagerErrorCode
- CIM_Processor.ConfigManagerUserConfig
- CIM_Processor.CreationClassName
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.Description
- CIM_Processor.DeviceID
- CIM_Processor.ErrorCleared
- CIM_Processor.ErrorDescription
- CIM_Processor.Family
- CIM_Processor.InstallDate
- CIM_Processor.LastErrorCode
- CIM_Processor.LoadPercentage
- CIM_Processor.MaxClockSpeed
- CIM_Processor.Name
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.PNPDeviceID
- CIM_Processor.PowerManagementCapabilities
- CIM_Processor.PowerManagementSupported
- CIM_Processor.Role
- CIM_Processor.Status
- CIM_Processor.StatusInfo
- CIM_Processor.Stepping
- CIM_Processor.SystemCreationClassName
- CIM_Processor.SystemName
- CIM_Processor.UniqueId
- CIM_Processor.UpgradeMethod
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0120ce0327c21098b8c2950bd5dfa9a9fe2a709c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483000"
---
# <a name="cim_processor-class-cimwin32-wmi-providers"></a><span data-ttu-id="91cf0-103">CIM_Processor, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="91cf0-103">CIM_Processor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="91cf0-104">La classe du **\_ processeur CIM** représente les fonctionnalités et la gestion du périphérique logique du processeur.</span><span class="sxs-lookup"><span data-stu-id="91cf0-104">The **CIM\_Processor** class represents the capabilities and management of the processor logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91cf0-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="91cf0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="91cf0-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="91cf0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="91cf0-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="91cf0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="91cf0-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="91cf0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="91cf0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91cf0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  uint16   AddressWidth;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Family;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint16   LoadPercentage;
  uint32   MaxClockSpeed;
  string   Name;
  string   OtherFamilyDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Role;
  string   Status;
  uint16   StatusInfo;
  string   Stepping;
  string   SystemCreationClassName;
  string   SystemName;
  string   UniqueId;
  uint16   UpgradeMethod;
};
```

## <a name="members"></a><span data-ttu-id="91cf0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="91cf0-110">Members</span></span>

<span data-ttu-id="91cf0-111">La classe de **\_ processeur CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="91cf0-111">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="91cf0-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="91cf0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="91cf0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91cf0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="91cf0-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="91cf0-114">Methods</span></span>

<span data-ttu-id="91cf0-115">La classe du **\_ processeur CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="91cf0-115">The **CIM\_Processor** class has these methods.</span></span>



| <span data-ttu-id="91cf0-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="91cf0-116">Method</span></span>                                                               | <span data-ttu-id="91cf0-117">Description</span><span class="sxs-lookup"><span data-stu-id="91cf0-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91cf0-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="91cf0-118">**Reset**</span></span>](reset-method-in-class-cim-processor.md)                 | <span data-ttu-id="91cf0-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="91cf0-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="91cf0-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="91cf0-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="91cf0-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="91cf0-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-processor.md) | <span data-ttu-id="91cf0-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="91cf0-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="91cf0-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="91cf0-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="91cf0-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91cf0-124">Properties</span></span>

<span data-ttu-id="91cf0-125">La classe du **\_ processeur CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="91cf0-125">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91cf0-126">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="91cf0-126">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91cf0-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-129">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-130">Largeur de l’adresse du processeur, en bits.</span><span class="sxs-lookup"><span data-stu-id="91cf0-130">Processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-131">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="91cf0-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-132">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91cf0-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-134">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="91cf0-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-135">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-135">Availability and status of the device.</span></span>

<span data-ttu-id="91cf0-136">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91cf0-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="91cf0-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91cf0-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="91cf0-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="91cf0-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="91cf0-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-140">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="91cf0-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="91cf0-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="91cf0-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="91cf0-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="91cf0-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="91cf0-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="91cf0-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="91cf0-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="91cf0-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="91cf0-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="91cf0-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="91cf0-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="91cf0-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="91cf0-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="91cf0-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="91cf0-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="91cf0-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="91cf0-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="91cf0-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="91cf0-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="91cf0-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-151">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="91cf0-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="91cf0-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="91cf0-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-153">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="91cf0-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="91cf0-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="91cf0-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-155">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="91cf0-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="91cf0-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="91cf0-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="91cf0-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="91cf0-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-158">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="91cf0-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="91cf0-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="91cf0-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-160">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="91cf0-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="91cf0-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="91cf0-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-162">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="91cf0-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="91cf0-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="91cf0-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-164">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="91cf0-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="91cf0-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="91cf0-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-166">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="91cf0-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91cf0-167">**Caption**</span><span class="sxs-lookup"><span data-stu-id="91cf0-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-170">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-171">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91cf0-171">Short textual description of the object.</span></span>

<span data-ttu-id="91cf0-172">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="91cf0-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-174">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91cf0-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-176">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91cf0-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-177">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="91cf0-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="91cf0-178">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="91cf0-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="91cf0-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="91cf0-180">(0)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-181">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="91cf0-181">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="91cf0-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="91cf0-183">(1)</span><span class="sxs-lookup"><span data-stu-id="91cf0-183">(1)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-184">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="91cf0-184">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91cf0-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="91cf0-186">(2)</span><span class="sxs-lookup"><span data-stu-id="91cf0-186">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="91cf0-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="91cf0-188">(3)</span><span class="sxs-lookup"><span data-stu-id="91cf0-188">(3)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-189">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="91cf0-189">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="91cf0-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="91cf0-191">(4)</span><span class="sxs-lookup"><span data-stu-id="91cf0-191">(4)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-192">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="91cf0-192">Device is not working properly.</span></span> <span data-ttu-id="91cf0-193">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="91cf0-193">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="91cf0-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="91cf0-195">(5)</span><span class="sxs-lookup"><span data-stu-id="91cf0-195">(5)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-196">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="91cf0-196">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="91cf0-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="91cf0-198"> (6)</span><span class="sxs-lookup"><span data-stu-id="91cf0-198">(6)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-199">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="91cf0-199">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="91cf0-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="91cf0-201">(7)</span><span class="sxs-lookup"><span data-stu-id="91cf0-201">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="91cf0-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="91cf0-203">(8)</span><span class="sxs-lookup"><span data-stu-id="91cf0-203">(8)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-204">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="91cf0-204">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="91cf0-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="91cf0-206">(9)</span><span class="sxs-lookup"><span data-stu-id="91cf0-206">(9)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-207">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="91cf0-207">Device is not working properly.</span></span> <span data-ttu-id="91cf0-208">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-208">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="91cf0-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="91cf0-210">(10)</span><span class="sxs-lookup"><span data-stu-id="91cf0-210">(10)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-211">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-211">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="91cf0-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="91cf0-213">(11)</span><span class="sxs-lookup"><span data-stu-id="91cf0-213">(11)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-214">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-214">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="91cf0-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="91cf0-216">douze</span><span class="sxs-lookup"><span data-stu-id="91cf0-216">(12)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-217">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="91cf0-217">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="91cf0-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="91cf0-219">(13)</span><span class="sxs-lookup"><span data-stu-id="91cf0-219">(13)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-220">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-220">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="91cf0-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="91cf0-222">(14)</span><span class="sxs-lookup"><span data-stu-id="91cf0-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-223">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="91cf0-223">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="91cf0-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="91cf0-225">(15)</span><span class="sxs-lookup"><span data-stu-id="91cf0-225">(15)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-226">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="91cf0-226">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="91cf0-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="91cf0-228">(16)</span><span class="sxs-lookup"><span data-stu-id="91cf0-228">(16)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-229">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-229">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="91cf0-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="91cf0-231">(17)</span><span class="sxs-lookup"><span data-stu-id="91cf0-231">(17)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-232">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="91cf0-232">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91cf0-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="91cf0-234">(18)</span><span class="sxs-lookup"><span data-stu-id="91cf0-234">(18)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-235">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="91cf0-235">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="91cf0-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="91cf0-237">(19)</span><span class="sxs-lookup"><span data-stu-id="91cf0-237">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="91cf0-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="91cf0-239">(20)</span><span class="sxs-lookup"><span data-stu-id="91cf0-239">(20)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-240">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="91cf0-240">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="91cf0-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="91cf0-242">(21)</span><span class="sxs-lookup"><span data-stu-id="91cf0-242">(21)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-243">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="91cf0-243">System failure.</span></span> <span data-ttu-id="91cf0-244">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="91cf0-244">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="91cf0-245">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-245">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="91cf0-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="91cf0-247">(22)</span><span class="sxs-lookup"><span data-stu-id="91cf0-247">(22)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-248">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="91cf0-248">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="91cf0-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="91cf0-250">(23)</span><span class="sxs-lookup"><span data-stu-id="91cf0-250">(23)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-251">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="91cf0-251">System failure.</span></span> <span data-ttu-id="91cf0-252">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="91cf0-252">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="91cf0-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="91cf0-254">(24)</span><span class="sxs-lookup"><span data-stu-id="91cf0-254">(24)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-255">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="91cf0-255">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="91cf0-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="91cf0-257">(25)</span><span class="sxs-lookup"><span data-stu-id="91cf0-257">(25)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-258">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="91cf0-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="91cf0-260">(26)</span><span class="sxs-lookup"><span data-stu-id="91cf0-260">(26)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-261">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="91cf0-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="91cf0-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="91cf0-263">(27)</span><span class="sxs-lookup"><span data-stu-id="91cf0-263">(27)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-264">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="91cf0-264">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="91cf0-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="91cf0-266">(28)</span><span class="sxs-lookup"><span data-stu-id="91cf0-266">(28)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-267">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="91cf0-267">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="91cf0-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="91cf0-269">(29)</span><span class="sxs-lookup"><span data-stu-id="91cf0-269">(29)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-270">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="91cf0-270">Device is disabled.</span></span> <span data-ttu-id="91cf0-271">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="91cf0-271">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="91cf0-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="91cf0-273">(30)</span><span class="sxs-lookup"><span data-stu-id="91cf0-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-274">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="91cf0-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91cf0-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="91cf0-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="91cf0-276">31</span><span class="sxs-lookup"><span data-stu-id="91cf0-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-277">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="91cf0-277">Device is not working properly.</span></span> <span data-ttu-id="91cf0-278">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="91cf0-278">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91cf0-279">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="91cf0-279">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-280">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91cf0-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-282">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91cf0-282">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-283">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="91cf0-283">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="91cf0-284">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-285">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91cf0-285">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-288">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91cf0-288">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-289">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="91cf0-289">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="91cf0-290">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="91cf0-290">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="91cf0-291">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-292">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="91cf0-292">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-293">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91cf0-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-295">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 006,6 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" mégahertz ")</span><span class="sxs-lookup"><span data-stu-id="91cf0-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-296">Vitesse actuelle (en mégahertz) du processeur.</span><span class="sxs-lookup"><span data-stu-id="91cf0-296">Current speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-297">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="91cf0-297">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-298">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91cf0-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-300">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-301">Largeur des données du processeur, en bits.</span><span class="sxs-lookup"><span data-stu-id="91cf0-301">Processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-302">**Description**</span><span class="sxs-lookup"><span data-stu-id="91cf0-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-305">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="91cf0-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-306">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91cf0-306">Textual description of the object.</span></span>

<span data-ttu-id="91cf0-307">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="91cf0-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-311">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91cf0-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-312">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="91cf0-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="91cf0-313">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="91cf0-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-315">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91cf0-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-317">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="91cf0-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="91cf0-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="91cf0-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-322">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="91cf0-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="91cf0-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-324">**Famille**</span><span class="sxs-lookup"><span data-stu-id="91cf0-324">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-325">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91cf0-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-327">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 014,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processeur CIM**.**OtherFamilyDescription**")</span><span class="sxs-lookup"><span data-stu-id="91cf0-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|014.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-328">Type de la famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="91cf0-328">Processor family type.</span></span>

<span data-ttu-id="91cf0-329">Cette propriété est héritée **du \_ processeur CIM**.</span><span class="sxs-lookup"><span data-stu-id="91cf0-329">This property is inherited from **CIM\_Processor**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91cf0-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="91cf0-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91cf0-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="91cf0-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="91cf0-332"><span id="8086"></span>**8086** (3)</span><span class="sxs-lookup"><span data-stu-id="91cf0-332"><span id="8086"></span>**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="91cf0-333"><span id="80286"></span>**80286** (4)</span><span class="sxs-lookup"><span data-stu-id="91cf0-333"><span id="80286"></span>**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="91cf0-334"><span id="80386"></span>**80386** (5)</span><span class="sxs-lookup"><span data-stu-id="91cf0-334"><span id="80386"></span>**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="91cf0-335"><span id="80486"></span>**80486** (6)</span><span class="sxs-lookup"><span data-stu-id="91cf0-335"><span id="80486"></span>**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="91cf0-336"><span id="8087"></span>**8087** (7)</span><span class="sxs-lookup"><span data-stu-id="91cf0-336"><span id="8087"></span>**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="91cf0-337"><span id="80287"></span>**80287** (8)</span><span class="sxs-lookup"><span data-stu-id="91cf0-337"><span id="80287"></span>**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="91cf0-338"><span id="80387"></span>**80387** (9)</span><span class="sxs-lookup"><span data-stu-id="91cf0-338"><span id="80387"></span>**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="91cf0-339"><span id="80487"></span>**80487** (10)</span><span class="sxs-lookup"><span data-stu-id="91cf0-339"><span id="80487"></span>**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="91cf0-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium (R)** (11)</span><span class="sxs-lookup"><span data-stu-id="91cf0-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium(R) brand** (11)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-341">La personnalisation de la Pentium</span><span class="sxs-lookup"><span data-stu-id="91cf0-341">Pentium brand</span></span>

</dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="91cf0-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium (R) Pro** (12)</span><span class="sxs-lookup"><span data-stu-id="91cf0-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium(R) Pro** (12)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-343">Pentium Pro</span><span class="sxs-lookup"><span data-stu-id="91cf0-343">Pentium Pro</span></span>

</dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="91cf0-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium (R) II** (13)</span><span class="sxs-lookup"><span data-stu-id="91cf0-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium(R) II** (13)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-345">Pentium II</span><span class="sxs-lookup"><span data-stu-id="91cf0-345">Pentium II</span></span>

</dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="91cf0-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Processeur Pentium (R) avec technologie MMX (TM)** (14)</span><span class="sxs-lookup"><span data-stu-id="91cf0-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-347">Processeur Pentium avec technologie MMX</span><span class="sxs-lookup"><span data-stu-id="91cf0-347">Pentium processor with MMX technology</span></span>

</dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="91cf0-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron (TM)** (15)</span><span class="sxs-lookup"><span data-stu-id="91cf0-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron(TM)** (15)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-349">Celeron</span><span class="sxs-lookup"><span data-stu-id="91cf0-349">Celeron</span></span>

</dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="91cf0-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r_:xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium (R) II Xeon (TM)** (16)</span><span class="sxs-lookup"><span data-stu-id="91cf0-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-351">Pentium II Xeon</span><span class="sxs-lookup"><span data-stu-id="91cf0-351">Pentium II Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="91cf0-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium (R) III** (17)</span><span class="sxs-lookup"><span data-stu-id="91cf0-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium(R) III** (17)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-353">Pentium III</span><span class="sxs-lookup"><span data-stu-id="91cf0-353">Pentium III</span></span>

</dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="91cf0-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**Famille M1** (18)</span><span class="sxs-lookup"><span data-stu-id="91cf0-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="91cf0-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**Famille m2** (19)</span><span class="sxs-lookup"><span data-stu-id="91cf0-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="91cf0-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**Famille K5** (24)</span><span class="sxs-lookup"><span data-stu-id="91cf0-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**K5 Family** (24)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-357">Famille de processeurs AMD Duron</span><span class="sxs-lookup"><span data-stu-id="91cf0-357">AMD Duron  Processor Family</span></span>

</dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="91cf0-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**Famille K6** (25)</span><span class="sxs-lookup"><span data-stu-id="91cf0-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**K6 Family** (25)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-359">Famille K5</span><span class="sxs-lookup"><span data-stu-id="91cf0-359">K5 Family</span></span>

</dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="91cf0-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span><span class="sxs-lookup"><span data-stu-id="91cf0-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="91cf0-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span><span class="sxs-lookup"><span data-stu-id="91cf0-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="91cf0-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**Famille de processeurs AMD Athlon (TM)** (28)</span><span class="sxs-lookup"><span data-stu-id="91cf0-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-363">Famille de processeurs AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="91cf0-363">AMD Athlon Processor Family</span></span>

</dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="91cf0-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**Processeur AMD (R) Duron (TM)** (29)</span><span class="sxs-lookup"><span data-stu-id="91cf0-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-365">Processeur AMD Duron</span><span class="sxs-lookup"><span data-stu-id="91cf0-365">AMD  Duron Processor</span></span>

</dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="91cf0-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**Famille AMD29000** (30)</span><span class="sxs-lookup"><span data-stu-id="91cf0-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**AMD29000 Family** (30)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-367">Famille AMD2900</span><span class="sxs-lookup"><span data-stu-id="91cf0-367">AMD2900 Family</span></span>

</dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="91cf0-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2 +** (31)</span><span class="sxs-lookup"><span data-stu-id="91cf0-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="91cf0-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Famille Power PC** (32)</span><span class="sxs-lookup"><span data-stu-id="91cf0-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="91cf0-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span><span class="sxs-lookup"><span data-stu-id="91cf0-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="91cf0-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span><span class="sxs-lookup"><span data-stu-id="91cf0-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="91cf0-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603 +** (35)</span><span class="sxs-lookup"><span data-stu-id="91cf0-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="91cf0-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span><span class="sxs-lookup"><span data-stu-id="91cf0-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="91cf0-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span><span class="sxs-lookup"><span data-stu-id="91cf0-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="91cf0-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span><span class="sxs-lookup"><span data-stu-id="91cf0-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="91cf0-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span><span class="sxs-lookup"><span data-stu-id="91cf0-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="91cf0-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Famille alpha** (48)</span><span class="sxs-lookup"><span data-stu-id="91cf0-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="91cf0-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)</span><span class="sxs-lookup"><span data-stu-id="91cf0-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="91cf0-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)</span><span class="sxs-lookup"><span data-stu-id="91cf0-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="91cf0-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)</span><span class="sxs-lookup"><span data-stu-id="91cf0-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="91cf0-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)</span><span class="sxs-lookup"><span data-stu-id="91cf0-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="91cf0-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)</span><span class="sxs-lookup"><span data-stu-id="91cf0-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="91cf0-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)</span><span class="sxs-lookup"><span data-stu-id="91cf0-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="91cf0-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)</span><span class="sxs-lookup"><span data-stu-id="91cf0-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="91cf0-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**Famille mips** (64)</span><span class="sxs-lookup"><span data-stu-id="91cf0-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="91cf0-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**R4000 mips** (65)</span><span class="sxs-lookup"><span data-stu-id="91cf0-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="91cf0-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**R4200 mips** (66)</span><span class="sxs-lookup"><span data-stu-id="91cf0-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="91cf0-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**R4400 mips** (67)</span><span class="sxs-lookup"><span data-stu-id="91cf0-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="91cf0-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**R4600 mips** (68)</span><span class="sxs-lookup"><span data-stu-id="91cf0-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="91cf0-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**R10000 mips** (69)</span><span class="sxs-lookup"><span data-stu-id="91cf0-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="91cf0-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**Famille sparc** (80)</span><span class="sxs-lookup"><span data-stu-id="91cf0-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="91cf0-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span><span class="sxs-lookup"><span data-stu-id="91cf0-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="91cf0-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**MICROSPARC II** (82)</span><span class="sxs-lookup"><span data-stu-id="91cf0-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="91cf0-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**MicroSPARC IIep** (83)</span><span class="sxs-lookup"><span data-stu-id="91cf0-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="91cf0-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span><span class="sxs-lookup"><span data-stu-id="91cf0-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="91cf0-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**ULTRASPARC II** (85)</span><span class="sxs-lookup"><span data-stu-id="91cf0-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="91cf0-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (86)</span><span class="sxs-lookup"><span data-stu-id="91cf0-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="91cf0-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**ULTRASPARC III** (87)</span><span class="sxs-lookup"><span data-stu-id="91cf0-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="91cf0-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)</span><span class="sxs-lookup"><span data-stu-id="91cf0-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="91cf0-400"><span id="68040"></span>**68040** (96)</span><span class="sxs-lookup"><span data-stu-id="91cf0-400"><span id="68040"></span>**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="91cf0-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**famille 68xxx** (97)</span><span class="sxs-lookup"><span data-stu-id="91cf0-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="91cf0-402"><span id="68000"></span>**68000** (98)</span><span class="sxs-lookup"><span data-stu-id="91cf0-402"><span id="68000"></span>**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="91cf0-403"><span id="68010"></span>**68010** (99)</span><span class="sxs-lookup"><span data-stu-id="91cf0-403"><span id="68010"></span>**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="91cf0-404"><span id="68020"></span>**68020** (100)</span><span class="sxs-lookup"><span data-stu-id="91cf0-404"><span id="68020"></span>**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="91cf0-405"><span id="68030"></span>**68030** (101)</span><span class="sxs-lookup"><span data-stu-id="91cf0-405"><span id="68030"></span>**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="91cf0-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Famille Hobbit** (112)</span><span class="sxs-lookup"><span data-stu-id="91cf0-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="91cf0-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Famille Crusoe (TM) TM5000** (120)</span><span class="sxs-lookup"><span data-stu-id="91cf0-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-408">Famille Crusoe TM5000</span><span class="sxs-lookup"><span data-stu-id="91cf0-408">Crusoe TM5000 Family</span></span>

</dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="91cf0-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Famille Crusoe (TM) TM3000** (121)</span><span class="sxs-lookup"><span data-stu-id="91cf0-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-410">Famille Crusoe TM3000</span><span class="sxs-lookup"><span data-stu-id="91cf0-410">Crusoe TM3000 Family</span></span>

</dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="91cf0-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Famille Efficeon (TM) TM8000** (122)</span><span class="sxs-lookup"><span data-stu-id="91cf0-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-412">Famille Efficeon8000</span><span class="sxs-lookup"><span data-stu-id="91cf0-412">Efficeon8000 Family</span></span>

</dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="91cf0-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span><span class="sxs-lookup"><span data-stu-id="91cf0-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="91cf0-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Processeur Itanium (** 130)</span><span class="sxs-lookup"><span data-stu-id="91cf0-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Itanium(TM) Processor** (130)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-415">Processeur Itanium</span><span class="sxs-lookup"><span data-stu-id="91cf0-415">Itanium  Processor</span></span>

</dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="91cf0-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**Famille de processeurs AMD Athlon (TM) 64** (131)</span><span class="sxs-lookup"><span data-stu-id="91cf0-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-417">AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="91cf0-417">AMD Athlon</span></span> 

</dd> <dt>

<span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>

<span data-ttu-id="91cf0-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**Famille AMD Opteron (TM)** (132)</span><span class="sxs-lookup"><span data-stu-id="91cf0-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**AMD Opteron(TM) Family** (132)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-419">Famille AMD Opteron</span><span class="sxs-lookup"><span data-stu-id="91cf0-419">AMD Opteron  Family</span></span>

</dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="91cf0-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**Famille PA-RISC** (144)</span><span class="sxs-lookup"><span data-stu-id="91cf0-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="91cf0-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span><span class="sxs-lookup"><span data-stu-id="91cf0-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="91cf0-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span><span class="sxs-lookup"><span data-stu-id="91cf0-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="91cf0-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span><span class="sxs-lookup"><span data-stu-id="91cf0-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="91cf0-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span><span class="sxs-lookup"><span data-stu-id="91cf0-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="91cf0-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span><span class="sxs-lookup"><span data-stu-id="91cf0-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="91cf0-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span><span class="sxs-lookup"><span data-stu-id="91cf0-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="91cf0-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**Famille V30** (160)</span><span class="sxs-lookup"><span data-stu-id="91cf0-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="91cf0-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium (R) III Xeon (TM)** (176)</span><span class="sxs-lookup"><span data-stu-id="91cf0-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-429">Pentium III Xeon</span><span class="sxs-lookup"><span data-stu-id="91cf0-429">Pentium III Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="91cf0-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Processeur Pentium (r) III avec technologie Intel (r) SpeedStep (TM)** (177)</span><span class="sxs-lookup"><span data-stu-id="91cf0-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-431">Processeur Pentium III avec technologie Intel SpeedStep</span><span class="sxs-lookup"><span data-stu-id="91cf0-431">Pentium III Processor with Intel SpeedStep Technology</span></span>

</dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="91cf0-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium (R) 4** (178)</span><span class="sxs-lookup"><span data-stu-id="91cf0-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium(R) 4** (178)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-433">Pentium 4</span><span class="sxs-lookup"><span data-stu-id="91cf0-433">Pentium 4</span></span>

</dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="91cf0-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel (R) Xeon (TM)** (179)</span><span class="sxs-lookup"><span data-stu-id="91cf0-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-435">Processeur Intel Xeon</span><span class="sxs-lookup"><span data-stu-id="91cf0-435">Intel Xeon</span></span>

</dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="91cf0-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**Famille AS400** (180)</span><span class="sxs-lookup"><span data-stu-id="91cf0-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="91cf0-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Processeur Intel (R) Xeon (TM) MP** (181)</span><span class="sxs-lookup"><span data-stu-id="91cf0-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-438">Processeur Intel Xeon MP</span><span class="sxs-lookup"><span data-stu-id="91cf0-438">Intel Xeon Processor MP</span></span>

</dd> <dt>

<span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>

<span data-ttu-id="91cf0-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**Famille AMD AthlonXP (TM)** (182)</span><span class="sxs-lookup"><span data-stu-id="91cf0-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**AMD AthlonXP(TM) Family** (182)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-440">Famille AMD AthlonXP</span><span class="sxs-lookup"><span data-stu-id="91cf0-440">AMD AthlonXP Family</span></span>

</dd> <dt>

<span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>

<span data-ttu-id="91cf0-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**Famille AMD AthlonMP (TM)** (183)</span><span class="sxs-lookup"><span data-stu-id="91cf0-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**AMD AthlonMP(TM) Family** (183)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-442">Famille AMD AthlonMP</span><span class="sxs-lookup"><span data-stu-id="91cf0-442">AMD AthlonMP Family</span></span>

</dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="91cf0-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel (r) Itanium (r) 2** (184)</span><span class="sxs-lookup"><span data-stu-id="91cf0-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-444">Intel Itanium 2</span><span class="sxs-lookup"><span data-stu-id="91cf0-444">Intel Itanium 2</span></span>

</dd> <dt>

<span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>

<span data-ttu-id="91cf0-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Processeur Intel Pentium M** (185)</span><span class="sxs-lookup"><span data-stu-id="91cf0-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Intel Pentium M Processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="91cf0-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span><span class="sxs-lookup"><span data-stu-id="91cf0-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>

<span data-ttu-id="91cf0-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**Famille IBM390** (200)</span><span class="sxs-lookup"><span data-stu-id="91cf0-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**IBM390 Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="G4"></span><span id="g4"></span>

<span data-ttu-id="91cf0-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span><span class="sxs-lookup"><span data-stu-id="91cf0-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="G5"></span><span id="g5"></span>

<span data-ttu-id="91cf0-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span><span class="sxs-lookup"><span data-stu-id="91cf0-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="G6"></span><span id="g6"></span>

<span data-ttu-id="91cf0-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span><span class="sxs-lookup"><span data-stu-id="91cf0-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>

<span data-ttu-id="91cf0-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**base z/architecture** (204)</span><span class="sxs-lookup"><span data-stu-id="91cf0-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/Architecture base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="91cf0-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span><span class="sxs-lookup"><span data-stu-id="91cf0-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="91cf0-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span><span class="sxs-lookup"><span data-stu-id="91cf0-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="91cf0-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span><span class="sxs-lookup"><span data-stu-id="91cf0-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="91cf0-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span><span class="sxs-lookup"><span data-stu-id="91cf0-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="91cf0-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span><span class="sxs-lookup"><span data-stu-id="91cf0-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="91cf0-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span><span class="sxs-lookup"><span data-stu-id="91cf0-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="91cf0-458"><span id="6x86"></span><span id="6X86"></span>**6 x86** (300)</span><span class="sxs-lookup"><span data-stu-id="91cf0-458"><span id="6x86"></span><span id="6X86"></span>**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="91cf0-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span><span class="sxs-lookup"><span data-stu-id="91cf0-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="91cf0-460"><span id="MII"></span><span id="mii"></span>**MII** (302)</span><span class="sxs-lookup"><span data-stu-id="91cf0-460"><span id="MII"></span><span id="mii"></span>**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="91cf0-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span><span class="sxs-lookup"><span data-stu-id="91cf0-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="91cf0-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span><span class="sxs-lookup"><span data-stu-id="91cf0-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="91cf0-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Processeur vidéo** (500)</span><span class="sxs-lookup"><span data-stu-id="91cf0-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Video Processor** (500)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91cf0-464">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="91cf0-464">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-465">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="91cf0-465">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-467">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="91cf0-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-468">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91cf0-468">Date and time the object was installed.</span></span> <span data-ttu-id="91cf0-469">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="91cf0-469">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="91cf0-470">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-470">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-471">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="91cf0-471">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-472">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91cf0-472">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-473">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-473">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-474">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="91cf0-474">Last error code reported by the logical device.</span></span>

<span data-ttu-id="91cf0-475">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-476">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="91cf0-476">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-477">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91cf0-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-478">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-479">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrProcessorLoad "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" percent ")</span><span class="sxs-lookup"><span data-stu-id="91cf0-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-480">Chargement du processeur, en moyenne au cours de la dernière minute, en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="91cf0-480">Loading of the processor, averaged over the last minute, in a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-481">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="91cf0-481">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-482">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91cf0-482">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-483">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-484">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 006,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" mégahertz ")</span><span class="sxs-lookup"><span data-stu-id="91cf0-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-485">Vitesse maximale (en mégahertz) du processeur.</span><span class="sxs-lookup"><span data-stu-id="91cf0-485">Maximum speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-486">**Nom**</span><span class="sxs-lookup"><span data-stu-id="91cf0-486">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-488">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-489">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="91cf0-489">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-490">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="91cf0-490">Label by which the object is known.</span></span> <span data-ttu-id="91cf0-491">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="91cf0-491">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="91cf0-492">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-492">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-493">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="91cf0-493">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-494">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-495">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-496">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ processeur CIM**.**Family**»)</span><span class="sxs-lookup"><span data-stu-id="91cf0-496">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-497">Description du type de la famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="91cf0-497">Description of the processor family type.</span></span> <span data-ttu-id="91cf0-498">Cette propriété est utilisée lorsque la propriété **Family** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="91cf0-498">This property is used when the **Family** property is set to 1 ("Other").</span></span> <span data-ttu-id="91cf0-499">Cette chaîne doit être définie sur Null lorsque la propriété **Family** est une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="91cf0-499">This string should be set to null when the **Family** property is a value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="91cf0-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-501">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-502">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-503">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91cf0-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-504">Identificateur d’appareil Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="91cf0-504">Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="91cf0-505">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="91cf0-506">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="91cf0-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="91cf0-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-508">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91cf0-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-509">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-510">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="91cf0-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="91cf0-511">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="91cf0-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91cf0-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="91cf0-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="91cf0-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="91cf0-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="91cf0-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="91cf0-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="91cf0-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="91cf0-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-516">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="91cf0-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="91cf0-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="91cf0-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-518">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="91cf0-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="91cf0-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="91cf0-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-520">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="91cf0-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="91cf0-521">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="91cf0-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="91cf0-522">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="91cf0-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="91cf0-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="91cf0-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-524">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="91cf0-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="91cf0-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="91cf0-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-526">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="91cf0-526">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91cf0-527">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="91cf0-527">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-528">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91cf0-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-529">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-530">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="91cf0-530">If **True**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="91cf0-531">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="91cf0-531">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="91cf0-532">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="91cf0-532">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="91cf0-533">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="91cf0-533">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="91cf0-534">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-534">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-535">**Rôle**</span><span class="sxs-lookup"><span data-stu-id="91cf0-535">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-536">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-536">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-537">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-538">Chaîne de forme libre qui décrit le rôle du processeur.</span><span class="sxs-lookup"><span data-stu-id="91cf0-538">Free-form string that describes the role of the processor.</span></span> <span data-ttu-id="91cf0-539">Par exemple, « processeur central » ou « processeur mathématique ».</span><span class="sxs-lookup"><span data-stu-id="91cf0-539">For example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-540">**État**</span><span class="sxs-lookup"><span data-stu-id="91cf0-540">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-541">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-542">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-543">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="91cf0-543">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-544">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91cf0-544">Current status of the object.</span></span>

<span data-ttu-id="91cf0-545">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-545">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="91cf0-546">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="91cf0-546">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="91cf0-547">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-547">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="91cf0-548">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-548">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="91cf0-549">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-549">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91cf0-550">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="91cf0-550">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="91cf0-551">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-551">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="91cf0-552">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-552">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="91cf0-553">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-553">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="91cf0-554">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-554">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="91cf0-555">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-555">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="91cf0-556">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-556">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="91cf0-557">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-557">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="91cf0-558">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="91cf0-558">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91cf0-559">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="91cf0-559">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-560">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91cf0-560">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-561">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-562">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="91cf0-562">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-563">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="91cf0-563">State of the logical device.</span></span> <span data-ttu-id="91cf0-564">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="91cf0-564">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="91cf0-565">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-565">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91cf0-566">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="91cf0-566">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91cf0-567">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="91cf0-567">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="91cf0-568">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="91cf0-568">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="91cf0-569">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="91cf0-569">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="91cf0-570">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="91cf0-570">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91cf0-571">**Exécution pas à pas**</span><span class="sxs-lookup"><span data-stu-id="91cf0-571">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-572">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-572">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-573">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-573">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-574">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ processeur CIM**».**Family**»)</span><span class="sxs-lookup"><span data-stu-id="91cf0-574">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-575">Chaîne de forme libre qui indique le niveau de révision du processeur au sein de la famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="91cf0-575">Free-form string that indicates the revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-576">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91cf0-576">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-577">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-578">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-579">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91cf0-579">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-580">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="91cf0-580">Scoping system's creation class name.</span></span>

<span data-ttu-id="91cf0-581">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-581">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-582">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="91cf0-582">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-583">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-584">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-585">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91cf0-585">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-586">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="91cf0-586">Scoping system's name.</span></span>

<span data-ttu-id="91cf0-587">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-588">**UniqueId**</span><span class="sxs-lookup"><span data-stu-id="91cf0-588">**UniqueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-589">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91cf0-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-590">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-590">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-591">Identificateur global unique du processeur.</span><span class="sxs-lookup"><span data-stu-id="91cf0-591">Globally unique identifier for the processor.</span></span> <span data-ttu-id="91cf0-592">Cet identificateur peut uniquement être unique au sein d’une famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="91cf0-592">This identifier can only be unique within a processor family.</span></span>

</dd> <dt>

<span data-ttu-id="91cf0-593">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="91cf0-593">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91cf0-594">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91cf0-594">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-595">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91cf0-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91cf0-596">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Processeur DMTF \| 006,7 ")</span><span class="sxs-lookup"><span data-stu-id="91cf0-596">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.7")</span></span>
</dt> </dl>

<span data-ttu-id="91cf0-597">Les informations de socket de processeur, qui incluent des données sur la mise à niveau du processeur (si les mises à niveau sont prises en charge).</span><span class="sxs-lookup"><span data-stu-id="91cf0-597">CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91cf0-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="91cf0-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91cf0-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="91cf0-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="91cf0-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Carte fille** (3)</span><span class="sxs-lookup"><span data-stu-id="91cf0-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="91cf0-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**Connecteur ZIF** (4)</span><span class="sxs-lookup"><span data-stu-id="91cf0-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="91cf0-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Remplacement/** superposition (5)</span><span class="sxs-lookup"><span data-stu-id="91cf0-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Replacement/Piggy Back** (5)</span></span>


</dt> <dd>

<span data-ttu-id="91cf0-603">Remplacement ou remontée</span><span class="sxs-lookup"><span data-stu-id="91cf0-603">Replacement or piggy back</span></span>

</dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="91cf0-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (6)</span><span class="sxs-lookup"><span data-stu-id="91cf0-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="91cf0-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**Socket LIF** (7)</span><span class="sxs-lookup"><span data-stu-id="91cf0-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="91cf0-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Emplacement 1** (8)</span><span class="sxs-lookup"><span data-stu-id="91cf0-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="91cf0-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Emplacement 2** (9)</span><span class="sxs-lookup"><span data-stu-id="91cf0-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="91cf0-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**Socket de broche 370** (10)</span><span class="sxs-lookup"><span data-stu-id="91cf0-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="91cf0-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Emplacement A** (11)</span><span class="sxs-lookup"><span data-stu-id="91cf0-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="91cf0-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Emplacement M** (12)</span><span class="sxs-lookup"><span data-stu-id="91cf0-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="91cf0-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span><span class="sxs-lookup"><span data-stu-id="91cf0-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="91cf0-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (socket 462)** (14)</span><span class="sxs-lookup"><span data-stu-id="91cf0-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="91cf0-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span><span class="sxs-lookup"><span data-stu-id="91cf0-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="91cf0-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span><span class="sxs-lookup"><span data-stu-id="91cf0-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="91cf0-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span><span class="sxs-lookup"><span data-stu-id="91cf0-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="91cf0-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span><span class="sxs-lookup"><span data-stu-id="91cf0-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span></span>


<span data-ttu-id="91cf0-617"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="91cf0-617"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="91cf0-618">Notes</span><span class="sxs-lookup"><span data-stu-id="91cf0-618">Remarks</span></span>

<span data-ttu-id="91cf0-619">La classe de **\_ processeur CIM** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-619">The **CIM\_Processor** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="91cf0-620">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="91cf0-620">WMI does not implement this class.</span></span> <span data-ttu-id="91cf0-621">Pour les classes WMI dérivées du **\_ processeur CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="91cf0-621">For WMI classes derived from **CIM\_Processor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="91cf0-622">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="91cf0-622">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="91cf0-623">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="91cf0-623">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="91cf0-624">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91cf0-624">Requirements</span></span>



| <span data-ttu-id="91cf0-625">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91cf0-625">Requirement</span></span> | <span data-ttu-id="91cf0-626">Valeur</span><span class="sxs-lookup"><span data-stu-id="91cf0-626">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91cf0-627">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91cf0-627">Minimum supported client</span></span><br/> | <span data-ttu-id="91cf0-628">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91cf0-628">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91cf0-629">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91cf0-629">Minimum supported server</span></span><br/> | <span data-ttu-id="91cf0-630">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91cf0-630">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91cf0-631">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="91cf0-631">Namespace</span></span><br/>                | <span data-ttu-id="91cf0-632">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="91cf0-632">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91cf0-633">MOF</span><span class="sxs-lookup"><span data-stu-id="91cf0-633">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91cf0-634"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91cf0-634"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91cf0-635">DLL</span><span class="sxs-lookup"><span data-stu-id="91cf0-635">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91cf0-636"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91cf0-636"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91cf0-637">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91cf0-637">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91cf0-638">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="91cf0-638">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

