---
description: La \_ classe d’alimentation CIM représente les fonctionnalités et la gestion de l’unité logique d’alimentation.
ms.assetid: a9b79564-01d9-42a4-8586-782f179c179f
ms.tgt_platform: multiple
title: Classe CIM_PowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply
- CIM_PowerSupply.ActiveInputVoltage
- CIM_PowerSupply.Availability
- CIM_PowerSupply.Caption
- CIM_PowerSupply.ConfigManagerErrorCode
- CIM_PowerSupply.ConfigManagerUserConfig
- CIM_PowerSupply.CreationClassName
- CIM_PowerSupply.Description
- CIM_PowerSupply.DeviceID
- CIM_PowerSupply.ErrorCleared
- CIM_PowerSupply.ErrorDescription
- CIM_PowerSupply.InstallDate
- CIM_PowerSupply.IsSwitchingSupply
- CIM_PowerSupply.LastErrorCode
- CIM_PowerSupply.Name
- CIM_PowerSupply.PNPDeviceID
- CIM_PowerSupply.PowerManagementCapabilities
- CIM_PowerSupply.PowerManagementSupported
- CIM_PowerSupply.Range1InputFrequencyHigh
- CIM_PowerSupply.Range1InputFrequencyLow
- CIM_PowerSupply.Range1InputVoltageHigh
- CIM_PowerSupply.Range1InputVoltageLow
- CIM_PowerSupply.Range2InputFrequencyHigh
- CIM_PowerSupply.Range2InputFrequencyLow
- CIM_PowerSupply.Range2InputVoltageHigh
- CIM_PowerSupply.Range2InputVoltageLow
- CIM_PowerSupply.Status
- CIM_PowerSupply.StatusInfo
- CIM_PowerSupply.SystemCreationClassName
- CIM_PowerSupply.SystemName
- CIM_PowerSupply.TotalOutputPower
- CIM_PowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35a1eb73c258b800bb8b33ad7aa75ea86cd0ef4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200963"
---
# <a name="cim_powersupply-class"></a><span data-ttu-id="cebe8-103">\_Classe d’alimentation CIM</span><span class="sxs-lookup"><span data-stu-id="cebe8-103">CIM\_PowerSupply class</span></span>

<span data-ttu-id="cebe8-104">La **classe \_ d’alimentation CIM** représente les fonctionnalités et la gestion de l’unité logique d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="cebe8-104">The **CIM\_PowerSupply** class represents the capabilities and management of the power supply logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cebe8-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="cebe8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cebe8-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cebe8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cebe8-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cebe8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cebe8-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="cebe8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cebe8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cebe8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C547-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PowerSupply : CIM_LogicalDevice
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="cebe8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="cebe8-110">Members</span></span>

<span data-ttu-id="cebe8-111">La classe d' **\_ alimentation CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cebe8-111">The **CIM\_PowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="cebe8-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cebe8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cebe8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cebe8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cebe8-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cebe8-114">Methods</span></span>

<span data-ttu-id="cebe8-115">La classe d' **\_ alimentation CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cebe8-115">The **CIM\_PowerSupply** class has these methods.</span></span>



| <span data-ttu-id="cebe8-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="cebe8-116">Method</span></span>                                                                 | <span data-ttu-id="cebe8-117">Description</span><span class="sxs-lookup"><span data-stu-id="cebe8-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cebe8-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="cebe8-118">**Reset**</span></span>](reset-method-in-class-cim-powersupply.md)                 | <span data-ttu-id="cebe8-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="cebe8-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="cebe8-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="cebe8-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="cebe8-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cebe8-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-powersupply.md) | <span data-ttu-id="cebe8-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="cebe8-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="cebe8-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="cebe8-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cebe8-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cebe8-124">Properties</span></span>

<span data-ttu-id="cebe8-125">La classe d' **\_ alimentation CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cebe8-125">The **CIM\_PowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cebe8-126">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="cebe8-126">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cebe8-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-130">Plage de tensions en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="cebe8-130">Voltage range that is currently in use.</span></span> <span data-ttu-id="cebe8-131">Si l’approvisionnement ne dessine pas de puissance, la valeur 6 (« aucune ») peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cebe8-131">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="cebe8-132">Ces informations sont nécessaires dans le cas d’un onduleur (UPS), une sous-classe de la **source \_ d’alimentation CIM**.</span><span class="sxs-lookup"><span data-stu-id="cebe8-132">This information is necessary in the case of an uninterruptible power supply (UPS), a subclass of **CIM\_PowerSupply**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cebe8-133">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="cebe8-133">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cebe8-134">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="cebe8-134">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="cebe8-135">**Plage 1** (3)</span><span class="sxs-lookup"><span data-stu-id="cebe8-135">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="cebe8-136">**Plage 2** (4)</span><span class="sxs-lookup"><span data-stu-id="cebe8-136">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="cebe8-137">**Les deux** (5)</span><span class="sxs-lookup"><span data-stu-id="cebe8-137">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="cebe8-138">**Ni** (6)</span><span class="sxs-lookup"><span data-stu-id="cebe8-138">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cebe8-139">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="cebe8-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cebe8-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-142">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-143">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-143">Availability and status of the device.</span></span>

<span data-ttu-id="cebe8-144">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cebe8-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="cebe8-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cebe8-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="cebe8-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="cebe8-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="cebe8-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-148">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="cebe8-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="cebe8-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="cebe8-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="cebe8-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="cebe8-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cebe8-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="cebe8-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="cebe8-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="cebe8-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="cebe8-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="cebe8-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="cebe8-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="cebe8-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cebe8-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="cebe8-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="cebe8-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="cebe8-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="cebe8-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="cebe8-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="cebe8-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="cebe8-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-159">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="cebe8-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="cebe8-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="cebe8-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-161">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="cebe8-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="cebe8-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="cebe8-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-163">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="cebe8-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="cebe8-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="cebe8-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="cebe8-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="cebe8-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-166">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="cebe8-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="cebe8-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="cebe8-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-168">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="cebe8-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="cebe8-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="cebe8-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-170">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="cebe8-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="cebe8-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="cebe8-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-172">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="cebe8-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="cebe8-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="cebe8-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-174">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="cebe8-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cebe8-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cebe8-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-178">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-179">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cebe8-179">Short textual description of the object.</span></span>

<span data-ttu-id="cebe8-180">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cebe8-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-182">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-184">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cebe8-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-185">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="cebe8-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="cebe8-186">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="cebe8-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="cebe8-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="cebe8-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-189">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="cebe8-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="cebe8-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="cebe8-191">(1)</span><span class="sxs-lookup"><span data-stu-id="cebe8-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-192">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="cebe8-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cebe8-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="cebe8-194">(2)</span><span class="sxs-lookup"><span data-stu-id="cebe8-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="cebe8-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="cebe8-196">(3)</span><span class="sxs-lookup"><span data-stu-id="cebe8-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-197">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="cebe8-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cebe8-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="cebe8-199">(4)</span><span class="sxs-lookup"><span data-stu-id="cebe8-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-200">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="cebe8-200">Device is not working properly.</span></span> <span data-ttu-id="cebe8-201">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="cebe8-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="cebe8-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="cebe8-203">(5)</span><span class="sxs-lookup"><span data-stu-id="cebe8-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-204">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="cebe8-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="cebe8-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="cebe8-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="cebe8-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-207">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="cebe8-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="cebe8-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="cebe8-209">(7)</span><span class="sxs-lookup"><span data-stu-id="cebe8-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="cebe8-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="cebe8-211">(8)</span><span class="sxs-lookup"><span data-stu-id="cebe8-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-212">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="cebe8-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="cebe8-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="cebe8-214">(9)</span><span class="sxs-lookup"><span data-stu-id="cebe8-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-215">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="cebe8-215">Device is not working properly.</span></span> <span data-ttu-id="cebe8-216">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="cebe8-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="cebe8-218">(10)</span><span class="sxs-lookup"><span data-stu-id="cebe8-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-219">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="cebe8-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="cebe8-221">(11)</span><span class="sxs-lookup"><span data-stu-id="cebe8-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-222">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="cebe8-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="cebe8-224">douze</span><span class="sxs-lookup"><span data-stu-id="cebe8-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-225">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cebe8-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="cebe8-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="cebe8-227">(13)</span><span class="sxs-lookup"><span data-stu-id="cebe8-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-228">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="cebe8-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="cebe8-230">(14)</span><span class="sxs-lookup"><span data-stu-id="cebe8-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-231">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="cebe8-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="cebe8-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="cebe8-233">(15)</span><span class="sxs-lookup"><span data-stu-id="cebe8-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-234">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="cebe8-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="cebe8-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="cebe8-236">(16)</span><span class="sxs-lookup"><span data-stu-id="cebe8-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-237">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="cebe8-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="cebe8-239">(17)</span><span class="sxs-lookup"><span data-stu-id="cebe8-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-240">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="cebe8-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cebe8-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="cebe8-242">(18)</span><span class="sxs-lookup"><span data-stu-id="cebe8-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-243">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="cebe8-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="cebe8-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="cebe8-245">(19)</span><span class="sxs-lookup"><span data-stu-id="cebe8-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cebe8-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="cebe8-247">(20)</span><span class="sxs-lookup"><span data-stu-id="cebe8-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-248">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="cebe8-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="cebe8-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="cebe8-250">(21)</span><span class="sxs-lookup"><span data-stu-id="cebe8-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-251">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="cebe8-251">System failure.</span></span> <span data-ttu-id="cebe8-252">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="cebe8-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="cebe8-253">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="cebe8-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="cebe8-255">(22)</span><span class="sxs-lookup"><span data-stu-id="cebe8-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-256">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="cebe8-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="cebe8-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="cebe8-258">(23)</span><span class="sxs-lookup"><span data-stu-id="cebe8-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-259">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="cebe8-259">System failure.</span></span> <span data-ttu-id="cebe8-260">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="cebe8-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="cebe8-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="cebe8-262">(24)</span><span class="sxs-lookup"><span data-stu-id="cebe8-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-263">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="cebe8-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cebe8-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cebe8-265">(25)</span><span class="sxs-lookup"><span data-stu-id="cebe8-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-266">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cebe8-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cebe8-268">(26)</span><span class="sxs-lookup"><span data-stu-id="cebe8-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-269">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebe8-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="cebe8-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="cebe8-271">(27)</span><span class="sxs-lookup"><span data-stu-id="cebe8-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-272">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="cebe8-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="cebe8-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="cebe8-274">(28)</span><span class="sxs-lookup"><span data-stu-id="cebe8-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-275">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="cebe8-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="cebe8-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="cebe8-277">(29)</span><span class="sxs-lookup"><span data-stu-id="cebe8-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-278">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="cebe8-278">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="cebe8-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="cebe8-280">(30)</span><span class="sxs-lookup"><span data-stu-id="cebe8-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-281">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="cebe8-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cebe8-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cebe8-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="cebe8-283">31</span><span class="sxs-lookup"><span data-stu-id="cebe8-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-284">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="cebe8-284">Device is not working properly.</span></span> <span data-ttu-id="cebe8-285">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="cebe8-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cebe8-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="cebe8-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-287">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cebe8-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-289">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cebe8-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-290">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cebe8-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="cebe8-291">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cebe8-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-295">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cebe8-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-296">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="cebe8-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cebe8-297">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="cebe8-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cebe8-298">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-299">**Description**</span><span class="sxs-lookup"><span data-stu-id="cebe8-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-302">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cebe8-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-303">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cebe8-303">Textual description of the object.</span></span>

<span data-ttu-id="cebe8-304">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cebe8-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-306">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-308">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cebe8-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-309">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="cebe8-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="cebe8-310">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="cebe8-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-312">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cebe8-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-314">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="cebe8-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="cebe8-315">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cebe8-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-319">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="cebe8-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="cebe8-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cebe8-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-322">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cebe8-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-324">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-325">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cebe8-325">Date and time the object was installed.</span></span> <span data-ttu-id="cebe8-326">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="cebe8-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cebe8-327">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-328">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="cebe8-328">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-329">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cebe8-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-331">Si la **valeur est true**, l’alimentation est une alimentation de commutation (et linéaire).</span><span class="sxs-lookup"><span data-stu-id="cebe8-331">If **TRUE**, the power supply is a switching (versus linear) supply.</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-332">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cebe8-332">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-333">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-335">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="cebe8-335">Last error code reported by the logical device.</span></span>

<span data-ttu-id="cebe8-336">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-337">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cebe8-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-340">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cebe8-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-341">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="cebe8-341">Label by which the object is known.</span></span> <span data-ttu-id="cebe8-342">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="cebe8-342">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cebe8-343">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cebe8-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-347">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cebe8-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-348">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="cebe8-348">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="cebe8-349">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cebe8-350">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="cebe8-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="cebe8-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-352">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cebe8-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-354">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="cebe8-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="cebe8-355">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="cebe8-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cebe8-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="cebe8-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="cebe8-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="cebe8-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cebe8-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="cebe8-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cebe8-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="cebe8-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-360">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="cebe8-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="cebe8-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="cebe8-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-362">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="cebe8-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="cebe8-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="cebe8-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-364">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cebe8-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="cebe8-365">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="cebe8-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="cebe8-366">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="cebe8-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="cebe8-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="cebe8-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-368">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="cebe8-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="cebe8-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="cebe8-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cebe8-370">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="cebe8-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cebe8-371">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="cebe8-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-372">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cebe8-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-374">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="cebe8-374">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="cebe8-375">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cebe8-375">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="cebe8-376">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cebe8-376">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="cebe8-377">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cebe8-377">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="cebe8-378">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-379">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="cebe8-379">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-380">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-382">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« Hertz »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-383">Fréquence (en Hertz) à l’extrémité supérieure de la plage de fréquences d’entrée de l’alimentation 1.</span><span class="sxs-lookup"><span data-stu-id="cebe8-383">Frequency (in hertz) at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="cebe8-384">La valeur 0 signifie DC.</span><span class="sxs-lookup"><span data-stu-id="cebe8-384">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-385">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="cebe8-385">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-386">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-388">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,17 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-389">Fréquence (en Hertz) à l’extrémité inférieure de la plage de fréquences d’entrée de l’alimentation 1.</span><span class="sxs-lookup"><span data-stu-id="cebe8-389">Frequency (in hertz) at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="cebe8-390">La valeur 0 signifie DC.</span><span class="sxs-lookup"><span data-stu-id="cebe8-390">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-391">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="cebe8-391">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-392">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-394">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,8 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-395">Tension élevée de la plage de tension en entrée 1 pour la source d’alimentation, en millivolts.</span><span class="sxs-lookup"><span data-stu-id="cebe8-395">High voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="cebe8-396">La valeur 0 indique « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="cebe8-396">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-397">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="cebe8-397">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-398">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-400">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,7 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-401">Tension basse de la plage de tension en entrée 1 pour la source d’alimentation, en millivolts.</span><span class="sxs-lookup"><span data-stu-id="cebe8-401">Low voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="cebe8-402">La valeur 0 indique « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="cebe8-402">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-403">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="cebe8-403">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-404">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-406">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,20 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-407">Fréquence (en Hertz) à l’extrémité supérieure de la plage de fréquences d’entrée de l’alimentation 2.</span><span class="sxs-lookup"><span data-stu-id="cebe8-407">Frequency (in hertz) at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="cebe8-408">La valeur 0 signifie DC.</span><span class="sxs-lookup"><span data-stu-id="cebe8-408">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-409">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="cebe8-409">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-410">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-412">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,19 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-412">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-413">Fréquence (en Hertz) à l’extrémité inférieure de la plage de fréquences d’entrée de l’alimentation 2.</span><span class="sxs-lookup"><span data-stu-id="cebe8-413">Frequency (in hertz) at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="cebe8-414">La valeur 0 signifie DC.</span><span class="sxs-lookup"><span data-stu-id="cebe8-414">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-415">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="cebe8-415">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-416">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-418">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,12 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-419">Tension élevée de la plage de tension en entrée 2 pour l’alimentation, en millivolts.</span><span class="sxs-lookup"><span data-stu-id="cebe8-419">High voltage of input voltage range 2 for the power supply, in millivolts.</span></span> <span data-ttu-id="cebe8-420">La valeur 0 indique « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="cebe8-420">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-421">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="cebe8-421">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-422">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-422">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-423">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-424">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-425">Tension basse de la plage de tension en entrée 2 pour cette alimentation, en millivolts.</span><span class="sxs-lookup"><span data-stu-id="cebe8-425">Low voltage of input voltage range 2 for this power supply, in Millivolts.</span></span> <span data-ttu-id="cebe8-426">La valeur 0 indique « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="cebe8-426">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-427">**État**</span><span class="sxs-lookup"><span data-stu-id="cebe8-427">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-428">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-430">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="cebe8-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-431">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cebe8-431">Current status of the object.</span></span>

<span data-ttu-id="cebe8-432">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cebe8-433">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cebe8-433">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cebe8-434">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-434">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cebe8-435">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-435">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cebe8-436">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-436">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cebe8-437">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="cebe8-437">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cebe8-438">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-438">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cebe8-439">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-439">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cebe8-440">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-440">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cebe8-441">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-441">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cebe8-442">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-442">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cebe8-443">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-443">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cebe8-444">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-444">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cebe8-445">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="cebe8-445">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cebe8-446">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cebe8-446">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-447">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cebe8-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-449">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-449">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-450">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="cebe8-450">State of the logical device.</span></span> <span data-ttu-id="cebe8-451">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="cebe8-451">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="cebe8-452">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cebe8-453">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="cebe8-453">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cebe8-454">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="cebe8-454">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cebe8-455">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="cebe8-455">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cebe8-456">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="cebe8-456">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cebe8-457">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="cebe8-457">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cebe8-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cebe8-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-459">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-461">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cebe8-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-462">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="cebe8-462">Scoping system's creation class name.</span></span>

<span data-ttu-id="cebe8-463">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cebe8-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-465">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cebe8-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-467">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cebe8-467">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-468">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="cebe8-468">Scoping system's name.</span></span>

<span data-ttu-id="cebe8-469">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-470">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="cebe8-470">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-471">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cebe8-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-473">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,21 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatts ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-474">Puissance de sortie totale de l’alimentation, en milliwatts.</span><span class="sxs-lookup"><span data-stu-id="cebe8-474">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="cebe8-475">La valeur 0 indique « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="cebe8-475">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="cebe8-476">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="cebe8-476">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cebe8-477">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cebe8-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-478">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cebe8-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cebe8-479">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Alimentation DMTF \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="cebe8-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="cebe8-480">Type de basculement de plage de tension en entrée implémenté dans le bloc d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="cebe8-480">Type of input voltage range switching implemented in the power supply.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cebe8-481">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="cebe8-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cebe8-482">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="cebe8-482">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="cebe8-483">**Manuel** (3)</span><span class="sxs-lookup"><span data-stu-id="cebe8-483">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="cebe8-484">**Commutateur AutoSwitch** (4)</span><span class="sxs-lookup"><span data-stu-id="cebe8-484">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="cebe8-485">**Large plage** (5)</span><span class="sxs-lookup"><span data-stu-id="cebe8-485">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cebe8-486">**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="cebe8-486">**Not Applicable** (6)</span></span>


<span data-ttu-id="cebe8-487"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cebe8-487"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cebe8-488">Notes</span><span class="sxs-lookup"><span data-stu-id="cebe8-488">Remarks</span></span>

<span data-ttu-id="cebe8-489">La classe d' **\_ alimentation CIM** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-489">The **CIM\_PowerSupply** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cebe8-490">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="cebe8-490">WMI does not implement this class.</span></span> <span data-ttu-id="cebe8-491">Pour la classe WMI dérivée de la **\_ alimentation CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cebe8-491">For WMI classed derived from **CIM\_PowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cebe8-492">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="cebe8-492">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cebe8-493">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cebe8-493">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cebe8-494">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cebe8-494">Requirements</span></span>



| <span data-ttu-id="cebe8-495">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cebe8-495">Requirement</span></span> | <span data-ttu-id="cebe8-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="cebe8-496">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cebe8-497">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cebe8-497">Minimum supported client</span></span><br/> | <span data-ttu-id="cebe8-498">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cebe8-498">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cebe8-499">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cebe8-499">Minimum supported server</span></span><br/> | <span data-ttu-id="cebe8-500">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cebe8-500">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cebe8-501">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cebe8-501">Namespace</span></span><br/>                | <span data-ttu-id="cebe8-502">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="cebe8-502">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cebe8-503">MOF</span><span class="sxs-lookup"><span data-stu-id="cebe8-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cebe8-504"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cebe8-504"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cebe8-505">DLL</span><span class="sxs-lookup"><span data-stu-id="cebe8-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cebe8-506"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cebe8-506"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cebe8-507">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cebe8-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cebe8-508">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="cebe8-508">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

