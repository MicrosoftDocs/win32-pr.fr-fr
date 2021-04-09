---
description: La \_ classe WMI Heatpipe WMI représente les propriétés d’un appareil de refroidissement de caloduc.
ms.assetid: c6e24cb2-e29a-4cd5-af62-b8e48a5936f9
ms.tgt_platform: multiple
title: Classe Win32_HeatPipe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_HeatPipe
- Win32_HeatPipe.Reset
- Win32_HeatPipe.SetPowerState
- Win32_HeatPipe.ActiveCooling
- Win32_HeatPipe.Availability
- Win32_HeatPipe.Caption
- Win32_HeatPipe.ConfigManagerErrorCode
- Win32_HeatPipe.ConfigManagerUserConfig
- Win32_HeatPipe.CreationClassName
- Win32_HeatPipe.Description
- Win32_HeatPipe.DeviceID
- Win32_HeatPipe.ErrorCleared
- Win32_HeatPipe.ErrorDescription
- Win32_HeatPipe.InstallDate
- Win32_HeatPipe.LastErrorCode
- Win32_HeatPipe.Name
- Win32_HeatPipe.PNPDeviceID
- Win32_HeatPipe.PowerManagementCapabilities
- Win32_HeatPipe.PowerManagementSupported
- Win32_HeatPipe.Status
- Win32_HeatPipe.StatusInfo
- Win32_HeatPipe.SystemCreationClassName
- Win32_HeatPipe.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f89b8f059a5c80f4d40c70007d8870211e79f93f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033740"
---
# <a name="win32_heatpipe-class"></a><span data-ttu-id="a0ea1-103">\_Classe Heatpipe Win32</span><span class="sxs-lookup"><span data-stu-id="a0ea1-103">Win32\_HeatPipe class</span></span>

<span data-ttu-id="a0ea1-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ Heatpipe** WMI représente les propriétés d’un appareil de refroidissement de caloduc.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-104">The **Win32\_HeatPipe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a heat pipe cooling device.</span></span>

<span data-ttu-id="a0ea1-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ea1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0ea1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB7-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_HeatPipe : CIM_HeatPipe
{
  boolean  ActiveCooling;
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
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="a0ea1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a0ea1-107">Members</span></span>

<span data-ttu-id="a0ea1-108">La classe **Win32 \_ Heatpipe** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a0ea1-108">The **Win32\_HeatPipe** class has these types of members:</span></span>

-   [<span data-ttu-id="a0ea1-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0ea1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0ea1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0ea1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0ea1-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0ea1-111">Methods</span></span>

<span data-ttu-id="a0ea1-112">La classe **Win32 \_ Heatpipe** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-112">The **Win32\_HeatPipe** class has these methods.</span></span>



| <span data-ttu-id="a0ea1-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0ea1-113">Method</span></span>            | <span data-ttu-id="a0ea1-114">Description</span><span class="sxs-lookup"><span data-stu-id="a0ea1-114">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ea1-115">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-115">**Reset**</span></span>         | <span data-ttu-id="a0ea1-116">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-116">Not implemented.</span></span> <span data-ttu-id="a0ea1-117">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ Heatpipe**](cim-heatpipe.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-117">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_HeatPipe**](cim-heatpipe.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="a0ea1-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-118">**SetPowerState**</span></span> | <span data-ttu-id="a0ea1-119">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-119">Not implemented.</span></span> <span data-ttu-id="a0ea1-120">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ Heatpipe**](cim-heatpipe.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-120">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_HeatPipe**](cim-heatpipe.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a0ea1-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0ea1-121">Properties</span></span>

<span data-ttu-id="a0ea1-122">La classe **Win32 \_ Heatpipe** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-122">The **Win32\_HeatPipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0ea1-123">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-123">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-124">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-126">Si la **valeur est true**, le périphérique de refroidissement fournit un refroidissement actif non passif.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-126">If **TRUE**, the cooling device provides active cooling not passive.</span></span>

<span data-ttu-id="a0ea1-127">Cette propriété est héritée de la [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-127">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-128">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-131">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-132">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-132">Availability and status of the device.</span></span>

<span data-ttu-id="a0ea1-133">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0ea1-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0ea1-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a0ea1-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-137">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="a0ea1-137">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a0ea1-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a0ea1-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a0ea1-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a0ea1-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a0ea1-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a0ea1-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a0ea1-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a0ea1-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a0ea1-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a0ea1-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-148">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a0ea1-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-150">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a0ea1-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-152">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-152">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a0ea1-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a0ea1-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-155">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a0ea1-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-157">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a0ea1-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-159">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a0ea1-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-161">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a0ea1-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-163">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0ea1-164">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-167">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-168">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-168">Short description of the object a one-line string.</span></span>

<span data-ttu-id="a0ea1-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-170">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-173">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-174">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a0ea1-175">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a0ea1-176"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-176"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a0ea1-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-177">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-178">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-178">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a0ea1-179"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-179"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a0ea1-180">(1)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-180">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-181">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-181">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0ea1-182"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-182"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a0ea1-183">(2)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-183">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a0ea1-184"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-184"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a0ea1-185">(3)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-185">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-186">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-186">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a0ea1-187"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-187"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a0ea1-188">(4)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-188">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-189">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-189">Device is not working properly.</span></span> <span data-ttu-id="a0ea1-190">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-190">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a0ea1-191"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-191"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a0ea1-192">(5)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-192">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-193">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-193">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a0ea1-194"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-194"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a0ea1-195"> (6)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-195">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-196">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-196">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a0ea1-197"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-197"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a0ea1-198">(7)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-198">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a0ea1-199"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-199"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a0ea1-200">(8)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-200">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-201">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-201">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a0ea1-202"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-202"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a0ea1-203">(9)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-203">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-204">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-204">Device is not working properly.</span></span> <span data-ttu-id="a0ea1-205">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-205">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a0ea1-206"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-206"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a0ea1-207">(10)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-207">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-208">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-208">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a0ea1-209"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-209"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a0ea1-210">(11)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-210">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-211">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-211">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a0ea1-212"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-212"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a0ea1-213">douze</span><span class="sxs-lookup"><span data-stu-id="a0ea1-213">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-214">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-214">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a0ea1-215"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-215"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a0ea1-216">(13)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-216">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-217">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-217">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a0ea1-218"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-218"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a0ea1-219">(14)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-219">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-220">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-220">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a0ea1-221"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-221"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a0ea1-222">(15)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-222">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-223">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-223">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a0ea1-224"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-224"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a0ea1-225">(16)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-225">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-226">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-226">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a0ea1-227"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-227"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a0ea1-228">(17)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-229">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-229">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0ea1-230"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-230"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a0ea1-231">(18)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-231">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-232">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-232">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a0ea1-233"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-233"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a0ea1-234">(19)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-234">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a0ea1-235"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-235"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a0ea1-236">(20)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-236">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-237">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-237">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a0ea1-238"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-238"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a0ea1-239">(21)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-239">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-240">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-240">System failure.</span></span> <span data-ttu-id="a0ea1-241">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-241">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a0ea1-242">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-242">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a0ea1-243"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-243"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a0ea1-244">(22)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-244">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-245">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-245">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a0ea1-246"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-246"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a0ea1-247">(23)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-247">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-248">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-248">System failure.</span></span> <span data-ttu-id="a0ea1-249">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-249">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a0ea1-250"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-250"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a0ea1-251">(24)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-251">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-252">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-252">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a0ea1-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a0ea1-254">(25)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-254">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-255">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a0ea1-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a0ea1-257">(26)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-257">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-258">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a0ea1-259"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-259"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a0ea1-260">(27)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-260">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-261">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-261">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a0ea1-262"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-262"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a0ea1-263">(28)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-263">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-264">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-264">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a0ea1-265"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-265"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a0ea1-266">(29)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-266">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-267">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-267">Device is disabled.</span></span> <span data-ttu-id="a0ea1-268">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-268">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a0ea1-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a0ea1-270">(30)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-270">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-271">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-271">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0ea1-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a0ea1-273">31</span><span class="sxs-lookup"><span data-stu-id="a0ea1-273">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-274">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-274">Device is not working properly.</span></span> <span data-ttu-id="a0ea1-275">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-275">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0ea1-276">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-276">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-277">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-277">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-279">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-280">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-280">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a0ea1-281">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-281">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-282">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-282">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-283">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-285">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-285">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-286">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-286">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a0ea1-287">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-287">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="a0ea1-288">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-289">**Description**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-289">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-290">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-292">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-293">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-293">Description of the object.</span></span>

<span data-ttu-id="a0ea1-294">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-295">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-295">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-298">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-298">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-299">Identificateur unique du canal de chaleur.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-299">Unique identifier of the heat pipe.</span></span>

<span data-ttu-id="a0ea1-300">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-301">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-301">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-302">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-304">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-304">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="a0ea1-305">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-306">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-306">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-309">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-309">More information about the error that is recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="a0ea1-310">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-312">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-314">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-315">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-315">Date and time the object was installed.</span></span> <span data-ttu-id="a0ea1-316">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-316">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a0ea1-317">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-318">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-318">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-319">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-319">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-321">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-321">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a0ea1-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-323">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-326">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-327">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-327">Label by which the object is known.</span></span> <span data-ttu-id="a0ea1-328">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-328">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a0ea1-329">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-330">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-330">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-333">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-333">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-334">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-334">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a0ea1-335">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a0ea1-336">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="a0ea1-336">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-338">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-340">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-340">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a0ea1-341">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-341">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0ea1-342"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-342"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a0ea1-343"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-343"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-344">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-344">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a0ea1-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a0ea1-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-347">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a0ea1-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-349">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a0ea1-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-351">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-351">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a0ea1-352">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-352">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a0ea1-353">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a0ea1-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-355">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-355">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a0ea1-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a0ea1-357">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0ea1-357">Timed Power-On Supported</span></span>

<span data-ttu-id="a0ea1-358">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0ea1-359">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-359">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-360">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-362">Si la **valeur est true**, l’appareil peut être géré par l’alimentation mis en mode veille, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-362">If **TRUE**, the device can be power-managed put into suspend mode, and so on.</span></span> <span data-ttu-id="a0ea1-363">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, uniquement si l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-363">The property does not indicate that power management features are enabled currently, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="a0ea1-364">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-365">**État**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-366">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-368">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-369">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-369">Current status of the object.</span></span> <span data-ttu-id="a0ea1-370">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a0ea1-371">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a0ea1-372">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="a0ea1-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a0ea1-373">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a0ea1-374">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a0ea1-375">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a0ea1-376">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0ea1-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a0ea1-377">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a0ea1-378">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a0ea1-379">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0ea1-380">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a0ea1-381">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a0ea1-382">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a0ea1-383">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a0ea1-384">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a0ea1-385">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a0ea1-386">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a0ea1-387">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a0ea1-388">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0ea1-389">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-389">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-390">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-392">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a0ea1-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-393">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-393">State of the logical device.</span></span> <span data-ttu-id="a0ea1-394">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-394">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a0ea1-395">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-395">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0ea1-396">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0ea1-397">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-397">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a0ea1-398">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-398">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a0ea1-399">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-399">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a0ea1-400">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-400">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0ea1-401">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-401">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-402">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-404">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-405">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-405">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="a0ea1-406">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ea1-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ea1-408">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0ea1-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ea1-410">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0ea1-410">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0ea1-411">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="a0ea1-411">Name of the scoping system.</span></span>

<span data-ttu-id="a0ea1-412">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0ea1-413">Notes</span><span class="sxs-lookup"><span data-stu-id="a0ea1-413">Remarks</span></span>

<span data-ttu-id="a0ea1-414">La classe **Win32 \_ Heatpipe** est dérivée de [**CIM \_ Heatpipe**](cim-heatpipe.md).</span><span class="sxs-lookup"><span data-stu-id="a0ea1-414">The **Win32\_HeatPipe** class is derived from [**CIM\_HeatPipe**](cim-heatpipe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ea1-415">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0ea1-415">Requirements</span></span>



| <span data-ttu-id="a0ea1-416">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0ea1-416">Requirement</span></span> | <span data-ttu-id="a0ea1-417">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0ea1-417">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ea1-418">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0ea1-418">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ea1-419">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0ea1-419">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0ea1-420">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0ea1-420">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ea1-421">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0ea1-421">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0ea1-422">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a0ea1-422">Namespace</span></span><br/>                | <span data-ttu-id="a0ea1-423">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a0ea1-423">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a0ea1-424">MOF</span><span class="sxs-lookup"><span data-stu-id="a0ea1-424">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0ea1-425"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0ea1-425"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0ea1-426">DLL</span><span class="sxs-lookup"><span data-stu-id="a0ea1-426">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0ea1-427"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0ea1-427"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0ea1-428">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0ea1-428">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ea1-429">**\_Heatpipe CIM**</span><span class="sxs-lookup"><span data-stu-id="a0ea1-429">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dt>

[<span data-ttu-id="a0ea1-430">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="a0ea1-430">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

