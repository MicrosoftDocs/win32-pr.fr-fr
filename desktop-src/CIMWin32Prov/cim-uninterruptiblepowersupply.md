---
description: La \_ classe CIM UninterruptiblePowerSupply représente les fonctionnalités et la gestion d’un onduleur.
ms.assetid: 27ddc955-906b-40b9-981b-96872356477c
ms.tgt_platform: multiple
title: Classe CIM_UninterruptiblePowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply
- CIM_UninterruptiblePowerSupply.ActiveInputVoltage
- CIM_UninterruptiblePowerSupply.Availability
- CIM_UninterruptiblePowerSupply.Caption
- CIM_UninterruptiblePowerSupply.ConfigManagerErrorCode
- CIM_UninterruptiblePowerSupply.ConfigManagerUserConfig
- CIM_UninterruptiblePowerSupply.CreationClassName
- CIM_UninterruptiblePowerSupply.Description
- CIM_UninterruptiblePowerSupply.DeviceID
- CIM_UninterruptiblePowerSupply.ErrorCleared
- CIM_UninterruptiblePowerSupply.ErrorDescription
- CIM_UninterruptiblePowerSupply.EstimatedChargeRemaining
- CIM_UninterruptiblePowerSupply.EstimatedRunTime
- CIM_UninterruptiblePowerSupply.InstallDate
- CIM_UninterruptiblePowerSupply.IsSwitchingSupply
- CIM_UninterruptiblePowerSupply.LastErrorCode
- CIM_UninterruptiblePowerSupply.Name
- CIM_UninterruptiblePowerSupply.PNPDeviceID
- CIM_UninterruptiblePowerSupply.PowerManagementCapabilities
- CIM_UninterruptiblePowerSupply.PowerManagementSupported
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range1InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range1InputVoltageLow
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range2InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range2InputVoltageLow
- CIM_UninterruptiblePowerSupply.RemainingCapacityStatus
- CIM_UninterruptiblePowerSupply.Status
- CIM_UninterruptiblePowerSupply.StatusInfo
- CIM_UninterruptiblePowerSupply.SystemCreationClassName
- CIM_UninterruptiblePowerSupply.SystemName
- CIM_UninterruptiblePowerSupply.TimeOnBackup
- CIM_UninterruptiblePowerSupply.TotalOutputPower
- CIM_UninterruptiblePowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 214517fd6518cf2ca406523c61f522ae9c1adc46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512880"
---
# <a name="cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="1d91c-103">\_Classe CIM UninterruptiblePowerSupply</span><span class="sxs-lookup"><span data-stu-id="1d91c-103">CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="1d91c-104">La classe **CIM \_ UninterruptiblePowerSupply** représente les fonctionnalités et la gestion d’un onduleur.</span><span class="sxs-lookup"><span data-stu-id="1d91c-104">The **CIM\_UninterruptiblePowerSupply** class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span> <span data-ttu-id="1d91c-105">Les propriétés de l’appareil UPS indiquent quand une alimentation entrante est réduite ou amplifiée, ainsi que les informations agrégées des piles, des générateurs, etc., qui composent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-105">The properties of the UPS device indicate when incoming power is trimmed or boosted, and the aggregated information of the batteries, generators, and so on, that make up the device.</span></span> <span data-ttu-id="1d91c-106">Les composants individuels (par exemple, plusieurs batteries) peuvent également être modélisés indépendamment et associés à l’onduleur.</span><span class="sxs-lookup"><span data-stu-id="1d91c-106">The individual components (for example, multiple batteries) can also be independently modeled and associated with the UPS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d91c-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1d91c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1d91c-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1d91c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1d91c-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1d91c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1d91c-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1d91c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d91c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d91c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UninterruptiblePowerSupply : CIM_PowerSupply
{
  uint16   ActiveInputVoltage;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  datetime InstallDate;
  boolean  IsSwitchingSupply;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Range1InputFrequencyHigh;
  uint32   Range1InputFrequencyLow;
  uint32   Range1InputVoltageHigh;
  uint32   Range1InputVoltageLow;
  uint32   Range2InputFrequencyHigh;
  uint32   Range2InputFrequencyLow;
  uint32   Range2InputVoltageHigh;
  uint32   Range2InputVoltageLow;
  uint16   RemainingCapacityStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBackup;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="1d91c-112">Membres</span><span class="sxs-lookup"><span data-stu-id="1d91c-112">Members</span></span>

<span data-ttu-id="1d91c-113">La classe **CIM \_ UninterruptiblePowerSupply** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d91c-113">The **CIM\_UninterruptiblePowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="1d91c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1d91c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d91c-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1d91c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d91c-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1d91c-116">Methods</span></span>

<span data-ttu-id="1d91c-117">La classe **CIM \_ UninterruptiblePowerSupply** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1d91c-117">The **CIM\_UninterruptiblePowerSupply** class has these methods.</span></span>



| <span data-ttu-id="1d91c-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="1d91c-118">Method</span></span>                                                                                | <span data-ttu-id="1d91c-119">Description</span><span class="sxs-lookup"><span data-stu-id="1d91c-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d91c-120">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="1d91c-120">**Reset**</span></span>](reset-method-in-class-cim-uninterruptiblepowersupply.md)                 | <span data-ttu-id="1d91c-121">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="1d91c-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="1d91c-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="1d91c-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="1d91c-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1d91c-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-uninterruptiblepowersupply.md) | <span data-ttu-id="1d91c-124">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="1d91c-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="1d91c-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="1d91c-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1d91c-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1d91c-126">Properties</span></span>

<span data-ttu-id="1d91c-127">La classe **CIM \_ UninterruptiblePowerSupply** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d91c-127">The **CIM\_UninterruptiblePowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d91c-128">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="1d91c-128">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d91c-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-131">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-132">La plage des tensions d’entrée est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="1d91c-132">Input voltage range is currently in use.</span></span> <span data-ttu-id="1d91c-133">Si l’approvisionnement ne dessine pas de puissance, la valeur 6 (« aucune ») peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1d91c-133">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="1d91c-134">Ces informations sont nécessaires dans le cas d’un UPS, une sous-classe de l' [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-134">This information is necessary in the case of a UPS, a subclass of [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="1d91c-135">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-135">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d91c-136">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="1d91c-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d91c-137">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="1d91c-137">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="1d91c-138">**Plage 1** (3)</span><span class="sxs-lookup"><span data-stu-id="1d91c-138">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="1d91c-139">**Plage 2** (4)</span><span class="sxs-lookup"><span data-stu-id="1d91c-139">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="1d91c-140">**Les deux** (5)</span><span class="sxs-lookup"><span data-stu-id="1d91c-140">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="1d91c-141">**Ni** (6)</span><span class="sxs-lookup"><span data-stu-id="1d91c-141">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d91c-142">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="1d91c-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d91c-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-145">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-146">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-146">Availability and status of the device.</span></span>

<span data-ttu-id="1d91c-147">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d91c-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="1d91c-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d91c-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="1d91c-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1d91c-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="1d91c-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-151">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="1d91c-151">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1d91c-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="1d91c-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1d91c-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="1d91c-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d91c-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="1d91c-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1d91c-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="1d91c-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1d91c-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="1d91c-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1d91c-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="1d91c-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d91c-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="1d91c-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1d91c-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="1d91c-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1d91c-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="1d91c-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1d91c-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="1d91c-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-162">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="1d91c-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1d91c-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="1d91c-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-164">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="1d91c-164">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1d91c-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="1d91c-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-166">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="1d91c-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1d91c-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="1d91c-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1d91c-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="1d91c-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-169">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="1d91c-169">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1d91c-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="1d91c-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-171">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="1d91c-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1d91c-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="1d91c-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-173">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="1d91c-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1d91c-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="1d91c-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-175">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="1d91c-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1d91c-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="1d91c-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-177">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="1d91c-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d91c-178">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1d91c-178">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-181">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-182">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d91c-182">Short textual description of the object.</span></span>

<span data-ttu-id="1d91c-183">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-184">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d91c-184">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-185">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-185">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-187">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d91c-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-188">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="1d91c-188">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1d91c-189">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-189">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1d91c-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1d91c-191"> (0)</span><span class="sxs-lookup"><span data-stu-id="1d91c-191">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-192">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="1d91c-192">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1d91c-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1d91c-194">(1)</span><span class="sxs-lookup"><span data-stu-id="1d91c-194">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-195">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="1d91c-195">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d91c-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1d91c-197">(2)</span><span class="sxs-lookup"><span data-stu-id="1d91c-197">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1d91c-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1d91c-199">(3)</span><span class="sxs-lookup"><span data-stu-id="1d91c-199">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-200">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="1d91c-200">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1d91c-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1d91c-202">(4)</span><span class="sxs-lookup"><span data-stu-id="1d91c-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-203">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="1d91c-203">Device is not working properly.</span></span> <span data-ttu-id="1d91c-204">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="1d91c-204">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1d91c-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1d91c-206">(5)</span><span class="sxs-lookup"><span data-stu-id="1d91c-206">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-207">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="1d91c-207">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1d91c-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1d91c-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="1d91c-209">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-210">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="1d91c-210">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1d91c-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1d91c-212">(7)</span><span class="sxs-lookup"><span data-stu-id="1d91c-212">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1d91c-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1d91c-214">(8)</span><span class="sxs-lookup"><span data-stu-id="1d91c-214">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-215">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="1d91c-215">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1d91c-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1d91c-217">(9)</span><span class="sxs-lookup"><span data-stu-id="1d91c-217">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-218">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="1d91c-218">Device is not working properly.</span></span> <span data-ttu-id="1d91c-219">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-219">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1d91c-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1d91c-221">(10)</span><span class="sxs-lookup"><span data-stu-id="1d91c-221">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-222">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-222">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1d91c-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1d91c-224">(11)</span><span class="sxs-lookup"><span data-stu-id="1d91c-224">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-225">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-225">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1d91c-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1d91c-227">douze</span><span class="sxs-lookup"><span data-stu-id="1d91c-227">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-228">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1d91c-228">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1d91c-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1d91c-230">(13)</span><span class="sxs-lookup"><span data-stu-id="1d91c-230">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-231">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-231">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1d91c-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1d91c-233">(14)</span><span class="sxs-lookup"><span data-stu-id="1d91c-233">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-234">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="1d91c-234">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1d91c-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1d91c-236">(15)</span><span class="sxs-lookup"><span data-stu-id="1d91c-236">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-237">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="1d91c-237">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1d91c-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1d91c-239">(16)</span><span class="sxs-lookup"><span data-stu-id="1d91c-239">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-240">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-240">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1d91c-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1d91c-242">(17)</span><span class="sxs-lookup"><span data-stu-id="1d91c-242">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-243">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="1d91c-243">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d91c-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1d91c-245">(18)</span><span class="sxs-lookup"><span data-stu-id="1d91c-245">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-246">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="1d91c-246">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1d91c-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1d91c-248">(19)</span><span class="sxs-lookup"><span data-stu-id="1d91c-248">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1d91c-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1d91c-250">(20)</span><span class="sxs-lookup"><span data-stu-id="1d91c-250">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-251">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="1d91c-251">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1d91c-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1d91c-253">(21)</span><span class="sxs-lookup"><span data-stu-id="1d91c-253">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-254">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="1d91c-254">System failure.</span></span> <span data-ttu-id="1d91c-255">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="1d91c-255">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1d91c-256">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-256">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1d91c-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1d91c-258">(22)</span><span class="sxs-lookup"><span data-stu-id="1d91c-258">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-259">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="1d91c-259">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1d91c-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1d91c-261">(23)</span><span class="sxs-lookup"><span data-stu-id="1d91c-261">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-262">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="1d91c-262">System failure.</span></span> <span data-ttu-id="1d91c-263">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="1d91c-263">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1d91c-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1d91c-265">(24)</span><span class="sxs-lookup"><span data-stu-id="1d91c-265">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-266">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="1d91c-266">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1d91c-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1d91c-268">(25)</span><span class="sxs-lookup"><span data-stu-id="1d91c-268">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-269">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1d91c-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1d91c-271">(26)</span><span class="sxs-lookup"><span data-stu-id="1d91c-271">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-272">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d91c-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1d91c-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1d91c-274">(27)</span><span class="sxs-lookup"><span data-stu-id="1d91c-274">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-275">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="1d91c-275">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1d91c-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1d91c-277">(28)</span><span class="sxs-lookup"><span data-stu-id="1d91c-277">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-278">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="1d91c-278">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1d91c-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1d91c-280">(29)</span><span class="sxs-lookup"><span data-stu-id="1d91c-280">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-281">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="1d91c-281">Device is disabled.</span></span> <span data-ttu-id="1d91c-282">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="1d91c-282">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1d91c-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1d91c-284">(30)</span><span class="sxs-lookup"><span data-stu-id="1d91c-284">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-285">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="1d91c-285">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d91c-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="1d91c-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1d91c-287">31</span><span class="sxs-lookup"><span data-stu-id="1d91c-287">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-288">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="1d91c-288">Device is not working properly.</span></span> <span data-ttu-id="1d91c-289">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="1d91c-289">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d91c-290">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1d91c-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-291">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1d91c-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-293">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d91c-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-294">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1d91c-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1d91c-295">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d91c-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-299">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d91c-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-300">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="1d91c-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1d91c-301">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="1d91c-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1d91c-302">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-303">**Description**</span><span class="sxs-lookup"><span data-stu-id="1d91c-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-306">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="1d91c-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-307">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d91c-307">Textual description of the object.</span></span>

<span data-ttu-id="1d91c-308">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d91c-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-312">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d91c-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-313">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="1d91c-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="1d91c-314">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-315">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1d91c-315">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-316">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1d91c-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-318">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="1d91c-318">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1d91c-319">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-320">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1d91c-320">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-323">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="1d91c-323">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="1d91c-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-325">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="1d91c-325">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-326">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d91c-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-328">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie de l’onduleur DMTF \| 001,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pourcentage ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-329">Pourcentage estimé du coût total restant pour un onduleur qui utilise la technologie de batterie.</span><span class="sxs-lookup"><span data-stu-id="1d91c-329">Percentage estimate of the remaining full charge for a UPS that uses battery technology.</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-330">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="1d91c-330">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-331">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-333">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie de l’onduleur DMTF \| 001,3 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutes ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-334">Durée estimée, en minutes, jusqu’à épuisement de la batterie, du générateur ou d’une autre source d’alimentation dans les conditions de charge en cours si l’alimentation de l’utilitaire est désactivée, ou si elle est perdue et reste désactivée.</span><span class="sxs-lookup"><span data-stu-id="1d91c-334">Estimated time, in minutes, until the battery, generator, or other power source is depleted under the present load conditions if the utility power is off, or is lost and remains off.</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d91c-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-336">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d91c-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-338">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-339">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d91c-339">Date and time the object was installed.</span></span> <span data-ttu-id="1d91c-340">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="1d91c-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1d91c-341">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-342">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="1d91c-342">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-343">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1d91c-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-345">Si la **valeur est true**, l’alimentation est une alimentation de commutation (plutôt que linéaire).</span><span class="sxs-lookup"><span data-stu-id="1d91c-345">If **TRUE**, the power supply is a switching (rather than linear) supply.</span></span>

<span data-ttu-id="1d91c-346">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-346">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d91c-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-348">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-350">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="1d91c-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1d91c-351">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-352">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1d91c-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-355">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1d91c-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-356">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="1d91c-356">Label by which the object is known.</span></span> <span data-ttu-id="1d91c-357">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="1d91c-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1d91c-358">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-359">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d91c-359">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-362">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d91c-362">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-363">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="1d91c-363">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="1d91c-364">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1d91c-365">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="1d91c-365">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-366">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1d91c-366">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-367">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d91c-367">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-369">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="1d91c-369">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1d91c-370">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="1d91c-370">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d91c-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="1d91c-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1d91c-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="1d91c-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1d91c-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="1d91c-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1d91c-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="1d91c-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-375">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="1d91c-375">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1d91c-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="1d91c-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-377">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="1d91c-377">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1d91c-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="1d91c-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-379">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1d91c-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1d91c-380">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="1d91c-380">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="1d91c-381">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1d91c-381">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1d91c-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="1d91c-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-383">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="1d91c-383">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1d91c-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="1d91c-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-385">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="1d91c-385">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d91c-386">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1d91c-386">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-387">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1d91c-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-389">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="1d91c-389">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="1d91c-390">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d91c-390">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1d91c-391">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1d91c-391">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="1d91c-392">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d91c-392">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="1d91c-393">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-394">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="1d91c-394">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-395">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-395">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-397">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« Hertz »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-397">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-398">Fréquence, en Hertz, à l’extrémité supérieure de la plage de fréquences d’entrée de l’alimentation 1.</span><span class="sxs-lookup"><span data-stu-id="1d91c-398">Frequency, in hertz, at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="1d91c-399">La valeur 0 (zéro) signifie DC.</span><span class="sxs-lookup"><span data-stu-id="1d91c-399">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="1d91c-400">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-400">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-401">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="1d91c-401">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-402">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-404">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,17 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-405">Fréquence, en Hertz, à l’extrémité inférieure de la plage de fréquences d’entrée de l’alimentation 1.</span><span class="sxs-lookup"><span data-stu-id="1d91c-405">Frequency, in hertz, at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="1d91c-406">La valeur 0 (zéro) signifie DC.</span><span class="sxs-lookup"><span data-stu-id="1d91c-406">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="1d91c-407">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-407">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-408">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="1d91c-408">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-409">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-411">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span><span class="sxs-lookup"><span data-stu-id="1d91c-411">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-412">Si la tension, en millivolts, s’élève au-dessus de la valeur spécifiée par la propriété **Range1InputVoltageHigh** , l’onduleur compensera en découpant la tension.</span><span class="sxs-lookup"><span data-stu-id="1d91c-412">If the voltage, in millivolts, rises above the value specified by the **Range1InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="1d91c-413">La valeur 0 (zéro) indique que la tension au niveau de laquelle la suppression se produit est inconnue.</span><span class="sxs-lookup"><span data-stu-id="1d91c-413">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="1d91c-414">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-414">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-415">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="1d91c-415">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-416">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-418">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span><span class="sxs-lookup"><span data-stu-id="1d91c-418">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-419">Si la tension, en millivolts, chute sous la valeur spécifiée par la propriété **Range1InputVoltageLow** , l’onduleur compensera en amplifiant la tension à l’aide de ses sources d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="1d91c-419">If the voltage, in millivolts, drops below the value specified by the **Range1InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="1d91c-420">La valeur 0 indique que la tension à laquelle l’augmentation se produit est inconnue.</span><span class="sxs-lookup"><span data-stu-id="1d91c-420">A value of 0 indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="1d91c-421">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-421">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-422">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="1d91c-422">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-423">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-423">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-425">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,20 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-426">Fréquence, en Hertz, à l’extrémité supérieure de la plage de fréquences d’entrée de l’alimentation 2.</span><span class="sxs-lookup"><span data-stu-id="1d91c-426">Frequency, in hertz, at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="1d91c-427">La valeur 0 (zéro) signifie DC.</span><span class="sxs-lookup"><span data-stu-id="1d91c-427">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="1d91c-428">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-428">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-429">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="1d91c-429">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-430">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-432">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,19 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-433">Fréquence, en Hertz, à l’extrémité inférieure de la plage de fréquences d’entrée de l’alimentation. 2.</span><span class="sxs-lookup"><span data-stu-id="1d91c-433">Frequency, in hertz, at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="1d91c-434">La valeur 0 signifie DC.</span><span class="sxs-lookup"><span data-stu-id="1d91c-434">A value of 0 implies DC.</span></span>

<span data-ttu-id="1d91c-435">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-435">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-436">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="1d91c-436">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-437">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-437">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-438">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-439">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span><span class="sxs-lookup"><span data-stu-id="1d91c-439">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-440">Si la tension, en millivolts, s’élève au-dessus de la valeur spécifiée par la propriété **Range2InputVoltageHigh** , l’onduleur compensera en découpant la tension.</span><span class="sxs-lookup"><span data-stu-id="1d91c-440">If the voltage, in millivolts, rises above the value specified by the **Range2InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="1d91c-441">La valeur 0 (zéro) indique que la tension au niveau de laquelle la suppression se produit est inconnue.</span><span class="sxs-lookup"><span data-stu-id="1d91c-441">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="1d91c-442">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-442">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-443">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="1d91c-443">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-444">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-444">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-446">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span><span class="sxs-lookup"><span data-stu-id="1d91c-446">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-447">Si la tension, en millivolts, chute sous la valeur spécifiée par la propriété **Range2InputVoltageLow** , l’onduleur compensera en amplifiant la tension à l’aide de ses sources d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="1d91c-447">If the voltage, in millivolts, drops below the value specified by the **Range2InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="1d91c-448">La valeur 0 (zéro) indique que la tension à laquelle l’augmentation se produit est inconnue.</span><span class="sxs-lookup"><span data-stu-id="1d91c-448">A value of 0 (zero) indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="1d91c-449">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-449">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-450">**RemainingCapacityStatus**</span><span class="sxs-lookup"><span data-stu-id="1d91c-450">**RemainingCapacityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-451">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d91c-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-452">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-453">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Batterie de l' \| onduleur DMTF \| 001,1»)</span><span class="sxs-lookup"><span data-stu-id="1d91c-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-454">Indication de la capacité restante sur les piles, le générateur ou autre source de l’onduleur.</span><span class="sxs-lookup"><span data-stu-id="1d91c-454">Indication of the capacity remaining in the UPS's batteries, generator, or other source.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d91c-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (1)</span><span class="sxs-lookup"><span data-stu-id="1d91c-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="1d91c-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span><span class="sxs-lookup"><span data-stu-id="1d91c-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-457">Les minutes estimées restantes de l’exécution sont supérieures à l’état de faible consommation défini par l’onduleur (en général, deux minutes).</span><span class="sxs-lookup"><span data-stu-id="1d91c-457">Remaining estimated minutes of run-time is greater than the UPS's defined low-power state (typically, two minutes).</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="1d91c-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Faible** (3)</span><span class="sxs-lookup"><span data-stu-id="1d91c-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-459">Les minutes estimées restantes du runtime sont inférieures ou égales à l’état de faible consommation défini par l’onduleur.</span><span class="sxs-lookup"><span data-stu-id="1d91c-459">Remaining estimated minutes of run-time is less than or equal to the UPS's defined low-power state.</span></span>

</dd> <dt>

<span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>

<span data-ttu-id="1d91c-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Épuisé** (4)</span><span class="sxs-lookup"><span data-stu-id="1d91c-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Depleted** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1d91c-461">L’onduleur ne pourra pas supporter la charge actuelle lorsque la puissance de l’utilitaire est perdue (y compris la possibilité que la puissance de l’utilitaire soit actuellement absente).</span><span class="sxs-lookup"><span data-stu-id="1d91c-461">The UPS will be unable to sustain the present load when the utility power is lost (including the possibility that the utility power is currently absent).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d91c-462">**État**</span><span class="sxs-lookup"><span data-stu-id="1d91c-462">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-463">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-464">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-465">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="1d91c-465">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-466">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d91c-466">Current status of the object.</span></span> <span data-ttu-id="1d91c-467">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-467">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1d91c-468">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d91c-468">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1d91c-469">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-469">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1d91c-470">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-470">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d91c-471">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-471">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d91c-472">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="1d91c-472">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1d91c-473">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-473">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1d91c-474">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-474">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1d91c-475">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-475">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1d91c-476">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-476">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1d91c-477">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-477">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1d91c-478">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-478">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1d91c-479">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-479">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1d91c-480">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="1d91c-480">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d91c-481">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1d91c-481">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-482">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d91c-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-483">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-484">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-485">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="1d91c-485">State of the logical device.</span></span> <span data-ttu-id="1d91c-486">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="1d91c-486">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1d91c-487">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d91c-488">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="1d91c-488">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d91c-489">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="1d91c-489">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1d91c-490">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="1d91c-490">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1d91c-491">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="1d91c-491">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d91c-492">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="1d91c-492">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d91c-493">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d91c-493">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-494">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-495">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-496">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d91c-496">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-497">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="1d91c-497">Scoping system's creation class name.</span></span>

<span data-ttu-id="1d91c-498">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-498">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-499">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d91c-499">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-500">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d91c-500">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-501">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-502">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d91c-502">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-503">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="1d91c-503">Scoping system's name.</span></span>

<span data-ttu-id="1d91c-504">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-504">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-505">**TimeOnBackup**</span><span class="sxs-lookup"><span data-stu-id="1d91c-505">**TimeOnBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-506">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-508">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie de l’onduleur DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" secondes ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-508">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-509">Temps écoulé, en secondes, depuis la dernière commutation de l’onduleur sur la puissance de la batterie, le générateur ou autre source d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="1d91c-509">Elapsed time, in seconds, since the UPS last switched to battery power, generator, or other power source.</span></span> <span data-ttu-id="1d91c-510">Ou bien, le temps écoulé depuis le dernier redémarrage de l’onduleur, selon la valeur la moins élevée.</span><span class="sxs-lookup"><span data-stu-id="1d91c-510">Or, the time since the UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="1d91c-511">Si l’onduleur est en ligne, la valeur 0 (zéro) est retournée.</span><span class="sxs-lookup"><span data-stu-id="1d91c-511">If the UPS is online, 0 (zero) will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-512">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="1d91c-512">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-513">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d91c-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-514">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-515">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,21 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatts ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-515">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-516">Puissance de sortie totale de l’alimentation, en milliwatts.</span><span class="sxs-lookup"><span data-stu-id="1d91c-516">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="1d91c-517">La valeur 0 (zéro) indique Unknown.</span><span class="sxs-lookup"><span data-stu-id="1d91c-517">A value of 0 (zero) denotes unknown.</span></span>

<span data-ttu-id="1d91c-518">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-518">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d91c-519">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="1d91c-519">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d91c-520">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d91c-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-521">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d91c-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d91c-522">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="1d91c-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="1d91c-523">Type de basculement de plage d’entrée-tension implémenté dans le bloc d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="1d91c-523">Type of input-voltage range switching implemented in the power supply.</span></span>

<span data-ttu-id="1d91c-524">Cette propriété est héritée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-524">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d91c-525">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="1d91c-525">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d91c-526">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="1d91c-526">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="1d91c-527">**Manuel** (3)</span><span class="sxs-lookup"><span data-stu-id="1d91c-527">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="1d91c-528">**Commutateur AutoSwitch** (4)</span><span class="sxs-lookup"><span data-stu-id="1d91c-528">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="1d91c-529">**Large plage** (5)</span><span class="sxs-lookup"><span data-stu-id="1d91c-529">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d91c-530">**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="1d91c-530">**Not Applicable** (6)</span></span>


<span data-ttu-id="1d91c-531"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1d91c-531"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="1d91c-532">Notes</span><span class="sxs-lookup"><span data-stu-id="1d91c-532">Remarks</span></span>

<span data-ttu-id="1d91c-533">La classe **CIM \_ UninterruptiblePowerSupply** est dérivée de la [**\_ alimentation CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-533">The **CIM\_UninterruptiblePowerSupply** class is derived from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="1d91c-534">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="1d91c-534">WMI does not implement this class.</span></span> <span data-ttu-id="1d91c-535">Pour les classes WMI dérivées de **CIM \_ UninterruptiblePowerSupply**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1d91c-535">For WMI classes derived from **CIM\_UninterruptiblePowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1d91c-536">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1d91c-536">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1d91c-537">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1d91c-537">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d91c-538">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d91c-538">Requirements</span></span>



| <span data-ttu-id="1d91c-539">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d91c-539">Requirement</span></span> | <span data-ttu-id="1d91c-540">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d91c-540">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d91c-541">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d91c-541">Minimum supported client</span></span><br/> | <span data-ttu-id="1d91c-542">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d91c-542">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d91c-543">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d91c-543">Minimum supported server</span></span><br/> | <span data-ttu-id="1d91c-544">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d91c-544">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d91c-545">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d91c-545">Namespace</span></span><br/>                | <span data-ttu-id="1d91c-546">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1d91c-546">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d91c-547">MOF</span><span class="sxs-lookup"><span data-stu-id="1d91c-547">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d91c-548"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d91c-548"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d91c-549">DLL</span><span class="sxs-lookup"><span data-stu-id="1d91c-549">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d91c-550"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d91c-550"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d91c-551">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d91c-551">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d91c-552">**\_Alimentation CIM**</span><span class="sxs-lookup"><span data-stu-id="1d91c-552">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> </dl>

 

