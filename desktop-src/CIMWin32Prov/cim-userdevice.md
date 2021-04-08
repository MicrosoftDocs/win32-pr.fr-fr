---
description: La \_ classe USERDEVICE CIM est une classe parente à partir de laquelle d’autres classes, telles que le \_ clavier CIM ou CIM \_ desktopmonitor, descendent. Les appareils utilisateur sont des périphériques logiques qui permettent à l’utilisateur d’un système informatique d’entrer, d’afficher ou d’entendre des données.
ms.assetid: 311a065a-df9b-4c4b-bdc4-d3de89ce2f3d
ms.tgt_platform: multiple
title: CIM_UserDevice, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.Availability
- CIM_UserDevice.Caption
- CIM_UserDevice.ConfigManagerErrorCode
- CIM_UserDevice.ConfigManagerUserConfig
- CIM_UserDevice.CreationClassName
- CIM_UserDevice.Description
- CIM_UserDevice.DeviceID
- CIM_UserDevice.ErrorCleared
- CIM_UserDevice.ErrorDescription
- CIM_UserDevice.InstallDate
- CIM_UserDevice.IsLocked
- CIM_UserDevice.LastErrorCode
- CIM_UserDevice.Name
- CIM_UserDevice.PNPDeviceID
- CIM_UserDevice.PowerManagementCapabilities
- CIM_UserDevice.PowerManagementSupported
- CIM_UserDevice.Status
- CIM_UserDevice.StatusInfo
- CIM_UserDevice.SystemCreationClassName
- CIM_UserDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b8a91082679c38d7741f9a8d7b43c7f9705333f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110046"
---
# <a name="cim_userdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="cb7b1-104">CIM_UserDevice, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-104">CIM_UserDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cb7b1-105">La **classe \_ UserDevice CIM** est une classe parente à partir de laquelle d’autres classes, telles que le [**\_ clavier CIM**](cim-keyboard.md) ou [**CIM \_ desktopmonitor**](cim-desktopmonitor.md), descendent.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-105">The **CIM\_UserDevice** class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="cb7b1-106">Les appareils utilisateur sont des périphériques logiques qui permettent à l’utilisateur d’un système informatique d’entrer, d’afficher ou d’entendre des données.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-106">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb7b1-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cb7b1-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cb7b1-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cb7b1-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb7b1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb7b1-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C533-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
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
  boolean  IsLocked;
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

## <a name="members"></a><span data-ttu-id="cb7b1-112">Membres</span><span class="sxs-lookup"><span data-stu-id="cb7b1-112">Members</span></span>

<span data-ttu-id="cb7b1-113">La classe **CIM \_ UserDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb7b1-113">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="cb7b1-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb7b1-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb7b1-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb7b1-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb7b1-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb7b1-116">Methods</span></span>

<span data-ttu-id="cb7b1-117">La classe **CIM \_ UserDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-117">The **CIM\_UserDevice** class has these methods.</span></span>



| <span data-ttu-id="cb7b1-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb7b1-118">Method</span></span>                                                                | <span data-ttu-id="cb7b1-119">Description</span><span class="sxs-lookup"><span data-stu-id="cb7b1-119">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb7b1-120">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-120">**Reset**</span></span>](reset-method-in-class-cim-userdevice.md)                 | <span data-ttu-id="cb7b1-121">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="cb7b1-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="cb7b1-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-userdevice.md) | <span data-ttu-id="cb7b1-124">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="cb7b1-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cb7b1-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb7b1-126">Properties</span></span>

<span data-ttu-id="cb7b1-127">La classe **CIM \_ UserDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-127">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb7b1-128">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-131">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-132">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-132">Availability and status of the device.</span></span>

<span data-ttu-id="cb7b1-133">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb7b1-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb7b1-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="cb7b1-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="cb7b1-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="cb7b1-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cb7b1-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="cb7b1-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="cb7b1-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="cb7b1-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cb7b1-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="cb7b1-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="cb7b1-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="cb7b1-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-147">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="cb7b1-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-149">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="cb7b1-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-151">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-151">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="cb7b1-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="cb7b1-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-154">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="cb7b1-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-156">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="cb7b1-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-158">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="cb7b1-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-160">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="cb7b1-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-162">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cb7b1-163">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-163">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-166">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-167">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-167">Short textual description of the object.</span></span>

<span data-ttu-id="cb7b1-168">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-169">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-169">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-172">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-172">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-173">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-173">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="cb7b1-174">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-174">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="cb7b1-175"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-175"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="cb7b1-176"> (0)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-176">(0)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-177">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-177">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="cb7b1-178"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-178"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="cb7b1-179">(1)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-179">(1)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-180">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-180">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cb7b1-181"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-181"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="cb7b1-182">(2)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-182">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="cb7b1-183"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-183"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="cb7b1-184">(3)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-184">(3)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-185">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-185">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cb7b1-186"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-186"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="cb7b1-187">(4)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-187">(4)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-188">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-188">Device is not working properly.</span></span> <span data-ttu-id="cb7b1-189">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-189">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="cb7b1-190"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-190"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="cb7b1-191">(5)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-191">(5)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-192">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-192">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="cb7b1-193"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-193"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="cb7b1-194"> (6)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-194">(6)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-195">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-195">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="cb7b1-196"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-196"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="cb7b1-197">(7)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-197">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="cb7b1-198"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-198"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="cb7b1-199">(8)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-199">(8)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-200">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-200">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="cb7b1-201"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-201"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="cb7b1-202">(9)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-202">(9)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-203">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-203">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="cb7b1-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="cb7b1-205">(10)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-205">(10)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-206">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-206">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="cb7b1-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="cb7b1-208">(11)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-208">(11)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-209">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-209">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="cb7b1-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="cb7b1-211">douze</span><span class="sxs-lookup"><span data-stu-id="cb7b1-211">(12)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-212">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-212">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="cb7b1-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="cb7b1-214">(13)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-214">(13)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-215">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-215">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="cb7b1-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="cb7b1-217">(14)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-217">(14)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-218">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-218">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="cb7b1-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="cb7b1-220">(15)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-220">(15)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-221">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-221">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="cb7b1-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="cb7b1-223">(16)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-223">(16)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-224">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-224">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="cb7b1-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="cb7b1-226">(17)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-226">(17)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-227">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-227">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cb7b1-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="cb7b1-229">(18)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-229">(18)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-230">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-230">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="cb7b1-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="cb7b1-232">(19)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-232">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cb7b1-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="cb7b1-234">(20)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-235">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-235">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="cb7b1-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="cb7b1-237">(21)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-237">(21)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-238">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-238">System failure.</span></span> <span data-ttu-id="cb7b1-239">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-239">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="cb7b1-240">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-240">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="cb7b1-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="cb7b1-242">(22)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-242">(22)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-243">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-243">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="cb7b1-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="cb7b1-245">(23)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-245">(23)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-246">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-246">System failure.</span></span> <span data-ttu-id="cb7b1-247">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-247">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="cb7b1-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="cb7b1-249">(24)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-249">(24)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-250">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-250">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cb7b1-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cb7b1-252">(25)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-252">(25)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-253">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-253">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cb7b1-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cb7b1-255">(26)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-255">(26)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-256">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="cb7b1-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="cb7b1-258">(27)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-258">(27)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-259">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-259">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="cb7b1-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="cb7b1-261">(28)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-261">(28)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-262">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-262">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="cb7b1-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="cb7b1-264">(29)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-264">(29)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-265">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-265">Device is disabled.</span></span> <span data-ttu-id="cb7b1-266">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-266">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="cb7b1-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="cb7b1-268">(30)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-268">(30)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-269">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-269">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cb7b1-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="cb7b1-271">31</span><span class="sxs-lookup"><span data-stu-id="cb7b1-271">(31)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-272">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-272">Device is not working properly.</span></span> <span data-ttu-id="cb7b1-273">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-273">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cb7b1-274">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-274">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-275">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-277">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-278">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-278">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="cb7b1-279">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-279">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-280">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-280">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-283">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-283">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-284">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-284">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cb7b1-285">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-285">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cb7b1-286">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-287">**Description**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-287">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-290">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-290">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-291">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-291">Textual description of the object.</span></span>

<span data-ttu-id="cb7b1-292">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-292">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-293">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-293">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-296">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-297">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-297">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="cb7b1-298">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-299">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-299">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-300">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-302">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-302">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="cb7b1-303">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-304">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-304">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-307">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-307">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="cb7b1-308">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-309">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-309">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-310">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-312">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-313">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-313">Date and time the object was installed.</span></span> <span data-ttu-id="cb7b1-314">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-314">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cb7b1-315">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-315">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-316">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-316">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-317">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-319">Si la **valeur est true**, l’appareil est verrouillé, ce qui empêche l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-319">If **TRUE**, the device is locked, preventing user input or output.</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-320">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-321">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-323">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="cb7b1-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-325">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-325">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-328">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-329">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-329">Label by which the object is known.</span></span> <span data-ttu-id="cb7b1-330">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-330">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cb7b1-331">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-331">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-332">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-332">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-335">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-335">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-336">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-336">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="cb7b1-337">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cb7b1-338">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="cb7b1-338">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-339">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-339">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-340">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-342">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-342">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="cb7b1-343">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-343">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb7b1-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="cb7b1-345"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-345"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cb7b1-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cb7b1-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-348">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-348">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="cb7b1-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-350">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-350">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="cb7b1-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-352">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-352">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="cb7b1-353">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-353">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="cb7b1-354">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-354">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="cb7b1-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-356">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="cb7b1-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cb7b1-358">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cb7b1-359">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-359">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-360">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-362">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-362">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="cb7b1-363">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cb7b1-363">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="cb7b1-364">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-364">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="cb7b1-365">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cb7b1-365">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="cb7b1-366">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-367">**État**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-367">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-368">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-370">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-370">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-371">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-371">Current status of the object.</span></span> <span data-ttu-id="cb7b1-372">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cb7b1-373">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb7b1-373">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cb7b1-374">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-374">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cb7b1-375">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-375">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cb7b1-376">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-376">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb7b1-377">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-377">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cb7b1-378">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-378">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cb7b1-379">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-379">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cb7b1-380">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-380">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cb7b1-381">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-381">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cb7b1-382">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-382">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cb7b1-383">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-383">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cb7b1-384">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-384">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cb7b1-385">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-385">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cb7b1-386">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-386">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-387">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-389">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="cb7b1-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-390">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-390">State of the logical device.</span></span> <span data-ttu-id="cb7b1-391">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-391">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="cb7b1-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb7b1-393">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb7b1-394">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cb7b1-395">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-395">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cb7b1-396">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-396">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cb7b1-397">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-397">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cb7b1-398">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-398">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-399">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-401">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-401">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-402">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-402">Scoping system's creation class name.</span></span>

<span data-ttu-id="cb7b1-403">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb7b1-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb7b1-405">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb7b1-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb7b1-407">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cb7b1-407">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cb7b1-408">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-408">Scoping system's name.</span></span>

<span data-ttu-id="cb7b1-409">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb7b1-410">Notes</span><span class="sxs-lookup"><span data-stu-id="cb7b1-410">Remarks</span></span>

<span data-ttu-id="cb7b1-411">La classe **CIM \_ UserDevice** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-411">The **CIM\_UserDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cb7b1-412">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-412">WMI does not implement this class.</span></span> <span data-ttu-id="cb7b1-413">Pour les classes WMI dérivées de **CIM \_ UserDevice**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b1-413">For WMI classes derived from **CIM\_UserDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cb7b1-414">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-414">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cb7b1-415">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cb7b1-415">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb7b1-416">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb7b1-416">Requirements</span></span>



| <span data-ttu-id="cb7b1-417">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb7b1-417">Requirement</span></span> | <span data-ttu-id="cb7b1-418">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb7b1-418">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7b1-419">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb7b1-419">Minimum supported client</span></span><br/> | <span data-ttu-id="cb7b1-420">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb7b1-420">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb7b1-421">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb7b1-421">Minimum supported server</span></span><br/> | <span data-ttu-id="cb7b1-422">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb7b1-422">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb7b1-423">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb7b1-423">Namespace</span></span><br/>                | <span data-ttu-id="cb7b1-424">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="cb7b1-424">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb7b1-425">MOF</span><span class="sxs-lookup"><span data-stu-id="cb7b1-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb7b1-426"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb7b1-426"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb7b1-427">DLL</span><span class="sxs-lookup"><span data-stu-id="cb7b1-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb7b1-428"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb7b1-428"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb7b1-429">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb7b1-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb7b1-430">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="cb7b1-430">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

