---
description: Le \_ ParallelPort Win32 &\# 32 ; La classe WMI représente les propriétés d’un port parallèle sur un système d’ordinateur exécutant Windows.
ms.assetid: 986bd27f-71b0-4a40-a421-a8bfc0f081be
ms.tgt_platform: multiple
title: Classe Win32_ParallelPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ParallelPort
- Win32_ParallelPort.Reset
- Win32_ParallelPort.SetPowerState
- Win32_ParallelPort.Availability
- Win32_ParallelPort.Capabilities
- Win32_ParallelPort.CapabilityDescriptions
- Win32_ParallelPort.Caption
- Win32_ParallelPort.ConfigManagerErrorCode
- Win32_ParallelPort.ConfigManagerUserConfig
- Win32_ParallelPort.CreationClassName
- Win32_ParallelPort.Description
- Win32_ParallelPort.DeviceID
- Win32_ParallelPort.DMASupport
- Win32_ParallelPort.ErrorCleared
- Win32_ParallelPort.ErrorDescription
- Win32_ParallelPort.InstallDate
- Win32_ParallelPort.LastErrorCode
- Win32_ParallelPort.MaxNumberControlled
- Win32_ParallelPort.Name
- Win32_ParallelPort.OSAutoDiscovered
- Win32_ParallelPort.PNPDeviceID
- Win32_ParallelPort.PowerManagementCapabilities
- Win32_ParallelPort.PowerManagementSupported
- Win32_ParallelPort.ProtocolSupported
- Win32_ParallelPort.Status
- Win32_ParallelPort.StatusInfo
- Win32_ParallelPort.SystemCreationClassName
- Win32_ParallelPort.SystemName
- Win32_ParallelPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: da2ed3b34f3655067fd5ae41c31424e7599789c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111339"
---
# <a name="win32_parallelport-class"></a><span data-ttu-id="a7b26-103">\_Classe ParallelPort Win32</span><span class="sxs-lookup"><span data-stu-id="a7b26-103">Win32\_ParallelPort class</span></span>

<span data-ttu-id="a7b26-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ParallelPort** WMI représente les propriétés d’un port parallèle sur un système d’ordinateur exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="a7b26-104">The **Win32\_ParallelPort** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a parallel port on a computer system running Windows.</span></span>

<span data-ttu-id="a7b26-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a7b26-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a7b26-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="a7b26-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b26-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7b26-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class  Win32_ParallelPort : CIM_ParallelController
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DMASupport;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="a7b26-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a7b26-108">Members</span></span>

<span data-ttu-id="a7b26-109">La classe **Win32 \_ ParallelPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a7b26-109">The **Win32\_ParallelPort** class has these types of members:</span></span>

-   [<span data-ttu-id="a7b26-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a7b26-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a7b26-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7b26-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a7b26-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a7b26-112">Methods</span></span>

<span data-ttu-id="a7b26-113">La classe **Win32 \_ ParallelPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a7b26-113">The **Win32\_ParallelPort** class has these methods.</span></span>



| <span data-ttu-id="a7b26-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="a7b26-114">Method</span></span>            | <span data-ttu-id="a7b26-115">Description</span><span class="sxs-lookup"><span data-stu-id="a7b26-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b26-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="a7b26-116">**Reset**</span></span>         | <span data-ttu-id="a7b26-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a7b26-117">Not implemented.</span></span> <span data-ttu-id="a7b26-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="a7b26-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a7b26-119">**SetPowerState**</span></span> | <span data-ttu-id="a7b26-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a7b26-120">Not implemented.</span></span> <span data-ttu-id="a7b26-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a7b26-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7b26-122">Properties</span></span>

<span data-ttu-id="a7b26-123">La classe **Win32 \_ ParallelPort** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a7b26-123">The **Win32\_ParallelPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7b26-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="a7b26-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a7b26-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-127">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a7b26-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-128">Availability and status of the device.</span></span>

<span data-ttu-id="a7b26-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a7b26-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a7b26-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7b26-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="a7b26-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a7b26-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="a7b26-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="a7b26-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a7b26-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="a7b26-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a7b26-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="a7b26-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a7b26-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="a7b26-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a7b26-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="a7b26-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a7b26-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="a7b26-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a7b26-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="a7b26-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a7b26-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="a7b26-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a7b26-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="a7b26-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a7b26-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="a7b26-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a7b26-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="a7b26-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="a7b26-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a7b26-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="a7b26-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="a7b26-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a7b26-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="a7b26-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="a7b26-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a7b26-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="a7b26-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a7b26-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="a7b26-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="a7b26-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a7b26-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="a7b26-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-153">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="a7b26-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a7b26-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="a7b26-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-155">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="a7b26-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a7b26-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="a7b26-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-157">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="a7b26-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a7b26-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="a7b26-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-159">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="a7b26-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a7b26-160">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="a7b26-160">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-161">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a7b26-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-163">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Ports parallèles DMTF \| 003,8 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="a7b26-163">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-164">Tableau des fonctionnalités du contrôleur parallèle.</span><span class="sxs-lookup"><span data-stu-id="a7b26-164">Array of the capabilities of the parallel controller.</span></span>

<span data-ttu-id="a7b26-165">Cette propriété est héritée de la [**\_ ParallelController CIM**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-165">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7b26-166">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a7b26-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a7b26-167">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a7b26-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="a7b26-168">**Compatible XT/AT** (2)</span><span class="sxs-lookup"><span data-stu-id="a7b26-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="a7b26-169">**Compatible PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="a7b26-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="a7b26-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="a7b26-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="a7b26-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="a7b26-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="a7b26-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="a7b26-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="a7b26-173">**PC-98-Hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="a7b26-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="a7b26-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="a7b26-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7b26-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a7b26-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-176">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="a7b26-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-178">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ParallelController**](cim-parallelcontroller.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="a7b26-178">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-179">Tableau d’explications plus détaillées sur les fonctionnalités du contrôleur parallèle indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="a7b26-179">Array of more detailed explanations for any of the parallel controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="a7b26-180">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="a7b26-180">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="a7b26-181">Cette propriété est héritée de la [**\_ ParallelController CIM**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-181">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a7b26-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-185">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-186">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="a7b26-186">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="a7b26-187">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a7b26-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-189">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7b26-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-191">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a7b26-191">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-192">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="a7b26-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a7b26-193">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a7b26-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a7b26-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="a7b26-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-196">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="a7b26-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a7b26-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a7b26-198">(1)</span><span class="sxs-lookup"><span data-stu-id="a7b26-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-199">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="a7b26-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a7b26-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a7b26-201">(2)</span><span class="sxs-lookup"><span data-stu-id="a7b26-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a7b26-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a7b26-203">(3)</span><span class="sxs-lookup"><span data-stu-id="a7b26-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-204">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="a7b26-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a7b26-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a7b26-206">(4)</span><span class="sxs-lookup"><span data-stu-id="a7b26-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-207">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="a7b26-207">Device is not working properly.</span></span> <span data-ttu-id="a7b26-208">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="a7b26-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a7b26-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a7b26-210">(5)</span><span class="sxs-lookup"><span data-stu-id="a7b26-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-211">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="a7b26-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a7b26-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a7b26-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="a7b26-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-214">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="a7b26-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a7b26-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a7b26-216">(7)</span><span class="sxs-lookup"><span data-stu-id="a7b26-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a7b26-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a7b26-218">(8)</span><span class="sxs-lookup"><span data-stu-id="a7b26-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-219">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="a7b26-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a7b26-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a7b26-221">(9)</span><span class="sxs-lookup"><span data-stu-id="a7b26-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-222">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="a7b26-222">Device is not working properly.</span></span> <span data-ttu-id="a7b26-223">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a7b26-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a7b26-225">(10)</span><span class="sxs-lookup"><span data-stu-id="a7b26-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-226">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a7b26-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a7b26-228">(11)</span><span class="sxs-lookup"><span data-stu-id="a7b26-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-229">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a7b26-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a7b26-231">douze</span><span class="sxs-lookup"><span data-stu-id="a7b26-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-232">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a7b26-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a7b26-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a7b26-234">(13)</span><span class="sxs-lookup"><span data-stu-id="a7b26-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-235">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a7b26-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a7b26-237">(14)</span><span class="sxs-lookup"><span data-stu-id="a7b26-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-238">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="a7b26-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a7b26-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a7b26-240">(15)</span><span class="sxs-lookup"><span data-stu-id="a7b26-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-241">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="a7b26-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a7b26-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a7b26-243">(16)</span><span class="sxs-lookup"><span data-stu-id="a7b26-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-244">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a7b26-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a7b26-246">(17)</span><span class="sxs-lookup"><span data-stu-id="a7b26-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-247">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="a7b26-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a7b26-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a7b26-249">(18)</span><span class="sxs-lookup"><span data-stu-id="a7b26-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-250">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="a7b26-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a7b26-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a7b26-252">(19)</span><span class="sxs-lookup"><span data-stu-id="a7b26-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a7b26-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a7b26-254">(20)</span><span class="sxs-lookup"><span data-stu-id="a7b26-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-255">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="a7b26-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a7b26-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a7b26-257">(21)</span><span class="sxs-lookup"><span data-stu-id="a7b26-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-258">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="a7b26-258">System failure.</span></span> <span data-ttu-id="a7b26-259">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="a7b26-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a7b26-260">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a7b26-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a7b26-262">(22)</span><span class="sxs-lookup"><span data-stu-id="a7b26-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-263">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a7b26-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a7b26-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a7b26-265">(23)</span><span class="sxs-lookup"><span data-stu-id="a7b26-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-266">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="a7b26-266">System failure.</span></span> <span data-ttu-id="a7b26-267">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="a7b26-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a7b26-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a7b26-269">(24)</span><span class="sxs-lookup"><span data-stu-id="a7b26-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-270">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="a7b26-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a7b26-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a7b26-272">(25)</span><span class="sxs-lookup"><span data-stu-id="a7b26-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-273">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a7b26-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a7b26-275">(26)</span><span class="sxs-lookup"><span data-stu-id="a7b26-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-276">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7b26-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a7b26-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a7b26-278">(27)</span><span class="sxs-lookup"><span data-stu-id="a7b26-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-279">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="a7b26-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a7b26-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a7b26-281">(28)</span><span class="sxs-lookup"><span data-stu-id="a7b26-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-282">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="a7b26-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a7b26-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a7b26-284">(29)</span><span class="sxs-lookup"><span data-stu-id="a7b26-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-285">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a7b26-285">Device is disabled.</span></span> <span data-ttu-id="a7b26-286">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="a7b26-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a7b26-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a7b26-288">(30)</span><span class="sxs-lookup"><span data-stu-id="a7b26-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-289">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="a7b26-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a7b26-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a7b26-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a7b26-291">31</span><span class="sxs-lookup"><span data-stu-id="a7b26-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-292">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="a7b26-292">Device is not working properly.</span></span> <span data-ttu-id="a7b26-293">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="a7b26-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a7b26-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a7b26-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-295">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a7b26-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-297">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a7b26-297">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-298">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a7b26-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a7b26-299">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a7b26-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-303">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a7b26-303">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-304">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="a7b26-304">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a7b26-305">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="a7b26-305">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="a7b26-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-307">**Description**</span><span class="sxs-lookup"><span data-stu-id="a7b26-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-310">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a7b26-310">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-311">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7b26-311">Description of the object.</span></span>

<span data-ttu-id="a7b26-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a7b26-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-314">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-316">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« DeviceID »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-316">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-317">Identificateur du port parallèle.</span><span class="sxs-lookup"><span data-stu-id="a7b26-317">Identifier of the parallel port.</span></span>

<span data-ttu-id="a7b26-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-319">**DMASupport**</span><span class="sxs-lookup"><span data-stu-id="a7b26-319">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-320">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a7b26-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-322">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Ports parallèles DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="a7b26-322">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-323">Si la **valeur est true**, le port parallèle prend en charge DMA.</span><span class="sxs-lookup"><span data-stu-id="a7b26-323">If **TRUE**, the parallel port supports DMA.</span></span>

<span data-ttu-id="a7b26-324">Cette propriété est héritée de la [**\_ ParallelController CIM**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-324">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-325">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a7b26-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-326">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a7b26-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-328">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est effacée.</span><span class="sxs-lookup"><span data-stu-id="a7b26-328">If **TRUE**, the error reported in **LastErrorCode** is cleared.</span></span>

<span data-ttu-id="a7b26-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a7b26-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-333">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="a7b26-333">More information about the error recorded in **LastErrorCode**, and information about corrective actions that might be taken.</span></span>

<span data-ttu-id="a7b26-334">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a7b26-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-336">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7b26-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-338">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="a7b26-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-339">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7b26-339">Date and time the object was installed.</span></span> <span data-ttu-id="a7b26-340">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="a7b26-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a7b26-341">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a7b26-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-343">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7b26-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-345">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a7b26-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a7b26-346">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-347">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="a7b26-347">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-348">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7b26-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-350">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="a7b26-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-351">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="a7b26-351">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="a7b26-352">La valeur 0 (zéro) doit être utilisée si le nombre est inconnu.</span><span class="sxs-lookup"><span data-stu-id="a7b26-352">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="a7b26-353">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-353">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-354">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a7b26-354">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-357">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a7b26-357">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-358">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="a7b26-358">Label by which the object is known.</span></span> <span data-ttu-id="a7b26-359">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="a7b26-359">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a7b26-360">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-360">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-361">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="a7b26-361">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-362">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a7b26-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-364">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-364">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-365">Si la **valeur est true**, le port parallèle a été détecté automatiquement par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a7b26-365">If **TRUE**, the parallel port was automatically detected by the operating system.</span></span> <span data-ttu-id="a7b26-366">Si la **valeur est false**, cela signifie que le port a été détecté par d’autres moyens (par exemple, s’il est ajouté manuellement par le biais du panneau de configuration).</span><span class="sxs-lookup"><span data-stu-id="a7b26-366">If **FALSE**, the port was detected by other means (such as being manually added through the Control Panel).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-367">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a7b26-367">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-368">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-370">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a7b26-370">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-371">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a7b26-371">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a7b26-372">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a7b26-373">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="a7b26-373">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-374">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a7b26-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-375">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a7b26-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-377">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="a7b26-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a7b26-378">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="a7b26-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7b26-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a7b26-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a7b26-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="a7b26-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a7b26-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="a7b26-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a7b26-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="a7b26-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-383">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="a7b26-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a7b26-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="a7b26-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-385">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="a7b26-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a7b26-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="a7b26-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-387">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a7b26-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a7b26-388">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="a7b26-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a7b26-389">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-389">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a7b26-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="a7b26-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-391">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="a7b26-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a7b26-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="a7b26-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a7b26-393">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7b26-393">Timed Power-On Supported</span></span>

<span data-ttu-id="a7b26-394">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="a7b26-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a7b26-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a7b26-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-396">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a7b26-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-398">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, ce qui signifie qu’il peut être mis en mode de suspension, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a7b26-398">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="a7b26-399">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="a7b26-399">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="a7b26-400">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-401">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="a7b26-401">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-402">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a7b26-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-404">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a7b26-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-405">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="a7b26-405">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="a7b26-406">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-406">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="a7b26-407">Les valeurs sont répertoriées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="a7b26-407">Values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a7b26-408">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a7b26-408">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7b26-409">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="a7b26-409">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="a7b26-410">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="a7b26-410">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="a7b26-411">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="a7b26-411">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="a7b26-412">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="a7b26-412">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="a7b26-413">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="a7b26-413">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="a7b26-414">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="a7b26-414">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="a7b26-415">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="a7b26-415">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="a7b26-416">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="a7b26-416">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="a7b26-417">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="a7b26-417">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="a7b26-418">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="a7b26-418">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="a7b26-419">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="a7b26-419">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="a7b26-420">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="a7b26-420">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="a7b26-421">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="a7b26-421">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="a7b26-422">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="a7b26-422">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="a7b26-423">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="a7b26-423">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="a7b26-424">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="a7b26-424">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="a7b26-425">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="a7b26-425">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="a7b26-426">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="a7b26-426">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="a7b26-427">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="a7b26-427">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="a7b26-428">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="a7b26-428">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="a7b26-429">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="a7b26-429">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="a7b26-430">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="a7b26-430">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="a7b26-431">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="a7b26-431">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="a7b26-432">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="a7b26-432">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="a7b26-433">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="a7b26-433">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="a7b26-434">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="a7b26-434">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="a7b26-435">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="a7b26-435">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="a7b26-436">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="a7b26-436">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="a7b26-437">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="a7b26-437">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="a7b26-438">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="a7b26-438">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="a7b26-439">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="a7b26-439">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="a7b26-440">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="a7b26-440">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="a7b26-441">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="a7b26-441">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="a7b26-442">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="a7b26-442">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="a7b26-443">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="a7b26-443">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="a7b26-444">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="a7b26-444">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="a7b26-445">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="a7b26-445">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="a7b26-446">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="a7b26-446">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="a7b26-447">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="a7b26-447">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="a7b26-448">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="a7b26-448">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="a7b26-449">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="a7b26-449">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="a7b26-450">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="a7b26-450">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="a7b26-451">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="a7b26-451">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="a7b26-452">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="a7b26-452">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="a7b26-453">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="a7b26-453">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="a7b26-454">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="a7b26-454">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7b26-455">**État**</span><span class="sxs-lookup"><span data-stu-id="a7b26-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-456">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-458">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a7b26-458">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-459">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7b26-459">Current status of the object.</span></span> <span data-ttu-id="a7b26-460">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="a7b26-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a7b26-461">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="a7b26-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a7b26-462">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="a7b26-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a7b26-463">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="a7b26-463">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a7b26-464">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="a7b26-464">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a7b26-465">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a7b26-466">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7b26-466">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a7b26-467">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a7b26-468">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a7b26-469">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7b26-470">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="a7b26-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a7b26-471">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a7b26-472">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a7b26-473">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a7b26-474">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a7b26-475">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a7b26-476">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a7b26-477">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a7b26-478">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="a7b26-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7b26-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a7b26-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-480">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a7b26-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-482">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a7b26-482">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-483">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a7b26-483">State of the logical device.</span></span> <span data-ttu-id="a7b26-484">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="a7b26-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a7b26-485">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a7b26-486">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a7b26-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7b26-487">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="a7b26-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a7b26-488">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="a7b26-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a7b26-489">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="a7b26-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a7b26-490">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="a7b26-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7b26-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a7b26-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-492">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-493">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-494">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a7b26-494">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-495">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="a7b26-495">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="a7b26-496">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-496">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-497">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a7b26-497">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-498">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7b26-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-500">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a7b26-500">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-501">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="a7b26-501">Name of the scoping system.</span></span>

<span data-ttu-id="a7b26-502">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7b26-503">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="a7b26-503">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7b26-504">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7b26-504">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7b26-505">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7b26-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7b26-506">Date et heure de la dernière réinitialisation du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="a7b26-506">Date and time the controller was last reset.</span></span> <span data-ttu-id="a7b26-507">Cela peut signifier que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="a7b26-507">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="a7b26-508">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-508">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7b26-509">Notes</span><span class="sxs-lookup"><span data-stu-id="a7b26-509">Remarks</span></span>

<span data-ttu-id="a7b26-510">La classe **Win32 \_ ParallelPort** est dérivée de [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a7b26-510">The **Win32\_ParallelPort** class is derived from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b26-511">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7b26-511">Requirements</span></span>



| <span data-ttu-id="a7b26-512">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7b26-512">Requirement</span></span> | <span data-ttu-id="a7b26-513">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7b26-513">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b26-514">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7b26-514">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b26-515">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7b26-515">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7b26-516">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7b26-516">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b26-517">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7b26-517">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7b26-518">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a7b26-518">Namespace</span></span><br/>                | <span data-ttu-id="a7b26-519">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a7b26-519">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7b26-520">MOF</span><span class="sxs-lookup"><span data-stu-id="a7b26-520">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7b26-521"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7b26-521"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7b26-522">DLL</span><span class="sxs-lookup"><span data-stu-id="a7b26-522">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7b26-523"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7b26-523"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7b26-524">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7b26-524">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b26-525">**\_PARALLELCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="a7b26-525">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dt>

[<span data-ttu-id="a7b26-526">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="a7b26-526">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
