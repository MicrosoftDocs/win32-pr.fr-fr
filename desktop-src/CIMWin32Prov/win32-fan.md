---
description: La \_ classe WMI de ventilateur Win32 représente les propriétés d’un appareil de ventilateur dans le système informatique. Par exemple, le ventilateur de refroidissement de l’UC.
ms.assetid: ff48b788-d759-45cf-812f-a80dba0c9192
ms.tgt_platform: multiple
title: Classe Win32_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Fan
- Win32_Fan.Reset
- Win32_Fan.SetPowerState
- Win32_Fan.SetSpeed
- Win32_Fan.ActiveCooling
- Win32_Fan.Availability
- Win32_Fan.Caption
- Win32_Fan.ConfigManagerErrorCode
- Win32_Fan.ConfigManagerUserConfig
- Win32_Fan.CreationClassName
- Win32_Fan.Description
- Win32_Fan.DesiredSpeed
- Win32_Fan.DeviceID
- Win32_Fan.ErrorCleared
- Win32_Fan.ErrorDescription
- Win32_Fan.InstallDate
- Win32_Fan.LastErrorCode
- Win32_Fan.Name
- Win32_Fan.PNPDeviceID
- Win32_Fan.PowerManagementCapabilities
- Win32_Fan.PowerManagementSupported
- Win32_Fan.Status
- Win32_Fan.StatusInfo
- Win32_Fan.SystemCreationClassName
- Win32_Fan.SystemName
- Win32_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67f248b74fa665f30c9c3b9ffa51cb8cee5a5782
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523092"
---
# <a name="win32_fan-class"></a><span data-ttu-id="18d56-104">\_Classe de ventilateur Win32</span><span class="sxs-lookup"><span data-stu-id="18d56-104">Win32\_Fan class</span></span>

<span data-ttu-id="18d56-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ ventilateur Win32** représente les propriétés d’un appareil de ventilateur dans le système informatique.</span><span class="sxs-lookup"><span data-stu-id="18d56-105">The **Win32\_Fan** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a fan device in the computer system.</span></span> <span data-ttu-id="18d56-106">Par exemple, le ventilateur de refroidissement de l’UC.</span><span class="sxs-lookup"><span data-stu-id="18d56-106">For example, the CPU cooling fan.</span></span>

<span data-ttu-id="18d56-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="18d56-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="18d56-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="18d56-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d56-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18d56-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB5-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_Fan : CIM_Fan
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="18d56-110">Membres</span><span class="sxs-lookup"><span data-stu-id="18d56-110">Members</span></span>

<span data-ttu-id="18d56-111">La **classe \_ fan Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18d56-111">The **Win32\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="18d56-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18d56-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="18d56-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18d56-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18d56-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18d56-114">Methods</span></span>

<span data-ttu-id="18d56-115">La **classe \_ fan Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="18d56-115">The **Win32\_Fan** class has these methods.</span></span>



| <span data-ttu-id="18d56-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="18d56-116">Method</span></span>            | <span data-ttu-id="18d56-117">Description</span><span class="sxs-lookup"><span data-stu-id="18d56-117">Description</span></span>                                                                                                                                                                                  |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d56-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="18d56-118">**Reset**</span></span>         | <span data-ttu-id="18d56-119">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="18d56-119">Not implemented.</span></span> <span data-ttu-id="18d56-120">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans le [**\_ ventilateur CIM**](cim-fan.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="18d56-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="18d56-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="18d56-121">**SetPowerState**</span></span> | <span data-ttu-id="18d56-122">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="18d56-122">Not implemented.</span></span> <span data-ttu-id="18d56-123">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans le [**\_ ventilateur CIM**](cim-fan.md) pour la documentation.</span><span class="sxs-lookup"><span data-stu-id="18d56-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/> |
| <span data-ttu-id="18d56-124">**SetSpeed**</span><span class="sxs-lookup"><span data-stu-id="18d56-124">**SetSpeed**</span></span>      | <span data-ttu-id="18d56-125">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="18d56-125">Not implemented.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="18d56-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18d56-126">Properties</span></span>

<span data-ttu-id="18d56-127">La **classe \_ fan Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="18d56-127">The **Win32\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18d56-128">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="18d56-128">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18d56-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d56-131">Si la **valeur est true**, l’appareil de refroidissement fournit le refroidissement actif (par opposition à passif).</span><span class="sxs-lookup"><span data-stu-id="18d56-131">If **True**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="18d56-132">Cette propriété est héritée de la [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-132">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-133">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="18d56-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-134">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d56-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-136">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="18d56-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-137">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-137">Availability and status of the device.</span></span>

<span data-ttu-id="18d56-138">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18d56-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="18d56-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18d56-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="18d56-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="18d56-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="18d56-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-142">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="18d56-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="18d56-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="18d56-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="18d56-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="18d56-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18d56-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="18d56-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="18d56-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="18d56-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="18d56-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="18d56-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="18d56-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="18d56-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18d56-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="18d56-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="18d56-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="18d56-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="18d56-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="18d56-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="18d56-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="18d56-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-153">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="18d56-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="18d56-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="18d56-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-155">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="18d56-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="18d56-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="18d56-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-157">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="18d56-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="18d56-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="18d56-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="18d56-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="18d56-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-160">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="18d56-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="18d56-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="18d56-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-162">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="18d56-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="18d56-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="18d56-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-164">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="18d56-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="18d56-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="18d56-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-166">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="18d56-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="18d56-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="18d56-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-168">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="18d56-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18d56-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="18d56-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-172">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="18d56-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-173">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="18d56-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="18d56-174">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18d56-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-176">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18d56-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-178">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18d56-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-179">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="18d56-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="18d56-180">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="18d56-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="18d56-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="18d56-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="18d56-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-183">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="18d56-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="18d56-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="18d56-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="18d56-185">(1)</span><span class="sxs-lookup"><span data-stu-id="18d56-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-186">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="18d56-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18d56-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="18d56-188">(2)</span><span class="sxs-lookup"><span data-stu-id="18d56-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="18d56-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="18d56-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="18d56-190">(3)</span><span class="sxs-lookup"><span data-stu-id="18d56-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-191">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="18d56-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="18d56-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="18d56-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="18d56-193">(4)</span><span class="sxs-lookup"><span data-stu-id="18d56-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-194">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="18d56-194">Device is not working properly.</span></span> <span data-ttu-id="18d56-195">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="18d56-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="18d56-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="18d56-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="18d56-197">(5)</span><span class="sxs-lookup"><span data-stu-id="18d56-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-198">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="18d56-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="18d56-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="18d56-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="18d56-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="18d56-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-201">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="18d56-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="18d56-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="18d56-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="18d56-203">(7)</span><span class="sxs-lookup"><span data-stu-id="18d56-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="18d56-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="18d56-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="18d56-205">(8)</span><span class="sxs-lookup"><span data-stu-id="18d56-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-206">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="18d56-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="18d56-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="18d56-208">(9)</span><span class="sxs-lookup"><span data-stu-id="18d56-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-209">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="18d56-209">Device is not working properly.</span></span> <span data-ttu-id="18d56-210">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="18d56-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="18d56-212">(10)</span><span class="sxs-lookup"><span data-stu-id="18d56-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-213">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="18d56-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="18d56-215">(11)</span><span class="sxs-lookup"><span data-stu-id="18d56-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-216">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="18d56-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="18d56-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="18d56-218">douze</span><span class="sxs-lookup"><span data-stu-id="18d56-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-219">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="18d56-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="18d56-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="18d56-221">(13)</span><span class="sxs-lookup"><span data-stu-id="18d56-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-222">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="18d56-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="18d56-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="18d56-224">(14)</span><span class="sxs-lookup"><span data-stu-id="18d56-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-225">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="18d56-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="18d56-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="18d56-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="18d56-227">(15)</span><span class="sxs-lookup"><span data-stu-id="18d56-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-228">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="18d56-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="18d56-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="18d56-230">(16)</span><span class="sxs-lookup"><span data-stu-id="18d56-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-231">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="18d56-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="18d56-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="18d56-233">(17)</span><span class="sxs-lookup"><span data-stu-id="18d56-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-234">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="18d56-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18d56-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="18d56-236">(18)</span><span class="sxs-lookup"><span data-stu-id="18d56-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-237">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="18d56-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="18d56-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="18d56-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="18d56-239">(19)</span><span class="sxs-lookup"><span data-stu-id="18d56-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="18d56-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="18d56-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="18d56-241">(20)</span><span class="sxs-lookup"><span data-stu-id="18d56-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-242">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="18d56-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="18d56-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="18d56-244">(21)</span><span class="sxs-lookup"><span data-stu-id="18d56-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-245">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="18d56-245">System failure.</span></span> <span data-ttu-id="18d56-246">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="18d56-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="18d56-247">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="18d56-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="18d56-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="18d56-249">(22)</span><span class="sxs-lookup"><span data-stu-id="18d56-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-250">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="18d56-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="18d56-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="18d56-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="18d56-252">(23)</span><span class="sxs-lookup"><span data-stu-id="18d56-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-253">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="18d56-253">System failure.</span></span> <span data-ttu-id="18d56-254">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="18d56-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="18d56-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="18d56-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="18d56-256">(24)</span><span class="sxs-lookup"><span data-stu-id="18d56-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-257">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="18d56-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="18d56-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="18d56-259">(25)</span><span class="sxs-lookup"><span data-stu-id="18d56-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-260">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="18d56-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="18d56-262">(26)</span><span class="sxs-lookup"><span data-stu-id="18d56-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-263">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="18d56-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="18d56-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="18d56-265">(27)</span><span class="sxs-lookup"><span data-stu-id="18d56-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-266">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="18d56-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="18d56-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="18d56-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="18d56-268">(28)</span><span class="sxs-lookup"><span data-stu-id="18d56-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-269">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="18d56-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="18d56-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="18d56-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="18d56-271">(29)</span><span class="sxs-lookup"><span data-stu-id="18d56-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-272">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="18d56-272">Device is disabled.</span></span> <span data-ttu-id="18d56-273">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="18d56-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="18d56-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="18d56-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="18d56-275">(30)</span><span class="sxs-lookup"><span data-stu-id="18d56-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-276">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="18d56-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="18d56-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="18d56-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="18d56-278">31</span><span class="sxs-lookup"><span data-stu-id="18d56-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-279">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="18d56-279">Device is not working properly.</span></span> <span data-ttu-id="18d56-280">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="18d56-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18d56-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="18d56-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-282">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18d56-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-284">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18d56-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-285">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18d56-285">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="18d56-286">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18d56-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-290">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18d56-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18d56-291">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="18d56-291">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="18d56-292">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="18d56-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="18d56-293">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-294">**Description**</span><span class="sxs-lookup"><span data-stu-id="18d56-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-297">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="18d56-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-298">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18d56-298">Description of the object.</span></span>

<span data-ttu-id="18d56-299">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-300">**DesiredSpeed**</span><span class="sxs-lookup"><span data-stu-id="18d56-300">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-301">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18d56-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-303">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« tours par minute »)</span><span class="sxs-lookup"><span data-stu-id="18d56-303">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-304">Vitesse de ventilateur actuellement demandée, définie en tours par minute, lorsqu’un ventilateur à vitesse variable est pris en charge (**VariableSpeed** a la **valeur true**).</span><span class="sxs-lookup"><span data-stu-id="18d56-304">Currently requested fan speed, defined in revolutions per minute, when a variable speed fan is supported (**VariableSpeed** is **TRUE**).</span></span> <span data-ttu-id="18d56-305">La vitesse actuelle est déterminée par un capteur ([**le \_ tachymètre CIM**](cim-tachometer.md)) associé au ventilateur à l’aide de la relation [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="18d56-305">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="18d56-306">Cette propriété est héritée [**du \_ ventilateur CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-306">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

<span data-ttu-id="18d56-307">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="18d56-307">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="18d56-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-311">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="18d56-311">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-312">Identifie l’appareil de ventilateur.</span><span class="sxs-lookup"><span data-stu-id="18d56-312">Identifies the fan device.</span></span> <span data-ttu-id="18d56-313">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="18d56-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-315">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18d56-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d56-317">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="18d56-317">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="18d56-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18d56-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d56-322">Chaîne de forme libre fournissant plus d’informations sur l’erreur enregistrée dans la propriété **LastErrorCode** , ainsi que des informations sur toutes les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="18d56-322">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="18d56-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18d56-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-325">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18d56-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-327">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="18d56-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-328">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18d56-328">Date and time the object was installed.</span></span> <span data-ttu-id="18d56-329">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="18d56-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="18d56-330">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-331">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18d56-331">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-332">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18d56-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d56-334">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18d56-334">Last error code reported by the logical device.</span></span>

<span data-ttu-id="18d56-335">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-336">**Nom**</span><span class="sxs-lookup"><span data-stu-id="18d56-336">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-339">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="18d56-339">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-340">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="18d56-340">Label by which the object is known.</span></span> <span data-ttu-id="18d56-341">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="18d56-341">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="18d56-342">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-343">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="18d56-343">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-344">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-346">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="18d56-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-347">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18d56-347">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="18d56-348">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="18d56-349">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="18d56-349">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="18d56-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18d56-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-351">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d56-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18d56-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d56-353">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="18d56-353">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="18d56-354">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="18d56-354">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18d56-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18d56-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="18d56-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="18d56-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-357">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="18d56-357">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18d56-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="18d56-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="18d56-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="18d56-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-360">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="18d56-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="18d56-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="18d56-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-362">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="18d56-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="18d56-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="18d56-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-364">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18d56-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="18d56-365">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="18d56-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="18d56-366">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="18d56-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="18d56-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="18d56-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-368">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="18d56-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="18d56-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="18d56-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="18d56-370">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d56-370">Timed Power-On Supported</span></span>

<span data-ttu-id="18d56-371">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="18d56-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18d56-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="18d56-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-373">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18d56-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d56-375">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="18d56-375">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="18d56-376">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="18d56-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="18d56-377">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-378">**État**</span><span class="sxs-lookup"><span data-stu-id="18d56-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-381">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="18d56-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-382">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18d56-382">Current status of the object.</span></span> <span data-ttu-id="18d56-383">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="18d56-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="18d56-384">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="18d56-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="18d56-385">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="18d56-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="18d56-386">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="18d56-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="18d56-387">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="18d56-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="18d56-388">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="18d56-389">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="18d56-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18d56-390">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="18d56-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="18d56-391">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="18d56-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18d56-392">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="18d56-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18d56-393">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="18d56-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="18d56-394">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="18d56-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="18d56-395">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="18d56-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="18d56-396">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="18d56-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="18d56-397">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="18d56-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="18d56-398">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="18d56-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="18d56-399">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="18d56-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="18d56-400">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="18d56-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="18d56-401">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="18d56-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18d56-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="18d56-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-403">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d56-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-405">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="18d56-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="18d56-406">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18d56-406">State of the logical device.</span></span> <span data-ttu-id="18d56-407">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d56-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="18d56-408">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18d56-409">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="18d56-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18d56-410">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="18d56-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="18d56-411">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="18d56-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="18d56-412">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="18d56-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="18d56-413">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="18d56-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18d56-414">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18d56-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-417">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18d56-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18d56-418">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18d56-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="18d56-419">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-420">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18d56-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d56-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d56-423">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18d56-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18d56-424">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18d56-424">Name of the scoping system.</span></span>

<span data-ttu-id="18d56-425">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="18d56-426">**VariableSpeed**</span><span class="sxs-lookup"><span data-stu-id="18d56-426">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d56-427">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18d56-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18d56-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d56-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d56-429">Si la **valeur est true**, le ventilateur prend en charge des vitesses variables.</span><span class="sxs-lookup"><span data-stu-id="18d56-429">If **True**, the fan supports variable speeds.</span></span>

<span data-ttu-id="18d56-430">Cette propriété est héritée [**du \_ ventilateur CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-430">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18d56-431">Notes</span><span class="sxs-lookup"><span data-stu-id="18d56-431">Remarks</span></span>

<span data-ttu-id="18d56-432">La **classe \_ fan Win32** est dérivée [**du \_ ventilateur CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="18d56-432">The **Win32\_Fan** class is derived from [**CIM\_Fan**](cim-fan.md).</span></span>

## <a name="examples"></a><span data-ttu-id="18d56-433">Exemples</span><span class="sxs-lookup"><span data-stu-id="18d56-433">Examples</span></span>

<span data-ttu-id="18d56-434">L’exemple PowerShell [List Computer fan information](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) PowerShell récupère des informations sur les ventilateurs installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="18d56-434">The [List Computer Fan Information](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) PowerShell sample retrieves information about the cooling fans installed in a computer.</span></span>

<span data-ttu-id="18d56-435">L’exemple suivant récupère des informations sur les ventilateurs installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="18d56-435">The following sample retrieves information about the cooling fans installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_Fan") 
 
For Each objItem in colItems 
    Wscript.Echo "Active Cooling: " & objItem.ActiveCooling 
    Wscript.Echo "Availability: " & objItem.Availability 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
    Wscript.Echo 
Next
```


```PowerShell
$colItems = Get-WmiObject Win32_Fan -Namespace "root\cimv2"
foreach ($objItem in $colItems)
{
    "Active Cooling: " + $objItem.ActiveCooling 
    "Availability: " + $objItem.Availability 
    "Device ID: " + $objItem.DeviceID 
    "Name: " + $objItem.Name 
    "Status Information: " + $objItem.StatusInfo 
}
```





## <a name="requirements"></a><span data-ttu-id="18d56-436">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18d56-436">Requirements</span></span>



| <span data-ttu-id="18d56-437">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18d56-437">Requirement</span></span> | <span data-ttu-id="18d56-438">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d56-438">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18d56-439">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d56-439">Minimum supported client</span></span><br/> | <span data-ttu-id="18d56-440">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18d56-440">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18d56-441">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d56-441">Minimum supported server</span></span><br/> | <span data-ttu-id="18d56-442">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18d56-442">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18d56-443">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18d56-443">Namespace</span></span><br/>                | <span data-ttu-id="18d56-444">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="18d56-444">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18d56-445">MOF</span><span class="sxs-lookup"><span data-stu-id="18d56-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18d56-446"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18d56-446"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18d56-447">DLL</span><span class="sxs-lookup"><span data-stu-id="18d56-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18d56-448"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18d56-448"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d56-449">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d56-449">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d56-450">**\_Ventilateur CIM**</span><span class="sxs-lookup"><span data-stu-id="18d56-450">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dt>

[<span data-ttu-id="18d56-451">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="18d56-451">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

