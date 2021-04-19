---
description: La \_ classe WMI SCSIController WMI représente un contrôleur SCSI sur un système informatique exécutant Windows.
ms.assetid: 14ed523e-d505-40fa-81d5-3a71eb9f078e
ms.tgt_platform: multiple
title: Classe Win32_SCSIController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIController
- Win32_SCSIController.Reset
- Win32_SCSIController.SetPowerState
- Win32_SCSIController.Availability
- Win32_SCSIController.Caption
- Win32_SCSIController.ConfigManagerErrorCode
- Win32_SCSIController.ConfigManagerUserConfig
- Win32_SCSIController.ControllerTimeouts
- Win32_SCSIController.CreationClassName
- Win32_SCSIController.Description
- Win32_SCSIController.DeviceID
- Win32_SCSIController.DeviceMap
- Win32_SCSIController.DriverName
- Win32_SCSIController.ErrorCleared
- Win32_SCSIController.ErrorDescription
- Win32_SCSIController.HardwareVersion
- Win32_SCSIController.Index
- Win32_SCSIController.InstallDate
- Win32_SCSIController.LastErrorCode
- Win32_SCSIController.Manufacturer
- Win32_SCSIController.MaxDataWidth
- Win32_SCSIController.MaxNumberControlled
- Win32_SCSIController.MaxTransferRate
- Win32_SCSIController.Name
- Win32_SCSIController.PNPDeviceID
- Win32_SCSIController.PowerManagementCapabilities
- Win32_SCSIController.PowerManagementSupported
- Win32_SCSIController.ProtectionManagement
- Win32_SCSIController.ProtocolSupported
- Win32_SCSIController.Status
- Win32_SCSIController.StatusInfo
- Win32_SCSIController.SystemCreationClassName
- Win32_SCSIController.SystemName
- Win32_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f8ba77d626ada787ed18fd9855333fa813f3ab7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512905"
---
# <a name="win32_scsicontroller-class"></a><span data-ttu-id="073d2-103">\_Classe SCSIController Win32</span><span class="sxs-lookup"><span data-stu-id="073d2-103">Win32\_SCSIController class</span></span>

<span data-ttu-id="073d2-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SCSIController** WMI représente un contrôleur SCSI sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="073d2-104">The **Win32\_SCSIController** [WMI class](../wmisdk/retrieving-a-class.md) represents a SCSI controller on a computer system running Windows.</span></span>

<span data-ttu-id="073d2-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="073d2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="073d2-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="073d2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="073d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="073d2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SCSIController : CIM_SCSIController
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  string   DeviceMap;
  string   DriverName;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareVersion;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="073d2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="073d2-108">Members</span></span>

<span data-ttu-id="073d2-109">La classe **Win32 \_ SCSIController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="073d2-109">The **Win32\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="073d2-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="073d2-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="073d2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="073d2-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="073d2-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="073d2-112">Methods</span></span>

<span data-ttu-id="073d2-113">La classe **Win32 \_ SCSIController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="073d2-113">The **Win32\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="073d2-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="073d2-114">Method</span></span>            | <span data-ttu-id="073d2-115">Description</span><span class="sxs-lookup"><span data-stu-id="073d2-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="073d2-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="073d2-116">**Reset**</span></span>         | <span data-ttu-id="073d2-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="073d2-117">Not implemented.</span></span> <span data-ttu-id="073d2-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/>                 |
| <span data-ttu-id="073d2-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="073d2-119">**SetPowerState**</span></span> | <span data-ttu-id="073d2-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="073d2-120">Not implemented.</span></span> <span data-ttu-id="073d2-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="073d2-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="073d2-122">Properties</span></span>

<span data-ttu-id="073d2-123">La classe **Win32 \_ SCSIController** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="073d2-123">The **Win32\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="073d2-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="073d2-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="073d2-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-127">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="073d2-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-128">Availability and status of the device.</span></span>

<span data-ttu-id="073d2-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="073d2-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="073d2-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="073d2-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="073d2-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="073d2-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="073d2-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="073d2-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="073d2-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="073d2-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="073d2-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="073d2-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="073d2-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="073d2-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="073d2-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="073d2-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="073d2-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="073d2-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="073d2-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="073d2-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="073d2-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="073d2-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="073d2-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="073d2-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="073d2-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="073d2-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="073d2-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="073d2-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="073d2-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="073d2-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="073d2-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="073d2-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="073d2-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="073d2-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="073d2-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="073d2-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="073d2-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="073d2-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="073d2-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="073d2-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="073d2-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="073d2-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-153">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="073d2-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="073d2-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="073d2-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-155">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="073d2-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="073d2-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="073d2-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-157">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="073d2-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="073d2-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="073d2-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-159">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="073d2-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="073d2-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="073d2-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-163">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="073d2-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-164">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="073d2-164">Short description of the object.</span></span>

<span data-ttu-id="073d2-165">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="073d2-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="073d2-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-169">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="073d2-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-170">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="073d2-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="073d2-171">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="073d2-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="073d2-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="073d2-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="073d2-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-174">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="073d2-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="073d2-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="073d2-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="073d2-176">(1)</span><span class="sxs-lookup"><span data-stu-id="073d2-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-177">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="073d2-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="073d2-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="073d2-179">(2)</span><span class="sxs-lookup"><span data-stu-id="073d2-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="073d2-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="073d2-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="073d2-181">(3)</span><span class="sxs-lookup"><span data-stu-id="073d2-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-182">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="073d2-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="073d2-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="073d2-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="073d2-184">(4)</span><span class="sxs-lookup"><span data-stu-id="073d2-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-185">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="073d2-185">Device is not working properly.</span></span> <span data-ttu-id="073d2-186">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="073d2-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="073d2-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="073d2-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="073d2-188">(5)</span><span class="sxs-lookup"><span data-stu-id="073d2-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-189">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="073d2-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="073d2-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="073d2-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="073d2-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="073d2-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-192">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="073d2-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="073d2-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="073d2-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="073d2-194">(7)</span><span class="sxs-lookup"><span data-stu-id="073d2-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="073d2-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="073d2-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="073d2-196">(8)</span><span class="sxs-lookup"><span data-stu-id="073d2-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-197">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="073d2-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="073d2-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="073d2-199">(9)</span><span class="sxs-lookup"><span data-stu-id="073d2-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-200">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="073d2-200">Device is not working properly.</span></span> <span data-ttu-id="073d2-201">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="073d2-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="073d2-203">(10)</span><span class="sxs-lookup"><span data-stu-id="073d2-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-204">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="073d2-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="073d2-206">(11)</span><span class="sxs-lookup"><span data-stu-id="073d2-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-207">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="073d2-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="073d2-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="073d2-209">douze</span><span class="sxs-lookup"><span data-stu-id="073d2-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-210">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="073d2-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="073d2-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="073d2-212">(13)</span><span class="sxs-lookup"><span data-stu-id="073d2-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-213">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="073d2-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="073d2-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="073d2-215">(14)</span><span class="sxs-lookup"><span data-stu-id="073d2-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-216">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="073d2-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="073d2-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="073d2-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="073d2-218">(15)</span><span class="sxs-lookup"><span data-stu-id="073d2-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-219">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="073d2-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="073d2-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="073d2-221">(16)</span><span class="sxs-lookup"><span data-stu-id="073d2-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-222">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="073d2-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="073d2-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="073d2-224">(17)</span><span class="sxs-lookup"><span data-stu-id="073d2-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-225">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="073d2-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="073d2-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="073d2-227">(18)</span><span class="sxs-lookup"><span data-stu-id="073d2-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-228">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="073d2-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="073d2-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="073d2-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="073d2-230">(19)</span><span class="sxs-lookup"><span data-stu-id="073d2-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="073d2-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="073d2-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="073d2-232">(20)</span><span class="sxs-lookup"><span data-stu-id="073d2-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-233">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="073d2-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="073d2-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="073d2-235">(21)</span><span class="sxs-lookup"><span data-stu-id="073d2-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-236">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="073d2-236">System failure.</span></span> <span data-ttu-id="073d2-237">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="073d2-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="073d2-238">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="073d2-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="073d2-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="073d2-240">(22)</span><span class="sxs-lookup"><span data-stu-id="073d2-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-241">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="073d2-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="073d2-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="073d2-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="073d2-243">(23)</span><span class="sxs-lookup"><span data-stu-id="073d2-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="073d2-244">System failure.</span></span> <span data-ttu-id="073d2-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="073d2-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="073d2-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="073d2-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="073d2-247">(24)</span><span class="sxs-lookup"><span data-stu-id="073d2-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-248">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="073d2-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="073d2-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="073d2-250">(25)</span><span class="sxs-lookup"><span data-stu-id="073d2-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-251">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="073d2-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="073d2-253">(26)</span><span class="sxs-lookup"><span data-stu-id="073d2-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-254">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="073d2-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="073d2-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="073d2-256">(27)</span><span class="sxs-lookup"><span data-stu-id="073d2-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-257">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="073d2-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="073d2-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="073d2-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="073d2-259">(28)</span><span class="sxs-lookup"><span data-stu-id="073d2-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-260">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="073d2-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="073d2-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="073d2-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="073d2-262">(29)</span><span class="sxs-lookup"><span data-stu-id="073d2-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-263">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="073d2-263">Device is disabled.</span></span> <span data-ttu-id="073d2-264">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="073d2-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="073d2-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="073d2-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="073d2-266">(30)</span><span class="sxs-lookup"><span data-stu-id="073d2-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-267">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="073d2-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="073d2-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="073d2-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="073d2-269">31</span><span class="sxs-lookup"><span data-stu-id="073d2-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-270">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="073d2-270">Device is not working properly.</span></span> <span data-ttu-id="073d2-271">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="073d2-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="073d2-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="073d2-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-273">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="073d2-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-275">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="073d2-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-276">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="073d2-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="073d2-277">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-278">**ControllerTimeouts**</span><span class="sxs-lookup"><span data-stu-id="073d2-278">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-279">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="073d2-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="073d2-281">Nombre d’expirations de délai qui se sont produites après la valeur **TimeOfLastReset** .</span><span class="sxs-lookup"><span data-stu-id="073d2-281">Number of time-outs that have occurred after the **TimeOfLastReset** value.</span></span>

<span data-ttu-id="073d2-282">Cette propriété est héritée de la [**\_ SCSIController CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-282">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="073d2-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-284">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-286">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="073d2-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="073d2-287">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="073d2-287">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="073d2-288">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="073d2-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="073d2-289">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-290">**Description**</span><span class="sxs-lookup"><span data-stu-id="073d2-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-291">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-293">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="073d2-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-294">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="073d2-294">Description of the object.</span></span>

<span data-ttu-id="073d2-295">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="073d2-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-299">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SCSI")</span><span class="sxs-lookup"><span data-stu-id="073d2-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-300">Identificateur unique du contrôleur SCSI avec d’autres périphériques sur le système.</span><span class="sxs-lookup"><span data-stu-id="073d2-300">Unique identifier of the SCSI controller with other devices on the system.</span></span>

<span data-ttu-id="073d2-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-302">**DeviceMap**</span><span class="sxs-lookup"><span data-stu-id="073d2-302">**DeviceMap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-305">Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| matériel \\ \\ DeviceMap \\ \\ SCSI \| ScsiPort »)</span><span class="sxs-lookup"><span data-stu-id="073d2-305">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-306">Ordre dans lequel les appareils sont répertoriés avec ce contrôleur SCSI.</span><span class="sxs-lookup"><span data-stu-id="073d2-306">Order in which the devices are listed with this SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="073d2-307">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="073d2-307">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-310">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \| PortDriver")</span><span class="sxs-lookup"><span data-stu-id="073d2-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|PortDriver")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-311">Nom du fichier de pilote du contrôleur SCSI.</span><span class="sxs-lookup"><span data-stu-id="073d2-311">Driver file name of the SCSI controller.</span></span>

<span data-ttu-id="073d2-312">Exemple : « Adaptec »</span><span class="sxs-lookup"><span data-stu-id="073d2-312">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="073d2-313">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="073d2-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-314">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="073d2-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="073d2-316">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="073d2-316">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="073d2-317">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="073d2-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="073d2-321">Chaîne de forme libre fournissant plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="073d2-321">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="073d2-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-323">**HardwareVersion**</span><span class="sxs-lookup"><span data-stu-id="073d2-323">**HardwareVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-326">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ enum \\ \\ root \| HWRevision")</span><span class="sxs-lookup"><span data-stu-id="073d2-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|HWRevision")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-327">Numéro de version matérielle du contrôleur SCSI.</span><span class="sxs-lookup"><span data-stu-id="073d2-327">Hardware version number of the SCSI controller.</span></span>

<span data-ttu-id="073d2-328">Exemple : « 1,25 »</span><span class="sxs-lookup"><span data-stu-id="073d2-328">Example: "1.25"</span></span>

</dd> <dt>

<span data-ttu-id="073d2-329">**Index**</span><span class="sxs-lookup"><span data-stu-id="073d2-329">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-330">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="073d2-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-332">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SCSI \| ScsiPort »)</span><span class="sxs-lookup"><span data-stu-id="073d2-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-333">Numéro d’index du contrôleur SCSI dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="073d2-333">Index number of the SCSI controller in the system registry.</span></span>

<span data-ttu-id="073d2-334">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="073d2-334">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="073d2-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="073d2-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-336">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="073d2-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-338">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="073d2-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-339">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="073d2-339">Date and time the object was installed.</span></span> <span data-ttu-id="073d2-340">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="073d2-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="073d2-341">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="073d2-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-343">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="073d2-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="073d2-345">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="073d2-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="073d2-346">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-347">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="073d2-347">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-348">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-350">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ enum \\ \\ root \| MFG")</span><span class="sxs-lookup"><span data-stu-id="073d2-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-351">Nom du fabricant du contrôleur SCSI.</span><span class="sxs-lookup"><span data-stu-id="073d2-351">Name of the SCSI controller manufacturer.</span></span>

<span data-ttu-id="073d2-352">Exemple : « Adaptec »</span><span class="sxs-lookup"><span data-stu-id="073d2-352">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="073d2-353">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="073d2-353">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-354">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="073d2-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-356">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="073d2-356">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-357">Largeur maximale des données (en bits) prise en charge par le contrôleur SCSI.</span><span class="sxs-lookup"><span data-stu-id="073d2-357">Maximum data width (in bits) supported by the SCSI controller.</span></span>

<span data-ttu-id="073d2-358">Cette propriété est héritée de la [**\_ SCSIController CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-358">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-359">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="073d2-359">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-360">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="073d2-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-362">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="073d2-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-363">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="073d2-363">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="073d2-364">La valeur 0 (zéro) doit être utilisée si le nombre est inconnu.</span><span class="sxs-lookup"><span data-stu-id="073d2-364">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="073d2-365">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-365">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-366">**MaxTransferRate**</span><span class="sxs-lookup"><span data-stu-id="073d2-366">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-367">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="073d2-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-369">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="073d2-369">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-370">Taux de transfert maximal (en bits par seconde) pris en charge par le contrôleur SCSI.</span><span class="sxs-lookup"><span data-stu-id="073d2-370">Maximum transfer rate (in bits per second) supported by the SCSI controller.</span></span>

<span data-ttu-id="073d2-371">Cette propriété est héritée de la [**\_ SCSIController CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-371">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<span data-ttu-id="073d2-372">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-373">**Nom**</span><span class="sxs-lookup"><span data-stu-id="073d2-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-376">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="073d2-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-377">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="073d2-377">Label by which the object is known.</span></span> <span data-ttu-id="073d2-378">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="073d2-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="073d2-379">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="073d2-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-383">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="073d2-383">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-384">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="073d2-384">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="073d2-385">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="073d2-386">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="073d2-386">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="073d2-387">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="073d2-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-388">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="073d2-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="073d2-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="073d2-390">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="073d2-390">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="073d2-391">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="073d2-391">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="073d2-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="073d2-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="073d2-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="073d2-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="073d2-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="073d2-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="073d2-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="073d2-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-396">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="073d2-396">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="073d2-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="073d2-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-398">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="073d2-398">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="073d2-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="073d2-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-400">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="073d2-400">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="073d2-401">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="073d2-401">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="073d2-402">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-402">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="073d2-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="073d2-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-404">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="073d2-404">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="073d2-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="073d2-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="073d2-406">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="073d2-406">Timed Power-On Supported</span></span>

<span data-ttu-id="073d2-407">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="073d2-407">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="073d2-408">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="073d2-408">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-409">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="073d2-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="073d2-411">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="073d2-411">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="073d2-412">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="073d2-412">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="073d2-413">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-414">**ProtectionManagement**</span><span class="sxs-lookup"><span data-stu-id="073d2-414">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-415">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="073d2-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-417">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Contrôleur de stockage DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="073d2-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-418">Prise en charge du contrôleur SCSI pour la redondance ou la protection contre les défaillances de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="073d2-418">Support of the SCSI controller for redundancy or protection against device failures.</span></span>

<span data-ttu-id="073d2-419">Cette propriété est héritée de la [**\_ SCSIController CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-419">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="073d2-420">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="073d2-420">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="073d2-421">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="073d2-421">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="073d2-422">**Non protégé** (3)</span><span class="sxs-lookup"><span data-stu-id="073d2-422">**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="073d2-423">**Protégé** (4)</span><span class="sxs-lookup"><span data-stu-id="073d2-423">**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="073d2-424">**Protégé par le biais de SCC (commande du contrôleur SCSI-3)** (5)</span><span class="sxs-lookup"><span data-stu-id="073d2-424">**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="073d2-425">**Protégé par le biais de SCC-2 (commande du contrôleur SCSI-3)** (6)</span><span class="sxs-lookup"><span data-stu-id="073d2-425">**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="073d2-426">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="073d2-426">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-427">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="073d2-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-429">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="073d2-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-430">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="073d2-430">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="073d2-431">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-431">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="073d2-432">La liste suivante indique les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="073d2-432">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="073d2-433">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="073d2-433">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="073d2-434">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="073d2-434">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="073d2-435">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="073d2-435">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="073d2-436">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="073d2-436">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="073d2-437">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="073d2-437">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="073d2-438">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="073d2-438">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="073d2-439">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="073d2-439">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="073d2-440">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="073d2-440">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="073d2-441">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="073d2-441">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="073d2-442">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="073d2-442">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="073d2-443">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="073d2-443">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="073d2-444">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="073d2-444">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="073d2-445">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="073d2-445">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="073d2-446">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="073d2-446">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="073d2-447">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="073d2-447">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="073d2-448">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="073d2-448">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="073d2-449">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="073d2-449">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="073d2-450">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="073d2-450">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="073d2-451">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="073d2-451">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="073d2-452">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="073d2-452">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="073d2-453">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="073d2-453">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="073d2-454">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="073d2-454">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="073d2-455">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="073d2-455">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="073d2-456">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="073d2-456">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="073d2-457">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="073d2-457">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="073d2-458">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="073d2-458">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="073d2-459">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="073d2-459">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="073d2-460">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="073d2-460">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="073d2-461">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="073d2-461">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="073d2-462">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="073d2-462">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="073d2-463">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="073d2-463">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="073d2-464">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="073d2-464">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="073d2-465">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="073d2-465">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="073d2-466">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="073d2-466">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="073d2-467">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="073d2-467">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="073d2-468">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="073d2-468">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="073d2-469">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="073d2-469">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="073d2-470">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="073d2-470">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="073d2-471">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="073d2-471">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="073d2-472">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="073d2-472">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="073d2-473">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="073d2-473">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="073d2-474">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="073d2-474">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="073d2-475">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="073d2-475">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="073d2-476">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="073d2-476">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="073d2-477">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="073d2-477">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="073d2-478">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="073d2-478">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="073d2-479">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="073d2-479">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="073d2-480">**État**</span><span class="sxs-lookup"><span data-stu-id="073d2-480">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-483">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="073d2-483">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-484">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="073d2-484">Current status of the object.</span></span> <span data-ttu-id="073d2-485">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="073d2-485">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="073d2-486">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="073d2-486">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="073d2-487">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="073d2-487">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="073d2-488">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="073d2-488">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="073d2-489">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="073d2-489">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="073d2-490">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-490">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="073d2-491">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="073d2-491">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="073d2-492">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="073d2-492">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="073d2-493">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="073d2-493">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="073d2-494">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="073d2-494">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="073d2-495">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="073d2-495">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="073d2-496">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="073d2-496">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="073d2-497">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="073d2-497">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="073d2-498">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="073d2-498">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="073d2-499">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="073d2-499">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="073d2-500">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="073d2-500">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="073d2-501">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="073d2-501">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="073d2-502">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="073d2-502">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="073d2-503">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="073d2-503">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="073d2-504">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="073d2-504">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-505">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="073d2-505">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-506">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-507">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="073d2-507">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="073d2-508">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="073d2-508">State of the logical device.</span></span> <span data-ttu-id="073d2-509">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="073d2-509">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="073d2-510">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="073d2-511">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="073d2-511">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="073d2-512">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="073d2-512">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="073d2-513">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="073d2-513">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="073d2-514">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="073d2-514">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="073d2-515">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="073d2-515">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="073d2-516">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="073d2-516">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-517">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-518">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-518">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-519">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="073d2-519">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="073d2-520">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="073d2-520">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="073d2-521">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-522">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="073d2-522">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="073d2-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d2-525">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="073d2-525">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="073d2-526">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="073d2-526">Name of the scoping system.</span></span>

<span data-ttu-id="073d2-527">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="073d2-528">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="073d2-528">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d2-529">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="073d2-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="073d2-530">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="073d2-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="073d2-531">Date et heure de la dernière réinitialisation de ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="073d2-531">Date and time this controller was last reset.</span></span> <span data-ttu-id="073d2-532">Cela peut signifier que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="073d2-532">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="073d2-533">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-533">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="073d2-534">Notes</span><span class="sxs-lookup"><span data-stu-id="073d2-534">Remarks</span></span>

<span data-ttu-id="073d2-535">La classe **Win32 \_ SCSIController** est dérivée de [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="073d2-535">The **Win32\_SCSIController** class is derived from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="073d2-536">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="073d2-536">Requirements</span></span>



| <span data-ttu-id="073d2-537">Condition requise</span><span class="sxs-lookup"><span data-stu-id="073d2-537">Requirement</span></span> | <span data-ttu-id="073d2-538">Valeur</span><span class="sxs-lookup"><span data-stu-id="073d2-538">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="073d2-539">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="073d2-539">Minimum supported client</span></span><br/> | <span data-ttu-id="073d2-540">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="073d2-540">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="073d2-541">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="073d2-541">Minimum supported server</span></span><br/> | <span data-ttu-id="073d2-542">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="073d2-542">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="073d2-543">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="073d2-543">Namespace</span></span><br/>                | <span data-ttu-id="073d2-544">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="073d2-544">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="073d2-545">MOF</span><span class="sxs-lookup"><span data-stu-id="073d2-545">MOF</span></span><br/>                      | <dl> <span data-ttu-id="073d2-546"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="073d2-546"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="073d2-547">DLL</span><span class="sxs-lookup"><span data-stu-id="073d2-547">DLL</span></span><br/>                      | <dl> <span data-ttu-id="073d2-548"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="073d2-548"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="073d2-549">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="073d2-549">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073d2-550">**\_SCSICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="073d2-550">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dt>

[<span data-ttu-id="073d2-551">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="073d2-551">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
