---
description: Représente un système informatique exécutant Windows.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Win32_ComputerSystem, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110350"
---
# <a name="win32_computersystem-class"></a><span data-ttu-id="4445c-103">\_Classe Win32 ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="4445c-103">Win32\_ComputerSystem class</span></span>

<span data-ttu-id="4445c-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ComputerSystem** représente un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="4445c-104">The **Win32\_ComputerSystem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a computer system running Windows.</span></span>

<span data-ttu-id="4445c-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4445c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4445c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4445c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a><span data-ttu-id="4445c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4445c-107">Members</span></span>

<span data-ttu-id="4445c-108">La classe **Win32 \_ ComputerSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4445c-108">The **Win32\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="4445c-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4445c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4445c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4445c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4445c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4445c-111">Methods</span></span>

<span data-ttu-id="4445c-112">La classe **Win32 \_ ComputerSystem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4445c-112">The **Win32\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="4445c-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="4445c-113">Method</span></span>                                                                                          | <span data-ttu-id="4445c-114">Description</span><span class="sxs-lookup"><span data-stu-id="4445c-114">Description</span></span>                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4445c-115">**JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="4445c-115">**JoinDomainOrWorkgroup**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | <span data-ttu-id="4445c-116">Ajoute un système informatique à un domaine ou à un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="4445c-116">Adds a computer system to a domain or workgroup.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="4445c-117">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="4445c-117">**Rename**</span></span>](rename-method-in-class-win32-computersystem.md)                                   | <span data-ttu-id="4445c-118">Renomme un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4445c-118">Renames a local computer.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="4445c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4445c-119">**SetPowerState**</span></span>                                                                               | <span data-ttu-id="4445c-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="4445c-120">Not implemented.</span></span> <span data-ttu-id="4445c-121">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-121">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span><br/> |
| [<span data-ttu-id="4445c-122">**UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="4445c-122">**UnjoinDomainOrWorkgroup**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | <span data-ttu-id="4445c-123">Supprime un système informatique d’un domaine ou d’un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="4445c-123">Removes a computer system from a domain or workgroup.</span></span><br/>                                                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="4445c-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4445c-124">Properties</span></span>

<span data-ttu-id="4445c-125">La classe **Win32 \_ ComputerSystem** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4445c-125">The **Win32\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4445c-126">**AdminPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="4445c-126">**AdminPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 24 \| Hardware Security Settings \| AdminPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="4445c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|AdminPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-130">Paramètres de sécurité du matériel système pour l’état du mot de passe administrateur.</span><span class="sxs-lookup"><span data-stu-id="4445c-130">System hardware security settings for administrator password status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4445c-131">**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-131">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4445c-132">**Activé** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-132">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="4445c-133">**Non implémenté** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-133">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-134">**Inconnu** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-134">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-135">**AutomaticManagedPagefile**</span><span class="sxs-lookup"><span data-stu-id="4445c-135">**AutomaticManagedPagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-136">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4445c-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-139">Si la **valeur est true**, le système gère le fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="4445c-139">If **True**, the system manages the page file.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-140">**AutomaticResetBootOption**</span><span class="sxs-lookup"><span data-stu-id="4445c-140">**AutomaticResetBootOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-141">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4445c-143">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| reboot")</span><span class="sxs-lookup"><span data-stu-id="4445c-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-144">Si la **valeur est true**, l’option de démarrage à réinitialisation automatique est activée.</span><span class="sxs-lookup"><span data-stu-id="4445c-144">If **True**, the automatic reset boot option is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-145">**AutomaticResetCapability**</span><span class="sxs-lookup"><span data-stu-id="4445c-145">**AutomaticResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-149">Si la **valeur est true**, la réinitialisation automatique est activée.</span><span class="sxs-lookup"><span data-stu-id="4445c-149">If **True**, the automatic reset is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-150">**BootOptionOnLimit**</span><span class="sxs-lookup"><span data-stu-id="4445c-150">**BootOptionOnLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-153">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| type 23 \| - \| option de démarrage on Limit »)</span><span class="sxs-lookup"><span data-stu-id="4445c-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilites\|Boot Option on Limit")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-154">La limite des options de démarrage est activée.</span><span class="sxs-lookup"><span data-stu-id="4445c-154">Boot option limit is ON.</span></span> <span data-ttu-id="4445c-155">Identifie l’action système lorsque la valeur **resetLimit** est atteinte.</span><span class="sxs-lookup"><span data-stu-id="4445c-155">Identifies the system action when the **ResetLimit** value is reached.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="4445c-156">**Réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-156">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="4445c-157">**Système d’exploitation** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-157">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="4445c-158">**Utilitaires système** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-158">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="4445c-159">**Ne pas redémarrer** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-159">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-160">**BootOptionOnWatchDog**</span><span class="sxs-lookup"><span data-stu-id="4445c-160">**BootOptionOnWatchDog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-161">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-163">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 23 \| Capabilities \| option Boot option")</span><span class="sxs-lookup"><span data-stu-id="4445c-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilities\|Boot Option")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-164">Type d’action de redémarrage après l’expiration du minuteur de surveillance.</span><span class="sxs-lookup"><span data-stu-id="4445c-164">Type of reboot action after the time on the watchdog timer is elapsed.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="4445c-165">**Réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-165">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="4445c-166">**Système d’exploitation** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-166">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="4445c-167">**Utilitaires système** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-167">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="4445c-168">**Ne pas redémarrer** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-168">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-169">**BootROMSupported**</span><span class="sxs-lookup"><span data-stu-id="4445c-169">**BootROMSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-170">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-172">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-173">Si la **valeur est true**, indique si une ROM de démarrage est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4445c-173">If **True**, indicates whether a boot ROM is supported.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-174">**BootStatus**</span><span class="sxs-lookup"><span data-stu-id="4445c-174">**BootStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-175">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4445c-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-177">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 32 \| System Boot information \| Boot Status")</span><span class="sxs-lookup"><span data-stu-id="4445c-177">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 32\|System Boot Information\|Boot Status")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-178">Champs d’État et de données supplémentaires identifiant l’état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="4445c-178">Status and Additional Data fields that identify the boot status.</span></span>

<span data-ttu-id="4445c-179">Cette valeur provient du membre **État de démarrage** de la structure d' **informations de démarrage du système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="4445c-179">This value comes from the **Boot Status** member of the **System Boot Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="4445c-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4445c-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-181">**BootupState**</span><span class="sxs-lookup"><span data-stu-id="4445c-181">**BootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-184">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT")</span><span class="sxs-lookup"><span data-stu-id="4445c-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)\|SM\_CLEANBOOT")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-185">Le système est démarré.</span><span class="sxs-lookup"><span data-stu-id="4445c-185">System is started.</span></span> <span data-ttu-id="4445c-186">Le démarrage de la prévention de défaillance contourne les fichiers de démarrage de l’utilisateur également appelés SafeBoot.</span><span class="sxs-lookup"><span data-stu-id="4445c-186">Fail-safe boot bypasses the user startup files also called SafeBoot.</span></span>

<span data-ttu-id="4445c-187">La liste suivante contient les valeurs requises :</span><span class="sxs-lookup"><span data-stu-id="4445c-187">The following list contains the required values:</span></span>

<dl> <dd><span data-ttu-id="4445c-188">« Démarrage normal »</span><span class="sxs-lookup"><span data-stu-id="4445c-188">"Normal boot"</span></span></dd> <dd><span data-ttu-id="4445c-189">« Démarrage sans échec »</span><span class="sxs-lookup"><span data-stu-id="4445c-189">"Fail-safe boot"</span></span></dd> <dd><span data-ttu-id="4445c-190">« Défaillance avec le démarrage réseau »</span><span class="sxs-lookup"><span data-stu-id="4445c-190">"Fail-safe with network boot"</span></span></dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

<span data-ttu-id="4445c-191">**Démarrage normal** (« démarrage normal »)</span><span class="sxs-lookup"><span data-stu-id="4445c-191">**Normal boot** ("Normal boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

<span data-ttu-id="4445c-192">**Démarrage** de la prévention de défaillance (« démarrage sécurisé »)</span><span class="sxs-lookup"><span data-stu-id="4445c-192">**Fail-safe boot** ("Fail-safe boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

<span data-ttu-id="4445c-193">**Prévention de défaillance avec démarrage réseau** (« défaillance avec démarrage réseau »)</span><span class="sxs-lookup"><span data-stu-id="4445c-193">**Fail-safe with network boot** ("Fail-safe with network boot")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-194">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4445c-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-197">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="4445c-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-198">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="4445c-198">Short description of the object a one-line string.</span></span>

<span data-ttu-id="4445c-199">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-200">**ChassisBootupState**</span><span class="sxs-lookup"><span data-stu-id="4445c-200">**ChassisBootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-201">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-203">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 3 \| État de démarrage")</span><span class="sxs-lookup"><span data-stu-id="4445c-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Bootup State")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-204">État de démarrage du châssis.</span><span class="sxs-lookup"><span data-stu-id="4445c-204">Boot up state of the chassis.</span></span>

<span data-ttu-id="4445c-205">Cette valeur provient du membre d' **État de démarrage** de la structure du **boîtier ou du châssis du système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="4445c-205">This value comes from the **Boot-up State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4445c-206">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-206">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-207">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-207">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="4445c-208">**Sécurité** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-208">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4445c-209">**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-209">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4445c-210">**Critique** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-210">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="4445c-211">**Non récupérable** (6)</span><span class="sxs-lookup"><span data-stu-id="4445c-211">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-212">**ChassisSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="4445c-212">**ChassisSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-215">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| type 3 \| \| SKU Number Number »)</span><span class="sxs-lookup"><span data-stu-id="4445c-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Chassis\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-216">Numéro de référence du châssis ou du boîtier sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="4445c-216">The chassis or enclosure SKU number as a string.</span></span>

<span data-ttu-id="4445c-217">Cette valeur provient du membre **numéro de référence (SKU** ) de la structure du **boîtier du système ou du châssis** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="4445c-217">This value comes from the **SKU Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="4445c-218">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4445c-218">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-219">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4445c-219">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-222">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4445c-222">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4445c-223">Nom de la première classe concrète dans la chaîne d’héritage d’une instance.</span><span class="sxs-lookup"><span data-stu-id="4445c-223">Name of the first concrete class in the inheritance chain of an instance.</span></span> <span data-ttu-id="4445c-224">Vous pouvez utiliser cette propriété avec d’autres propriétés de la classe pour identifier toutes les instances de la classe et ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="4445c-224">You can use this property with other properties of the class to identify all instances of the class and its subclasses.</span></span>

<span data-ttu-id="4445c-225">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-225">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-226">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="4445c-226">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-227">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="4445c-227">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-228">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4445c-229">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Time structures \| [**\_ \_ information fuseau horaire**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="4445c-229">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-230">Durée pendant laquelle le système informatique unitaire est décalé par rapport au temps universel coordonné (UTC, Universal Time Coordinated).</span><span class="sxs-lookup"><span data-stu-id="4445c-230">Amount of time the unitary computer system is offset from Coordinated Universal Time (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-231">**DaylightInEffect**</span><span class="sxs-lookup"><span data-stu-id="4445c-231">**DaylightInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-232">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-234">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span><span class="sxs-lookup"><span data-stu-id="4445c-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Functions\|[**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-235">Si la **valeur est true**, le mode d’économie d’heure est activé.</span><span class="sxs-lookup"><span data-stu-id="4445c-235">If **True**, the daylight savings mode is ON.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-236">**Description**</span><span class="sxs-lookup"><span data-stu-id="4445c-236">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-239">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4445c-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-240">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4445c-240">Description of the object.</span></span>

<span data-ttu-id="4445c-241">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-241">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-242">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="4445c-242">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-245">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| GetComputerNameEx \| ComputerNameDnsHostname")</span><span class="sxs-lookup"><span data-stu-id="4445c-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetComputerNameEx\|ComputerNameDnsHostname")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-246">Nom de l’ordinateur local en fonction du serveur de noms de domaine (DNS).</span><span class="sxs-lookup"><span data-stu-id="4445c-246">Name of local computer according to the domain name server (DNS).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-247">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="4445c-247">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-250">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management Structures \| [**wksta \_ info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ LANGROUP")</span><span class="sxs-lookup"><span data-stu-id="4445c-250">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**WKSTA\_INFO\_100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100)\|wki100\_langroup")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-251">Nom du domaine auquel un ordinateur appartient.</span><span class="sxs-lookup"><span data-stu-id="4445c-251">Name of the domain to which a computer belongs.</span></span>

> [!Note]  
> <span data-ttu-id="4445c-252">Si l’ordinateur ne fait pas partie d’un domaine, le nom du groupe de travail est retourné.</span><span class="sxs-lookup"><span data-stu-id="4445c-252">If the computer is not part of a domain, then the name of the workgroup is returned.</span></span>

 

</dd> <dt>

<span data-ttu-id="4445c-253">**DomainRole**</span><span class="sxs-lookup"><span data-stu-id="4445c-253">**DomainRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-254">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-256">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Directory Service (DS) structures \| [**DSROLE \_ principal \_ Domain \_ info \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ \_ rôle machine**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| rôle")</span><span class="sxs-lookup"><span data-stu-id="4445c-256">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Directory Service (Ds) Structures\| [**DSROLE\_PRIMARY\_DOMAIN\_INFO\_BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic)\|[**DSROLE\_MACHINE\_ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role)\| MachineRole")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-257">Rôle d’un ordinateur dans un groupe de travail de domaine attribué.</span><span class="sxs-lookup"><span data-stu-id="4445c-257">Role of a computer in an assigned domain workgroup.</span></span> <span data-ttu-id="4445c-258">Un groupe de travail de domaine est un ensemble d’ordinateurs sur le même réseau.</span><span class="sxs-lookup"><span data-stu-id="4445c-258">A domain workgroup is a collection of computers on the same network.</span></span> <span data-ttu-id="4445c-259">Par exemple, une propriété **DomainRole** peut indiquer qu’un ordinateur est une station de travail membre.</span><span class="sxs-lookup"><span data-stu-id="4445c-259">For example, a **DomainRole** property may show that a computer is a member workstation.</span></span>

<span data-ttu-id="4445c-260">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-260">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

<span data-ttu-id="4445c-261">**Station de travail autonome** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-261">**Standalone Workstation** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

<span data-ttu-id="4445c-262">**Station de travail membre** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-262">**Member Workstation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

<span data-ttu-id="4445c-263">**Serveur autonome** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-263">**Standalone Server** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

<span data-ttu-id="4445c-264">**Serveur membre** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-264">**Member Server** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="4445c-265">**Contrôleur de domaine secondaire** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-265">**Backup Domain Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="4445c-266">**Contrôleur de domaine principal** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-266">**Primary Domain Controller** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-267">**EnableDaylightSavingsTime**</span><span class="sxs-lookup"><span data-stu-id="4445c-267">**EnableDaylightSavingsTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-268">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-269">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4445c-270">Active l’heure d’été (DST) sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4445c-270">Enables daylight savings time (DST) on a computer.</span></span> <span data-ttu-id="4445c-271">La valeur **true** indique que l’heure système passe à une heure en avance ou en retard au démarrage ou à la fin de l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="4445c-271">A value of **True** indicates that the system time changes to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="4445c-272">La valeur **false** indique que l’heure système ne passe pas à une heure avant ou après le début ou la fin de l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="4445c-272">A value of **False** indicates that the system time does not change to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="4445c-273">La valeur **null** indique que l’état de l’heure d’été est inconnu sur un système.</span><span class="sxs-lookup"><span data-stu-id="4445c-273">A value of **NULL** indicates that the DST status is unknown on a system.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-274">**FrontPanelResetStatus**</span><span class="sxs-lookup"><span data-stu-id="4445c-274">**FrontPanelResetStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-275">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-277">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 24 \| Hardware Security Settings \| FrontPanelResetStatus")</span><span class="sxs-lookup"><span data-stu-id="4445c-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|FrontPanelResetStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-278">Le tableau suivant répertorie les paramètres de sécurité matérielle pour le bouton Réinitialiser sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4445c-278">The following table lists the hardware security settings for the reset button on a computer.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4445c-279">**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-279">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4445c-280">**Activé** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-280">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="4445c-281">**Non implémenté** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-281">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-282">**Inconnu** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-282">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-283">**HypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="4445c-283">**HypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-284">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-286">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-286">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-287">Si la **valeur est true**, un hyperviseur est présent.</span><span class="sxs-lookup"><span data-stu-id="4445c-287">If **True**, a hypervisor is present.</span></span>

<span data-ttu-id="4445c-288">**Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="4445c-288">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-289">**InfraredSupported**</span><span class="sxs-lookup"><span data-stu-id="4445c-289">**InfraredSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-290">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-292">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-292">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-293">Si la **valeur est true**, un port infrarouge (IR) existe sur un système informatique.</span><span class="sxs-lookup"><span data-stu-id="4445c-293">If **True**, an infrared (IR) port exists on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-294">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="4445c-294">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-295">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4445c-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4445c-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4445c-297">Données requises pour trouver le périphérique de chargement initial ou le service de démarrage pour demander que le système d’exploitation démarre.</span><span class="sxs-lookup"><span data-stu-id="4445c-297">Data required to find the initial load device or boot service to request that the operating system start up.</span></span>

<span data-ttu-id="4445c-298">Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-298">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<span data-ttu-id="4445c-299">**Windows Server 2008 R2 :** Cette propriété est disponible, mais vide.</span><span class="sxs-lookup"><span data-stu-id="4445c-299">**Windows Server 2008 R2:** This property is available, but empty.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4445c-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-301">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4445c-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-303">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="4445c-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-304">L’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="4445c-304">Object is installed.</span></span> <span data-ttu-id="4445c-305">Un objet n’a pas besoin d’une valeur pour indiquer qu’il est installé.</span><span class="sxs-lookup"><span data-stu-id="4445c-305">An object does not need a value to indicate that it is installed.</span></span>

<span data-ttu-id="4445c-306">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-307">**KeyboardPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="4445c-307">**KeyboardPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-308">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-310">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 24 \| Hardware Security Settings \| KeyboardPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="4445c-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|KeyboardPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-311">Paramètres de sécurité du matériel système pour l’état du mot de passe du clavier.</span><span class="sxs-lookup"><span data-stu-id="4445c-311">System hardware security settings for Keyboard Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4445c-312">**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-312">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4445c-313">**Activé** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-313">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="4445c-314">**Non implémenté** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-314">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-315">**Inconnu** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-315">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-316">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="4445c-316">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4445c-319">Entrée de tableau de la propriété **InitialLoadInfo** qui contient les données pour démarrer le système d’exploitation chargé.</span><span class="sxs-lookup"><span data-stu-id="4445c-319">Array entry of the **InitialLoadInfo** property that contains the data to start the loaded operating system.</span></span>

<span data-ttu-id="4445c-320">Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-320">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-321">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="4445c-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-324">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 1 \| System information \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="4445c-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-325">Nom du fabricant de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4445c-325">Name of a computer manufacturer.</span></span>

<span data-ttu-id="4445c-326">Exemple : Adventure Works</span><span class="sxs-lookup"><span data-stu-id="4445c-326">Example: Adventure Works</span></span>

</dd> <dt>

<span data-ttu-id="4445c-327">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="4445c-327">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-330">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 1 \| System information \| Product Name")</span><span class="sxs-lookup"><span data-stu-id="4445c-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Product Name")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-331">Nom de produit qu’un fabricant donne à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4445c-331">Product name that a manufacturer gives to a computer.</span></span> <span data-ttu-id="4445c-332">Cette propriété doit avoir une valeur.</span><span class="sxs-lookup"><span data-stu-id="4445c-332">This property must have a value.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-333">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4445c-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-336">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4445c-336">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4445c-337">Clé d’une instance de [**\_ système CIM**](cim-system.md) dans un environnement d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="4445c-337">Key of a [**CIM\_System**](cim-system.md) instance in an enterprise environment.</span></span>

<span data-ttu-id="4445c-338">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-339">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="4445c-339">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4445c-342">Valeur de **nom** de système d’ordinateur générée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4445c-342">Computer system **Name** value that is generated automatically.</span></span> <span data-ttu-id="4445c-343">L' [**objet \_ ComputerSystem CIM**](cim-computersystem.md) et ses dérivés sont des objets de niveau supérieur du Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="4445c-343">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of the Common Information Model (CIM).</span></span> <span data-ttu-id="4445c-344">Ils fournissent l’étendue de plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="4445c-344">They provide the scope for several components.</span></span> <span data-ttu-id="4445c-345">Des [**clés \_ système CIM**](cim-system.md) uniques sont nécessaires, mais vous pouvez définir une méthode heuristique pour créer le nom **\_ ComputerSystem CIM** qui génère le même nom et qui est indépendant du protocole de découverte.</span><span class="sxs-lookup"><span data-stu-id="4445c-345">Unique [**CIM\_System**](cim-system.md) keys are required, but you can define a heuristic to create the **CIM\_ComputerSystem** name that generates the same name, and is independent from the discovery protocol.</span></span> <span data-ttu-id="4445c-346">Cela empêche les problèmes d’inventaire et de gestion lorsque la même ressource ou entité est découverte plusieurs fois, mais ne peut pas être résolue en un seul objet.</span><span class="sxs-lookup"><span data-stu-id="4445c-346">This prevents inventory and management problems when the same asset or entity is discovered multiple times, but cannot be resolved to one object.</span></span> <span data-ttu-id="4445c-347">L’utilisation d’une méthode heuristique est recommandée, mais pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4445c-347">Using a heuristic is recommended, but not required.</span></span>

<span data-ttu-id="4445c-348">L’heuristique est décrite dans la spécification CIM v2 Common Model Specification et suppose que les règles documentées sont utilisées pour déterminer et assigner un nom.</span><span class="sxs-lookup"><span data-stu-id="4445c-348">The heuristic is outlined in the CIM V2 Common Model specification, and assumes that the documented rules are used to determine and assign a name.</span></span> <span data-ttu-id="4445c-349">La liste des valeurs de **NameFormat** définit la commande permettant d’attribuer un nom de système informatique.</span><span class="sxs-lookup"><span data-stu-id="4445c-349">The **NameFormat** values list defines the order to assign a computer system name.</span></span> <span data-ttu-id="4445c-350">Plusieurs règles sont mappées à la même valeur.</span><span class="sxs-lookup"><span data-stu-id="4445c-350">Several rules map to the same value.</span></span>

<span data-ttu-id="4445c-351">La valeur de [**\_ nom CIM CIM**](cim-computersystem.md) calculée à l’aide de l’heuristique est la valeur de clé du système.</span><span class="sxs-lookup"><span data-stu-id="4445c-351">The [**CIM\_ComputerSystem Name**](cim-computersystem.md) value that is calculated using the heuristic is the key value of the system.</span></span> <span data-ttu-id="4445c-352">Toutefois, utilisez des alias pour attribuer un nom différent pour **le \_ ComputerSystem CIM**, qui peut être plus propre à votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="4445c-352">However, use aliases to assign a different name for **CIM\_ComputerSystem**, which can be more unique to your company.</span></span>

<span data-ttu-id="4445c-353">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-353">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="4445c-354">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4445c-354">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="4445c-355">**IP** (« IP »)</span><span class="sxs-lookup"><span data-stu-id="4445c-355">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="4445c-356">**Composer** (« composer »)</span><span class="sxs-lookup"><span data-stu-id="4445c-356">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="4445c-357">**HID** (« HID »)</span><span class="sxs-lookup"><span data-stu-id="4445c-357">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="4445c-358">**NWA** (« NWA »)</span><span class="sxs-lookup"><span data-stu-id="4445c-358">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="4445c-359">**Hwa** (« Hwa »)</span><span class="sxs-lookup"><span data-stu-id="4445c-359">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="4445c-360">**X25** (« x25 »)</span><span class="sxs-lookup"><span data-stu-id="4445c-360">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="4445c-361">**RNIS** (« RNIS »)</span><span class="sxs-lookup"><span data-stu-id="4445c-361">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="4445c-362">**IPX** (« IPX »)</span><span class="sxs-lookup"><span data-stu-id="4445c-362">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="4445c-363">**DCC** (« DCC »)</span><span class="sxs-lookup"><span data-stu-id="4445c-363">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="4445c-364">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="4445c-364">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="4445c-365">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="4445c-365">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="4445c-366">**SNA** (« SNA »)</span><span class="sxs-lookup"><span data-stu-id="4445c-366">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="4445c-367">**OID/OSI** (« OID/OSI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-367">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4445c-368">**Autre** (« autre »)</span><span class="sxs-lookup"><span data-stu-id="4445c-368">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-369">**NetworkServerModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="4445c-369">**NetworkServerModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-370">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-372">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management Structures \| [**Server \_ info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ type \| VP \_ type \_ Server")</span><span class="sxs-lookup"><span data-stu-id="4445c-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SERVER\_INFO\_101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101)\|sv101\_type\|SV\_TYPE\_SERVER")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-373">Si la **valeur est true**, le mode serveur réseau est activé.</span><span class="sxs-lookup"><span data-stu-id="4445c-373">If **True**, the network Server Mode is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-374">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="4445c-374">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-375">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4445c-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-377">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-377">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-378">Nombre de processeurs logiques disponibles sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4445c-378">Number of logical processors available on the computer.</span></span>

<span data-ttu-id="4445c-379">Vous pouvez utiliser **NumberOfLogicalProcessors** et **NumberOfProcessors** pour déterminer si l’ordinateur est l’hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="4445c-379">You can use **NumberOfLogicalProcessors** and **NumberOfProcessors** to determine if the computer is hyperthreading.</span></span> <span data-ttu-id="4445c-380">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4445c-380">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-381">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="4445c-381">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-382">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4445c-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-384">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| System Information structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors")</span><span class="sxs-lookup"><span data-stu-id="4445c-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|dwNumberOfProcessors")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-385">Nombre de processeurs physiques actuellement disponibles sur un système.</span><span class="sxs-lookup"><span data-stu-id="4445c-385">Number of physical processors currently available on a system.</span></span> <span data-ttu-id="4445c-386">Il s’agit du nombre de processeurs activés pour un système, qui n’inclut pas les processeurs désactivés.</span><span class="sxs-lookup"><span data-stu-id="4445c-386">This is the number of enabled processors for a system, which does not include the disabled processors.</span></span> <span data-ttu-id="4445c-387">Si un système informatique a deux processeurs physiques contenant chacun deux processeurs logiques, la valeur de **NumberOfProcessors** est 2 et **NumberOfLogicalProcessors** est 4.</span><span class="sxs-lookup"><span data-stu-id="4445c-387">If a computer system has two physical processors each containing two logical processors, then the value of **NumberOfProcessors** is 2 and **NumberOfLogicalProcessors** is 4.</span></span> <span data-ttu-id="4445c-388">Les processeurs peuvent être multicœurs ou ils peuvent être des processeurs hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="4445c-388">The processors may be multicore or they may be hyperthreading processors.</span></span> <span data-ttu-id="4445c-389">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4445c-389">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-390">**OEMLogoBitmap**</span><span class="sxs-lookup"><span data-stu-id="4445c-390">**OEMLogoBitmap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-391">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="4445c-391">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4445c-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-393">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-394">Liste de données pour une image bitmap créée par le fabricant d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="4445c-394">List of data for a bitmap that the original equipment manufacturer (OEM) creates.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-395">**OEMStringArray**</span><span class="sxs-lookup"><span data-stu-id="4445c-395">**OEMStringArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-396">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4445c-396">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4445c-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-398">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 11 \| " chaînes OEM ")</span><span class="sxs-lookup"><span data-stu-id="4445c-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 11\|OEM Strings")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-399">Liste des chaînes de forme libre qu’un OEM définit.</span><span class="sxs-lookup"><span data-stu-id="4445c-399">List of free-form strings that an OEM defines.</span></span> <span data-ttu-id="4445c-400">Par exemple, un OEM définit les numéros des documents de référence système, les informations de contact du fabricant, etc.</span><span class="sxs-lookup"><span data-stu-id="4445c-400">For example, an OEM defines the part numbers for system reference documents, manufacturer contact information, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-401">**PartOfDomain**</span><span class="sxs-lookup"><span data-stu-id="4445c-401">**PartOfDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-402">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-404">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="4445c-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-405">Si la **valeur est true**, l’ordinateur fait partie d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="4445c-405">If **True**, the computer is part of a domain.</span></span> <span data-ttu-id="4445c-406">Si la valeur est **null**, cela indique que l’ordinateur n’est pas dans un domaine ou que l’État est inconnu.</span><span class="sxs-lookup"><span data-stu-id="4445c-406">If the value is **NULL**, the computer is not in a domain or the status is unknown.</span></span> <span data-ttu-id="4445c-407">Si vous supprimez l’ordinateur d’un domaine, la valeur devient **false**.</span><span class="sxs-lookup"><span data-stu-id="4445c-407">If you remove the computer from a domain, the value becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-408">**PauseAfterReset**</span><span class="sxs-lookup"><span data-stu-id="4445c-408">**PauseAfterReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-409">Type de données : **sint64**</span><span class="sxs-lookup"><span data-stu-id="4445c-409">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-411">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« SMBIOS \| type 23 \| timeout »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« milliseconds »)</span><span class="sxs-lookup"><span data-stu-id="4445c-411">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-412">Délai avant le lancement d’un redémarrage en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="4445c-412">Time delay before a reboot is initiated in milliseconds.</span></span> <span data-ttu-id="4445c-413">Elle est utilisée après un cycle d’alimentation du système, une réinitialisation du système local ou distant et une réinitialisation automatique du système.</span><span class="sxs-lookup"><span data-stu-id="4445c-413">It is used after a system power cycle, local or remote system reset, and automatic system reset.</span></span> <span data-ttu-id="4445c-414">La valeur 1 (moins un) indique que la valeur de pause est inconnue.</span><span class="sxs-lookup"><span data-stu-id="4445c-414">A value of  1 (minus one) indicates that the pause value is unknown.</span></span>

<span data-ttu-id="4445c-415">**Windows Vista :** Cette propriété peut retourner un nombre inconnu.</span><span class="sxs-lookup"><span data-stu-id="4445c-415">**Windows Vista:** This property may return an unknown number.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-416">**PCSystemType**</span><span class="sxs-lookup"><span data-stu-id="4445c-416">**PCSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-417">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-419">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="4445c-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-420">Type de l’ordinateur en cours d’utilisation, tel qu’un ordinateur portable, un ordinateur de bureau ou une tablette.</span><span class="sxs-lookup"><span data-stu-id="4445c-420">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="4445c-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Non spécifié** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="4445c-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Bureau** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="4445c-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="4445c-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Station de travail** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="4445c-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Serveur d’entreprise** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="4445c-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Serveur Soho** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO Server** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-427">Serveur SOHO (Small Office and Home Office)</span><span class="sxs-lookup"><span data-stu-id="4445c-427">Small Office and Home Office (SOHO) Server</span></span>

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="4445c-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**PC d’appliance** (6)</span><span class="sxs-lookup"><span data-stu-id="4445c-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="4445c-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Serveur de performances** (7)</span><span class="sxs-lookup"><span data-stu-id="4445c-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="4445c-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span><span class="sxs-lookup"><span data-stu-id="4445c-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-431">**PCSystemTypeEx**</span><span class="sxs-lookup"><span data-stu-id="4445c-431">**PCSystemTypeEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-432">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-433">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-434">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="4445c-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-435">Type de l’ordinateur en cours d’utilisation, tel qu’un ordinateur portable, un ordinateur de bureau ou une tablette.</span><span class="sxs-lookup"><span data-stu-id="4445c-435">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<span data-ttu-id="4445c-436">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="4445c-436">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="4445c-437">**Non spécifié** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-437">**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="4445c-438">**Bureau** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-438">**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="4445c-439">**Mobile** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-439">**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="4445c-440">**Station de travail** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-440">**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="4445c-441">**Serveur d’entreprise** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-441">**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="4445c-442">**Serveur Soho** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-442">**SOHO Server** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="4445c-443">**PC d’appliance** (6)</span><span class="sxs-lookup"><span data-stu-id="4445c-443">**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="4445c-444">**Serveur de performances** (7)</span><span class="sxs-lookup"><span data-stu-id="4445c-444">**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

<span data-ttu-id="4445c-445">**Ardoise** (8)</span><span class="sxs-lookup"><span data-stu-id="4445c-445">**Slate** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="4445c-446">**Maximum** (9)</span><span class="sxs-lookup"><span data-stu-id="4445c-446">**Maximum** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-447">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4445c-447">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-448">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-448">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4445c-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-450">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Contrôle d’alimentation du système DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="4445c-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-451">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="4445c-451">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4445c-452">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="4445c-452">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4445c-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4445c-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4445c-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-457">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="4445c-457">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4445c-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-459">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="4445c-459">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4445c-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-461">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4445c-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4445c-462">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="4445c-462">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4445c-463">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="4445c-463">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4445c-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="4445c-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-465">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="4445c-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4445c-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="4445c-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-467">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="4445c-467">Timed Power-On Supported</span></span>

<span data-ttu-id="4445c-468">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="4445c-468">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-469">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4445c-469">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-470">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4445c-470">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-471">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4445c-472">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, par exemple, un appareil peut être mis en mode de suspension, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="4445c-472">If **True**, device can be power-managed, for example, a device can be put into suspend mode, and so on.</span></span> <span data-ttu-id="4445c-473">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais elle indique que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="4445c-473">This property does not indicate that power management features are enabled currently, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="4445c-474">Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-474">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-475">**PowerOnPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="4445c-475">**PowerOnPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-476">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-476">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-478">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 24 \| Hardware Security Settings \| PowerOnPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="4445c-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|PowerOnPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-479">Paramètres de sécurité du matériel système pour Power-On l’état du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4445c-479">System hardware security settings for Power-On Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4445c-480">**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-480">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4445c-481">**Activé** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-481">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="4445c-482">**Non implémenté** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-482">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-483">**Inconnu** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-483">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-484">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="4445c-484">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-485">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-486">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4445c-487">État d’alimentation actuel d’un ordinateur et du système d’exploitation qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="4445c-487">Current power state of a computer and its associated operating system.</span></span> <span data-ttu-id="4445c-488">Les États d’économie d’énergie ont les valeurs suivantes : valeur 4 (inconnu) indique que le système est connu pour être en mode d’économie d’énergie, mais son état exact dans ce mode est inconnu. 2 (mode faible puissance) indique que le système est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées. 3 (veille) indique que le système ne fonctionne pas, mais qu’il peut être mis à la pleine puissance rapidement ; et 7 (avertissement) indique que le système informatique est dans un état d’avertissement et qu’il s’agit d’un mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="4445c-488">The power saving states have the following values: Value 4 (Unknown) indicates that the system is known to be in a power save mode, but its exact status in this mode is unknown; 2 (Low Power Mode) indicates that the system is in a power save state, but still functioning and may exhibit degraded performance; 3 (Standby) indicates that the system is not functioning, but could be brought to full power quickly; and 7 (Warning) indicates that the computer system is in a warning state and a power save mode.</span></span>

<span data-ttu-id="4445c-489">Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-489">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="4445c-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Pleine puissance** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4445c-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4445c-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4445c-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4445c-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4445c-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (6)</span><span class="sxs-lookup"><span data-stu-id="4445c-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4445c-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (7)</span><span class="sxs-lookup"><span data-stu-id="4445c-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="4445c-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Économie **d’énergie-mise en veille prolongée** (8)</span><span class="sxs-lookup"><span data-stu-id="4445c-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-499">Économie d’énergie en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="4445c-499">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="4445c-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Économie **d’énergie-désactivation douce** (9)</span><span class="sxs-lookup"><span data-stu-id="4445c-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-501">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="4445c-501">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-502">**PowerSupplyState**</span><span class="sxs-lookup"><span data-stu-id="4445c-502">**PowerSupplyState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-503">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-503">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-504">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-505">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 3 \| Enclosure System ou châssis \| Power Supply State")</span><span class="sxs-lookup"><span data-stu-id="4445c-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Power Supply State")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-506">État de l’alimentation ou des fournitures lors du dernier démarrage.</span><span class="sxs-lookup"><span data-stu-id="4445c-506">State of the power supply or supplies when last booted.</span></span>

<span data-ttu-id="4445c-507">Cette valeur provient du membre de l' **État** de l’alimentation du **boîtier du système ou** de la structure du châssis dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="4445c-507">This value comes from the **Power Supply State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="4445c-508">La liste suivante identifie les valeurs de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4445c-508">The following list identifies the values for this property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4445c-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="4445c-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Sécurité** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4445c-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4445c-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="4445c-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non récupérable** (6)</span><span class="sxs-lookup"><span data-stu-id="4445c-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non-recoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-515">Non récupérable</span><span class="sxs-lookup"><span data-stu-id="4445c-515">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-516">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="4445c-516">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-517">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-518">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4445c-519">Informations de contact pour le propriétaire du système principal, par exemple, numéro de téléphone, adresse de messagerie, etc.</span><span class="sxs-lookup"><span data-stu-id="4445c-519">Contact information for the primary system owner, for example, phone number, email address, and so on.</span></span>

<span data-ttu-id="4445c-520">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-520">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-521">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="4445c-521">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-522">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-523">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-524">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4445c-524">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4445c-525">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="4445c-525">Name of the primary system owner.</span></span>

<span data-ttu-id="4445c-526">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-526">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-527">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="4445c-527">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-528">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-529">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-530">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001,4»)</span><span class="sxs-lookup"><span data-stu-id="4445c-530">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-531">S’il est activé, la valeur est 4 et le système d’ordinateur unitaire peut être réinitialisé à l’aide des boutons d’alimentation et de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="4445c-531">If enabled, the value is 4 and the unitary computer system can be reset using the power and reset buttons.</span></span> <span data-ttu-id="4445c-532">Si elle est désactivée, la valeur est 3 et aucune réinitialisation n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="4445c-532">If disabled, the value is 3, and a reset is not allowed.</span></span>

<span data-ttu-id="4445c-533">Cette propriété est héritée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-533">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4445c-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4445c-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4445c-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="4445c-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Non implémenté** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Not Implemented** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4445c-539">Non récupérable</span><span class="sxs-lookup"><span data-stu-id="4445c-539">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-540">**ResetCount**</span><span class="sxs-lookup"><span data-stu-id="4445c-540">**ResetCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-541">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="4445c-541">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-542">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-543">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 23 \| System Reset rereset \| Count")</span><span class="sxs-lookup"><span data-stu-id="4445c-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\|Reset Count")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-544">Nombre de réinitialisations automatiques depuis la dernière réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="4445c-544">Number of automatic resets since the last reset.</span></span> <span data-ttu-id="4445c-545">La valeur 1 (moins un) indique que le nombre est inconnu.</span><span class="sxs-lookup"><span data-stu-id="4445c-545">A value of  1 (minus one) indicates that the count is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-546">**ResetLimit**</span><span class="sxs-lookup"><span data-stu-id="4445c-546">**ResetLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-547">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="4445c-547">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-548">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-549">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 23 \| System Reset reconfigure \| Limit")</span><span class="sxs-lookup"><span data-stu-id="4445c-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\| Reset Limit")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-550">Nombre de tentatives de réinitialisation du système consécutives.</span><span class="sxs-lookup"><span data-stu-id="4445c-550">Number of consecutive times a system reset is attempted.</span></span> <span data-ttu-id="4445c-551">La valeur 1 (moins un) indique que la limite est inconnue.</span><span class="sxs-lookup"><span data-stu-id="4445c-551">A value of  1 (minus one) indicates that the limit is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-552">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="4445c-552">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-553">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4445c-553">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4445c-554">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4445c-555">Liste qui spécifie les rôles d’un système dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="4445c-555">List that specifies the roles of a system in the information technology environment.</span></span>

<span data-ttu-id="4445c-556">Cette propriété est héritée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-556">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-557">**État**</span><span class="sxs-lookup"><span data-stu-id="4445c-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-558">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-559">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-560">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4445c-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-561">État actuel d’un objet.</span><span class="sxs-lookup"><span data-stu-id="4445c-561">Current status of an object.</span></span>

<span data-ttu-id="4445c-562">Pour Win32_ComputerSystem, l’État est toujours « OK ».</span><span class="sxs-lookup"><span data-stu-id="4445c-562">For Win32_ComputerSystem, the Status is always “OK”.</span></span>

<span data-ttu-id="4445c-563">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-563">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dl>

</dd> <dt>

<span data-ttu-id="4445c-564">**SupportContactDescription**</span><span class="sxs-lookup"><span data-stu-id="4445c-564">**SupportContactDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-565">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4445c-565">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4445c-566">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-567">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| support information")</span><span class="sxs-lookup"><span data-stu-id="4445c-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring)\|Support Information")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-568">Liste des informations de contact du support technique pour le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="4445c-568">List of the support contact information for the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-569">**SystemFamily**</span><span class="sxs-lookup"><span data-stu-id="4445c-569">**SystemFamily**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-570">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-571">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-572">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 1 \| System information \| Family")</span><span class="sxs-lookup"><span data-stu-id="4445c-572">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Family")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-573">Famille à laquelle appartient un ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="4445c-573">The family to which a particular computer belongs.</span></span> <span data-ttu-id="4445c-574">Une famille fait référence à un ensemble d’ordinateurs similaires, mais non identiques à ceux d’un point de vue matériel ou logiciel.</span><span class="sxs-lookup"><span data-stu-id="4445c-574">A family refers to a set of computers that are similar but not identical from a hardware or software point of view.</span></span>

<span data-ttu-id="4445c-575">Cette valeur provient du membre de la **famille** de la structure des **informations système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="4445c-575">This value comes from the **Family** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="4445c-576">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4445c-576">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-577">**SystemSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="4445c-577">**SystemSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-578">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-579">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-580">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 1 \| Information System information \| Number numéro SKU")</span><span class="sxs-lookup"><span data-stu-id="4445c-580">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-581">Identifie une configuration d’ordinateur spécifique pour la vente.</span><span class="sxs-lookup"><span data-stu-id="4445c-581">Identifies a particular computer configuration for sale.</span></span> <span data-ttu-id="4445c-582">Il est parfois également appelé ID de produit ou numéro de bon de commande.</span><span class="sxs-lookup"><span data-stu-id="4445c-582">It is sometimes also called a product ID or purchase order number.</span></span>

<span data-ttu-id="4445c-583">Cette valeur provient du membre **numéro de référence (SKU** ) de la structure des **informations système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="4445c-583">This value comes from the **SKU Number** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="4445c-584">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4445c-584">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-585">**SystemStartupDelay**</span><span class="sxs-lookup"><span data-stu-id="4445c-585">**SystemStartupDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-586">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-586">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-587">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-587">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4445c-588">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| Boot Loader \| timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span><span class="sxs-lookup"><span data-stu-id="4445c-588">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint)\|Boot Loader\|timeout"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-589">**SystemStartupDelay** ne peut plus être utilisé, car Boot.ini n’est pas utilisé pour configurer le démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="4445c-589">**SystemStartupDelay** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="4445c-590">Utilisez plutôt les [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fournies par le fournisseur WMI données de configuration de démarrage (BCD) (BCD) ou la commande **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="4445c-590">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-591">**SystemStartupOptions**</span><span class="sxs-lookup"><span data-stu-id="4445c-591">**SystemStartupOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-592">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4445c-592">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4445c-593">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-593">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4445c-594">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| Operating Systems")</span><span class="sxs-lookup"><span data-stu-id="4445c-594">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection)\|Operating Systems")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-595">**SystemStartupOptions** ne peut plus être utilisé, car Boot.ini n’est pas utilisé pour configurer le démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="4445c-595">**SystemStartupOptions** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="4445c-596">Utilisez plutôt les [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fournies par le fournisseur WMI données de configuration de démarrage (BCD) (BCD) ou la commande **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="4445c-596">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-597">**SystemStartupSetting**</span><span class="sxs-lookup"><span data-stu-id="4445c-597">**SystemStartupSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-598">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="4445c-598">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-599">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-599">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4445c-600">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilèges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« SeSystemEnvironmentPrivilege »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4445c-600">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-601">**SystemStartupSetting** ne peut plus être utilisé, car Boot.ini n’est pas utilisé pour configurer le démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="4445c-601">**SystemStartupSetting** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="4445c-602">Utilisez plutôt les [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fournies par le fournisseur WMI données de configuration de démarrage (BCD) (BCD) ou la commande **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="4445c-602">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="4445c-603">**SystemType**</span><span class="sxs-lookup"><span data-stu-id="4445c-603">**SystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-604">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-605">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-605">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-606">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| System Information structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture")</span><span class="sxs-lookup"><span data-stu-id="4445c-606">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|wProcessorArchitecture")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-607">Système s’exécutant sur l’ordinateur Windows.</span><span class="sxs-lookup"><span data-stu-id="4445c-607">System running on the Windows-based computer.</span></span> <span data-ttu-id="4445c-608">Cette propriété doit avoir une valeur.</span><span class="sxs-lookup"><span data-stu-id="4445c-608">This property must have a value.</span></span>

<span data-ttu-id="4445c-609">La liste suivante identifie certaines des valeurs possibles pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4445c-609">The following list identifies some of the possible values for this property.</span></span>

<dl> <dd><span data-ttu-id="4445c-610">« PC basé sur x64 »</span><span class="sxs-lookup"><span data-stu-id="4445c-610">"x64-based PC"</span></span></dd> <dd><span data-ttu-id="4445c-611">« PC x86 »</span><span class="sxs-lookup"><span data-stu-id="4445c-611">"X86-based PC"</span></span></dd> <dd><span data-ttu-id="4445c-612">« PC basé sur MIPS »</span><span class="sxs-lookup"><span data-stu-id="4445c-612">"MIPS-based PC"</span></span></dd> <dd><span data-ttu-id="4445c-613">« PC à base alpha »</span><span class="sxs-lookup"><span data-stu-id="4445c-613">"Alpha-based PC"</span></span></dd> <dd><span data-ttu-id="4445c-614">« Power PC »</span><span class="sxs-lookup"><span data-stu-id="4445c-614">"Power PC"</span></span></dd> <dd><span data-ttu-id="4445c-615">« SH-x PC »</span><span class="sxs-lookup"><span data-stu-id="4445c-615">"SH-x PC"</span></span></dd> <dd><span data-ttu-id="4445c-616">« StrongARM PC »</span><span class="sxs-lookup"><span data-stu-id="4445c-616">"StrongARM PC"</span></span></dd> <dd><span data-ttu-id="4445c-617">« PC Intel 64 bits »</span><span class="sxs-lookup"><span data-stu-id="4445c-617">"64-bit Intel PC"</span></span></dd> <dd><span data-ttu-id="4445c-618">« PC alpha 64 bits »</span><span class="sxs-lookup"><span data-stu-id="4445c-618">"64-bit Alpha PC"</span></span></dd> <dd><span data-ttu-id="4445c-619">Connue</span><span class="sxs-lookup"><span data-stu-id="4445c-619">"Unknown"</span></span></dd> <dd><span data-ttu-id="4445c-620">« PC x86-Nec98 »</span><span class="sxs-lookup"><span data-stu-id="4445c-620">"X86-Nec98 PC"</span></span></dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

<span data-ttu-id="4445c-621">**PC x86** (« PC x86 »)</span><span class="sxs-lookup"><span data-stu-id="4445c-621">**X86-based PC** ("X86-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

<span data-ttu-id="4445c-622">**PC basé sur mips** (« PC basé sur mips »)</span><span class="sxs-lookup"><span data-stu-id="4445c-622">**MIPS-based PC** ("MIPS-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

<span data-ttu-id="4445c-623">**PC à base alpha** (« PC à base alpha »)</span><span class="sxs-lookup"><span data-stu-id="4445c-623">**Alpha-based PC** ("Alpha-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

<span data-ttu-id="4445c-624">**Power PC** (« Power PC »)</span><span class="sxs-lookup"><span data-stu-id="4445c-624">**Power PC** ("Power PC")</span></span>


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

<span data-ttu-id="4445c-625">**SH-x PC** (« SH-x PC »)</span><span class="sxs-lookup"><span data-stu-id="4445c-625">**SH-x PC** ("SH-x PC")</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

<span data-ttu-id="4445c-626">**StrongARM PC** (« StrongARM PC »)</span><span class="sxs-lookup"><span data-stu-id="4445c-626">**StrongARM PC** ("StrongARM PC")</span></span>


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

<span data-ttu-id="4445c-627">**PC intel 64 bits** (« pc Intel 64 bits »)</span><span class="sxs-lookup"><span data-stu-id="4445c-627">**64-bit Intel PC** ("64-bit Intel PC")</span></span>


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

<span data-ttu-id="4445c-628">**PC avec processeur x64** (« PC basé sur x64 »)</span><span class="sxs-lookup"><span data-stu-id="4445c-628">**x64-based PC** ("x64-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-629">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="4445c-629">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

<span data-ttu-id="4445c-630">**PC x86-NEC98 PC** (« PC x86-NEC98 »)</span><span class="sxs-lookup"><span data-stu-id="4445c-630">**X86-Nec98 PC** ("X86-Nec98 PC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-631">**ThermalState**</span><span class="sxs-lookup"><span data-stu-id="4445c-631">**ThermalState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-632">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-632">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-633">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-634">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 3 \| Enclosure System ou châssis \| thermal State")</span><span class="sxs-lookup"><span data-stu-id="4445c-634">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Thermal State")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-635">État thermique du système au dernier démarrage.</span><span class="sxs-lookup"><span data-stu-id="4445c-635">Thermal state of the system when last booted.</span></span>

<span data-ttu-id="4445c-636">Cette valeur provient du membre d' **état thermique** de la structure du **boîtier ou du châssis du système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="4445c-636">This value comes from the **Thermal State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4445c-637">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-637">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-638">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-638">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="4445c-639">**Sécurité** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-639">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4445c-640">**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-640">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4445c-641">**Critique** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-641">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="4445c-642">**Non récupérable** (6)</span><span class="sxs-lookup"><span data-stu-id="4445c-642">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-643">**TotalPhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="4445c-643">**TotalPhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-644">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4445c-644">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-645">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-646">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| gestion de mémoire \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="4445c-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus)\|dwTotalPhys"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-647">Taille totale de la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="4445c-647">Total size of physical memory.</span></span> <span data-ttu-id="4445c-648">Sachez que, dans certains cas, cette propriété peut ne pas retourner une valeur exacte pour la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="4445c-648">Be aware that, under some circumstances, this property may not return an accurate value for the physical memory.</span></span> <span data-ttu-id="4445c-649">Par exemple, il n’est pas exact si le BIOS utilise une partie de la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="4445c-649">For example, it is not accurate if the BIOS is using some of the physical memory.</span></span> <span data-ttu-id="4445c-650">Pour obtenir une valeur précise, utilisez à la place la propriété **Capacity** dans [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="4445c-650">For an accurate value, use the **Capacity** property in [**Win32\_PhysicalMemory**](win32-physicalmemory.md) instead.</span></span>

<span data-ttu-id="4445c-651">Exemple : 67108864</span><span class="sxs-lookup"><span data-stu-id="4445c-651">Example: 67108864</span></span>

<span data-ttu-id="4445c-652">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4445c-652">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4445c-653">**UserName**</span><span class="sxs-lookup"><span data-stu-id="4445c-653">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-654">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-654">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-655">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-655">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-656">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| System Information Functions \| [**getUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)»)</span><span class="sxs-lookup"><span data-stu-id="4445c-656">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Functions\|[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-657">Nom d’un utilisateur qui a ouvert une session actuellement.</span><span class="sxs-lookup"><span data-stu-id="4445c-657">Name of a user that is logged on currently.</span></span> <span data-ttu-id="4445c-658">Cette propriété doit avoir une valeur.</span><span class="sxs-lookup"><span data-stu-id="4445c-658">This property must have a value.</span></span> <span data-ttu-id="4445c-659">Dans une session des services Terminal Server, **username** retourne le nom de l’utilisateur qui est connecté à la console, et non celui de l’utilisateur connecté pendant la session du service Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="4445c-659">In a terminal services session, **UserName** returns the name of the user that is logged on to the console not the user logged on during the terminal service session.</span></span>

<span data-ttu-id="4445c-660">Exemple : JeffSmith</span><span class="sxs-lookup"><span data-stu-id="4445c-660">Example: jeffsmith</span></span>

</dd> <dt>

<span data-ttu-id="4445c-661">**WakeUpType**</span><span class="sxs-lookup"><span data-stu-id="4445c-661">**WakeUpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-662">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4445c-662">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-663">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4445c-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4445c-664">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 1 \| System information \| type Wake-up type")</span><span class="sxs-lookup"><span data-stu-id="4445c-664">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Wake-up Type")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-665">Événement qui provoque la mise sous tension du système.</span><span class="sxs-lookup"><span data-stu-id="4445c-665">Event that causes the system to power up.</span></span>

<span data-ttu-id="4445c-666">Cette valeur provient du membre de **type de mise en éveil** de la structure des **informations système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="4445c-666">This value comes from the **Wake-up Type** member of the **System Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="4445c-667">**Réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="4445c-667">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4445c-668">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4445c-668">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4445c-669">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4445c-669">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

<span data-ttu-id="4445c-670">**Minuteur APM** (3)</span><span class="sxs-lookup"><span data-stu-id="4445c-670">**APM Timer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

<span data-ttu-id="4445c-671">**Sonnerie de modem** (4)</span><span class="sxs-lookup"><span data-stu-id="4445c-671">**Modem Ring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

<span data-ttu-id="4445c-672">**Réseau local distant** (5)</span><span class="sxs-lookup"><span data-stu-id="4445c-672">**LAN Remote** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

<span data-ttu-id="4445c-673">**Commutateur d’alimentation** (6)</span><span class="sxs-lookup"><span data-stu-id="4445c-673">**Power Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

<span data-ttu-id="4445c-674">**PME \# PCI** Commission(7</span><span class="sxs-lookup"><span data-stu-id="4445c-674">**PCI PME\#** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

<span data-ttu-id="4445c-675">**Alimentation secteur restaurée** (8)</span><span class="sxs-lookup"><span data-stu-id="4445c-675">**AC Power Restored** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4445c-676">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="4445c-676">**Workgroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4445c-677">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4445c-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4445c-678">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4445c-678">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4445c-679">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="4445c-679">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="4445c-680">Nom du groupe de travail pour cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4445c-680">Name of the workgroup for this computer.</span></span> <span data-ttu-id="4445c-681">Si la valeur de la propriété **PartOfDomain** est **false**, le nom du groupe de travail est retourné.</span><span class="sxs-lookup"><span data-stu-id="4445c-681">If the value of the **PartOfDomain** property is **False**, then the name of the workgroup is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4445c-682">Notes</span><span class="sxs-lookup"><span data-stu-id="4445c-682">Remarks</span></span>

<span data-ttu-id="4445c-683">Pour déterminer le nombre total d’instances de processeur associées à un objet système informatique, utilisez la classe d’association [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="4445c-683">To determine the total number of processor instances associated with a computer system object, use the [**Win32\_ComputerSystemProcessor**](win32-computersystemprocessor.md) association class.</span></span>

<span data-ttu-id="4445c-684">Plusieurs instances de [**\_ processeur Win32**](win32-processor.md) sont associées à une instance **\_ ComputerSystem Win32** avec plusieurs processeurs physiques.</span><span class="sxs-lookup"><span data-stu-id="4445c-684">A **Win32\_ComputerSystem** instance that has multiple physical processors has multiple [**Win32\_Processor**](win32-processor.md) instances associated with it.</span></span> <span data-ttu-id="4445c-685">Si la valeur de **NumberOfLogicalProcessors** est supérieure à la valeur de **NumberOfProcessors** , le système informatique est soit un système multicœur, soit un ou plusieurs processeurs activés pour l’hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="4445c-685">If the value of **NumberOfLogicalProcessors** is greater than the value of **NumberOfProcessors** then the computer system is either a multicore system or has one or more processors enabled for hyperthreading.</span></span> <span data-ttu-id="4445c-686">Pour plus d’informations, consultez les propriétés **NumberOfLogicalProcessors** et **NumberOfCores** et la section Notes dans le **\_ processeur Win32**.</span><span class="sxs-lookup"><span data-stu-id="4445c-686">For more information, see the **NumberOfLogicalProcessors** and **NumberOfCores** properties and Remarks section in **Win32\_Processor**.</span></span>

<span data-ttu-id="4445c-687">La classe **Win32 \_ ComputerSystem** est dérivée de la [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="4445c-687">The **Win32\_ComputerSystem** class is derived from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4445c-688">Exemples</span><span class="sxs-lookup"><span data-stu-id="4445c-688">Examples</span></span>

<span data-ttu-id="4445c-689">L' [exemple de code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) du centre de script suivant utilise **Win32 \_ ComputerSystem** pour récupérer des informations à partir de plusieurs systèmes informatiques et les afficher dans une interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="4445c-689">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) uses the **Win32\_ComputerSystem** to retrieve information from a number of computer systems, and display them in a GUI.</span></span>

<span data-ttu-id="4445c-690">Vous trouverez un exemple de script qui obtient les données du système d’exploitation et du processeur à partir de **Win32 \_ ComputerSystem**, du [**\_ processeur Win32**](win32-processor.md)et de [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) dans les exemples de sujets relatifs au [**\_ processeur Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="4445c-690">You can find an example script that obtains operating system and processor data from **Win32\_ComputerSystem**, [**Win32\_Processor**](win32-processor.md), and [**Win32\_OperatingSystem**](win32-operatingsystem.md) in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="4445c-691">L’exemple VBScript suivant décrit comment récupérer le nom de domaine de l’ordinateur local à partir d’instances de **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="4445c-691">The following VBScript sample describes how to retrieve the domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



<span data-ttu-id="4445c-692">L’exemple perl suivant décrit comment récupérer le nom de l’ordinateur local à partir des instances de **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="4445c-692">The following Perl sample describes how to retrieve the local machine name from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="4445c-693">L’exemple perl suivant décrit comment récupérer le nom de domaine DNS de l’ordinateur local à partir des instances de **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="4445c-693">The following Perl sample describes how to retrieve the DNS domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="4445c-694">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4445c-694">Requirements</span></span>



| <span data-ttu-id="4445c-695">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4445c-695">Requirement</span></span> | <span data-ttu-id="4445c-696">Valeur</span><span class="sxs-lookup"><span data-stu-id="4445c-696">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4445c-697">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4445c-697">Minimum supported client</span></span><br/> | <span data-ttu-id="4445c-698">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4445c-698">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4445c-699">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4445c-699">Minimum supported server</span></span><br/> | <span data-ttu-id="4445c-700">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4445c-700">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4445c-701">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4445c-701">Namespace</span></span><br/>                | <span data-ttu-id="4445c-702">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4445c-702">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4445c-703">MOF</span><span class="sxs-lookup"><span data-stu-id="4445c-703">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4445c-704"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4445c-704"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4445c-705">DLL</span><span class="sxs-lookup"><span data-stu-id="4445c-705">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4445c-706"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4445c-706"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4445c-707">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4445c-707">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4445c-708">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="4445c-708">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dt>

<span data-ttu-id="4445c-709">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4445c-709">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4445c-710">Tâches WMI : comptes et domaines</span><span class="sxs-lookup"><span data-stu-id="4445c-710">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="4445c-711">Tâches WMI : matériel de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="4445c-711">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="4445c-712">Tâches WMI : gestion des postes de travail</span><span class="sxs-lookup"><span data-stu-id="4445c-712">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

