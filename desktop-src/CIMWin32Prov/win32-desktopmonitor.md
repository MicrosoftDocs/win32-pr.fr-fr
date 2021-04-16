---
description: Représente le type de moniteur ou d’écran d’affichage attaché au système de l’ordinateur.
ms.assetid: 922be3c1-3c7b-4418-a72f-ab5ada91a7a4
ms.tgt_platform: multiple
title: Classe Win32_DesktopMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DesktopMonitor
- Win32_DesktopMonitor.Reset
- Win32_DesktopMonitor.SetPowerState
- Win32_DesktopMonitor.Availability
- Win32_DesktopMonitor.Bandwidth
- Win32_DesktopMonitor.Caption
- Win32_DesktopMonitor.ConfigManagerErrorCode
- Win32_DesktopMonitor.ConfigManagerUserConfig
- Win32_DesktopMonitor.CreationClassName
- Win32_DesktopMonitor.Description
- Win32_DesktopMonitor.DeviceID
- Win32_DesktopMonitor.DisplayType
- Win32_DesktopMonitor.ErrorCleared
- Win32_DesktopMonitor.ErrorDescription
- Win32_DesktopMonitor.InstallDate
- Win32_DesktopMonitor.IsLocked
- Win32_DesktopMonitor.LastErrorCode
- Win32_DesktopMonitor.MonitorManufacturer
- Win32_DesktopMonitor.MonitorType
- Win32_DesktopMonitor.Name
- Win32_DesktopMonitor.PixelsPerXLogicalInch
- Win32_DesktopMonitor.PixelsPerYLogicalInch
- Win32_DesktopMonitor.PNPDeviceID
- Win32_DesktopMonitor.PowerManagementCapabilities
- Win32_DesktopMonitor.PowerManagementSupported
- Win32_DesktopMonitor.ScreenHeight
- Win32_DesktopMonitor.ScreenWidth
- Win32_DesktopMonitor.Status
- Win32_DesktopMonitor.StatusInfo
- Win32_DesktopMonitor.SystemCreationClassName
- Win32_DesktopMonitor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccf986957d73dd93837b0ab7a1e10b50aec5e8f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524292"
---
# <a name="win32_desktopmonitor-class"></a><span data-ttu-id="80038-103">\_Classe desktopmonitor Win32</span><span class="sxs-lookup"><span data-stu-id="80038-103">Win32\_DesktopMonitor class</span></span>

<span data-ttu-id="80038-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ desktopmonitor** WMI représente le type de moniteur ou d’écran d’affichage attaché au système informatique.</span><span class="sxs-lookup"><span data-stu-id="80038-104">The **Win32\_DesktopMonitor** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the type of monitor or display device attached to the computer system.</span></span>

<span data-ttu-id="80038-105">Le matériel qui n’est pas compatible avec le modèle WDDM (Windows Display Driver Model) retourne des valeurs de propriété inexactes pour les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="80038-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="80038-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="80038-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="80038-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="80038-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="80038-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80038-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF0-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_DesktopMonitor : CIM_DesktopMonitor
{
  uint16   Availability;
  uint32   Bandwidth;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="80038-109">Membres</span><span class="sxs-lookup"><span data-stu-id="80038-109">Members</span></span>

<span data-ttu-id="80038-110">La classe **Win32 \_ desktopmonitor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80038-110">The **Win32\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="80038-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="80038-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="80038-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80038-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="80038-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="80038-113">Methods</span></span>

<span data-ttu-id="80038-114">La classe **Win32 \_ desktopmonitor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="80038-114">The **Win32\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="80038-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="80038-115">Method</span></span>            | <span data-ttu-id="80038-116">Description</span><span class="sxs-lookup"><span data-stu-id="80038-116">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80038-117">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="80038-117">**Reset**</span></span>         | <span data-ttu-id="80038-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="80038-118">Not implemented.</span></span> <span data-ttu-id="80038-119">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ desktopmonitor**](cim-desktopmonitor.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="80038-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="80038-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="80038-120">**SetPowerState**</span></span> | <span data-ttu-id="80038-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="80038-121">Not implemented.</span></span> <span data-ttu-id="80038-122">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ desktopmonitor**](cim-desktopmonitor.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="80038-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="80038-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80038-123">Properties</span></span>

<span data-ttu-id="80038-124">La classe **Win32 \_ desktopmonitor** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="80038-124">The **Win32\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80038-125">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="80038-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80038-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80038-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="80038-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="80038-129">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-129">Availability and status of the device.</span></span>

<span data-ttu-id="80038-130">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="80038-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="80038-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="80038-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="80038-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="80038-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="80038-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="80038-134">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="80038-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="80038-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="80038-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="80038-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="80038-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="80038-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="80038-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="80038-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="80038-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="80038-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="80038-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="80038-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="80038-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="80038-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="80038-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="80038-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="80038-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="80038-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="80038-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="80038-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="80038-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="80038-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="80038-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="80038-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="80038-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="80038-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="80038-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="80038-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="80038-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="80038-149">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="80038-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="80038-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="80038-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="80038-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="80038-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="80038-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="80038-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="80038-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="80038-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="80038-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="80038-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="80038-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="80038-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="80038-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="80038-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="80038-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="80038-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="80038-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="80038-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="80038-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="80038-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="80038-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="80038-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80038-161">**Bande passante**</span><span class="sxs-lookup"><span data-stu-id="80038-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80038-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80038-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-164">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« mégahertz »)</span><span class="sxs-lookup"><span data-stu-id="80038-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="80038-165">Bande passante du moniteur en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="80038-165">Monitor's bandwidth in megahertz.</span></span> <span data-ttu-id="80038-166">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="80038-166">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="80038-167">Cette propriété est héritée de la [**\_ desktopmonitor CIM**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="80038-167">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="80038-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-171">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="80038-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="80038-172">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80038-172">Short description of the object.</span></span>

<span data-ttu-id="80038-173">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80038-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="80038-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-175">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80038-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80038-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-177">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="80038-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="80038-178">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="80038-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="80038-179">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="80038-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="80038-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="80038-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="80038-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="80038-182">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="80038-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="80038-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="80038-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="80038-184">(1)</span><span class="sxs-lookup"><span data-stu-id="80038-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="80038-185">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="80038-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="80038-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="80038-187">(2)</span><span class="sxs-lookup"><span data-stu-id="80038-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="80038-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="80038-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="80038-189">(3)</span><span class="sxs-lookup"><span data-stu-id="80038-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="80038-190">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="80038-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="80038-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="80038-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="80038-192">(4)</span><span class="sxs-lookup"><span data-stu-id="80038-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="80038-193">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="80038-193">Device is not working properly.</span></span> <span data-ttu-id="80038-194">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="80038-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="80038-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="80038-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="80038-196">(5)</span><span class="sxs-lookup"><span data-stu-id="80038-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="80038-197">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="80038-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="80038-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="80038-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="80038-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="80038-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="80038-200">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="80038-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="80038-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="80038-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="80038-202">(7)</span><span class="sxs-lookup"><span data-stu-id="80038-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="80038-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="80038-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="80038-204">(8)</span><span class="sxs-lookup"><span data-stu-id="80038-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="80038-205">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="80038-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="80038-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="80038-207">(9)</span><span class="sxs-lookup"><span data-stu-id="80038-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="80038-208">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="80038-208">Device is not working properly.</span></span> <span data-ttu-id="80038-209">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="80038-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="80038-211">(10)</span><span class="sxs-lookup"><span data-stu-id="80038-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="80038-212">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="80038-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="80038-214">(11)</span><span class="sxs-lookup"><span data-stu-id="80038-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="80038-215">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="80038-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="80038-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="80038-217">douze</span><span class="sxs-lookup"><span data-stu-id="80038-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="80038-218">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="80038-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="80038-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="80038-220">(13)</span><span class="sxs-lookup"><span data-stu-id="80038-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="80038-221">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="80038-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="80038-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="80038-223">(14)</span><span class="sxs-lookup"><span data-stu-id="80038-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="80038-224">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="80038-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="80038-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="80038-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="80038-226">(15)</span><span class="sxs-lookup"><span data-stu-id="80038-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="80038-227">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="80038-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="80038-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="80038-229">(16)</span><span class="sxs-lookup"><span data-stu-id="80038-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="80038-230">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="80038-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="80038-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="80038-232">(17)</span><span class="sxs-lookup"><span data-stu-id="80038-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="80038-233">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="80038-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="80038-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="80038-235">(18)</span><span class="sxs-lookup"><span data-stu-id="80038-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="80038-236">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="80038-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="80038-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="80038-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="80038-238">(19)</span><span class="sxs-lookup"><span data-stu-id="80038-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="80038-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="80038-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="80038-240">(20)</span><span class="sxs-lookup"><span data-stu-id="80038-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="80038-241">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="80038-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="80038-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="80038-243">(21)</span><span class="sxs-lookup"><span data-stu-id="80038-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="80038-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="80038-244">System failure.</span></span> <span data-ttu-id="80038-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="80038-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="80038-246">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="80038-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="80038-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="80038-248">(22)</span><span class="sxs-lookup"><span data-stu-id="80038-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="80038-249">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="80038-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="80038-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="80038-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="80038-251">(23)</span><span class="sxs-lookup"><span data-stu-id="80038-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="80038-252">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="80038-252">System failure.</span></span> <span data-ttu-id="80038-253">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="80038-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="80038-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="80038-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="80038-255">(24)</span><span class="sxs-lookup"><span data-stu-id="80038-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="80038-256">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="80038-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="80038-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="80038-258">(25)</span><span class="sxs-lookup"><span data-stu-id="80038-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="80038-259">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="80038-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="80038-261">(26)</span><span class="sxs-lookup"><span data-stu-id="80038-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="80038-262">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="80038-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="80038-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="80038-264">(27)</span><span class="sxs-lookup"><span data-stu-id="80038-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="80038-265">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="80038-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="80038-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="80038-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="80038-267">(28)</span><span class="sxs-lookup"><span data-stu-id="80038-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="80038-268">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="80038-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="80038-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="80038-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="80038-270">(29)</span><span class="sxs-lookup"><span data-stu-id="80038-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="80038-271">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="80038-271">Device is disabled.</span></span> <span data-ttu-id="80038-272">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="80038-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="80038-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="80038-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="80038-274">(30)</span><span class="sxs-lookup"><span data-stu-id="80038-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="80038-275">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="80038-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="80038-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="80038-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="80038-277">31</span><span class="sxs-lookup"><span data-stu-id="80038-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="80038-278">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="80038-278">Device is not working properly.</span></span> <span data-ttu-id="80038-279">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="80038-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80038-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="80038-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-281">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80038-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80038-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-283">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="80038-283">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="80038-284">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="80038-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="80038-285">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="80038-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-287">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-289">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="80038-289">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="80038-290">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="80038-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="80038-291">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="80038-291">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="80038-292">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-293">**Description**</span><span class="sxs-lookup"><span data-stu-id="80038-293">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-296">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="80038-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="80038-297">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80038-297">Description of the object.</span></span>

<span data-ttu-id="80038-298">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80038-298">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-299">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="80038-299">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-302">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Windows GDI \| HMONITOR")</span><span class="sxs-lookup"><span data-stu-id="80038-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows GDI\|HMONITOR")</span></span>
</dt> </dl>

<span data-ttu-id="80038-303">Identificateur unique d’un moniteur d’ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="80038-303">Unique identifier of a desktop monitor.</span></span>

<span data-ttu-id="80038-304">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-305">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="80038-305">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-306">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80038-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80038-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-308">Type de moniteur de bureau ou CRT.</span><span class="sxs-lookup"><span data-stu-id="80038-308">Type of desktop monitor or CRT.</span></span>

<span data-ttu-id="80038-309">Cette propriété est héritée de la [**\_ desktopmonitor CIM**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="80038-309">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="80038-310">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="80038-310">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="80038-311">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="80038-311">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="80038-312">**Couleur multibalayage** (2)</span><span class="sxs-lookup"><span data-stu-id="80038-312">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="80038-313">**Multiscann monochrome** (3)</span><span class="sxs-lookup"><span data-stu-id="80038-313">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="80038-314">**Couleur de fréquence fixe** (4)</span><span class="sxs-lookup"><span data-stu-id="80038-314">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="80038-315">**Fréquence fixe monochrome** (5)</span><span class="sxs-lookup"><span data-stu-id="80038-315">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="80038-316">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="80038-316">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-317">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80038-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80038-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-319">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="80038-319">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="80038-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-321">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="80038-321">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-324">Chaîne de forme libre fournissant plus d’informations sur l’erreur enregistrée dans **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="80038-324">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="80038-325">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-326">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="80038-326">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-327">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80038-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80038-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-329">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="80038-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="80038-330">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80038-330">Date and time the object was installed.</span></span> <span data-ttu-id="80038-331">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="80038-331">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="80038-332">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80038-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-333">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="80038-333">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-334">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80038-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80038-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-336">Si la **valeur est true**, l’appareil est verrouillé, ce qui empêche l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="80038-336">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="80038-337">Cette propriété est héritée de la [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-337">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-338">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="80038-338">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-339">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80038-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80038-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-341">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="80038-341">Last error code reported by the logical device.</span></span>

<span data-ttu-id="80038-342">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-343">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="80038-343">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-344">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-346">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="80038-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="80038-347">Nom du fabricant du moniteur.</span><span class="sxs-lookup"><span data-stu-id="80038-347">Name of the monitor manufacturer.</span></span>

<span data-ttu-id="80038-348">Exemple : « NEC »</span><span class="sxs-lookup"><span data-stu-id="80038-348">Example: "NEC"</span></span>

</dd> <dt>

<span data-ttu-id="80038-349">**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="80038-349">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-352">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="80038-352">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="80038-353">Type d’analyse.</span><span class="sxs-lookup"><span data-stu-id="80038-353">Type of monitor.</span></span>

<span data-ttu-id="80038-354">Exemple : « NEC 5FGp »</span><span class="sxs-lookup"><span data-stu-id="80038-354">Example: "NEC 5FGp"</span></span>

</dd> <dt>

<span data-ttu-id="80038-355">**Nom**</span><span class="sxs-lookup"><span data-stu-id="80038-355">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-356">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-358">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="80038-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="80038-359">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="80038-359">Label by which the object is known.</span></span> <span data-ttu-id="80038-360">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="80038-360">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="80038-361">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80038-361">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-362">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="80038-362">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-363">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80038-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80038-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-365">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| des fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels par pouce logique")</span><span class="sxs-lookup"><span data-stu-id="80038-365">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="80038-366">Résolution le long de l’axe x (sens horizontal) de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="80038-366">Resolution along the x-axis (horizontal direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="80038-367">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="80038-367">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-368">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80038-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80038-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-370">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| des fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels par pouce logique")</span><span class="sxs-lookup"><span data-stu-id="80038-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="80038-371">Résolution le long de l’axe y (direction verticale) de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="80038-371">Resolution along the y-axis (vertical direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="80038-372">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="80038-372">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-373">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-375">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="80038-375">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="80038-376">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="80038-376">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="80038-377">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="80038-378">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="80038-378">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="80038-379">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="80038-379">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-380">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80038-380">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="80038-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-382">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="80038-382">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="80038-383">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-383">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="80038-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="80038-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="80038-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="80038-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="80038-386">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="80038-386">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="80038-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="80038-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="80038-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="80038-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="80038-389">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="80038-389">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="80038-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="80038-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="80038-391">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="80038-391">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="80038-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="80038-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="80038-393">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="80038-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="80038-394">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="80038-394">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="80038-395">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="80038-395">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="80038-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="80038-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="80038-397">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="80038-397">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="80038-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="80038-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="80038-399">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="80038-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80038-400">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="80038-400">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-401">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80038-401">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80038-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-403">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="80038-403">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="80038-404">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="80038-404">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="80038-405">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-406">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="80038-406">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-407">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80038-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80038-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-409">Hauteur logique de l’affichage en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="80038-409">Logical height of the display in screen coordinates.</span></span>

<span data-ttu-id="80038-410">Cette propriété est héritée de la [**\_ desktopmonitor CIM**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="80038-410">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-411">**Largeur**</span><span class="sxs-lookup"><span data-stu-id="80038-411">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-412">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80038-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80038-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80038-414">Largeur logique de l’affichage en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="80038-414">Logical width of the display in screen coordinates.</span></span>

<span data-ttu-id="80038-415">Cette propriété est héritée de la [**\_ desktopmonitor CIM**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="80038-415">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-416">**État**</span><span class="sxs-lookup"><span data-stu-id="80038-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-417">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-419">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="80038-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="80038-420">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80038-420">Current status of the object.</span></span> <span data-ttu-id="80038-421">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="80038-421">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="80038-422">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="80038-422">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="80038-423">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="80038-423">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="80038-424">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="80038-424">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="80038-425">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="80038-425">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="80038-426">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80038-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="80038-427">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="80038-427">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="80038-428">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="80038-428">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="80038-429">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="80038-429">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="80038-430">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="80038-430">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="80038-431">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="80038-431">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="80038-432">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="80038-432">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="80038-433">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="80038-433">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="80038-434">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="80038-434">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="80038-435">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="80038-435">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="80038-436">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="80038-436">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="80038-437">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="80038-437">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="80038-438">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="80038-438">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="80038-439">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="80038-439">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="80038-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="80038-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-441">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80038-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80038-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-443">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="80038-443">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="80038-444">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="80038-444">State of the logical device.</span></span> <span data-ttu-id="80038-445">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="80038-445">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="80038-446">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="80038-447">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="80038-447">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="80038-448">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="80038-448">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="80038-449">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="80038-449">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="80038-450">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="80038-450">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="80038-451">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="80038-451">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="80038-452">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="80038-452">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-453">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-454">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-455">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="80038-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="80038-456">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="80038-456">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="80038-457">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="80038-458">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="80038-458">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80038-459">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80038-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80038-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80038-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80038-461">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="80038-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="80038-462">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="80038-462">Name of the scoping system.</span></span>

<span data-ttu-id="80038-463">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80038-464">Notes</span><span class="sxs-lookup"><span data-stu-id="80038-464">Remarks</span></span>

<span data-ttu-id="80038-465">La classe **Win32 \_ desktopmonitor** est dérivée de [**CIM \_ desktopmonitor**](cim-desktopmonitor.md), qui dérive de l' [**\_ affichage CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="80038-465">The **Win32\_DesktopMonitor** class is derived from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), which derives from [**CIM\_Display**](cim-display.md).</span></span> <span data-ttu-id="80038-466">**CIM \_ L’affichage** est dérivé de [**CIM \_ UserDevice**](cim-userdevice.md), qui dérive de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="80038-466">**CIM\_Display** is derived from [**CIM\_UserDevice**](cim-userdevice.md), which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="80038-467">Exemples</span><span class="sxs-lookup"><span data-stu-id="80038-467">Examples</span></span>

<span data-ttu-id="80038-468">L’exemple [PS créer un dessin de configuration d’ordinateur à l’aide de Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sur la Galerie TechNet utilise **Win32 \_ desktopmonitor** pour interagir avec le modèle Automation Visio afin de créer un dessin Visio.</span><span class="sxs-lookup"><span data-stu-id="80038-468">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_DesktopMonitor** to interact with the Visio automation model to create a Visio drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="80038-469">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80038-469">Requirements</span></span>



| <span data-ttu-id="80038-470">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80038-470">Requirement</span></span> | <span data-ttu-id="80038-471">Valeur</span><span class="sxs-lookup"><span data-stu-id="80038-471">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80038-472">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80038-472">Minimum supported client</span></span><br/> | <span data-ttu-id="80038-473">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80038-473">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80038-474">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80038-474">Minimum supported server</span></span><br/> | <span data-ttu-id="80038-475">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80038-475">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80038-476">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80038-476">Namespace</span></span><br/>                | <span data-ttu-id="80038-477">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="80038-477">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="80038-478">MOF</span><span class="sxs-lookup"><span data-stu-id="80038-478">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80038-479"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80038-479"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="80038-480">DLL</span><span class="sxs-lookup"><span data-stu-id="80038-480">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80038-481"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80038-481"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80038-482">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80038-482">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80038-483">**\_DESKTOPMONITOR CIM**</span><span class="sxs-lookup"><span data-stu-id="80038-483">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="80038-484">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="80038-484">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="80038-485">Tâches WMI : gestion des postes de travail</span><span class="sxs-lookup"><span data-stu-id="80038-485">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

