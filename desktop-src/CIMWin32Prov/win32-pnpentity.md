---
description: Epresents les propriétés d’un appareil Plug-and-Play.
ms.assetid: 621f4410-8d8f-4afa-b0f0-beed263f3a13
ms.tgt_platform: multiple
title: Classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity
- Win32_PnPEntity.Reset
- Win32_PnPEntity.SetPowerState
- Win32_PnPEntity.Availability
- Win32_PnPEntity.Caption
- Win32_PnPEntity.ClassGuid
- Win32_PnPEntity.CompatibleID
- Win32_PnPEntity.ConfigManagerErrorCode
- Win32_PnPEntity.ConfigManagerUserConfig
- Win32_PnPEntity.CreationClassName
- Win32_PnPEntity.Description
- Win32_PnPEntity.DeviceID
- Win32_PnPEntity.ErrorCleared
- Win32_PnPEntity.ErrorDescription
- Win32_PnPEntity.HardwareID
- Win32_PnPEntity.InstallDate
- Win32_PnPEntity.LastErrorCode
- Win32_PnPEntity.Manufacturer
- Win32_PnPEntity.Name
- Win32_PnPEntity.PNPClass
- Win32_PnPEntity.PNPDeviceID
- Win32_PnPEntity.PowerManagementCapabilities
- Win32_PnPEntity.PowerManagementSupported
- Win32_PnPEntity.Present
- Win32_PnPEntity.Service
- Win32_PnPEntity.Status
- Win32_PnPEntity.StatusInfo
- Win32_PnPEntity.SystemCreationClassName
- Win32_PnPEntity.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62eaa59944c9b71a1b8b3520969122ab23350bba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110234"
---
# <a name="win32_pnpentity-class"></a><span data-ttu-id="0d214-103">\_Classe PnPEntity Win32</span><span class="sxs-lookup"><span data-stu-id="0d214-103">Win32\_PnPEntity class</span></span>

<span data-ttu-id="0d214-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PnPEntity** WMI représente les propriétés d’un appareil plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="0d214-104">The **Win32\_PnPEntity** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a Plug and Play device.</span></span> <span data-ttu-id="0d214-105">Plug-and-Play entités sont affichées comme entrées dans le Gestionnaire de périphériques situé dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="0d214-105">Plug and Play entities are shown as entries in the Device Manager located in Control Panel.</span></span>

<span data-ttu-id="0d214-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0d214-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0d214-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0d214-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d214-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d214-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FE28FD98-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPEntity : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  string   ClassGuid;
  string   CompatibleID[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareID[];
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  string   PNPClass;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  Present;
  string   Service;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="0d214-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0d214-109">Members</span></span>

<span data-ttu-id="0d214-110">La classe **Win32 \_ PnPEntity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0d214-110">The **Win32\_PnPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="0d214-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0d214-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0d214-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d214-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0d214-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0d214-113">Methods</span></span>

<span data-ttu-id="0d214-114">La classe **Win32 \_ PnPEntity** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0d214-114">The **Win32\_PnPEntity** class has these methods.</span></span>



| <span data-ttu-id="0d214-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="0d214-115">Method</span></span>                                                             | <span data-ttu-id="0d214-116">Description</span><span class="sxs-lookup"><span data-stu-id="0d214-116">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d214-117">**Désactive**</span><span class="sxs-lookup"><span data-stu-id="0d214-117">**Disable**</span></span>](disable-win32-pnpentity.md)                         | <span data-ttu-id="0d214-118">Désactive cet appareil Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="0d214-118">Disables this Plug and Play device.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="0d214-119">**Activer**</span><span class="sxs-lookup"><span data-stu-id="0d214-119">**Enable**</span></span>](enable-win32-pnpentity.md)                           | <span data-ttu-id="0d214-120">Active cette Plug-and-Play appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-120">Enables this Plug and Play device.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="0d214-121">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="0d214-121">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md) | <span data-ttu-id="0d214-122">Obtient les propriétés spécifiées de cette Plug-and-Play appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-122">Gets the specified properties of this Plug and Play device.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="0d214-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="0d214-123">**Reset**</span></span>                                                          | <span data-ttu-id="0d214-124">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0d214-124">Not implemented.</span></span> <span data-ttu-id="0d214-125">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-125">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="0d214-126">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0d214-126">**SetPowerState**</span></span>                                                  | <span data-ttu-id="0d214-127">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0d214-127">Not implemented.</span></span> <span data-ttu-id="0d214-128">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-128">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0d214-129">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d214-129">Properties</span></span>

<span data-ttu-id="0d214-130">La classe **Win32 \_ PnPEntity** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0d214-130">The **Win32\_PnPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d214-131">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="0d214-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-132">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d214-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-134">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0d214-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-135">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-135">Availability and status of the device.</span></span>

<span data-ttu-id="0d214-136">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d214-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0d214-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d214-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0d214-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0d214-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="0d214-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-140">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="0d214-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0d214-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="0d214-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0d214-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="0d214-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d214-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="0d214-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0d214-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="0d214-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0d214-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="0d214-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0d214-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="0d214-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0d214-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="0d214-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0d214-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="0d214-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0d214-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="0d214-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0d214-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="0d214-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-151">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="0d214-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0d214-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="0d214-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-153">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="0d214-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0d214-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="0d214-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-155">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="0d214-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0d214-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="0d214-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0d214-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="0d214-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-158">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="0d214-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0d214-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="0d214-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-160">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="0d214-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0d214-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="0d214-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-162">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="0d214-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0d214-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="0d214-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-164">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="0d214-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0d214-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="0d214-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-166">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="0d214-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d214-167">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0d214-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-170">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0d214-170">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-171">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d214-171">Short description of the object.</span></span>

<span data-ttu-id="0d214-172">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-173">**ClassGuid**</span><span class="sxs-lookup"><span data-stu-id="0d214-173">**ClassGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-176">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0d214-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-177">Identificateur global unique (GUID) de cet Plug-and-Play appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-177">Globally unique identifier (GUID) of this Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="0d214-178">**CompatibleID**</span><span class="sxs-lookup"><span data-stu-id="0d214-178">**CompatibleID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-179">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0d214-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d214-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d214-181">Chaîne d’identification définie par le fournisseur que le programme d’installation utilise pour faire correspondre un appareil à un fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0d214-181">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="0d214-182">Une liste d’ID compatibles peut être associée à un appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-182">A device can have a list of compatible IDs associated with it.</span></span> <span data-ttu-id="0d214-183">Les ID compatibles doivent être classés par ordre décroissant d’adéquation.</span><span class="sxs-lookup"><span data-stu-id="0d214-183">The compatible IDs should be listed in order of decreasing suitability.</span></span> <span data-ttu-id="0d214-184">Si le programme d’installation ne parvient pas à localiser un fichier INF qui correspond à l’un des ID de matériel d’un appareil, il utilise des ID compatibles pour localiser un fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0d214-184">If Setup cannot locate an INF file that matches one of a device's hardware IDs, it uses compatible IDs to locate an INF file.</span></span> <span data-ttu-id="0d214-185">Un ID compatible a le même format qu’un **HardwareID**.</span><span class="sxs-lookup"><span data-stu-id="0d214-185">A compatible ID has the same format as a **HardwareID**.</span></span> <span data-ttu-id="0d214-186">Pour plus d’informations, consultez [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="0d214-186">For more information, see [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0d214-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-188">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d214-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-190">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0d214-190">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-191">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="0d214-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0d214-192">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0d214-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="0d214-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0d214-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="0d214-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-195">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="0d214-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0d214-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="0d214-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0d214-197">(1)</span><span class="sxs-lookup"><span data-stu-id="0d214-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-198">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="0d214-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0d214-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0d214-200">(2)</span><span class="sxs-lookup"><span data-stu-id="0d214-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0d214-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="0d214-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0d214-202">(3)</span><span class="sxs-lookup"><span data-stu-id="0d214-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-203">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="0d214-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0d214-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="0d214-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0d214-205">(4)</span><span class="sxs-lookup"><span data-stu-id="0d214-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-206">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0d214-206">Device is not working properly.</span></span> <span data-ttu-id="0d214-207">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="0d214-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0d214-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="0d214-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0d214-209">(5)</span><span class="sxs-lookup"><span data-stu-id="0d214-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-210">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="0d214-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0d214-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="0d214-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0d214-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="0d214-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-213">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="0d214-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0d214-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="0d214-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0d214-215">(7)</span><span class="sxs-lookup"><span data-stu-id="0d214-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0d214-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="0d214-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0d214-217">(8)</span><span class="sxs-lookup"><span data-stu-id="0d214-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-218">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="0d214-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0d214-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0d214-220">(9)</span><span class="sxs-lookup"><span data-stu-id="0d214-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-221">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0d214-221">Device is not working properly.</span></span> <span data-ttu-id="0d214-222">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-222">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0d214-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0d214-224">(10)</span><span class="sxs-lookup"><span data-stu-id="0d214-224">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-225">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-225">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0d214-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0d214-227">(11)</span><span class="sxs-lookup"><span data-stu-id="0d214-227">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-228">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-228">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0d214-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="0d214-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0d214-230">douze</span><span class="sxs-lookup"><span data-stu-id="0d214-230">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-231">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0d214-231">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0d214-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0d214-233">(13)</span><span class="sxs-lookup"><span data-stu-id="0d214-233">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-234">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-234">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0d214-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="0d214-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0d214-236">(14)</span><span class="sxs-lookup"><span data-stu-id="0d214-236">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-237">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="0d214-237">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0d214-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="0d214-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0d214-239">(15)</span><span class="sxs-lookup"><span data-stu-id="0d214-239">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-240">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="0d214-240">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0d214-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0d214-242">(16)</span><span class="sxs-lookup"><span data-stu-id="0d214-242">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-243">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-243">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0d214-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="0d214-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0d214-245">(17)</span><span class="sxs-lookup"><span data-stu-id="0d214-245">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-246">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="0d214-246">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0d214-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0d214-248">(18)</span><span class="sxs-lookup"><span data-stu-id="0d214-248">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-249">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="0d214-249">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0d214-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="0d214-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0d214-251">(19)</span><span class="sxs-lookup"><span data-stu-id="0d214-251">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0d214-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="0d214-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0d214-253">(20)</span><span class="sxs-lookup"><span data-stu-id="0d214-253">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-254">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="0d214-254">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0d214-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0d214-256">(21)</span><span class="sxs-lookup"><span data-stu-id="0d214-256">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-257">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="0d214-257">System failure.</span></span> <span data-ttu-id="0d214-258">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="0d214-258">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0d214-259">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-259">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0d214-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="0d214-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0d214-261">(22)</span><span class="sxs-lookup"><span data-stu-id="0d214-261">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-262">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0d214-262">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0d214-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="0d214-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0d214-264">(23)</span><span class="sxs-lookup"><span data-stu-id="0d214-264">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-265">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="0d214-265">System failure.</span></span> <span data-ttu-id="0d214-266">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="0d214-266">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0d214-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="0d214-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0d214-268">(24)</span><span class="sxs-lookup"><span data-stu-id="0d214-268">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-269">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="0d214-269">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0d214-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0d214-271">(25)</span><span class="sxs-lookup"><span data-stu-id="0d214-271">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-272">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0d214-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0d214-274">(26)</span><span class="sxs-lookup"><span data-stu-id="0d214-274">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-275">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0d214-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="0d214-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0d214-277">(27)</span><span class="sxs-lookup"><span data-stu-id="0d214-277">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-278">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="0d214-278">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0d214-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="0d214-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0d214-280">(28)</span><span class="sxs-lookup"><span data-stu-id="0d214-280">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-281">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="0d214-281">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0d214-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="0d214-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0d214-283">(29)</span><span class="sxs-lookup"><span data-stu-id="0d214-283">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-284">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0d214-284">Device is disabled.</span></span> <span data-ttu-id="0d214-285">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="0d214-285">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0d214-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="0d214-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0d214-287">(30)</span><span class="sxs-lookup"><span data-stu-id="0d214-287">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-288">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="0d214-288">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0d214-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="0d214-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0d214-290">31</span><span class="sxs-lookup"><span data-stu-id="0d214-290">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-291">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0d214-291">Device is not working properly.</span></span> <span data-ttu-id="0d214-292">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="0d214-292">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d214-293">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0d214-293">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-294">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d214-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-296">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0d214-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-297">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0d214-297">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0d214-298">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-299">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0d214-299">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-302">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="0d214-302">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="0d214-303">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0d214-303">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0d214-304">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0d214-304">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0d214-305">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-306">**Description**</span><span class="sxs-lookup"><span data-stu-id="0d214-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-309">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0d214-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-310">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d214-310">Description of the object.</span></span>

<span data-ttu-id="0d214-311">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0d214-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-315">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« DeviceID »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0d214-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-316">Identificateur de l’appareil Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="0d214-316">Identifier of the Plug and Play device.</span></span>

<span data-ttu-id="0d214-317">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0d214-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-319">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d214-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d214-321">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="0d214-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="0d214-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0d214-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d214-326">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="0d214-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="0d214-327">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-328">**HardwareID**</span><span class="sxs-lookup"><span data-stu-id="0d214-328">**HardwareID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-329">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0d214-329">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d214-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d214-331">Chaîne d’identification définie par le fournisseur que le programme d’installation utilise pour faire correspondre un appareil à un fichier INF.</span><span class="sxs-lookup"><span data-stu-id="0d214-331">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="0d214-332">Normalement, un appareil possède une liste associée d’ID matériels.</span><span class="sxs-lookup"><span data-stu-id="0d214-332">Normally, a device has an associated list of hardware IDs.</span></span> <span data-ttu-id="0d214-333">Le pilote de bus 1394, qui n’utilise pas d’ID de matériel, est une exception.</span><span class="sxs-lookup"><span data-stu-id="0d214-333">An exception is the 1394 bus driver, which does not use hardware IDs.</span></span> <span data-ttu-id="0d214-334">Le premier ID matériel de la liste doit être l’ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-334">The first hardware ID in the list should be the device ID.</span></span> <span data-ttu-id="0d214-335">Les ID restants doivent être classés par ordre décroissant d’adéquation.</span><span class="sxs-lookup"><span data-stu-id="0d214-335">The remaining IDs should be listed in order of decreasing suitability.</span></span>

<span data-ttu-id="0d214-336">Les ID de matériel s’affichent dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="0d214-336">Hardware IDs appear in one the following formats:</span></span>

-   <span data-ttu-id="0d214-337">énumérateur d’énumérateur \\ -spécifique-appareil-ID</span><span class="sxs-lookup"><span data-stu-id="0d214-337">enumerator\\enumerator-specific-device-ID</span></span>

    <span data-ttu-id="0d214-338">Il s’agit du format le plus courant pour les périphériques PnP individuels.</span><span class="sxs-lookup"><span data-stu-id="0d214-338">This is the most common format for individual PnP devices.</span></span> <span data-ttu-id="0d214-339">Le BIOS ou la ISAPNP est un exemple d’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0d214-339">An example of an enumerator is the BIOS or ISAPNP.</span></span>

-   <span data-ttu-id="0d214-340">\*ID spécifique à l’énumérateur</span><span class="sxs-lookup"><span data-stu-id="0d214-340">\*enumerator-specific ID</span></span>

    <span data-ttu-id="0d214-341">Un astérisque ( \* ) indique une utilisation par plus d’un énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0d214-341">An asterisk (\*) indicates use by more than one enumerator.</span></span>

-   <span data-ttu-id="0d214-342">ID spécifique à la classe de l’appareil</span><span class="sxs-lookup"><span data-stu-id="0d214-342">device-class-specific ID</span></span>

    <span data-ttu-id="0d214-343">Format personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0d214-343">A custom format.</span></span>

<span data-ttu-id="0d214-344">Voici quelques exemples d’ID de matériel :</span><span class="sxs-lookup"><span data-stu-id="0d214-344">Examples of Hardware IDs are:</span></span>

<dl> <dd><span data-ttu-id="0d214-345">\\ \* PNPOF08 racine</span><span class="sxs-lookup"><span data-stu-id="0d214-345">root\\\*PNPOF08</span></span></dd> <dd><span data-ttu-id="0d214-346">PC \\ VEN \_ 1000&DEV \_ 001&subsi \_ 00000000&Rev \_ 02</span><span class="sxs-lookup"><span data-stu-id="0d214-346">PC\\VEN\_1000&DEV\_001&SUBSYS\_00000000&REV\_02</span></span></dd> </dl>

<span data-ttu-id="0d214-347">Pour plus d’informations, consultez le [Kit de pilotes Windows](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="0d214-347">For more information, see the [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-348">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0d214-348">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-349">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0d214-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-351">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0d214-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-352">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d214-352">Date and time the object was installed.</span></span> <span data-ttu-id="0d214-353">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="0d214-353">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0d214-354">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-354">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-355">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0d214-355">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-356">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d214-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d214-358">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0d214-358">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0d214-359">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-360">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="0d214-360">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-363">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0d214-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-364">Nom du fabricant de l’appareil Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="0d214-364">Name of the manufacturer of the Plug and Play device.</span></span>

<span data-ttu-id="0d214-365">Exemple : « Acme »</span><span class="sxs-lookup"><span data-stu-id="0d214-365">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="0d214-366">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0d214-366">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-369">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0d214-369">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-370">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0d214-370">Label by which the object is known.</span></span> <span data-ttu-id="0d214-371">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0d214-371">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0d214-372">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-373">**PNPClass**</span><span class="sxs-lookup"><span data-stu-id="0d214-373">**PNPClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-376">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0d214-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

> [!WARNING]
> <span data-ttu-id="0d214-377">En dépit de la liste dans le fichier MOF, cette propriété n’existe pas réellement dans la classe.</span><span class="sxs-lookup"><span data-stu-id="0d214-377">This property, despite being listed in the MOF file, does not actually exist in the class.</span></span> <span data-ttu-id="0d214-378">La propriété est décrite ici uniquement pour des raisons d’exhaustivité et pour clarifier le fichier MOF lui-même.</span><span class="sxs-lookup"><span data-stu-id="0d214-378">The property is described here only for the sake of completeness, and to clarify the MOF file itself.</span></span>

 

<span data-ttu-id="0d214-379">Nom du type de ce Plug-and-Play appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-379">The name of the type of this Plug and Play device.</span></span>

<span data-ttu-id="0d214-380">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas dans le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="0d214-380">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not in the MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="0d214-381">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0d214-381">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-384">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0d214-384">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-385">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0d214-385">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0d214-386">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0d214-387">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="0d214-387">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0d214-388">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0d214-388">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-389">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d214-389">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d214-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d214-391">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0d214-391">Not implemented.</span></span>

<span data-ttu-id="0d214-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d214-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0d214-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-394">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="0d214-394">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0d214-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="0d214-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-396">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="0d214-396">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0d214-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="0d214-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-398">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="0d214-398">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0d214-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="0d214-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-400">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="0d214-400">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0d214-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="0d214-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-402">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="0d214-402">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0d214-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="0d214-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-404">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0d214-404">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="0d214-405">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="0d214-405">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="0d214-406">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-406">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0d214-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="0d214-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-408">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="0d214-408">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0d214-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="0d214-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0d214-410">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="0d214-410">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d214-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0d214-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-412">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d214-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d214-414">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0d214-414">Not implemented.</span></span>

<span data-ttu-id="0d214-415">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-416">**Présent**</span><span class="sxs-lookup"><span data-stu-id="0d214-416">**Present**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-417">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d214-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-419">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0d214-419">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-420">Indique si ce Plug-and-Play périphérique est actuellement dans le système.</span><span class="sxs-lookup"><span data-stu-id="0d214-420">Whether this Plug and Play device is currently in the system.</span></span>

<span data-ttu-id="0d214-421">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0d214-421">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0d214-422">**Service**</span><span class="sxs-lookup"><span data-stu-id="0d214-422">**Service**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-423">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-425">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="0d214-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-426">Nom du service qui prend en charge cet appareil Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="0d214-426">Name of the service that supports this Plug and Play device.</span></span> <span data-ttu-id="0d214-427">Pour plus d’informations, consultez [**Win32 \_ SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-427">For more information, see [**Win32\_SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span></span>

<span data-ttu-id="0d214-428">Exemple : « ATAPI »</span><span class="sxs-lookup"><span data-stu-id="0d214-428">Example: "atapi"</span></span>

</dd> <dt>

<span data-ttu-id="0d214-429">**État**</span><span class="sxs-lookup"><span data-stu-id="0d214-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-432">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0d214-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-433">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d214-433">Current status of the object.</span></span> <span data-ttu-id="0d214-434">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="0d214-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0d214-435">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="0d214-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0d214-436">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0d214-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0d214-437">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0d214-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0d214-438">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0d214-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0d214-439">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0d214-440">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d214-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0d214-441">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0d214-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0d214-442">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0d214-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0d214-443">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0d214-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d214-444">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0d214-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0d214-445">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0d214-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0d214-446">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0d214-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0d214-447">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0d214-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0d214-448">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0d214-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0d214-449">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0d214-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0d214-450">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0d214-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0d214-451">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0d214-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0d214-452">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0d214-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d214-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0d214-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-454">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d214-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-456">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0d214-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0d214-457">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0d214-457">State of the logical device.</span></span> <span data-ttu-id="0d214-458">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="0d214-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0d214-459">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d214-460">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0d214-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d214-461">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0d214-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0d214-462">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="0d214-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0d214-463">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="0d214-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d214-464">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="0d214-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d214-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0d214-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-466">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-467">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-468">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="0d214-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="0d214-469">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0d214-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="0d214-470">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d214-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0d214-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d214-472">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d214-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d214-473">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d214-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d214-474">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="0d214-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="0d214-475">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0d214-475">Name of the scoping system.</span></span>

<span data-ttu-id="0d214-476">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d214-477">Notes</span><span class="sxs-lookup"><span data-stu-id="0d214-477">Remarks</span></span>

<span data-ttu-id="0d214-478">La classe **Win32 \_ PnPEntity** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-478">The **Win32\_PnPEntity** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0d214-479">Exemples</span><span class="sxs-lookup"><span data-stu-id="0d214-479">Examples</span></span>

<span data-ttu-id="0d214-480">L’exemple [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell de la Galerie TechNet utilise pour **Win32 \_ PnPEntity** pour récupérer une liste de matériel non opérationnel à l’aide de WMI.</span><span class="sxs-lookup"><span data-stu-id="0d214-480">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_PnPEntity** to retrieve a list of non-working hardware using WMI.</span></span>

<span data-ttu-id="0d214-481">L’exemple de code VBScript suivant se connecte à un groupe d’ordinateurs distants dans le même domaine en créant un tableau de noms d’ordinateurs distants, puis en affichant les noms des appareils Plug-and-Play (instances de Win32 \_ PnPEntity) sur chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0d214-481">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of Win32\_PnPEntity—on each computer.</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer& "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="0d214-482">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d214-482">Requirements</span></span>



| <span data-ttu-id="0d214-483">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d214-483">Requirement</span></span> | <span data-ttu-id="0d214-484">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d214-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d214-485">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d214-485">Minimum supported client</span></span><br/> | <span data-ttu-id="0d214-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d214-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d214-487">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d214-487">Minimum supported server</span></span><br/> | <span data-ttu-id="0d214-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d214-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d214-489">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0d214-489">Namespace</span></span><br/>                | <span data-ttu-id="0d214-490">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0d214-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d214-491">MOF</span><span class="sxs-lookup"><span data-stu-id="0d214-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d214-492"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d214-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d214-493">DLL</span><span class="sxs-lookup"><span data-stu-id="0d214-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d214-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d214-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d214-495">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d214-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d214-496">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0d214-496">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="0d214-497">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="0d214-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0d214-498">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="0d214-498">Connecting to WMI on a Remote Computer</span></span>](../wmisdk/connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="0d214-499">Tâches WMI : matériel de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="0d214-499">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
