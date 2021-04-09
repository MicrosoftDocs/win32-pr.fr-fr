---
description: Représente les propriétés d’un périphérique audio sur un système informatique exécutant Windows.
ms.assetid: 5471ffe9-60a3-466f-a608-e6268ba73c2b
ms.tgt_platform: multiple
title: Classe Win32_SoundDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SoundDevice
- Win32_SoundDevice.Reset
- Win32_SoundDevice.SetPowerState
- Win32_SoundDevice.Availability
- Win32_SoundDevice.Caption
- Win32_SoundDevice.ConfigManagerErrorCode
- Win32_SoundDevice.ConfigManagerUserConfig
- Win32_SoundDevice.CreationClassName
- Win32_SoundDevice.Description
- Win32_SoundDevice.DeviceID
- Win32_SoundDevice.DMABufferSize
- Win32_SoundDevice.ErrorCleared
- Win32_SoundDevice.ErrorDescription
- Win32_SoundDevice.InstallDate
- Win32_SoundDevice.LastErrorCode
- Win32_SoundDevice.Manufacturer
- Win32_SoundDevice.MPU401Address
- Win32_SoundDevice.Name
- Win32_SoundDevice.PNPDeviceID
- Win32_SoundDevice.PowerManagementCapabilities
- Win32_SoundDevice.PowerManagementSupported
- Win32_SoundDevice.ProductName
- Win32_SoundDevice.Status
- Win32_SoundDevice.StatusInfo
- Win32_SoundDevice.SystemCreationClassName
- Win32_SoundDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73e0ef7cbc71872d26f75311b6d72ac48bbfae8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111483"
---
# <a name="win32_sounddevice-class"></a><span data-ttu-id="dfb13-103">\_Classe SoundDevice Win32</span><span class="sxs-lookup"><span data-stu-id="dfb13-103">Win32\_SoundDevice class</span></span>

<span data-ttu-id="dfb13-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ SoundDevice** représente les propriétés d’un périphérique audio sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="dfb13-104">The **Win32\_SoundDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a sound device on a computer system running Windows.</span></span>

<span data-ttu-id="dfb13-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dfb13-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dfb13-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="dfb13-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb13-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfb13-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SoundDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DMABufferSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MPU401Address;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="dfb13-108">Membres</span><span class="sxs-lookup"><span data-stu-id="dfb13-108">Members</span></span>

<span data-ttu-id="dfb13-109">La classe **Win32 \_ SoundDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dfb13-109">The **Win32\_SoundDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="dfb13-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dfb13-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dfb13-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dfb13-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dfb13-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dfb13-112">Methods</span></span>

<span data-ttu-id="dfb13-113">La classe **Win32 \_ SoundDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dfb13-113">The **Win32\_SoundDevice** class has these methods.</span></span>



| <span data-ttu-id="dfb13-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="dfb13-114">Method</span></span>            | <span data-ttu-id="dfb13-115">Description</span><span class="sxs-lookup"><span data-stu-id="dfb13-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb13-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="dfb13-116">**Reset**</span></span>         | <span data-ttu-id="dfb13-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="dfb13-117">Not implemented.</span></span> <span data-ttu-id="dfb13-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="dfb13-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dfb13-119">**SetPowerState**</span></span> | <span data-ttu-id="dfb13-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="dfb13-120">Not implemented.</span></span> <span data-ttu-id="dfb13-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dfb13-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dfb13-122">Properties</span></span>

<span data-ttu-id="dfb13-123">La classe **Win32 \_ SoundDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dfb13-123">The **Win32\_SoundDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfb13-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="dfb13-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dfb13-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-127">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="dfb13-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-128">Availability and status of the device.</span></span>

<span data-ttu-id="dfb13-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dfb13-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="dfb13-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dfb13-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="dfb13-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dfb13-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="dfb13-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="dfb13-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dfb13-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="dfb13-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dfb13-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="dfb13-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dfb13-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="dfb13-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dfb13-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="dfb13-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dfb13-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="dfb13-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dfb13-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="dfb13-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dfb13-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="dfb13-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dfb13-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="dfb13-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dfb13-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="dfb13-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dfb13-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="dfb13-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="dfb13-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dfb13-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="dfb13-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="dfb13-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dfb13-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="dfb13-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="dfb13-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dfb13-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="dfb13-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dfb13-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="dfb13-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="dfb13-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dfb13-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="dfb13-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-153">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="dfb13-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dfb13-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="dfb13-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-155">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="dfb13-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dfb13-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="dfb13-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-157">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="dfb13-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dfb13-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="dfb13-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-159">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="dfb13-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dfb13-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dfb13-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-163">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-164">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfb13-164">Short description of the object.</span></span>

<span data-ttu-id="dfb13-165">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dfb13-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfb13-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-169">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dfb13-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-170">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="dfb13-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="dfb13-171">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dfb13-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dfb13-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="dfb13-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-174">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="dfb13-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dfb13-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dfb13-176">(1)</span><span class="sxs-lookup"><span data-stu-id="dfb13-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-177">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="dfb13-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dfb13-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dfb13-179">(2)</span><span class="sxs-lookup"><span data-stu-id="dfb13-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dfb13-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dfb13-181">(3)</span><span class="sxs-lookup"><span data-stu-id="dfb13-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-182">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="dfb13-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dfb13-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dfb13-184">(4)</span><span class="sxs-lookup"><span data-stu-id="dfb13-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-185">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="dfb13-185">Device is not working properly.</span></span> <span data-ttu-id="dfb13-186">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="dfb13-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dfb13-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dfb13-188">(5)</span><span class="sxs-lookup"><span data-stu-id="dfb13-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-189">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="dfb13-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dfb13-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dfb13-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="dfb13-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-192">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="dfb13-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dfb13-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dfb13-194">(7)</span><span class="sxs-lookup"><span data-stu-id="dfb13-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dfb13-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dfb13-196">(8)</span><span class="sxs-lookup"><span data-stu-id="dfb13-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-197">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="dfb13-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dfb13-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dfb13-199">(9)</span><span class="sxs-lookup"><span data-stu-id="dfb13-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-200">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="dfb13-200">Device is not working properly.</span></span> <span data-ttu-id="dfb13-201">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dfb13-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dfb13-203">(10)</span><span class="sxs-lookup"><span data-stu-id="dfb13-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-204">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dfb13-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dfb13-206">(11)</span><span class="sxs-lookup"><span data-stu-id="dfb13-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-207">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dfb13-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dfb13-209">douze</span><span class="sxs-lookup"><span data-stu-id="dfb13-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-210">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="dfb13-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dfb13-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dfb13-212">(13)</span><span class="sxs-lookup"><span data-stu-id="dfb13-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-213">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dfb13-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dfb13-215">(14)</span><span class="sxs-lookup"><span data-stu-id="dfb13-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-216">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="dfb13-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dfb13-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dfb13-218">(15)</span><span class="sxs-lookup"><span data-stu-id="dfb13-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-219">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="dfb13-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dfb13-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dfb13-221">(16)</span><span class="sxs-lookup"><span data-stu-id="dfb13-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-222">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dfb13-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dfb13-224">(17)</span><span class="sxs-lookup"><span data-stu-id="dfb13-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-225">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="dfb13-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dfb13-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dfb13-227">(18)</span><span class="sxs-lookup"><span data-stu-id="dfb13-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-228">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="dfb13-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dfb13-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dfb13-230">(19)</span><span class="sxs-lookup"><span data-stu-id="dfb13-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dfb13-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dfb13-232">(20)</span><span class="sxs-lookup"><span data-stu-id="dfb13-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-233">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="dfb13-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dfb13-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dfb13-235">(21)</span><span class="sxs-lookup"><span data-stu-id="dfb13-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-236">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="dfb13-236">System failure.</span></span> <span data-ttu-id="dfb13-237">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="dfb13-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dfb13-238">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dfb13-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dfb13-240">(22)</span><span class="sxs-lookup"><span data-stu-id="dfb13-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-241">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="dfb13-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dfb13-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dfb13-243">(23)</span><span class="sxs-lookup"><span data-stu-id="dfb13-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="dfb13-244">System failure.</span></span> <span data-ttu-id="dfb13-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="dfb13-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dfb13-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dfb13-247">(24)</span><span class="sxs-lookup"><span data-stu-id="dfb13-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-248">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="dfb13-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dfb13-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dfb13-250">(25)</span><span class="sxs-lookup"><span data-stu-id="dfb13-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-251">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dfb13-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dfb13-253">(26)</span><span class="sxs-lookup"><span data-stu-id="dfb13-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-254">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dfb13-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dfb13-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dfb13-256">(27)</span><span class="sxs-lookup"><span data-stu-id="dfb13-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-257">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="dfb13-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dfb13-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dfb13-259">(28)</span><span class="sxs-lookup"><span data-stu-id="dfb13-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-260">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="dfb13-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dfb13-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dfb13-262">(29)</span><span class="sxs-lookup"><span data-stu-id="dfb13-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-263">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="dfb13-263">Device is disabled.</span></span> <span data-ttu-id="dfb13-264">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="dfb13-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dfb13-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dfb13-266">(30)</span><span class="sxs-lookup"><span data-stu-id="dfb13-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-267">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="dfb13-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dfb13-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="dfb13-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dfb13-269">31</span><span class="sxs-lookup"><span data-stu-id="dfb13-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-270">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="dfb13-270">Device is not working properly.</span></span> <span data-ttu-id="dfb13-271">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="dfb13-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dfb13-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="dfb13-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-273">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dfb13-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-275">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dfb13-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-276">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfb13-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dfb13-277">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dfb13-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-281">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dfb13-281">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-282">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="dfb13-282">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="dfb13-283">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="dfb13-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dfb13-284">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-285">**Description**</span><span class="sxs-lookup"><span data-stu-id="dfb13-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-288">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dfb13-288">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-289">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfb13-289">Description of the object.</span></span>

<span data-ttu-id="dfb13-290">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dfb13-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-294">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ MediaResources \\ \\ Wave \| DeviceID")</span><span class="sxs-lookup"><span data-stu-id="dfb13-294">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\wave\|DeviceID")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-295">Identificateur unique du périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="dfb13-295">Unique identifier of the sound device.</span></span>

<span data-ttu-id="dfb13-296">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-297">**DMABufferSize**</span><span class="sxs-lookup"><span data-stu-id="dfb13-297">**DMABufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-298">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dfb13-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-300">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »), [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-300">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-301">Taille de la mémoire tampon d’accès direct à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="dfb13-301">Size of the Direct Memory Access buffer.</span></span>

<span data-ttu-id="dfb13-302">Example: 4</span><span class="sxs-lookup"><span data-stu-id="dfb13-302">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-303">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="dfb13-303">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-304">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dfb13-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-306">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="dfb13-306">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="dfb13-307">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-308">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dfb13-308">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-311">Chaîne de forme libre fournissant plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="dfb13-311">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="dfb13-312">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dfb13-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-314">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dfb13-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-316">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="dfb13-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-317">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfb13-317">Date and time the object was installed.</span></span> <span data-ttu-id="dfb13-318">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="dfb13-318">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dfb13-319">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-320">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dfb13-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-321">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfb13-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-323">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="dfb13-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dfb13-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-325">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="dfb13-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-328">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-328">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-329">Fabricant du périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="dfb13-329">Manufacturer of the sound device.</span></span>

<span data-ttu-id="dfb13-330">Exemple : « Creative Labs »</span><span class="sxs-lookup"><span data-stu-id="dfb13-330">Example: "Creative Labs"</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-331">**Adresse mpu401**</span><span class="sxs-lookup"><span data-stu-id="dfb13-331">**MPU401Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-332">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfb13-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-334">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-335">Adresse d’e/s de départ affectée au port MPU-401 du périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="dfb13-335">Starting I/O address assigned to the MPU-401 port of the sound device.</span></span>

<span data-ttu-id="dfb13-336">Exemple : 300</span><span class="sxs-lookup"><span data-stu-id="dfb13-336">Example: 300</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-337">**Nom**</span><span class="sxs-lookup"><span data-stu-id="dfb13-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-340">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="dfb13-340">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-341">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="dfb13-341">Label by which the object is known.</span></span> <span data-ttu-id="dfb13-342">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="dfb13-342">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="dfb13-343">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dfb13-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-347">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dfb13-347">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-348">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="dfb13-348">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="dfb13-349">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dfb13-350">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="dfb13-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dfb13-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-352">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dfb13-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-354">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="dfb13-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dfb13-355">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="dfb13-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dfb13-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="dfb13-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dfb13-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="dfb13-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dfb13-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="dfb13-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dfb13-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="dfb13-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-360">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="dfb13-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dfb13-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="dfb13-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-362">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="dfb13-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dfb13-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="dfb13-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-364">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dfb13-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dfb13-365">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="dfb13-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="dfb13-366">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-366">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dfb13-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="dfb13-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-368">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="dfb13-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dfb13-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="dfb13-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dfb13-370">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfb13-370">Timed Power-On Supported</span></span>

<span data-ttu-id="dfb13-371">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="dfb13-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dfb13-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="dfb13-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-373">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dfb13-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-375">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="dfb13-375">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="dfb13-376">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="dfb13-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="dfb13-377">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-378">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="dfb13-378">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-381">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Multimedia structures \| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) \| szPname")</span><span class="sxs-lookup"><span data-stu-id="dfb13-381">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Multimedia Structures\|[**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)\|szPname")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-382">Nom de produit du périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="dfb13-382">Product name of the sound device.</span></span>

<span data-ttu-id="dfb13-383">Exemple : « Creative Labs SoundBlaster AWE64PNP »</span><span class="sxs-lookup"><span data-stu-id="dfb13-383">Example: "Creative Labs SoundBlaster AWE64PNP"</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-384">**État**</span><span class="sxs-lookup"><span data-stu-id="dfb13-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-385">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-386">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-387">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="dfb13-387">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-388">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfb13-388">Current status of the object.</span></span> <span data-ttu-id="dfb13-389">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="dfb13-389">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dfb13-390">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="dfb13-390">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="dfb13-391">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="dfb13-391">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dfb13-392">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="dfb13-392">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dfb13-393">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="dfb13-393">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dfb13-394">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-394">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dfb13-395">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dfb13-395">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dfb13-396">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-396">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dfb13-397">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-397">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dfb13-398">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-398">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dfb13-399">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="dfb13-399">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dfb13-400">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-400">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dfb13-401">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-401">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dfb13-402">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-402">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dfb13-403">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-403">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dfb13-404">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-404">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dfb13-405">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-405">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dfb13-406">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-406">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dfb13-407">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="dfb13-407">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dfb13-408">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dfb13-408">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-409">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dfb13-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-411">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dfb13-411">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-412">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="dfb13-412">State of the logical device.</span></span> <span data-ttu-id="dfb13-413">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="dfb13-413">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dfb13-414">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dfb13-415">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="dfb13-415">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dfb13-416">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="dfb13-416">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dfb13-417">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="dfb13-417">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dfb13-418">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="dfb13-418">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dfb13-419">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="dfb13-419">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dfb13-420">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dfb13-420">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-423">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dfb13-423">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-424">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="dfb13-424">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="dfb13-425">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfb13-426">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dfb13-426">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfb13-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dfb13-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dfb13-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfb13-429">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dfb13-429">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dfb13-430">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="dfb13-430">Name of the scoping system.</span></span>

<span data-ttu-id="dfb13-431">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfb13-432">Notes</span><span class="sxs-lookup"><span data-stu-id="dfb13-432">Remarks</span></span>

<span data-ttu-id="dfb13-433">La classe **Win32 \_ SoundDevice** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dfb13-433">The **Win32\_SoundDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dfb13-434">Exemples</span><span class="sxs-lookup"><span data-stu-id="dfb13-434">Examples</span></span>

<span data-ttu-id="dfb13-435">L’exemple de liste de propriétés de la [carte son](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) de l’exemple PowerShell récupère des informations sur toutes les cartes son installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dfb13-435">The [List Sound Card Properties](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) PowerShell sample retrieves information about all the sound cards installed in a computer.</span></span>

<span data-ttu-id="dfb13-436">L’exemple VBScript suivant récupère des informations sur toutes les cartes son installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dfb13-436">The following VBScript sample retrieves information about all the sound cards installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SoundDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "DMA Buffer Size: " & objItem.DMABufferSize 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "MPU 401 Address: " & objItem.MPU401Address 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Product Name: " & objItem.ProductName 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="dfb13-437">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfb13-437">Requirements</span></span>



| <span data-ttu-id="dfb13-438">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfb13-438">Requirement</span></span> | <span data-ttu-id="dfb13-439">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfb13-439">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb13-440">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfb13-440">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb13-441">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfb13-441">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfb13-442">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfb13-442">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb13-443">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfb13-443">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfb13-444">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dfb13-444">Namespace</span></span><br/>                | <span data-ttu-id="dfb13-445">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="dfb13-445">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dfb13-446">MOF</span><span class="sxs-lookup"><span data-stu-id="dfb13-446">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfb13-447"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfb13-447"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfb13-448">DLL</span><span class="sxs-lookup"><span data-stu-id="dfb13-448">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfb13-449"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfb13-449"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb13-450">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfb13-450">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb13-451">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="dfb13-451">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="dfb13-452">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="dfb13-452">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
