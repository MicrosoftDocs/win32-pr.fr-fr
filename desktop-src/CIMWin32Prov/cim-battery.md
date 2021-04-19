---
description: La \_ classe de batterie CIM représente les fonctionnalités et la gestion de l’unité logique de batterie. Cette classe s’applique aux batteries dans les systèmes d’ordinateurs portables et autres batteries internes et externes.
ms.assetid: af127b7a-021b-4cd8-af1b-176aff760858
ms.tgt_platform: multiple
title: Classe CIM_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Battery
- CIM_Battery.Caption
- CIM_Battery.Description
- CIM_Battery.InstallDate
- CIM_Battery.Name
- CIM_Battery.Status
- CIM_Battery.Availability
- CIM_Battery.ConfigManagerErrorCode
- CIM_Battery.ConfigManagerUserConfig
- CIM_Battery.CreationClassName
- CIM_Battery.DeviceID
- CIM_Battery.PowerManagementCapabilities
- CIM_Battery.ErrorCleared
- CIM_Battery.ErrorDescription
- CIM_Battery.LastErrorCode
- CIM_Battery.PNPDeviceID
- CIM_Battery.PowerManagementSupported
- CIM_Battery.StatusInfo
- CIM_Battery.SystemCreationClassName
- CIM_Battery.SystemName
- CIM_Battery.BatteryStatus
- CIM_Battery.Chemistry
- CIM_Battery.DesignCapacity
- CIM_Battery.DesignVoltage
- CIM_Battery.EstimatedChargeRemaining
- CIM_Battery.EstimatedRunTime
- CIM_Battery.ExpectedLife
- CIM_Battery.FullChargeCapacity
- CIM_Battery.MaxRechargeTime
- CIM_Battery.SmartBatteryVersion
- CIM_Battery.TimeOnBattery
- CIM_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3719b2700c69cfa58921bed1242aa8a6de158466
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515163"
---
# <a name="cim_battery-class"></a><span data-ttu-id="2fafa-104">\_Classe de batterie CIM</span><span class="sxs-lookup"><span data-stu-id="2fafa-104">CIM\_Battery class</span></span>

<span data-ttu-id="2fafa-105">La classe de **\_ batterie CIM** représente les fonctionnalités et la gestion de l’unité logique de batterie.</span><span class="sxs-lookup"><span data-stu-id="2fafa-105">The **CIM\_Battery** class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="2fafa-106">Cette classe s’applique aux batteries dans les systèmes d’ordinateurs portables et autres batteries internes et externes.</span><span class="sxs-lookup"><span data-stu-id="2fafa-106">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fafa-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2fafa-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2fafa-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2fafa-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2fafa-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2fafa-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2fafa-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2fafa-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fafa-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fafa-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C548-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Battery : CIM_LogicalDevice
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
  uint16   BatteryStatus;
  uint16   Chemistry;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  uint32   MaxRechargeTime;
  string   SmartBatteryVersion;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="2fafa-112">Membres</span><span class="sxs-lookup"><span data-stu-id="2fafa-112">Members</span></span>

<span data-ttu-id="2fafa-113">La classe de **\_ batterie CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2fafa-113">The **CIM\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="2fafa-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2fafa-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2fafa-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2fafa-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2fafa-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2fafa-116">Methods</span></span>

<span data-ttu-id="2fafa-117">La classe de **\_ batterie CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2fafa-117">The **CIM\_Battery** class has these methods.</span></span>



| <span data-ttu-id="2fafa-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="2fafa-118">Method</span></span>                                                             | <span data-ttu-id="2fafa-119">Description</span><span class="sxs-lookup"><span data-stu-id="2fafa-119">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fafa-120">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="2fafa-120">**Reset**</span></span>](reset-method-in-class-cim-battery.md)                 | <span data-ttu-id="2fafa-121">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2fafa-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="2fafa-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="2fafa-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="2fafa-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2fafa-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-battery.md) | <span data-ttu-id="2fafa-124">Définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="2fafa-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="2fafa-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="2fafa-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2fafa-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2fafa-126">Properties</span></span>

<span data-ttu-id="2fafa-127">La classe de **\_ batterie CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2fafa-127">The **CIM\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fafa-128">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="2fafa-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2fafa-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-131">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-132">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2fafa-132">Availability and status of the device.</span></span>

<span data-ttu-id="2fafa-133">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2fafa-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2fafa-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2fafa-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2fafa-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2fafa-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="2fafa-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2fafa-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="2fafa-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2fafa-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="2fafa-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2fafa-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="2fafa-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2fafa-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="2fafa-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2fafa-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="2fafa-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2fafa-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="2fafa-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2fafa-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="2fafa-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2fafa-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="2fafa-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2fafa-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="2fafa-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2fafa-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="2fafa-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-147">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2fafa-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2fafa-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="2fafa-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-149">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="2fafa-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2fafa-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="2fafa-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-151">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="2fafa-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2fafa-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="2fafa-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2fafa-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="2fafa-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-154">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="2fafa-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2fafa-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="2fafa-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-156">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="2fafa-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2fafa-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="2fafa-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-158">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="2fafa-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2fafa-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="2fafa-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-160">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="2fafa-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2fafa-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="2fafa-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-162">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="2fafa-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2fafa-163">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="2fafa-163">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-164">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2fafa-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-166">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-167">Description de l’état de facturation de la batterie.</span><span class="sxs-lookup"><span data-stu-id="2fafa-167">Description of the battery's charge status.</span></span> <span data-ttu-id="2fafa-168">La valeur 10 n’est pas valide dans le schéma CIM, qui ne représente aucune batterie en cours d’installation dans l’interface DMI (Desktop Management Interface).</span><span class="sxs-lookup"><span data-stu-id="2fafa-168">The value 10 is not valid in the CIM schema, which represents no battery being installed in Desktop Management Interface (DMI).</span></span> <span data-ttu-id="2fafa-169">Dans ce cas, l’objet ne doit pas être instancié.</span><span class="sxs-lookup"><span data-stu-id="2fafa-169">In this case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2fafa-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2fafa-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-171">Autre.</span><span class="sxs-lookup"><span data-stu-id="2fafa-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2fafa-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2fafa-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-173">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="2fafa-173">Unknown.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="2fafa-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Entièrement facturée** (3)</span><span class="sxs-lookup"><span data-stu-id="2fafa-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-175">Entièrement chargé.</span><span class="sxs-lookup"><span data-stu-id="2fafa-175">Fully charged.</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="2fafa-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Faible** (4)</span><span class="sxs-lookup"><span data-stu-id="2fafa-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-177">Faible.</span><span class="sxs-lookup"><span data-stu-id="2fafa-177">Low.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2fafa-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (5)</span><span class="sxs-lookup"><span data-stu-id="2fafa-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-179">Critique.</span><span class="sxs-lookup"><span data-stu-id="2fafa-179">Critical.</span></span>

</dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="2fafa-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>En **charge** (6)</span><span class="sxs-lookup"><span data-stu-id="2fafa-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-181">Perception.</span><span class="sxs-lookup"><span data-stu-id="2fafa-181">Charging.</span></span>

</dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="2fafa-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>En **charge et élevé** (7)</span><span class="sxs-lookup"><span data-stu-id="2fafa-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-183">En charge et élevé.</span><span class="sxs-lookup"><span data-stu-id="2fafa-183">Charging and high.</span></span>

</dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="2fafa-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>En **charge et bas** (8)</span><span class="sxs-lookup"><span data-stu-id="2fafa-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-185">En charge et bas.</span><span class="sxs-lookup"><span data-stu-id="2fafa-185">Charging and low.</span></span>

</dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="2fafa-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>En **charge et critique** (9)</span><span class="sxs-lookup"><span data-stu-id="2fafa-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-187">En charge et critique.</span><span class="sxs-lookup"><span data-stu-id="2fafa-187">Charging and critical.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="2fafa-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (10)</span><span class="sxs-lookup"><span data-stu-id="2fafa-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-189">Non défini.</span><span class="sxs-lookup"><span data-stu-id="2fafa-189">Undefined.</span></span>

</dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="2fafa-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partiellement facturé** (11)</span><span class="sxs-lookup"><span data-stu-id="2fafa-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-191">Partiellement facturé.</span><span class="sxs-lookup"><span data-stu-id="2fafa-191">Partially charged.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2fafa-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2fafa-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-195">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-196">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2fafa-196">A short textual description of the object.</span></span>

<span data-ttu-id="2fafa-197">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-198">**Chimique**</span><span class="sxs-lookup"><span data-stu-id="2fafa-198">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-199">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2fafa-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-201">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-202">Énumération qui décrit la chimie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="2fafa-202">Enumeration that describes the battery's chemistry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2fafa-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2fafa-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-204">Autre.</span><span class="sxs-lookup"><span data-stu-id="2fafa-204">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2fafa-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2fafa-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-206">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="2fafa-206">Unknown.</span></span>

</dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="2fafa-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Acidité** (3)</span><span class="sxs-lookup"><span data-stu-id="2fafa-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Lead Acid** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-208">L’acide principal.</span><span class="sxs-lookup"><span data-stu-id="2fafa-208">Lead acid.</span></span>

</dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="2fafa-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel cadmium** (4)</span><span class="sxs-lookup"><span data-stu-id="2fafa-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel Cadmium** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-210">Nickel cadmium.</span><span class="sxs-lookup"><span data-stu-id="2fafa-210">Nickel cadmium.</span></span>

</dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="2fafa-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel-métal-hydrure** (5)</span><span class="sxs-lookup"><span data-stu-id="2fafa-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel Metal Hydride** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-212">Nickel metal-hydrure.</span><span class="sxs-lookup"><span data-stu-id="2fafa-212">Nickel metal hydride.</span></span>

</dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="2fafa-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-ion** (6)</span><span class="sxs-lookup"><span data-stu-id="2fafa-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-ion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-214">Lithium-ion.</span><span class="sxs-lookup"><span data-stu-id="2fafa-214">Lithium ion.</span></span>

</dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="2fafa-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Air zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="2fafa-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinc air** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-216">Air zinc.</span><span class="sxs-lookup"><span data-stu-id="2fafa-216">Zinc air.</span></span>

</dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="2fafa-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium-polymère** (8)</span><span class="sxs-lookup"><span data-stu-id="2fafa-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium Polymer** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-218">Lithium-polymère.</span><span class="sxs-lookup"><span data-stu-id="2fafa-218">Lithium polymer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2fafa-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2fafa-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-220">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-222">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2fafa-222">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-223">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="2fafa-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2fafa-224">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2fafa-225">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-225">**This device is working properly.**</span></span> <span data-ttu-id="2fafa-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="2fafa-226">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2fafa-227">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-227">**This device is not configured correctly.**</span></span> <span data-ttu-id="2fafa-228">(1)</span><span class="sxs-lookup"><span data-stu-id="2fafa-228">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2fafa-229">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-229">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2fafa-230">(2)</span><span class="sxs-lookup"><span data-stu-id="2fafa-230">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2fafa-231">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-231">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2fafa-232">(3)</span><span class="sxs-lookup"><span data-stu-id="2fafa-232">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2fafa-233">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-233">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2fafa-234">(4)</span><span class="sxs-lookup"><span data-stu-id="2fafa-234">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2fafa-235">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-235">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2fafa-236">(5)</span><span class="sxs-lookup"><span data-stu-id="2fafa-236">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2fafa-237">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-237">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2fafa-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="2fafa-238">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2fafa-239">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-239">**Cannot filter.**</span></span> <span data-ttu-id="2fafa-240">(7)</span><span class="sxs-lookup"><span data-stu-id="2fafa-240">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2fafa-241">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-241">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2fafa-242">(8)</span><span class="sxs-lookup"><span data-stu-id="2fafa-242">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2fafa-243">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-243">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2fafa-244">(9)</span><span class="sxs-lookup"><span data-stu-id="2fafa-244">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2fafa-245">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-245">**This device cannot start.**</span></span> <span data-ttu-id="2fafa-246">(10)</span><span class="sxs-lookup"><span data-stu-id="2fafa-246">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2fafa-247">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-247">**This device failed.**</span></span> <span data-ttu-id="2fafa-248">(11)</span><span class="sxs-lookup"><span data-stu-id="2fafa-248">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2fafa-249">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-249">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2fafa-250">douze</span><span class="sxs-lookup"><span data-stu-id="2fafa-250">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2fafa-251">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-251">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2fafa-252">(13)</span><span class="sxs-lookup"><span data-stu-id="2fafa-252">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2fafa-253">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-253">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2fafa-254">(14)</span><span class="sxs-lookup"><span data-stu-id="2fafa-254">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2fafa-255">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-255">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2fafa-256">(15)</span><span class="sxs-lookup"><span data-stu-id="2fafa-256">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2fafa-257">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-257">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2fafa-258">(16)</span><span class="sxs-lookup"><span data-stu-id="2fafa-258">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2fafa-259">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-259">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2fafa-260">(17)</span><span class="sxs-lookup"><span data-stu-id="2fafa-260">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2fafa-261">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-261">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2fafa-262">(18)</span><span class="sxs-lookup"><span data-stu-id="2fafa-262">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2fafa-263">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-263">**Failure using the VxD loader.**</span></span> <span data-ttu-id="2fafa-264">(19)</span><span class="sxs-lookup"><span data-stu-id="2fafa-264">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2fafa-265">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-265">**Your registry might be corrupted.**</span></span> <span data-ttu-id="2fafa-266">(20)</span><span class="sxs-lookup"><span data-stu-id="2fafa-266">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2fafa-267">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-267">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2fafa-268">(21)</span><span class="sxs-lookup"><span data-stu-id="2fafa-268">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2fafa-269">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-269">**This device is disabled.**</span></span> <span data-ttu-id="2fafa-270">(22)</span><span class="sxs-lookup"><span data-stu-id="2fafa-270">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2fafa-271">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-271">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2fafa-272">(23)</span><span class="sxs-lookup"><span data-stu-id="2fafa-272">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2fafa-273">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-273">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2fafa-274">(24)</span><span class="sxs-lookup"><span data-stu-id="2fafa-274">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2fafa-275">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-275">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2fafa-276">(25)</span><span class="sxs-lookup"><span data-stu-id="2fafa-276">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2fafa-277">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2fafa-278">(26)</span><span class="sxs-lookup"><span data-stu-id="2fafa-278">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2fafa-279">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-279">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2fafa-280">(27)</span><span class="sxs-lookup"><span data-stu-id="2fafa-280">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2fafa-281">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-281">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2fafa-282">(28)</span><span class="sxs-lookup"><span data-stu-id="2fafa-282">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2fafa-283">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-283">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2fafa-284">(29)</span><span class="sxs-lookup"><span data-stu-id="2fafa-284">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2fafa-285">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-285">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2fafa-286">(30)</span><span class="sxs-lookup"><span data-stu-id="2fafa-286">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2fafa-287">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2fafa-287">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2fafa-288">31</span><span class="sxs-lookup"><span data-stu-id="2fafa-288">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2fafa-289">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2fafa-289">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-290">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2fafa-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-292">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2fafa-292">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-293">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2fafa-293">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2fafa-294">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-295">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2fafa-295">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-298">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2fafa-298">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-299">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="2fafa-299">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2fafa-300">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="2fafa-300">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2fafa-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-302">**Description**</span><span class="sxs-lookup"><span data-stu-id="2fafa-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-305">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2fafa-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-306">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2fafa-306">A textual description of the object.</span></span>

<span data-ttu-id="2fafa-307">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-308">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="2fafa-308">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-309">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-311">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,8 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatts heure-heures ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-312">Capacité conçue de la batterie en milliwatts heure heures.</span><span class="sxs-lookup"><span data-stu-id="2fafa-312">Designed capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="2fafa-313">Si cette propriété n’est pas prise en charge, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="2fafa-313">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-314">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="2fafa-314">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-315">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2fafa-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-317">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,9 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-317">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-318">Tension de la batterie en millivolts.</span><span class="sxs-lookup"><span data-stu-id="2fafa-318">Designed voltage of the battery in millivolts.</span></span> <span data-ttu-id="2fafa-319">Si cet attribut n’est pas pris en charge, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="2fafa-319">If this attribute is not supported, enter 0.</span></span>

<span data-ttu-id="2fafa-320">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2fafa-320">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-321">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2fafa-321">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-324">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2fafa-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-325">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2fafa-325">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2fafa-326">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-327">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2fafa-327">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-328">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2fafa-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-330">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="2fafa-330">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2fafa-331">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-332">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2fafa-332">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-335">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="2fafa-335">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2fafa-336">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-337">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="2fafa-337">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-338">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2fafa-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-340">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("pourcentage")</span><span class="sxs-lookup"><span data-stu-id="2fafa-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-341">Pourcentage estimé des frais complets restants.</span><span class="sxs-lookup"><span data-stu-id="2fafa-341">Estimated percentage of the remaining full charge.</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-342">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="2fafa-342">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-343">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-345">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutes ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-346">Durée estimée, en minutes, jusqu’à ce que la charge de la batterie soit épuisée dans les conditions de charge actuelles si l’alimentation de l’utilitaire est désactivée, est perdue et reste inactive, ou si un ordinateur portable est déconnecté d’une source d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="2fafa-346">Estimated time, in minutes, until the battery charge is depleted under the present load conditions if the utility power is off, is lost and remains off, or if a laptop is disconnected from a power source.</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-347">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="2fafa-347">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-348">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-350">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-350">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-351">Durée de vie prévue de la batterie, en minutes, en supposant que la batterie est entièrement chargée.</span><span class="sxs-lookup"><span data-stu-id="2fafa-351">Battery's expected lifetime, in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="2fafa-352">Cette propriété représente la durée de vie totale attendue de la batterie, pas sa durée de vie restante, qui est indiquée par la propriété **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="2fafa-352">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-353">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="2fafa-353">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-354">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-356">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatts heure-heures ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-357">Capacité de charge totale de la batterie en milliwatts heure heures.</span><span class="sxs-lookup"><span data-stu-id="2fafa-357">The full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="2fafa-358">Comparez cette valeur à la propriété **DesignCapacity** pour déterminer à quel moment la batterie doit être remplacée.</span><span class="sxs-lookup"><span data-stu-id="2fafa-358">Compare this value to the **DesignCapacity** property to determine when the battery requires replacement.</span></span> <span data-ttu-id="2fafa-359">La durée de vie d’une batterie est généralement lorsque la propriété **FullChargeCapacity** passe sous 80% de la propriété **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="2fafa-359">A battery's end-life is typically when the **FullChargeCapacity** property falls below 80 percent of the **DesignCapacity** property.</span></span> <span data-ttu-id="2fafa-360">Si cette propriété n’est pas prise en charge, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="2fafa-360">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-361">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2fafa-361">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-362">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2fafa-362">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-364">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-365">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="2fafa-365">Indicates when the object was installed.</span></span> <span data-ttu-id="2fafa-366">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="2fafa-366">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2fafa-367">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-367">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-368">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2fafa-368">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-369">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-371">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2fafa-371">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2fafa-372">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-373">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="2fafa-373">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-374">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-376">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-377">Durée maximale, en minutes, pour le chargement complet de la batterie.</span><span class="sxs-lookup"><span data-stu-id="2fafa-377">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="2fafa-378">Cette propriété représente le temps de rechargement d’une batterie entièrement épuisée, et non le temps de chargement restant en cours, qui est indiqué dans la propriété **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="2fafa-378">This property represents the time to recharge a fully depleted battery, not the current remaining charging time, which is indicated in the **TimeToFullCharge** property.</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-379">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2fafa-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-380">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-382">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2fafa-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-383">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="2fafa-383">Label by which the object is known.</span></span> <span data-ttu-id="2fafa-384">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="2fafa-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2fafa-385">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2fafa-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-389">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2fafa-389">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-390">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="2fafa-390">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2fafa-391">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="2fafa-391">Example: "\*PNP030b"</span></span>

<span data-ttu-id="2fafa-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2fafa-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-394">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2fafa-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-396">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="2fafa-396">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="2fafa-397">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2fafa-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2fafa-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-399">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="2fafa-399">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2fafa-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="2fafa-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-401">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2fafa-401">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2fafa-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="2fafa-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-403">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="2fafa-403">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2fafa-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="2fafa-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-405">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="2fafa-405">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2fafa-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="2fafa-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-407">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="2fafa-407">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2fafa-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="2fafa-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-409">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2fafa-409">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="2fafa-410">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="2fafa-410">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="2fafa-411">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2fafa-411">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2fafa-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="2fafa-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-413">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="2fafa-413">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2fafa-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="2fafa-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2fafa-415">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="2fafa-415">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2fafa-416">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2fafa-416">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-417">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2fafa-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-419">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="2fafa-419">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2fafa-420">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2fafa-420">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2fafa-421">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2fafa-421">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2fafa-422">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2fafa-422">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2fafa-423">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-423">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-424">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="2fafa-424">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-425">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-426">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-427">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-427">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-428">Numéro de version de la spécification de données de batterie intelligente qui est pris en charge par cette batterie.</span><span class="sxs-lookup"><span data-stu-id="2fafa-428">Smart battery data-specification version number that is supported by this battery.</span></span> <span data-ttu-id="2fafa-429">Si la batterie ne prend pas en charge cette fonction, la valeur doit être laissée vide.</span><span class="sxs-lookup"><span data-stu-id="2fafa-429">If the battery does not support this function, the value should be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-430">**État**</span><span class="sxs-lookup"><span data-stu-id="2fafa-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-431">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-433">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2fafa-433">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-434">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2fafa-434">String that indicates the current status of the object.</span></span> <span data-ttu-id="2fafa-435">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="2fafa-435">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2fafa-436">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="2fafa-436">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2fafa-437">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="2fafa-437">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2fafa-438">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="2fafa-438">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2fafa-439">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="2fafa-439">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2fafa-440">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="2fafa-440">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2fafa-441">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2fafa-442">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fafa-442">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2fafa-443">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2fafa-444">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2fafa-445">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2fafa-446">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="2fafa-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2fafa-447">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2fafa-448">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2fafa-449">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2fafa-450">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2fafa-451">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2fafa-452">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2fafa-453">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2fafa-454">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2fafa-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2fafa-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-456">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2fafa-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-458">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-459">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2fafa-459">State of the logical device.</span></span> <span data-ttu-id="2fafa-460">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="2fafa-460">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="2fafa-461">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2fafa-462">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2fafa-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2fafa-463">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2fafa-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2fafa-464">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="2fafa-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2fafa-465">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="2fafa-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2fafa-466">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="2fafa-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2fafa-467">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2fafa-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-468">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-470">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2fafa-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-471">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2fafa-471">The scoping system's creation class name.</span></span>

<span data-ttu-id="2fafa-472">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2fafa-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-474">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2fafa-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-476">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2fafa-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-477">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2fafa-477">The scoping system's name.</span></span>

<span data-ttu-id="2fafa-478">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-479">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="2fafa-479">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-480">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-482">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="2fafa-482">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-483">Temps écoulé, en secondes, depuis le dernier basculement de l’onduleur du système informatique vers la batterie, ou durée depuis le dernier redémarrage du système ou de l’onduleur, selon la valeur la plus petite.</span><span class="sxs-lookup"><span data-stu-id="2fafa-483">Elapsed time, in seconds, since the computer system's UPS last switched to battery power, or the amount of time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="2fafa-484">La valeur 0 est retournée si la batterie est « en ligne ».</span><span class="sxs-lookup"><span data-stu-id="2fafa-484">A value of 0 is returned if the battery is "online."</span></span>

</dd> <dt>

<span data-ttu-id="2fafa-485">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="2fafa-485">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fafa-486">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fafa-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fafa-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fafa-488">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,16 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutes ")</span><span class="sxs-lookup"><span data-stu-id="2fafa-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="2fafa-489">Temps restant, en minutes, pour charger entièrement la batterie à la vitesse de chargement et à l’utilisation actuelles.</span><span class="sxs-lookup"><span data-stu-id="2fafa-489">Remaining time, in minutes, to charge the battery fully at the current charging rate and use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fafa-490">Notes</span><span class="sxs-lookup"><span data-stu-id="2fafa-490">Remarks</span></span>

<span data-ttu-id="2fafa-491">La classe de **\_ batterie CIM** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-491">The **CIM\_Battery** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2fafa-492">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2fafa-492">WMI does not implement this class.</span></span> <span data-ttu-id="2fafa-493">Pour plus d’informations sur les classes dérivées de la **\_ batterie CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2fafa-493">For more information about classes derived from **CIM\_Battery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2fafa-494">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2fafa-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2fafa-495">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2fafa-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fafa-496">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fafa-496">Requirements</span></span>



| <span data-ttu-id="2fafa-497">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fafa-497">Requirement</span></span> | <span data-ttu-id="2fafa-498">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fafa-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fafa-499">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fafa-499">Minimum supported client</span></span><br/> | <span data-ttu-id="2fafa-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fafa-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fafa-501">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fafa-501">Minimum supported server</span></span><br/> | <span data-ttu-id="2fafa-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fafa-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fafa-503">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2fafa-503">Namespace</span></span><br/>                | <span data-ttu-id="2fafa-504">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2fafa-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2fafa-505">MOF</span><span class="sxs-lookup"><span data-stu-id="2fafa-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fafa-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fafa-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fafa-507">DLL</span><span class="sxs-lookup"><span data-stu-id="2fafa-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fafa-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fafa-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fafa-509">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fafa-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fafa-510">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2fafa-510">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

