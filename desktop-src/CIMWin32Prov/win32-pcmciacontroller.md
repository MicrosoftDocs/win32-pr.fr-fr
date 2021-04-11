---
description: Le \_ PCMCIAController Win32 &\# 32 ; La classe WMI gère les fonctionnalités d’un appareil de contrôleur de carte réseau d’ordinateur personnel (PCMCIA).
ms.assetid: 541f8ebd-e976-425a-817a-72ab151e8b93
ms.tgt_platform: multiple
title: Classe Win32_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PCMCIAController
- Win32_PCMCIAController.Reset
- Win32_PCMCIAController.SetPowerState
- Win32_PCMCIAController.Availability
- Win32_PCMCIAController.Caption
- Win32_PCMCIAController.ConfigManagerErrorCode
- Win32_PCMCIAController.ConfigManagerUserConfig
- Win32_PCMCIAController.CreationClassName
- Win32_PCMCIAController.Description
- Win32_PCMCIAController.DeviceID
- Win32_PCMCIAController.ErrorCleared
- Win32_PCMCIAController.ErrorDescription
- Win32_PCMCIAController.InstallDate
- Win32_PCMCIAController.LastErrorCode
- Win32_PCMCIAController.Manufacturer
- Win32_PCMCIAController.MaxNumberControlled
- Win32_PCMCIAController.Name
- Win32_PCMCIAController.PNPDeviceID
- Win32_PCMCIAController.PowerManagementCapabilities
- Win32_PCMCIAController.PowerManagementSupported
- Win32_PCMCIAController.ProtocolSupported
- Win32_PCMCIAController.Status
- Win32_PCMCIAController.StatusInfo
- Win32_PCMCIAController.SystemCreationClassName
- Win32_PCMCIAController.SystemName
- Win32_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 463be0c3924130ce0e2c0ff84c3852398b6cff99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201106"
---
# <a name="win32_pcmciacontroller-class"></a><span data-ttu-id="ee051-103">\_Classe PCMCIAController Win32</span><span class="sxs-lookup"><span data-stu-id="ee051-103">Win32\_PCMCIAController class</span></span>

<span data-ttu-id="ee051-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PCMCIAController** WMI gère les fonctionnalités d’un appareil de contrôleur de carte réseau d’ordinateur personnel (PCMCIA).</span><span class="sxs-lookup"><span data-stu-id="ee051-104">The **Win32\_PCMCIAController** [WMI class](../wmisdk/retrieving-a-class.md) manages the capabilities of a Personal Computer Memory Card Interface Adapter (PCMCIA of a PC Card) controller device.</span></span>

<span data-ttu-id="ee051-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ee051-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ee051-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ee051-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee051-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee051-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{98C7E2C6-D592-11d2-B355-00105A0A323A}"), AMENDMENT]
class Win32_PCMCIAController : CIM_PCMCIAController
{
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
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
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

## <a name="members"></a><span data-ttu-id="ee051-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ee051-108">Members</span></span>

<span data-ttu-id="ee051-109">La classe **Win32 \_ PCMCIAController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee051-109">The **Win32\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="ee051-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ee051-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ee051-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee051-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ee051-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ee051-112">Methods</span></span>

<span data-ttu-id="ee051-113">La classe **Win32 \_ PCMCIAController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ee051-113">The **Win32\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="ee051-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="ee051-114">Method</span></span>            | <span data-ttu-id="ee051-115">Description</span><span class="sxs-lookup"><span data-stu-id="ee051-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee051-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="ee051-116">**Reset**</span></span>         | <span data-ttu-id="ee051-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ee051-117">Not implemented.</span></span> <span data-ttu-id="ee051-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span><br/>                 |
| <span data-ttu-id="ee051-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ee051-119">**SetPowerState**</span></span> | <span data-ttu-id="ee051-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ee051-120">Not implemented.</span></span> <span data-ttu-id="ee051-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ee051-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee051-122">Properties</span></span>

<span data-ttu-id="ee051-123">La classe **Win32 \_ PCMCIAController** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee051-123">The **Win32\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee051-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="ee051-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee051-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-127">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="ee051-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-128">Availability and status of the device.</span></span>

<span data-ttu-id="ee051-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee051-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ee051-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee051-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ee051-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ee051-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="ee051-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="ee051-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ee051-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="ee051-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ee051-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="ee051-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ee051-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="ee051-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ee051-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="ee051-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ee051-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="ee051-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ee051-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="ee051-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ee051-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="ee051-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ee051-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="ee051-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ee051-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="ee051-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ee051-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="ee051-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="ee051-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ee051-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="ee051-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="ee051-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ee051-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="ee051-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="ee051-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ee051-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="ee051-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ee051-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="ee051-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="ee051-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ee051-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="ee051-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-153">Suspendu.</span><span class="sxs-lookup"><span data-stu-id="ee051-153">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ee051-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="ee051-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-155">Non prêt.</span><span class="sxs-lookup"><span data-stu-id="ee051-155">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ee051-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="ee051-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-157">Non configuré.</span><span class="sxs-lookup"><span data-stu-id="ee051-157">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ee051-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="ee051-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-159">Arrêté.</span><span class="sxs-lookup"><span data-stu-id="ee051-159">Quiesced.</span></span>

<span data-ttu-id="ee051-160">Le contrôleur PCMCIA n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ee051-160">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee051-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ee051-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-164">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="ee051-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-165">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee051-165">Short description of the object.</span></span>

<span data-ttu-id="ee051-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ee051-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee051-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-170">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ee051-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-171">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="ee051-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ee051-172">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ee051-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="ee051-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ee051-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="ee051-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-175">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="ee051-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ee051-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="ee051-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ee051-177">(1)</span><span class="sxs-lookup"><span data-stu-id="ee051-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-178">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="ee051-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ee051-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ee051-180">(2)</span><span class="sxs-lookup"><span data-stu-id="ee051-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ee051-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="ee051-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ee051-182">(3)</span><span class="sxs-lookup"><span data-stu-id="ee051-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-183">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="ee051-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ee051-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="ee051-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ee051-185">(4)</span><span class="sxs-lookup"><span data-stu-id="ee051-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-186">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="ee051-186">Device is not working properly.</span></span> <span data-ttu-id="ee051-187">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="ee051-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ee051-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="ee051-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ee051-189">(5)</span><span class="sxs-lookup"><span data-stu-id="ee051-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-190">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="ee051-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ee051-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="ee051-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ee051-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="ee051-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-193">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="ee051-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ee051-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="ee051-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ee051-195">(7)</span><span class="sxs-lookup"><span data-stu-id="ee051-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ee051-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="ee051-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ee051-197">(8)</span><span class="sxs-lookup"><span data-stu-id="ee051-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-198">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="ee051-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ee051-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ee051-200">(9)</span><span class="sxs-lookup"><span data-stu-id="ee051-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-201">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="ee051-201">Device is not working properly.</span></span> <span data-ttu-id="ee051-202">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ee051-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ee051-204">(10)</span><span class="sxs-lookup"><span data-stu-id="ee051-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-205">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ee051-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ee051-207">(11)</span><span class="sxs-lookup"><span data-stu-id="ee051-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-208">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ee051-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="ee051-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ee051-210">douze</span><span class="sxs-lookup"><span data-stu-id="ee051-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-211">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ee051-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ee051-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ee051-213">(13)</span><span class="sxs-lookup"><span data-stu-id="ee051-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-214">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ee051-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="ee051-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ee051-216">(14)</span><span class="sxs-lookup"><span data-stu-id="ee051-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-217">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="ee051-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ee051-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="ee051-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ee051-219">(15)</span><span class="sxs-lookup"><span data-stu-id="ee051-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-220">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="ee051-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ee051-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ee051-222">(16)</span><span class="sxs-lookup"><span data-stu-id="ee051-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-223">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ee051-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="ee051-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ee051-225">(17)</span><span class="sxs-lookup"><span data-stu-id="ee051-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-226">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="ee051-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ee051-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ee051-228">(18)</span><span class="sxs-lookup"><span data-stu-id="ee051-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-229">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="ee051-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ee051-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="ee051-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ee051-231">(19)</span><span class="sxs-lookup"><span data-stu-id="ee051-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ee051-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="ee051-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ee051-233">(20)</span><span class="sxs-lookup"><span data-stu-id="ee051-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-234">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="ee051-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ee051-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ee051-236">(21)</span><span class="sxs-lookup"><span data-stu-id="ee051-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-237">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="ee051-237">System failure.</span></span> <span data-ttu-id="ee051-238">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="ee051-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ee051-239">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ee051-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="ee051-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ee051-241">(22)</span><span class="sxs-lookup"><span data-stu-id="ee051-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-242">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="ee051-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ee051-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="ee051-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ee051-244">(23)</span><span class="sxs-lookup"><span data-stu-id="ee051-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-245">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="ee051-245">System failure.</span></span> <span data-ttu-id="ee051-246">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="ee051-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ee051-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="ee051-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ee051-248">(24)</span><span class="sxs-lookup"><span data-stu-id="ee051-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-249">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="ee051-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ee051-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ee051-251">(25)</span><span class="sxs-lookup"><span data-stu-id="ee051-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-252">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ee051-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ee051-254">(26)</span><span class="sxs-lookup"><span data-stu-id="ee051-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-255">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee051-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ee051-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="ee051-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ee051-257">(27)</span><span class="sxs-lookup"><span data-stu-id="ee051-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-258">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="ee051-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ee051-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="ee051-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ee051-260">(28)</span><span class="sxs-lookup"><span data-stu-id="ee051-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-261">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="ee051-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ee051-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="ee051-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ee051-263">(29)</span><span class="sxs-lookup"><span data-stu-id="ee051-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-264">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="ee051-264">Device is disabled.</span></span> <span data-ttu-id="ee051-265">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="ee051-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ee051-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="ee051-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ee051-267">(30)</span><span class="sxs-lookup"><span data-stu-id="ee051-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-268">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="ee051-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ee051-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ee051-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ee051-270">31</span><span class="sxs-lookup"><span data-stu-id="ee051-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-271">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="ee051-271">Device is not working properly.</span></span> <span data-ttu-id="ee051-272">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="ee051-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee051-273">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="ee051-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-274">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee051-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-276">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ee051-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-277">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee051-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ee051-278">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ee051-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-282">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ee051-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ee051-283">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="ee051-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="ee051-284">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="ee051-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ee051-285">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-286">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee051-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-287">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-289">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ee051-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-290">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee051-290">Description of the object.</span></span>

<span data-ttu-id="ee051-291">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ee051-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-295">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="ee051-295">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-296">Identificateur unique de cet appareil avec les autres périphériques utilisant le BIOS Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="ee051-296">Unique identifier of this device with other peripherals using the Plug and Play BIOS.</span></span> <span data-ttu-id="ee051-297">Cette propriété est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-297">This property is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-298">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ee051-298">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-299">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee051-299">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee051-301">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="ee051-301">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="ee051-302">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-303">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ee051-303">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee051-306">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="ee051-306">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="ee051-307">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ee051-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-309">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ee051-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-311">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="ee051-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-312">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee051-312">Date and time the object was installed.</span></span> <span data-ttu-id="ee051-313">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="ee051-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ee051-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-315">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ee051-315">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-316">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee051-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee051-318">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ee051-318">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ee051-319">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-320">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="ee051-320">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-323">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ee051-323">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-324">Nom du fabricant du contrôleur PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="ee051-324">Name of the PCMCIA controller manufacturer.</span></span>

<span data-ttu-id="ee051-325">Cette propriété est héritée de la [**\_ PCMCIAController CIM**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-325">This property is inherited from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span>

<span data-ttu-id="ee051-326">Exemple : « Acme »</span><span class="sxs-lookup"><span data-stu-id="ee051-326">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="ee051-327">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="ee051-327">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-328">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee051-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-330">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="ee051-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-331">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="ee051-331">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="ee051-332">La valeur 0 (zéro) doit être utilisée si le nombre est inconnu.</span><span class="sxs-lookup"><span data-stu-id="ee051-332">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="ee051-333">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-333">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-334">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ee051-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-335">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-337">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ee051-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-338">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="ee051-338">Label by which the object is known.</span></span> <span data-ttu-id="ee051-339">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="ee051-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="ee051-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-341">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ee051-341">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-344">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ee051-344">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-345">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ee051-345">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="ee051-346">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ee051-347">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="ee051-347">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ee051-348">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ee051-348">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-349">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee051-349">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee051-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee051-351">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="ee051-351">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ee051-352">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="ee051-352">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee051-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ee051-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ee051-354"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="ee051-354"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ee051-355"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="ee051-355"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ee051-356"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="ee051-356"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-357">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="ee051-357">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ee051-358"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="ee051-358"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-359">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="ee051-359">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ee051-360"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="ee051-360"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-361">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ee051-361">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ee051-362">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="ee051-362">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ee051-363">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-363">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ee051-364"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="ee051-364"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-365">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="ee051-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ee051-366"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="ee051-366"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ee051-367">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee051-367">Timed Power-On Supported</span></span>

<span data-ttu-id="ee051-368">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="ee051-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee051-369">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ee051-369">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-370">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ee051-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee051-372">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="ee051-372">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="ee051-373">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="ee051-373">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="ee051-374">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-375">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="ee051-375">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-376">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee051-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-378">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ee051-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-379">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="ee051-379">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="ee051-380">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-380">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="ee051-381">Les valeurs sont indiquées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="ee051-381">The values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee051-382">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ee051-382">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee051-383">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ee051-383">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="ee051-384">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="ee051-384">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="ee051-385">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="ee051-385">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="ee051-386">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="ee051-386">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="ee051-387">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="ee051-387">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="ee051-388">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="ee051-388">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="ee051-389">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="ee051-389">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="ee051-390">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="ee051-390">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="ee051-391">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="ee051-391">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="ee051-392">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="ee051-392">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="ee051-393">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="ee051-393">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="ee051-394">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="ee051-394">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="ee051-395">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="ee051-395">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="ee051-396">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="ee051-396">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="ee051-397">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="ee051-397">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="ee051-398">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="ee051-398">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="ee051-399">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="ee051-399">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="ee051-400">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="ee051-400">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="ee051-401">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="ee051-401">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="ee051-402">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="ee051-402">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="ee051-403">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="ee051-403">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="ee051-404">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="ee051-404">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="ee051-405">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="ee051-405">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="ee051-406">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="ee051-406">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="ee051-407">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="ee051-407">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="ee051-408">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="ee051-408">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="ee051-409">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="ee051-409">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="ee051-410">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="ee051-410">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="ee051-411">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="ee051-411">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="ee051-412">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="ee051-412">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="ee051-413">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="ee051-413">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="ee051-414">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="ee051-414">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="ee051-415">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="ee051-415">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="ee051-416">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="ee051-416">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="ee051-417">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="ee051-417">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="ee051-418">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="ee051-418">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="ee051-419">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="ee051-419">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="ee051-420">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="ee051-420">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="ee051-421">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="ee051-421">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="ee051-422">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="ee051-422">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="ee051-423">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="ee051-423">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="ee051-424">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="ee051-424">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="ee051-425">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="ee051-425">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="ee051-426">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="ee051-426">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="ee051-427">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="ee051-427">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="ee051-428">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="ee051-428">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee051-429">**État**</span><span class="sxs-lookup"><span data-stu-id="ee051-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-432">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ee051-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-433">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee051-433">Current status of the object.</span></span> <span data-ttu-id="ee051-434">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="ee051-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ee051-435">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="ee051-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ee051-436">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="ee051-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ee051-437">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="ee051-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ee051-438">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="ee051-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ee051-439">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ee051-440">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee051-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ee051-441">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="ee051-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ee051-442">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="ee051-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ee051-443">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="ee051-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee051-444">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="ee051-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ee051-445">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="ee051-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ee051-446">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ee051-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ee051-447">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="ee051-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ee051-448">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="ee051-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ee051-449">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="ee051-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ee051-450">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="ee051-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ee051-451">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="ee051-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ee051-452">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="ee051-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee051-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ee051-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-454">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee051-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-456">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ee051-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ee051-457">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ee051-457">State of the logical device.</span></span> <span data-ttu-id="ee051-458">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="ee051-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ee051-459">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee051-460">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ee051-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee051-461">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ee051-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ee051-462">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="ee051-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ee051-463">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="ee051-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ee051-464">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="ee051-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee051-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ee051-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-466">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-467">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-468">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ee051-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ee051-469">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ee051-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="ee051-470">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ee051-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-472">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee051-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-473">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee051-474">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ee051-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ee051-475">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ee051-475">Name of the scoping system.</span></span>

<span data-ttu-id="ee051-476">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee051-477">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="ee051-477">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee051-478">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ee051-478">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee051-479">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee051-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee051-480">Date et heure de la dernière réinitialisation du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="ee051-480">Date and time the controller was last reset.</span></span> <span data-ttu-id="ee051-481">Cela peut signifier que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="ee051-481">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="ee051-482">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-482">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee051-483">Notes</span><span class="sxs-lookup"><span data-stu-id="ee051-483">Remarks</span></span>

<span data-ttu-id="ee051-484">La classe **Win32 \_ PCMCIAController** est dérivée de [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="ee051-484">The **Win32\_PCMCIAController** class is derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee051-485">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee051-485">Requirements</span></span>



| <span data-ttu-id="ee051-486">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee051-486">Requirement</span></span> | <span data-ttu-id="ee051-487">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee051-487">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee051-488">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee051-488">Minimum supported client</span></span><br/> | <span data-ttu-id="ee051-489">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee051-489">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee051-490">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee051-490">Minimum supported server</span></span><br/> | <span data-ttu-id="ee051-491">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee051-491">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee051-492">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ee051-492">Namespace</span></span><br/>                | <span data-ttu-id="ee051-493">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ee051-493">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee051-494">MOF</span><span class="sxs-lookup"><span data-stu-id="ee051-494">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee051-495"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee051-495"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee051-496">DLL</span><span class="sxs-lookup"><span data-stu-id="ee051-496">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee051-497"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee051-497"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee051-498">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee051-498">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee051-499">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="ee051-499">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="ee051-500">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="ee051-500">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
